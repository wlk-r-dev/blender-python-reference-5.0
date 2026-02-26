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
    

base classes — [`bpy_struct`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct "bpy.types.bpy_struct"), [`ID`](bpy.types.ID.md#bpy.types.ID "bpy.types.ID")

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
    

[`ColorManagedInputColorspaceSettings`](../C/bpy.types.ColorManagedInputColorspaceSettings.md#bpy.types.ColorManagedInputColorspaceSettings "bpy.types.ColorManagedInputColorspaceSettings"), (readonly)

depth
    

Image bit depth

Type:
    

int in [0, inf], default 0, (readonly)

display_aspect
    

Display Aspect for this image, does not affect rendering

Type:
    

[`mathutils.Vector`](mathutils.md#mathutils.Vector "mathutils.Vector") of 2 items in [0.1, inf], default (1.0, 1.0)

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
    

[`PackedFile`](../P/bpy.types.PackedFile.md#bpy.types.PackedFile "bpy.types.PackedFile"), (readonly)

packed_files
    

Collection of packed images

Type:
    

[`bpy_prop_collection`](../_other/bpy.types.bpy_prop_collection.md#bpy.types.bpy_prop_collection "bpy.types.bpy_prop_collection") of [`ImagePackedFile`](bpy.types.ImagePackedFile.md#bpy.types.ImagePackedFile "bpy.types.ImagePackedFile"), (readonly)

pixels
    

Image buffer pixels in floating-point values

Type:
    

float in [-inf, inf], default 0.0

render_slots
    

Render slots of the image

Type:
    

[`RenderSlots`](../R/bpy.types.RenderSlots.md#bpy.types.RenderSlots "bpy.types.RenderSlots") [`bpy_prop_collection`](../_other/bpy.types.bpy_prop_collection.md#bpy.types.bpy_prop_collection "bpy.types.bpy_prop_collection") of [`RenderSlot`](../R/bpy.types.RenderSlot.md#bpy.types.RenderSlot "bpy.types.RenderSlot"), (readonly)

resolution
    

X/Y pixels per meter, for the image buffer

Type:
    

[`mathutils.Vector`](mathutils.md#mathutils.Vector "mathutils.Vector") of 2 items in [-inf, inf], default (0.0, 0.0)

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
    

[`Stereo3dFormat`](../S/bpy.types.Stereo3dFormat.md#bpy.types.Stereo3dFormat "bpy.types.Stereo3dFormat"), (readonly, never None)

tiles
    

Tiles of the image

Type:
    

[`UDIMTiles`](../U/bpy.types.UDIMTiles.md#bpy.types.UDIMTiles "bpy.types.UDIMTiles") [`bpy_prop_collection`](../_other/bpy.types.bpy_prop_collection.md#bpy.types.bpy_prop_collection "bpy.types.bpy_prop_collection") of [`UDIMTile`](../U/bpy.types.UDIMTile.md#bpy.types.UDIMTile "bpy.types.UDIMTile"), (readonly)

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

  * **scene** ([`Scene`](../S/bpy.types.Scene.md#bpy.types.Scene "bpy.types.Scene"), (optional)) – Scene to take image parameters from

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
    

**image_user** ([`ImageUser`](bpy.types.ImageUser.md#bpy.types.ImageUser "bpy.types.ImageUser"), (optional)) – Image user of the image to get filepath for

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
  * [`ID.name`](bpy.types.ID.md#bpy.types.ID.name "bpy.types.ID.name")
  * [`ID.name_full`](bpy.types.ID.md#bpy.types.ID.name_full "bpy.types.ID.name_full")
  * [`ID.id_type`](bpy.types.ID.md#bpy.types.ID.id_type "bpy.types.ID.id_type")
  * [`ID.session_uid`](bpy.types.ID.md#bpy.types.ID.session_uid "bpy.types.ID.session_uid")
  * [`ID.is_evaluated`](bpy.types.ID.md#bpy.types.ID.is_evaluated "bpy.types.ID.is_evaluated")
  * [`ID.original`](bpy.types.ID.md#bpy.types.ID.original "bpy.types.ID.original")
  * [`ID.users`](bpy.types.ID.md#bpy.types.ID.users "bpy.types.ID.users")
  * [`ID.use_fake_user`](bpy.types.ID.md#bpy.types.ID.use_fake_user "bpy.types.ID.use_fake_user")
  * [`ID.use_extra_user`](bpy.types.ID.md#bpy.types.ID.use_extra_user "bpy.types.ID.use_extra_user")
  * [`ID.is_embedded_data`](bpy.types.ID.md#bpy.types.ID.is_embedded_data "bpy.types.ID.is_embedded_data")

| 

  * [`ID.is_linked_packed`](bpy.types.ID.md#bpy.types.ID.is_linked_packed "bpy.types.ID.is_linked_packed")
  * [`ID.is_missing`](bpy.types.ID.md#bpy.types.ID.is_missing "bpy.types.ID.is_missing")
  * [`ID.is_runtime_data`](bpy.types.ID.md#bpy.types.ID.is_runtime_data "bpy.types.ID.is_runtime_data")
  * [`ID.is_editable`](bpy.types.ID.md#bpy.types.ID.is_editable "bpy.types.ID.is_editable")
  * [`ID.tag`](bpy.types.ID.md#bpy.types.ID.tag "bpy.types.ID.tag")
  * [`ID.is_library_indirect`](bpy.types.ID.md#bpy.types.ID.is_library_indirect "bpy.types.ID.is_library_indirect")
  * [`ID.library`](bpy.types.ID.md#bpy.types.ID.library "bpy.types.ID.library")
  * [`ID.library_weak_reference`](bpy.types.ID.md#bpy.types.ID.library_weak_reference "bpy.types.ID.library_weak_reference")
  * [`ID.asset_data`](bpy.types.ID.md#bpy.types.ID.asset_data "bpy.types.ID.asset_data")
  * [`ID.override_library`](bpy.types.ID.md#bpy.types.ID.override_library "bpy.types.ID.override_library")
  * [`ID.preview`](bpy.types.ID.md#bpy.types.ID.preview "bpy.types.ID.preview")

  
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

| 

  * [`bpy_struct.type_recast`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.type_recast "bpy.types.bpy_struct.type_recast")
  * [`bpy_struct.values`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.values "bpy.types.bpy_struct.values")
  * [`ID.bl_system_properties_get`](bpy.types.ID.md#bpy.types.ID.bl_system_properties_get "bpy.types.ID.bl_system_properties_get")
  * [`ID.rename`](bpy.types.ID.md#bpy.types.ID.rename "bpy.types.ID.rename")
  * [`ID.evaluated_get`](bpy.types.ID.md#bpy.types.ID.evaluated_get "bpy.types.ID.evaluated_get")
  * [`ID.copy`](bpy.types.ID.md#bpy.types.ID.copy "bpy.types.ID.copy")
  * [`ID.asset_mark`](bpy.types.ID.md#bpy.types.ID.asset_mark "bpy.types.ID.asset_mark")
  * [`ID.asset_clear`](bpy.types.ID.md#bpy.types.ID.asset_clear "bpy.types.ID.asset_clear")
  * [`ID.asset_generate_preview`](bpy.types.ID.md#bpy.types.ID.asset_generate_preview "bpy.types.ID.asset_generate_preview")
  * [`ID.override_create`](bpy.types.ID.md#bpy.types.ID.override_create "bpy.types.ID.override_create")
  * [`ID.override_hierarchy_create`](bpy.types.ID.md#bpy.types.ID.override_hierarchy_create "bpy.types.ID.override_hierarchy_create")
  * [`ID.user_clear`](bpy.types.ID.md#bpy.types.ID.user_clear "bpy.types.ID.user_clear")
  * [`ID.user_remap`](bpy.types.ID.md#bpy.types.ID.user_remap "bpy.types.ID.user_remap")
  * [`ID.make_local`](bpy.types.ID.md#bpy.types.ID.make_local "bpy.types.ID.make_local")
  * [`ID.user_of_id`](bpy.types.ID.md#bpy.types.ID.user_of_id "bpy.types.ID.user_of_id")
  * [`ID.animation_data_create`](bpy.types.ID.md#bpy.types.ID.animation_data_create "bpy.types.ID.animation_data_create")
  * [`ID.animation_data_clear`](bpy.types.ID.md#bpy.types.ID.animation_data_clear "bpy.types.ID.animation_data_clear")
  * [`ID.update_tag`](bpy.types.ID.md#bpy.types.ID.update_tag "bpy.types.ID.update_tag")
  * [`ID.preview_ensure`](bpy.types.ID.md#bpy.types.ID.preview_ensure "bpy.types.ID.preview_ensure")
  * [`ID.bl_rna_get_subclass`](bpy.types.ID.md#bpy.types.ID.bl_rna_get_subclass "bpy.types.ID.bl_rna_get_subclass")
  * [`ID.bl_rna_get_subclass_py`](bpy.types.ID.md#bpy.types.ID.bl_rna_get_subclass_py "bpy.types.ID.bl_rna_get_subclass_py")

  
---|---  
  
### References

  * [`bpy.context.edit_image`](../../bpy.context.md#bpy.context.edit_image "bpy.context.edit_image")
  * [`BlendData.images`](../B/bpy.types.BlendData.md#bpy.types.BlendData.images "bpy.types.BlendData.images")
  * [`BlendDataImages.load`](../B/bpy.types.BlendDataImages.md#bpy.types.BlendDataImages.load "bpy.types.BlendDataImages.load")
  * [`BlendDataImages.new`](../B/bpy.types.BlendDataImages.md#bpy.types.BlendDataImages.new "bpy.types.BlendDataImages.new")
  * [`BlendDataImages.remove`](../B/bpy.types.BlendDataImages.md#bpy.types.BlendDataImages.remove "bpy.types.BlendDataImages.remove")
  * [`CameraBackgroundImage.image`](../C/bpy.types.CameraBackgroundImage.md#bpy.types.CameraBackgroundImage.image "bpy.types.CameraBackgroundImage.image")
  * [`CompositorNodeCryptomatteV2.image`](../C/bpy.types.CompositorNodeCryptomatteV2.md#bpy.types.CompositorNodeCryptomatteV2.image "bpy.types.CompositorNodeCryptomatteV2.image")
  * [`CompositorNodeImage.image`](../C/bpy.types.CompositorNodeImage.md#bpy.types.CompositorNodeImage.image "bpy.types.CompositorNodeImage.image")
  * [`GeometryNodeInputImage.image`](../G/bpy.types.GeometryNodeInputImage.md#bpy.types.GeometryNodeInputImage.image "bpy.types.GeometryNodeInputImage.image")
  * [`ImagePaint.canvas`](bpy.types.ImagePaint.md#bpy.types.ImagePaint.canvas "bpy.types.ImagePaint.canvas")
  * [`ImagePaint.clone_image`](bpy.types.ImagePaint.md#bpy.types.ImagePaint.clone_image "bpy.types.ImagePaint.clone_image")
  * [`ImagePaint.stencil_image`](bpy.types.ImagePaint.md#bpy.types.ImagePaint.stencil_image "bpy.types.ImagePaint.stencil_image")
  * [`ImageTexture.image`](bpy.types.ImageTexture.md#bpy.types.ImageTexture.image "bpy.types.ImageTexture.image")

| 

  * [`Material.texture_paint_images`](../M/bpy.types.Material.md#bpy.types.Material.texture_paint_images "bpy.types.Material.texture_paint_images")
  * [`MaterialGPencilStyle.fill_image`](../M/bpy.types.MaterialGPencilStyle.md#bpy.types.MaterialGPencilStyle.fill_image "bpy.types.MaterialGPencilStyle.fill_image")
  * [`MaterialGPencilStyle.stroke_image`](../M/bpy.types.MaterialGPencilStyle.md#bpy.types.MaterialGPencilStyle.stroke_image "bpy.types.MaterialGPencilStyle.stroke_image")
  * [`MovieTrackingPlaneTrack.image`](../M/bpy.types.MovieTrackingPlaneTrack.md#bpy.types.MovieTrackingPlaneTrack.image "bpy.types.MovieTrackingPlaneTrack.image")
  * [`NodeSocketImage.default_value`](../N/bpy.types.NodeSocketImage.md#bpy.types.NodeSocketImage.default_value "bpy.types.NodeSocketImage.default_value")
  * [`NodeTreeInterfaceSocketImage.default_value`](../N/bpy.types.NodeTreeInterfaceSocketImage.md#bpy.types.NodeTreeInterfaceSocketImage.default_value "bpy.types.NodeTreeInterfaceSocketImage.default_value")
  * [`PaintModeSettings.canvas_image`](../P/bpy.types.PaintModeSettings.md#bpy.types.PaintModeSettings.canvas_image "bpy.types.PaintModeSettings.canvas_image")
  * [`ShaderNodeTexEnvironment.image`](../S/bpy.types.ShaderNodeTexEnvironment.md#bpy.types.ShaderNodeTexEnvironment.image "bpy.types.ShaderNodeTexEnvironment.image")
  * [`ShaderNodeTexImage.image`](../S/bpy.types.ShaderNodeTexImage.md#bpy.types.ShaderNodeTexImage.image "bpy.types.ShaderNodeTexImage.image")
  * [`SpaceImageEditor.image`](../S/bpy.types.SpaceImageEditor.md#bpy.types.SpaceImageEditor.image "bpy.types.SpaceImageEditor.image")
  * [`TextureNodeImage.image`](../T/bpy.types.TextureNodeImage.md#bpy.types.TextureNodeImage.image "bpy.types.TextureNodeImage.image")
  * [`UILayout.template_image_layers`](../U/bpy.types.UILayout.md#bpy.types.UILayout.template_image_layers "bpy.types.UILayout.template_image_layers")

  
---|---
  *[*]: Keyword-only parameters separator (PEP 3102)
  *[/]: Positional-only parameter separator (PEP 570)
