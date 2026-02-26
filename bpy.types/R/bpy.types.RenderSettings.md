# RenderSettings(bpy_struct)

base class — [`bpy_struct`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct "bpy.types.bpy_struct")

_class _bpy.types.RenderSettings(_bpy_struct_)
    

Rendering settings for a Scene data-block

bake
    

Type:
    

[`BakeSettings`](../B/bpy.types.BakeSettings.md#bpy.types.BakeSettings "bpy.types.BakeSettings"), (readonly, never None)

border_max_x
    

Maximum X value for the render region

Type:
    

float in [0, 1], default 1.0

border_max_y
    

Maximum Y value for the render region

Type:
    

float in [0, 1], default 1.0

border_min_x
    

Minimum X value for the render region

Type:
    

float in [0, 1], default 0.0

border_min_y
    

Minimum Y value for the render region

Type:
    

float in [0, 1], default 0.0

compositor_denoise_device
    

The device to use to process the denoise nodes in the compositor

  * `AUTO` Auto – Use the same device used by the compositor to process the denoise node.

  * `CPU` CPU – Use the CPU to process the denoise node.

  * `GPU` GPU – Use the GPU to process the denoise node if available, otherwise fallback to CPU.


Type:
    

enum in [`'AUTO'`, `'CPU'`, `'GPU'`], default `'AUTO'`

compositor_denoise_final_quality
    

The quality used by denoise nodes during the compositing of final renders if the nodes’ quality option is set to Follow Scene

  * `HIGH` High – High quality.

  * `BALANCED` Balanced – Balanced between performance and quality.

  * `FAST` Fast – High performance.


Type:
    

enum in [`'HIGH'`, `'BALANCED'`, `'FAST'`], default `'HIGH'`

compositor_denoise_preview_quality
    

The quality used by denoise nodes during viewport and interactive compositing if the nodes’ quality option is set to Follow Scene

  * `HIGH` High – High quality.

  * `BALANCED` Balanced – Balanced between performance and quality.

  * `FAST` Fast – High performance.


Type:
    

enum in [`'HIGH'`, `'BALANCED'`, `'FAST'`], default `'BALANCED'`

compositor_device
    

Set how compositing is executed

Type:
    

enum in [`'CPU'`, `'GPU'`], default `'CPU'`

compositor_precision
    

The precision of compositor intermediate result

  * `AUTO` Auto – Full precision for final renders, half precision otherwise.

  * `FULL` Full – Full precision.


Type:
    

enum in [`'AUTO'`, `'FULL'`], default `'AUTO'`

dither_intensity
    

Amount of dithering noise added to the rendered image to break up banding

Type:
    

float in [0, inf], default 1.0

engine
    

Engine to use for rendering

Type:
    

enum in [`'BLENDER_EEVEE'`], default `'BLENDER_EEVEE'`

ffmpeg
    

FFmpeg related settings for the scene

Type:
    

[`FFmpegSettings`](../F/bpy.types.FFmpegSettings.md#bpy.types.FFmpegSettings "bpy.types.FFmpegSettings"), (readonly)

file_extension
    

The file extension used for saving renders

Type:
    

string, default “”, (readonly, never None)

filepath
    

Directory/name to save animations, # characters define the position and padding of frame numbers

Type:
    

string, default “”, (never None, blend relative `//` prefix supported, Supports [template expressions](https://docs.blender.org/manual/en/5.0/files/file_paths.md#path-templates))

film_transparent
    

World background is transparent, for compositing the render over another background

Type:
    

boolean, default False

filter_size
    

Width over which the reconstruction filter combines samples

Type:
    

float in [0, 500], default 1.5

fps
    

Framerate, expressed in frames per second

Type:
    

int in [1, 32767], default 24

fps_base
    

Framerate base

Type:
    

float in [1e-05, 1e+06], default 1.0

frame_map_new
    

How many frames the Map Old will last

Type:
    

int in [1, 900], default 100

frame_map_old
    

Old mapping value in frames

Type:
    

int in [1, 900], default 100

hair_subdiv
    

Additional subdivision along the curves

Type:
    

int in [0, 3], default 0

hair_type
    

Curves shape type

Type:
    

enum in [`'STRAND'`, `'STRIP'`, `'CYLINDER'`], default `'STRAND'`

has_multiple_engines
    

More than one rendering engine is available

Type:
    

boolean, default False, (readonly)

image_settings
    

Type:
    

[`ImageFormatSettings`](../I/bpy.types.ImageFormatSettings.md#bpy.types.ImageFormatSettings "bpy.types.ImageFormatSettings"), (readonly, never None)

is_movie_format
    

When true the format is a movie

Type:
    

boolean, default False, (readonly)

line_thickness
    

Line thickness in pixels

Type:
    

float in [0, 10000], default 1.0

line_thickness_mode
    

Line thickness mode for Freestyle line drawing

  * `ABSOLUTE` Absolute – Specify unit line thickness in pixels.

  * `RELATIVE` Relative – Unit line thickness is scaled by the proportion of the present vertical image resolution to 480 pixels.


Type:
    

enum in [`'ABSOLUTE'`, `'RELATIVE'`], default `'ABSOLUTE'`

metadata_input
    

Where to take the metadata from

  * `SCENE` Scene – Use metadata from the current scene.

  * `STRIPS` Sequencer Strips – Use metadata from the strips in the sequencer.


Type:
    

enum in [`'SCENE'`, `'STRIPS'`], default `'SCENE'`

motion_blur_position
    

Offset for the shutter’s time interval, allows to change the motion blur trails

  * `START` Start on Frame – The shutter opens at the current frame.

  * `CENTER` Center on Frame – The shutter is open during the current frame.

  * `END` End on Frame – The shutter closes at the current frame.


Type:
    

enum in [`'START'`, `'CENTER'`, `'END'`], default `'CENTER'`

motion_blur_shutter
    

Time taken in frames between shutter open and close

Type:
    

float in [0, inf], default 0.5

motion_blur_shutter_curve
    

Curve defining the shutter’s openness over time

Type:
    

[`CurveMapping`](../C/bpy.types.CurveMapping.md#bpy.types.CurveMapping "bpy.types.CurveMapping"), (readonly)

pixel_aspect_x
    

Horizontal aspect ratio - for anamorphic or non-square pixel output

Type:
    

float in [1, 200], default 1.0

pixel_aspect_y
    

Vertical aspect ratio - for anamorphic or non-square pixel output

Type:
    

float in [1, 200], default 1.0

ppm_base
    

The base unit for pixels per meter.

Type:
    

float in [1e-05, 1e+06], default 0.0254

ppm_factor
    

The pixel density meta-data written to supported image formats. This value is multiplied by the PPM-base which defines the unit (typically inches or meters)

Type:
    

float in [1e-05, 1e+06], default 72.0

preview_pixel_size
    

Pixel size for viewport rendering

  * `AUTO` Automatic – Automatic pixel size, depends on the user interface scale.

  * `1` 1× – Render at full resolution.

  * `2` 2× – Render at 50% resolution.

  * `4` 4× – Render at 25% resolution.

  * `8` 8× – Render at 12.5% resolution.


Type:
    

enum in [`'AUTO'`, `'1'`, `'2'`, `'4'`, `'8'`], default `'AUTO'`

resolution_percentage
    

Percentage scale for render resolution

Type:
    

int in [1, 32767], default 100

resolution_x
    

Number of horizontal pixels in the rendered image

Type:
    

int in [4, 65536], default 1920

resolution_y
    

Number of vertical pixels in the rendered image

Type:
    

int in [4, 65536], default 1080

sequencer_gl_preview
    

Display method used in the sequencer view

Type:
    

enum in [Shading Type Items](../../bpy_types_enum_items/shading_type_items.md#rna-enum-shading-type-items), default `'SOLID'`

simplify_child_particles
    

Global child particles percentage

Type:
    

float in [0, 1], default 1.0

simplify_child_particles_render
    

Global child particles percentage during rendering

Type:
    

float in [0, 1], default 0.0

simplify_gpencil
    

Simplify Grease Pencil drawing

Type:
    

boolean, default False

simplify_gpencil_antialiasing
    

Use Antialiasing to smooth stroke edges

Type:
    

boolean, default True

simplify_gpencil_modifier
    

Display modifiers

Type:
    

boolean, default True

simplify_gpencil_onplay
    

Simplify Grease Pencil only during animation playback

Type:
    

boolean, default False

simplify_gpencil_shader_fx
    

Display Shader Effects

Type:
    

boolean, default True

simplify_gpencil_tint
    

Display layer tint

Type:
    

boolean, default True

simplify_gpencil_view_fill
    

Display fill strokes in the viewport

Type:
    

boolean, default True

simplify_subdivision
    

Global maximum subdivision level

Type:
    

int in [0, 32767], default 6

simplify_subdivision_render
    

Global maximum subdivision level during rendering

Type:
    

int in [0, 32767], default 0

simplify_volumes
    

Resolution percentage of volume objects in viewport

Type:
    

float in [0, 1], default 1.0

stamp_background
    

Color to use behind stamp text

Type:
    

float array of 4 items in [0, 1], default (0.0, 0.0, 0.0, 0.25)

stamp_font_size
    

Size of the font used when rendering stamp text

Type:
    

int in [8, 64], default 12

stamp_foreground
    

Color to use for stamp text

Type:
    

float array of 4 items in [0, 1], default (0.8, 0.8, 0.8, 1.0)

stamp_note_text
    

Custom text to appear in the stamp note

Type:
    

string, default “”, (never None)

stereo_views
    

Type:
    

[`bpy_prop_collection`](../_other/bpy.types.bpy_prop_collection.md#bpy.types.bpy_prop_collection "bpy.types.bpy_prop_collection") of [`SceneRenderView`](../S/bpy.types.SceneRenderView.md#bpy.types.SceneRenderView "bpy.types.SceneRenderView"), (readonly)

threads
    

Maximum number of CPU cores to use simultaneously while rendering (for multi-core/CPU systems)

Type:
    

int in [1, 1024], default 1

threads_mode
    

Determine the amount of render threads used

  * `AUTO` Auto-Detect – Automatically determine the number of threads, based on CPUs.

  * `FIXED` Fixed – Manually determine the number of threads.


Type:
    

enum in [`'AUTO'`, `'FIXED'`], default `'AUTO'`

use_border
    

Render a user-defined render region, within the frame size

Type:
    

boolean, default False

use_compositing
    

Process the render result through the compositing pipeline, if a compositing node group is assigned to the scene

Type:
    

boolean, default True

use_crop_to_border
    

Crop the rendered frame to the defined render region size

Type:
    

boolean, default False

use_file_extension
    

Add the file format extensions to the rendered file name (eg: filename + .jpg)

Type:
    

boolean, default True

use_freestyle
    

Draw stylized strokes using Freestyle

Type:
    

boolean, default False

use_high_quality_normals
    

Use high quality tangent space at the cost of lower performance

Type:
    

boolean, default False

use_lock_interface
    

Lock interface during rendering in favor of giving more memory to the renderer

Type:
    

boolean, default False

use_motion_blur
    

Use multi-sampled 3D scene motion blur

Type:
    

boolean, default False

use_multiview
    

Use multiple views in the scene

Type:
    

boolean, default False

use_overwrite
    

Overwrite existing files while rendering

Type:
    

boolean, default True

use_persistent_data
    

Keep render data around for faster re-renders and animation renders, at the cost of increased memory usage

Type:
    

boolean, default False

use_placeholder
    

Create empty placeholder files while rendering frames (similar to Unix ‘touch’)

Type:
    

boolean, default False

use_render_cache
    

Save render cache to EXR files (useful for heavy compositing, Note: affects indirectly rendered scenes)

Type:
    

boolean, default False

use_sequencer
    

Process the render (and composited) result through the video sequence editor pipeline, if sequencer strips exist

Type:
    

boolean, default True

use_sequencer_override_scene_strip
    

Use workbench render settings from the sequencer scene, instead of each individual scene used in the strip

Type:
    

boolean, default False

use_simplify
    

Enable simplification of scene for quicker preview renders

Type:
    

boolean, default False

use_simplify_normals
    

Skip computing custom normals and face corner normals for displaying meshes in the viewport

Type:
    

boolean, default False

use_single_layer
    

Only render the active layer. Only affects rendering from the interface, ignored for rendering from command line.

Type:
    

boolean, default False

use_spherical_stereo
    

Active render engine supports spherical stereo rendering

Type:
    

boolean, default False, (readonly)

use_stamp
    

Render the stamp info text in the rendered image

Type:
    

boolean, default False

use_stamp_camera
    

Include the name of the active camera in image metadata

Type:
    

boolean, default True

use_stamp_date
    

Include the current date in image/video metadata

Type:
    

boolean, default True

use_stamp_filename
    

Include the .blend filename in image/video metadata

Type:
    

boolean, default True

use_stamp_frame
    

Include the frame number in image metadata

Type:
    

boolean, default True

use_stamp_frame_range
    

Include the rendered frame range in image/video metadata

Type:
    

boolean, default False

use_stamp_hostname
    

Include the hostname of the machine that rendered the frame

Type:
    

boolean, default False

use_stamp_labels
    

Display stamp labels (“Camera” in front of camera name, etc.)

Type:
    

boolean, default True

use_stamp_lens
    

Include the active camera’s lens in image metadata

Type:
    

boolean, default False

use_stamp_marker
    

Include the name of the last marker in image metadata

Type:
    

boolean, default False

use_stamp_memory
    

Include the peak memory usage in image metadata

Type:
    

boolean, default True

use_stamp_note
    

Include a custom note in image/video metadata

Type:
    

boolean, default False

use_stamp_render_time
    

Include the render time in image metadata

Type:
    

boolean, default True

use_stamp_scene
    

Include the name of the active scene in image/video metadata

Type:
    

boolean, default True

use_stamp_sequencer_strip
    

Include the name of the foreground sequence strip in image metadata

Type:
    

boolean, default False

use_stamp_time
    

Include the rendered frame timecode as HH:MM:SS.FF in image metadata

Type:
    

boolean, default True

views
    

Type:
    

[`RenderViews`](bpy.types.RenderViews.md#bpy.types.RenderViews "bpy.types.RenderViews") [`bpy_prop_collection`](../_other/bpy.types.bpy_prop_collection.md#bpy.types.bpy_prop_collection "bpy.types.bpy_prop_collection") of [`SceneRenderView`](../S/bpy.types.SceneRenderView.md#bpy.types.SceneRenderView "bpy.types.SceneRenderView"), (readonly)

views_format
    

  * `STEREO_3D` Stereo 3D – Single stereo camera system, adjust the stereo settings in the camera panel.

  * `MULTIVIEW` Multi-View – Multi camera system, adjust the cameras individually.


Type:
    

enum in [`'STEREO_3D'`, `'MULTIVIEW'`], default `'STEREO_3D'`

frame_path(_*_ , _frame =-2147483648_, _preview =False_, _view =''_)
    

Return the absolute path to the filename to be written for a given frame

Parameters:
    

  * **frame** (_int in_ _[__-inf_ _,__inf_ _]__,__(__optional_ _)_) – Frame number to use, if unset the current frame will be used

  * **preview** (_boolean_ _,__(__optional_ _)_) – Preview, Use preview range

  * **view** (_string_ _,__(__optional_ _,__never None_ _)_) – View, The name of the view to use to replace the “%” chars


Returns:
    

File Path, The resulting filepath from the scenes render settings

Return type:
    

string, (never None)

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

## Inherited Properties

  * [`bpy_struct.id_data`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.id_data "bpy.types.bpy_struct.id_data")

| 


  
---|---  
  
## Inherited Functions

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
  
## References

  * [`RenderEngine.render`](bpy.types.RenderEngine.md#bpy.types.RenderEngine.render "bpy.types.RenderEngine.render")

| 

  * [`Scene.render`](../S/bpy.types.Scene.md#bpy.types.Scene.render "bpy.types.Scene.render")

  
---|---
  *[*]: Keyword-only parameters separator (PEP 3102)
  *[/]: Positional-only parameter separator (PEP 570)
