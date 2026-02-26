# Image(ID)

## Image Data

The Image data-block is a shallow wrapper around image or video file(s) (on disk, as packed data, or generated).

All actual data like the pixel buffer, size, resolution etc. is cached in an `imbuf.types.ImBuf` image buffer (or several buffers in some cases, like UDIM textures, multi-views, animations…).

Several properties and functions of the Image data-block are then actually using/modifying its image buffer, and not the Image data-block itself.

Warning

One key limitation is that image buffers are not shared between different Image data-blocks, and they are not duplicated when copying an image.

So until a modified image buffer is saved on disk, duplicating its Image data-block will not propagate the underlying buffer changes to the new Image.

This example script generates an Image data-block with a given size, change its first pixel, rescale it, and duplicates the image.

The duplicated image still has the same size and colors as the original image at its creation, all editing in the original image’s buffer is ‘lost’ in its copy.
    
    
    import bpy
    
    image_src = bpy.data.images.new('src', 1024, 102)
    print(image_src.size)
    print(image_src.pixels[0:4])
    
    image_src.scale(1024, 720)
    image_src.pixels[0:4] = (0.5, 0.5, 0.5, 0.5)
    image_src.update()
    print(image_src.size)
    print(image_src.pixels[0:4])
    
    image_dest = image_src.copy()
    image_dest.update()
    print(image_dest.size)
    print(image_dest.pixels[0:4])
    

base classes — [[bpy_struct]], [[ID]]

_class _bpy.types.Image(_ID_)
    

Image data-block referencing an external or packed image

alpha_mode
    

Representation of alpha in the image file, to convert to and from when saving and loading the image

  * `STRAIGHT` Straight – Store RGB and alpha channels separately with alpha acting as a mask, also known as unassociated alpha. Commonly used by image editing applications and file formats like PNG..

  * `PREMUL` Premultiplied – Store RGB channels with alpha multiplied in, also known as associated alpha. The natural format for renders and used by file formats like OpenEXR..

  * `CHANNEL_PACKED` Channel Packed – Different images are packed in the RGB and alpha channels, and they should not affect each other. Channel packing is commonly used by game engines to save memory..

  * `NONE` None – Ignore alpha channel from the file and make image fully opaque.


Type:
    

enum in [`'STRAIGHT'`, `'PREMUL'`, `'CHANNEL_PACKED'`, `'NONE'`], default `'STRAIGHT'`

channels
    

Number of channels in pixels buffer

Type:
    

int in [0, inf], default 0, (readonly)

colorspace_settings
    

Input color space settings

Type:
    

[[ColorManagedInputColorspaceSettings]], (readonly)

depth
    

Image bit depth

Type:
    

int in [0, inf], default 0, (readonly)

display_aspect
    

Display Aspect for this image, does not affect rendering

Type:
    

[[mathutils.Vector]] of 2 items in [0.1, inf], default (1.0, 1.0)

file_format
    

Format used for re-saving this file

Type:
    

