# RenderEngine(bpy_struct)

## Simple Render Engine
    
    
    import bpy
    import array
    
    
    class CustomRenderEngine(bpy.types.RenderEngine):
        # These three members are used by Blender to set up the
        # RenderEngine; define its internal name, visible name and capabilities.
        bl_idname = "CUSTOM"
        bl_label = "Custom"
        bl_use_preview = True
    
        # Init is called whenever a new render engine instance is created. Multiple
        # instances may exist at the same time, for example for a viewport and final
        # render.
        # Note the generic arguments signature, and the call to the parent class
        # `__init__` methods, which are required for Blender to create the underlying
        # `RenderEngine` data.
        def __init__(self, *args, **kwargs):
            super().__init__(*args, **kwargs)
            self.scene_data = None
            self.draw_data = None
    
        # When the render engine instance is destroy, this is called. Clean up any
        # render engine data here, for example stopping running render threads.
        def __del__(self):
            # Own delete code...
            super().__del__()
    
        # This is the method called by Blender for both final renders (F12) and
        # small preview for materials, world and lights.
        def render(self, depsgraph):
            scene = depsgraph.scene
            scale = scene.render.resolution_percentage / 100.0
            self.size_x = int(scene.render.resolution_x * scale)
            self.size_y = int(scene.render.resolution_y * scale)
    
            # Fill the render result with a flat color. The frame-buffer is
            # defined as a list of pixels, each pixel itself being a list of
            # R,G,B,A values.
            if self.is_preview:
                color = [0.1, 0.2, 0.1, 1.0]
            else:
                color = [0.2, 0.1, 0.1, 1.0]
    
            pixel_count = self.size_x * self.size_y
            rect = [color] * pixel_count
    
            # Here we write the pixel values to the RenderResult
            result = self.begin_result(0, 0, self.size_x, self.size_y)
            layer = result.layers[0].passes["Combined"]
            layer.rect = rect
            self.end_result(result)
    
        # For viewport renders, this method gets called once at the start and
        # whenever the scene or 3D viewport changes. This method is where data
        # should be read from Blender in the same thread. Typically a render
        # thread will be started to do the work while keeping Blender responsive.
        def view_update(self, context, depsgraph):
            region = context.region
            view3d = context.space_data
            scene = depsgraph.scene
    
            # Get viewport dimensions
            dimensions = region.width, region.height
    
            if not self.scene_data:
                # First time initialization
                self.scene_data = []
                first_time = True
    
                # Loop over all datablocks used in the scene.
                for datablock in depsgraph.ids:
                    pass
            else:
                first_time = False
    
                # Test which datablocks changed
                for update in depsgraph.updates:
                    print("Datablock updated: ", update.id.name)
    
                # Test if any material was added, removed or changed.
                if depsgraph.id_type_updated('MATERIAL'):
                    print("Materials updated")
    
            # Loop over all object instances in the scene.
            if first_time or depsgraph.id_type_updated('OBJECT'):
                for instance in depsgraph.object_instances:
                    pass
    
        # For viewport renders, this method is called whenever Blender redraws
        # the 3D viewport. The renderer is expected to quickly draw the render
        # with OpenGL, and not perform other expensive work.
        # Blender will draw overlays for selection and editing on top of the
        # rendered image automatically.
        def view_draw(self, context, depsgraph):
            # Lazily import GPU module, so that the render engine works in
            # background mode where the GPU module can't be imported by default.
            import gpu
    
            region = context.region
            scene = depsgraph.scene
    
            # Get viewport dimensions
            dimensions = region.width, region.height
    
            # Bind shader that converts from scene linear to display space,
            gpu.state.blend_set('ALPHA_PREMULT')
            self.bind_display_space_shader(scene)
    
            if not self.draw_data or self.draw_data.dimensions != dimensions:
                self.draw_data = CustomDrawData(dimensions)
    
            self.draw_data.draw()
    
            self.unbind_display_space_shader()
            gpu.state.blend_set('NONE')
    
    
    class CustomDrawData:
        def __init__(self, dimensions):
            import gpu
    
            # Generate dummy float image buffer.
            self.dimensions = dimensions
            width, height = dimensions
    
            pixels = width * height * array.array('f', [0.1, 0.2, 0.1, 1.0])
            pixels = gpu.types.Buffer('FLOAT', width * height * 4, pixels)
    
            # Generate texture.
            self.texture = gpu.types.GPUTexture((width, height), format='RGBA16F', data=pixels)
    
            # Note: This is just a didactic example.
            # In this case it would be more convenient to fill the texture with:
            # self.texture.clear('FLOAT', value=[0.1, 0.2, 0.1, 1.0])
    
        def __del__(self):
            del self.texture
    
        def draw(self):
            from gpu_extras.presets import draw_texture_2d
            draw_texture_2d(self.texture, (0, 0), self.texture.width, self.texture.height)
    
    
    # RenderEngines also need to tell UI Panels that they are compatible with.
    # We recommend to enable all panels marked as BLENDER_RENDER, and then
    # exclude any panels that are replaced by custom panels registered by the
    # render engine, or that are not supported.
    def get_panels():
        exclude_panels = {
            'VIEWLAYER_PT_filter',
            'VIEWLAYER_PT_layer_passes',
        }
    
        panels = []
        for panel in bpy.types.Panel.__subclasses__():
            if hasattr(panel, 'COMPAT_ENGINES') and 'BLENDER_RENDER' in panel.COMPAT_ENGINES:
                if panel.__name__ not in exclude_panels:
                    panels.append(panel)
    
        return panels
    
    
    def register():
        # Register the RenderEngine.
        bpy.utils.register_class(CustomRenderEngine)
    
        for panel in get_panels():
            panel.COMPAT_ENGINES.add('CUSTOM')
    
    
    def unregister():
        bpy.utils.unregister_class(CustomRenderEngine)
    
        for panel in get_panels():
            if 'CUSTOM' in panel.COMPAT_ENGINES:
                panel.COMPAT_ENGINES.remove('CUSTOM')
    
    
    if __name__ == "__main__":
        register()
    