enum in [Image Type All Items](../../bpy_types_enum_items/image_type_all_items.md#rna-enum-image-type-all-items), default `'TARGA'`

filepath
    

Image/Movie file name

Type:
    

string, default “”, (never None, blend relative `//` prefix supported)

filepath_raw
    

Image/Movie file name (without data refreshing)

Type:
    

string, default “”, (never None, blend relative `//` prefix supported)

frame_duration
    

Duration (in frames) of the image (1 when not a video/sequence)

Type:
    

int in [0, inf], default 0, (readonly)

generated_color
    

Fill color for the generated image

Type:
    

float array of 4 items in [0, inf], default (0.0, 0.0, 0.0, 0.0)

generated_height
    

Generated image height

Type:
    

int in [1, 65536], default 1024

generated_type
    

Generated image type

Type:
    

enum in [Image Generated Type Items](../../bpy_types_enum_items/image_generated_type_items.md#rna-enum-image-generated-type-items), default `'UV_GRID'`

generated_width
    

Generated image width

Type:
    

int in [1, 65536], default 1024

has_data
    

True if the image data is loaded into memory

Type:
    

boolean, default False, (readonly)

is_dirty
    

Image has changed and is not saved

Type:
    

boolean, default False, (readonly)

is_float
    

True if this image is stored in floating-point buffer

Type:
    

boolean, default False, (readonly)

is_multiview
    

Image has more than one view

Type:
    

boolean, default False, (readonly)

is_stereo_3d
    

Image has left and right views

Type:
    

boolean, default False, (readonly)

packed_file
    

First packed file of the image

Type:
    

[[PackedFile]], (readonly)

packed_files
    

Collection of packed images

Type:
    

[[bpy_prop_collection]] of [[ImagePackedFile]], (readonly)

pixels
    

Image buffer pixels in floating-point values

Type:
    

float in [-inf, inf], default 0.0

render_slots
    

Render slots of the image

Type:
    

[[RenderSlots]] [[bpy_prop_collection]] of [[RenderSlot]], (readonly)

resolution
    

X/Y pixels per meter, for the image buffer

Type:
    

[[mathutils.Vector]] of 2 items in [-inf, inf], default (0.0, 0.0)

seam_margin
    

Margin to take into account when fixing UV seams during painting. Higher number would improve seam-fixes for mipmaps, but decreases performance.

Type:
    

int in [-32768, 32767], default 8

size
    

Width and height of the image buffer in pixels, zero when image data cannot be loaded

Type:
    

int array of 2 items in [-inf, inf], default (0, 0), (readonly)

source
    

Where the image comes from

  * `FILE` Single Image – Single image file.

  * `SEQUENCE` Image Sequence – Multiple image files, as a sequence.

  * `MOVIE` Movie – Movie file.

  * `GENERATED` Generated – Generated image.

  * `VIEWER` Viewer – Compositing node viewer.

  * `TILED` UDIM Tiles – Tiled UDIM image texture.


Type:
    

enum in [`'FILE'`, `'SEQUENCE'`, `'MOVIE'`, `'GENERATED'`, `'VIEWER'`, `'TILED'`], default `'FILE'`

stereo_3d_format
    

Settings for stereo 3d

Type:
    

[[Stereo3dFormat]], (readonly, never None)

tiles
    

Tiles of the image

Type:
    

[[UDIMTiles]] [[bpy_prop_collection]] of [[UDIMTile]], (readonly)

type
    

How to generate the image

Type:
    

enum in [`'IMAGE'`, `'MULTILAYER'`, `'UV_TEST'`, `'RENDER_RESULT'`, `'COMPOSITING'`], default `'IMAGE'`, (readonly)

use_deinterlace
    

Deinterlace movie file on load

Type:
    

boolean, default False

use_generated_float
    

Generate floating-point buffer

Type:
    

boolean, default False

use_half_precision
    

Use 16 bits per channel to lower the memory usage during rendering

Type:
    

boolean, default True

use_multiview
    

Use Multiple Views (when available)

Type:
    

boolean, default False

use_view_as_render
    

Apply render part of display transformation when displaying this image on the screen

Type:
    

boolean, default False

views_format
    

Mode to load image views

Type:
    

enum in [Views Format Items](../../bpy_types_enum_items/views_format_items.md#rna-enum-views-format-items), default `'INDIVIDUAL'`

save_render(_filepath_ , _*_ , _scene =None_, _quality =0_)
    

Save image to a specific path using a scenes render settings

Parameters:
    

  * **filepath** (_string_ _,__(__never None_ _)_) – Output path

  * **scene** ([[Scene]], (optional)) – Scene to take image parameters from

  * **quality** (_int in_ _[__0_ _,__100_ _]__,__(__optional_ _)_) – Quality, Quality for image formats that support lossy compression, uses default quality if not specified


save(_*_ , _filepath =''_, _quality =0_, _save_copy =False_)
    

Save image

Parameters:
    

  * **filepath** (_string_ _,__(__optional_ _,__never None_ _)_) – Output path, uses image data-block filepath if not specified

  * **quality** (_int in_ _[__0_ _,__100_ _]__,__(__optional_ _)_) – Quality, Quality for image formats that support lossy compression, uses default quality if not specified

  * **save_copy** (_boolean_ _,__(__optional_ _)_) – Save Copy, Save the image as a copy, without updating current image’s filepath


pack(_*_ , _data =''_, _data_len =0_)
    

Pack an image as embedded data into the .blend file

Parameters:
    

  * **data** (_byte string_ _,__(__optional_ _,__never None_ _)_) – data, Raw data (bytes, exact content of the embedded file)

  * **data_len** (_int in_ _[__0_ _,__inf_ _]__,__(__optional_ _)_) – data_len, length of given data (mandatory if data is provided)


unpack(_*_ , _method ='USE_LOCAL'_)
    

Save an image packed in the .blend file to disk

Parameters:
    

**method** (enum in [Unpack Method Items](../../bpy_types_enum_items/unpack_method_items.md#rna-enum-unpack-method-items), (optional)) – method, How to unpack

reload()
    

Reload the image from its source path

update()
    

Update the display image from the floating-point buffer

scale(_width_ , _height_ , _*_ , _frame =0_, _tile_index =0_)
    

Scale the buffer of the image, in pixels

Parameters:
    

  * **width** (_int in_ _[__1_ _,__inf_ _]_) – Width

  * **height** (_int in_ _[__1_ _,__inf_ _]_) – Height

  * **frame** (_int in_ _[__0_ _,__inf_ _]__,__(__optional_ _)_) – Frame, Frame (for image sequences)

  * **tile_index** (_int in_ _[__0_ _,__inf_ _]__,__(__optional_ _)_) – Tile, Tile index (for tiled images)


gl_touch(_*_ , _frame =0_, _layer_index =0_, _pass_index =0_)
    

Delay the image from being cleaned from the cache due inactivity

Parameters:
    

  * **frame** (_int in_ _[__0_ _,__inf_ _]__,__(__optional_ _)_) – Frame, Frame of image sequence or movie

  * **layer_index** (_int in_ _[__0_ _,__inf_ _]__,__(__optional_ _)_) – Layer, Index of layer that should be loaded

  * **pass_index** (_int in_ _[__0_ _,__inf_ _]__,__(__optional_ _)_) – Pass, Index of pass that should be loaded


Returns:
    

Error, OpenGL error value

Return type:
    

int in [-inf, inf]

gl_load(_*_ , _frame =0_, _layer_index =0_, _pass_index =0_)
    

Load the image into an OpenGL texture. On success, image.bindcode will contain the OpenGL texture bindcode. Colors read from the texture will be in scene linear color space and have premultiplied or straight alpha matching the image alpha mode.

Parameters:
    

  * **frame** (_int in_ _[__0_ _,__inf_ _]__,__(__optional_ _)_) – Frame, Frame of image sequence or movie

  * **layer_index** (_int in_ _[__0_ _,__inf_ _]__,__(__optional_ _)_) – Layer, Index of layer that should be loaded

  * **pass_index** (_int in_ _[__0_ _,__inf_ _]__,__(__optional_ _)_) – Pass, Index of pass that should be loaded


Returns:
    

Error, OpenGL error value

Return type:
    

int in [-inf, inf]

gl_free()
    

Free the image from OpenGL graphics memory

filepath_from_user(_*_ , _image_user =None_)
    

Return the absolute path to the filepath of an image frame specified by the image user

Parameters:
    

**image_user** ([[ImageUser]], (optional)) – Image user of the image to get filepath for

Returns:
    

File Path, The resulting filepath from the image and its user

Return type:
    

string, (never None)

buffers_free()
    

Free the image buffers from memory

_classmethod _bl_rna_get_subclass(_id_ , _default =None_, _/_)
    

Parameters:
    

**id** (_str_) – The RNA type identifier.

Returns:
    

The RNA type or default when not found.

Return type:
    

[[bpy.types.Struct]] subclass

_classmethod _bl_rna_get_subclass_py(_id_ , _default =None_, _/_)
    

Parameters:
    

**id** (_str_) – The RNA type identifier.

Returns:
    

The class or default when not found.

Return type:
    

type

### Inherited Properties

  * [[bpy_struct.id_data]]
  * [[ID.name]]
  * [[ID.name_full]]
  * [[ID.id_type]]
  * [[ID.session_uid]]
  * [[ID.is_evaluated]]
  * [[ID.original]]
  * [[ID.users]]
  * [[ID.use_fake_user]]
  * [[ID.use_extra_user]]
  * [[ID.is_embedded_data]]

| 

  * [[ID.is_linked_packed]]
  * [[ID.is_missing]]
  * [[ID.is_runtime_data]]
  * [[ID.is_editable]]
  * [[ID.tag]]
  * [[ID.is_library_indirect]]
  * [[ID.library]]
  * [[ID.library_weak_reference]]
  * [[ID.asset_data]]
  * [[ID.override_library]]
  * [[ID.preview]]

  
---|---  
  
### Inherited Functions

  * [[bpy_struct.as_pointer]]
  * [[bpy_struct.driver_add]]
  * [[bpy_struct.driver_remove]]
  * [[bpy_struct.get]]
  * [[bpy_struct.id_properties_clear]]
  * [[bpy_struct.id_properties_ensure]]
  * [[bpy_struct.id_properties_ui]]
  * [[bpy_struct.is_property_hidden]]
  * [[bpy_struct.is_property_overridable_library]]
  * [[bpy_struct.is_property_readonly]]
  * [[bpy_struct.is_property_set]]
  * [[bpy_struct.items]]
  * [[bpy_struct.keyframe_delete]]
  * [[bpy_struct.keyframe_insert]]
  * [[bpy_struct.keys]]
  * [[bpy_struct.path_from_id]]
  * [[bpy_struct.path_from_module]]
  * [[bpy_struct.path_resolve]]
  * [[bpy_struct.pop]]
  * [[bpy_struct.property_overridable_library_set]]
  * [[bpy_struct.property_unset]]
  * [[bpy_struct.rna_ancestors]]

| 

  * [[bpy_struct.type_recast]]
  * [[bpy_struct.values]]
  * [[ID.bl_system_properties_get]]
  * [[ID.rename]]
  * [[ID.evaluated_get]]
  * [[ID.copy]]
  * [[ID.asset_mark]]
  * [[ID.asset_clear]]
  * [[ID.asset_generate_preview]]
  * [[ID.override_create]]
  * [[ID.override_hierarchy_create]]
  * [[ID.user_clear]]
  * [[ID.user_remap]]
  * [[ID.make_local]]
  * [[ID.user_of_id]]
  * [[ID.animation_data_create]]
  * [[ID.animation_data_clear]]
  * [[ID.update_tag]]
  * [[ID.preview_ensure]]
  * [[ID.bl_rna_get_subclass]]
  * [[ID.bl_rna_get_subclass_py]]

  
---|---  
  
### References

  * [[bpy.context.edit_image]]
  * [[BlendData.images]]
  * [[BlendDataImages.load]]
  * [[BlendDataImages.new]]
  * [[BlendDataImages.remove]]
  * [[CameraBackgroundImage.image]]
  * [[CompositorNodeCryptomatteV2.image]]
  * [[CompositorNodeImage.image]]
  * [[GeometryNodeInputImage.image]]
  * [[ImagePaint.canvas]]
  * [[ImagePaint.clone_image]]
  * [[ImagePaint.stencil_image]]
  * [[ImageTexture.image]]

| 

  * [[Material.texture_paint_images]]
  * [[MaterialGPencilStyle.fill_image]]
  * [[MaterialGPencilStyle.stroke_image]]
  * [[MovieTrackingPlaneTrack.image]]
  * [[NodeSocketImage.default_value]]
  * [[NodeTreeInterfaceSocketImage.default_value]]
  * [[PaintModeSettings.canvas_image]]
  * [[ShaderNodeTexEnvironment.image]]
  * [[ShaderNodeTexImage.image]]
  * [[SpaceImageEditor.image]]
  * [[TextureNodeImage.image]]
  * [[UILayout.template_image_layers]]

  
---|---
  *[*]: Keyword-only parameters separator (PEP 3102)
  *[/]: Positional-only parameter separator (PEP 570)