## GPU Render Engine
    
    
    import bpy
    
    
    class CustomGPURenderEngine(bpy.types.RenderEngine):
        bl_idname = "CUSTOM_GPU"
        bl_label = "Custom GPU"
    
        # Request a GPU context to be created and activated for the render method.
        # This may be used either to perform the rendering itself, or to allocate
        # and fill a texture for more efficient drawing.
        bl_use_gpu_context = True
    
        def render(self, depsgraph):
            # Lazily import GPU module, since GPU context is only created on demand
            # for rendering and does not exist on register.
            import gpu
    
            # Perform rendering task.
            pass
    
    
    def register():
        bpy.utils.register_class(CustomGPURenderEngine)
    
    
    def unregister():
        bpy.utils.unregister_class(CustomGPURenderEngine)
    
    
    if __name__ == "__main__":
        register()
    

base class — [`bpy_struct`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct "bpy.types.bpy_struct")

subclasses — [`HydraRenderEngine`](../H/bpy.types.HydraRenderEngine.md#bpy.types.HydraRenderEngine "bpy.types.HydraRenderEngine")

_class _bpy.types.RenderEngine(_bpy_struct_)
    

Render engine

bl_idname
    

Type:
    

string, default “”, (never None)

bl_label
    

Type:
    

string, default “”, (never None)

bl_use_custom_freestyle
    

Handles freestyle rendering on its own, instead of delegating it to EEVEE

Type:
    

boolean, default False

bl_use_eevee_viewport
    

Uses EEVEE for viewport shading in Material Preview shading mode

Type:
    

boolean, default False

bl_use_gpu_context
    

Enable OpenGL context for the render method, for engines that render using OpenGL

Type:
    

boolean, default False

bl_use_image_save
    

Save images/movie to disk while rendering an animation. Disabling image saving is only supported when bl_use_postprocess is also disabled.

Type:
    

boolean, default True

bl_use_materialx
    

Use MaterialX for exporting materials to Hydra

Type:
    

boolean, default False

bl_use_postprocess
    

Apply compositing on render results

Type:
    

boolean, default False

bl_use_preview
    

Render engine supports being used for rendering previews of materials, lights and worlds

Type:
    

boolean, default False

bl_use_shading_nodes_custom
    

Don’t expose Cycles and EEVEE shading nodes in the node editor user interface, so separate nodes can be used instead

Type:
    

boolean, default True

bl_use_spherical_stereo
    

Support spherical stereo camera models

Type:
    

boolean, default False

bl_use_stereo_viewport
    

Support rendering stereo 3D viewport

Type:
    

boolean, default False

camera_override
    

Type:
    

[`Object`](../O/bpy.types.Object.md#bpy.types.Object "bpy.types.Object"), (readonly)

is_animation
    

Type:
    

boolean, default False

is_preview
    

Type:
    

boolean, default False

layer_override
    

Type:
    

boolean array of 20 items, default (False, False, False, False, False, False, False, False, False, False, False, False, False, False, False, False, False, False, False, False)

render
    

Type:
    

[`RenderSettings`](bpy.types.RenderSettings.md#bpy.types.RenderSettings "bpy.types.RenderSettings"), (readonly)

resolution_x
    

Type:
    

int in [-inf, inf], default 0, (readonly)

resolution_y
    

Type:
    

int in [-inf, inf], default 0, (readonly)

temporary_directory
    

Type:
    

string, default “”, (readonly, never None)

use_highlight_tiles
    

Type:
    

boolean, default False

update(_*_ , _data =None_, _depsgraph =None_)
    

Export scene data for render

render(_depsgraph_)
    

Render scene into an image

render_frame_finish()
    

Perform finishing operations after all view layers in a frame were rendered

draw(_context_ , _depsgraph_)
    

Draw render image

bake(_depsgraph_ , _object_ , _pass_type_ , _pass_filter_ , _width_ , _height_)
    

Bake passes

Parameters:
    

  * **pass_type** (enum in [Bake Pass Type Items](../../bpy_types_enum_items/bake_pass_type_items.md#rna-enum-bake-pass-type-items)) – Pass, Pass to bake

  * **pass_filter** (_int in_ _[__0_ _,__inf_ _]_) – Pass Filter, Filter to combined, diffuse, glossy and transmission passes

  * **width** (_int in_ _[__0_ _,__inf_ _]_) – Width, Image width

  * **height** (_int in_ _[__0_ _,__inf_ _]_) – Height, Image height


view_update(_context_ , _depsgraph_)
    

Update on data changes for viewport render

view_draw(_context_ , _depsgraph_)
    

Draw viewport render

update_script_node(_*_ , _node =None_)
    

Compile shader script node

update_render_passes(_*_ , _scene =None_, _renderlayer =None_)
    

Update the render passes that will be generated

update_custom_camera(_*_ , _cam =None_)
    

Compile custom camera

tag_redraw()
    

Request redraw for viewport rendering

tag_update()
    

Request update call for viewport rendering

begin_result(_x_ , _y_ , _w_ , _h_ , _*_ , _layer =''_, _view =''_)
    

Create render result to write linear floating-point render layers and passes

Parameters:
    

  * **x** (_int in_ _[__0_ _,__inf_ _]_) – X

  * **y** (_int in_ _[__0_ _,__inf_ _]_) – Y

  * **w** (_int in_ _[__0_ _,__inf_ _]_) – Width

  * **h** (_int in_ _[__0_ _,__inf_ _]_) – Height

  * **layer** (_string_ _,__(__optional_ _,__never None_ _)_) – Layer, Single layer to get render result for

  * **view** (_string_ _,__(__optional_ _,__never None_ _)_) – View, Single view to get render result for


Returns:
    

Result

Return type:
    

[`RenderResult`](bpy.types.RenderResult.md#bpy.types.RenderResult "bpy.types.RenderResult")

update_result(_result_)
    

Signal that pixels have been updated and can be redrawn in the user interface

Parameters:
    

**result** ([`RenderResult`](bpy.types.RenderResult.md#bpy.types.RenderResult "bpy.types.RenderResult")) – Result

end_result(_result_ , _*_ , _cancel =False_, _highlight =False_, _do_merge_results =False_)
    

All pixels in the render result have been set and are final

Parameters:
    

  * **result** ([`RenderResult`](bpy.types.RenderResult.md#bpy.types.RenderResult "bpy.types.RenderResult")) – Result

  * **cancel** (_boolean_ _,__(__optional_ _)_) – Cancel, Don’t mark tile as done, don’t merge results unless forced

  * **highlight** (_boolean_ _,__(__optional_ _)_) – Highlight, Don’t mark tile as done yet

  * **do_merge_results** (_boolean_ _,__(__optional_ _)_) – Merge Results, Merge results even if cancel=true


add_pass(_name_ , _channels_ , _chan_id_ , _*_ , _layer =''_)
    

Add a pass to the render layer

Parameters:
    

  * **name** (_string_ _,__(__never None_ _)_) – Name, Name of the Pass, without view or channel tag

  * **channels** (_int in_ _[__0_ _,__inf_ _]_) – Channels

  * **chan_id** (_string_ _,__(__never None_ _)_) – Channel IDs, Channel names, one character per channel

  * **layer** (_string_ _,__(__optional_ _,__never None_ _)_) – Layer, Single layer to add render pass to


get_result()
    

Get final result for non-pixel operations

Returns:
    

Result

Return type:
    

[`RenderResult`](bpy.types.RenderResult.md#bpy.types.RenderResult "bpy.types.RenderResult")

test_break()
    

Test if the render operation should been canceled, this is a fast call that should be used regularly for responsiveness

Returns:
    

Break

Return type:
    

boolean

pass_by_index_get(_layer_ , _index_)
    

pass_by_index_get

Parameters:
    

  * **layer** (_string_ _,__(__never None_ _)_) – Layer, Name of render layer to get pass for

  * **index** (_int in_ _[__0_ _,__inf_ _]_) – Index, Index of pass to get


Returns:
    

Index, Index of pass to get

Return type:
    

[`RenderPass`](bpy.types.RenderPass.md#bpy.types.RenderPass "bpy.types.RenderPass")

active_view_get()
    

active_view_get

Returns:
    

View, Single view active

Return type:
    

string, (never None)

active_view_set(_view_)
    

active_view_set

Parameters:
    

**view** (_string_ _,__(__never None_ _)_) – View, Single view to set as active

camera_shift_x(_camera_ , _*_ , _use_spherical_stereo =False_)
    

camera_shift_x

Parameters:
    

**use_spherical_stereo** (_boolean_ _,__(__optional_ _)_) – Spherical Stereo

Returns:
    

Shift X

Return type:
    

float in [0, inf]

camera_model_matrix(_camera_ , _*_ , _use_spherical_stereo =False_)
    

camera_model_matrix

Parameters:
    

**use_spherical_stereo** (_boolean_ _,__(__optional_ _)_) – Spherical Stereo

Returns:
    

Model Matrix, Normalized camera model matrix

Return type:
    

[`mathutils.Matrix`](mathutils.md#mathutils.Matrix "mathutils.Matrix") of 4 * 4 items in [-inf, inf]

use_spherical_stereo(_camera_)
    

use_spherical_stereo

Returns:
    

Spherical Stereo

Return type:
    

boolean

update_stats(_stats_ , _info_)
    

Update and signal to redraw render status text

Parameters:
    

  * **stats** (_string_ _,__(__never None_ _)_) – Stats

  * **info** (_string_ _,__(__never None_ _)_) – Info


frame_set(_frame_ , _subframe_)
    

Evaluate scene at a different frame (for motion blur)

Parameters:
    

  * **frame** (_int in_ _[__-inf_ _,__inf_ _]_) – Frame

  * **subframe** (_float in_ _[__0_ _,__1_ _]_) – Subframe


update_progress(_progress_)
    

Update progress percentage of render

Parameters:
    

**progress** (_float in_ _[__0_ _,__1_ _]_) – Percentage of render that’s done

update_memory_stats(_*_ , _memory_used =0.0_, _memory_peak =0.0_)
    

Update memory usage statistics

Parameters:
    

  * **memory_used** (_float in_ _[__0_ _,__inf_ _]__,__(__optional_ _)_) – Current memory usage in megabytes

  * **memory_peak** (_float in_ _[__0_ _,__inf_ _]__,__(__optional_ _)_) – Peak memory usage in megabytes


report(_type_ , _message_)
    

Report info, warning or error messages

Parameters:
    

  * **type** (enum set in [Wm Report Items](../../bpy_types_enum_items/wm_report_items.md#rna-enum-wm-report-items)) – Type

  * **message** (_string_ _,__(__never None_ _)_) – Report Message


error_set(_message_)
    

Set error message displaying after the render is finished

Parameters:
    

**message** (_string_ _,__(__never None_ _)_) – Report Message

bind_display_space_shader(_scene_)
    

Bind GLSL fragment shader that converts linear colors to display space colors using scene color management settings

unbind_display_space_shader()
    

Unbind GLSL display space shader, must always be called after binding the shader

support_display_space_shader(_scene_)
    

Test if GLSL display space shader is supported for the combination of graphics card and scene settings

Returns:
    

Supported

Return type:
    

boolean

get_preview_pixel_size(_scene_)
    

Get the pixel size that should be used for preview rendering

Returns:
    

Pixel Size

Return type:
    

int in [1, 8]

free_blender_memory()
    

Free Blender side memory of render engine

tile_highlight_set(_x_ , _y_ , _width_ , _height_ , _highlight_)
    

Set highlighted state of the given tile

Parameters:
    

  * **x** (_int in_ _[__0_ _,__inf_ _]_) – X

  * **y** (_int in_ _[__0_ _,__inf_ _]_) – Y

  * **width** (_int in_ _[__0_ _,__inf_ _]_) – Width

  * **height** (_int in_ _[__0_ _,__inf_ _]_) – Height

  * **highlight** (_boolean_) – Highlight


tile_highlight_clear_all()
    

The temp directory used by Blender

register_pass(_scene_ , _view_layer_ , _name_ , _channels_ , _chanid_ , _type_)
    

Register a render pass that will be part of the render with the current settings

Parameters:
    

  * **name** (_string_ _,__(__never None_ _)_) – Name

  * **channels** (_int in_ _[__1_ _,__8_ _]_) – Channels

  * **chanid** (_string_ _,__(__never None_ _)_) – Channel IDs

  * **type** (enum in [`'VALUE'`, `'VECTOR'`, `'COLOR'`]) – Type


_classmethod _bl_rna_get_subclass(_id_ , _default =None_, _/_)
    

Parameters:
    

**id** (_str_) – The RNA type identifier.

Returns:
    

The RNA type or default when not found.

Return type:
    

[`bpy.types.Struct`](../S/bpy.types.Struct.md#bpy.types.Struct "bpy.types.Struct") subclass

_classmethod _bl_rna_get_subclass_py(_id_ , _default =None_, _/_)
    

Parameters:
    

**id** (_str_) – The RNA type identifier.

Returns:
    

The class or default when not found.

Return type:
    

type

### Inherited Properties

  * [`bpy_struct.id_data`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.id_data "bpy.types.bpy_struct.id_data")

| 


  
---|---  
  
### Inherited Functions

  * [`bpy_struct.as_pointer`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.as_pointer "bpy.types.bpy_struct.as_pointer")
  * [`bpy_struct.driver_add`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.driver_add "bpy.types.bpy_struct.driver_add")
  * [`bpy_struct.driver_remove`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.driver_remove "bpy.types.bpy_struct.driver_remove")
  * [`bpy_struct.get`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.get "bpy.types.bpy_struct.get")
  * [`bpy_struct.id_properties_clear`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.id_properties_clear "bpy.types.bpy_struct.id_properties_clear")
  * [`bpy_struct.id_properties_ensure`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.id_properties_ensure "bpy.types.bpy_struct.id_properties_ensure")
  * [`bpy_struct.id_properties_ui`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.id_properties_ui "bpy.types.bpy_struct.id_properties_ui")
  * [`bpy_struct.is_property_hidden`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.is_property_hidden "bpy.types.bpy_struct.is_property_hidden")
  * [`bpy_struct.is_property_overridable_library`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.is_property_overridable_library "bpy.types.bpy_struct.is_property_overridable_library")
  * [`bpy_struct.is_property_readonly`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.is_property_readonly "bpy.types.bpy_struct.is_property_readonly")
  * [`bpy_struct.is_property_set`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.is_property_set "bpy.types.bpy_struct.is_property_set")
  * [`bpy_struct.items`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.items "bpy.types.bpy_struct.items")

| 

  * [`bpy_struct.keyframe_delete`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.keyframe_delete "bpy.types.bpy_struct.keyframe_delete")
  * [`bpy_struct.keyframe_insert`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.keyframe_insert "bpy.types.bpy_struct.keyframe_insert")
  * [`bpy_struct.keys`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.keys "bpy.types.bpy_struct.keys")
  * [`bpy_struct.path_from_id`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.path_from_id "bpy.types.bpy_struct.path_from_id")
  * [`bpy_struct.path_from_module`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.path_from_module "bpy.types.bpy_struct.path_from_module")
  * [`bpy_struct.path_resolve`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.path_resolve "bpy.types.bpy_struct.path_resolve")
  * [`bpy_struct.pop`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.pop "bpy.types.bpy_struct.pop")
  * [`bpy_struct.property_overridable_library_set`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.property_overridable_library_set "bpy.types.bpy_struct.property_overridable_library_set")
  * [`bpy_struct.property_unset`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.property_unset "bpy.types.bpy_struct.property_unset")
  * [`bpy_struct.rna_ancestors`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.rna_ancestors "bpy.types.bpy_struct.rna_ancestors")
  * [`bpy_struct.type_recast`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.type_recast "bpy.types.bpy_struct.type_recast")
  * [`bpy_struct.values`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.values "bpy.types.bpy_struct.values")

  
---|---
  *[*]: Keyword-only parameters separator (PEP 3102)
  *[/]: Positional-only parameter separator (PEP 570)
