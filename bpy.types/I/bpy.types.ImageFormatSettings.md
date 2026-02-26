# ImageFormatSettings(bpy_struct)

base class — [`bpy_struct`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct "bpy.types.bpy_struct")

_class _bpy.types.ImageFormatSettings(_bpy_struct_)
    

Settings for image formats

cineon_black
    

Log conversion reference blackpoint

Type:
    

int in [0, 1024], default 0

cineon_gamma
    

Log conversion gamma

Type:
    

float in [0, 10], default 0.0

cineon_white
    

Log conversion reference whitepoint

Type:
    

int in [0, 1024], default 0

color_depth
    

Bit depth per channel

Type:
    

enum in [Image Color Depth Items](../../bpy_types_enum_items/image_color_depth_items.md#rna-enum-image-color-depth-items), default `'8'`

color_management
    

Which color management settings to use for file saving

Type:
    

enum in [`'FOLLOW_SCENE'`, `'OVERRIDE'`], default `'FOLLOW_SCENE'`

color_mode
    

Choose BW for saving grayscale images, RGB for saving red, green and blue channels, and RGBA for saving red, green, blue and alpha channels

Type:
    

enum in [Image Color Mode Items](../../bpy_types_enum_items/image_color_mode_items.md#rna-enum-image-color-mode-items), default `'RGBA'`

compression
    

Amount of time to determine best compression: 0 = no compression with fast file output, 100 = maximum lossless compression with slow file output

Type:
    

int in [0, 100], default 15

display_settings
    

Settings of device saved image would be displayed on

Type:
    

[`ColorManagedDisplaySettings`](../C/bpy.types.ColorManagedDisplaySettings.md#bpy.types.ColorManagedDisplaySettings "bpy.types.ColorManagedDisplaySettings"), (readonly)

exr_codec
    

Compression codec settings for OpenEXR

Type:
    

enum in [Exr Codec Items](../../bpy_types_enum_items/exr_codec_items.md#rna-enum-exr-codec-items), default `'NONE'`

file_format
    

File format to save the rendered images as

Type:
    

enum in [Image Type All Items](../../bpy_types_enum_items/image_type_all_items.md#rna-enum-image-type-all-items), default `'PNG'`

has_linear_colorspace
    

File format expects linear color space

Type:
    

boolean, default False, (readonly)

jpeg2k_codec
    

Codec settings for JPEG 2000

Type:
    

enum in [`'JP2'`, `'J2K'`], default `'JP2'`

linear_colorspace_settings
    

Output color space settings

Type:
    

[`ColorManagedInputColorspaceSettings`](../C/bpy.types.ColorManagedInputColorspaceSettings.md#bpy.types.ColorManagedInputColorspaceSettings "bpy.types.ColorManagedInputColorspaceSettings"), (readonly)

media_type
    

The type of media to save

Type:
    

enum in [`'IMAGE'`, `'MULTI_LAYER_IMAGE'`, `'VIDEO'`], default `'IMAGE'`

quality
    

Quality for image formats that support lossy compression

Type:
    

int in [0, 100], default 90

stereo_3d_format
    

Settings for stereo 3D

Type:
    

[`Stereo3dFormat`](../S/bpy.types.Stereo3dFormat.md#bpy.types.Stereo3dFormat "bpy.types.Stereo3dFormat"), (readonly, never None)

tiff_codec
    

Compression mode for TIFF

Type:
    

enum in [`'NONE'`, `'DEFLATE'`, `'LZW'`, `'PACKBITS'`], default `'DEFLATE'`

use_cineon_log
    

Convert to logarithmic color space

Type:
    

boolean, default False

use_exr_interleave
    

Use legacy interleaved storage of views, layers and passes for compatibility with applications that do not support more efficient multi-part OpenEXR files.

Type:
    

boolean, default False

use_jpeg2k_cinema_48
    

Use OpenJPEG Cinema Preset (48fps)

Type:
    

boolean, default False

use_jpeg2k_cinema_preset
    

Use OpenJPEG Cinema Preset

Type:
    

boolean, default False

use_jpeg2k_ycc
    

Save luminance-chrominance-chrominance channels instead of RGB colors

Type:
    

boolean, default False

use_preview
    

When rendering animations, save JPG preview images in same directory

Type:
    

boolean, default False

view_settings
    

Color management settings applied on image before saving

Type:
    

[`ColorManagedViewSettings`](../C/bpy.types.ColorManagedViewSettings.md#bpy.types.ColorManagedViewSettings "bpy.types.ColorManagedViewSettings"), (readonly)

views_format
    

Format of multiview media

Type:
    

enum in [Views Format Multiview Items](../../bpy_types_enum_items/views_format_multiview_items.md#rna-enum-views-format-multiview-items), default `'INDIVIDUAL'`

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

  * [`CompositorNodeOutputFile.format`](../C/bpy.types.CompositorNodeOutputFile.md#bpy.types.CompositorNodeOutputFile.format "bpy.types.CompositorNodeOutputFile.format")
  * [`NodeCompositorFileOutputItem.format`](../N/bpy.types.NodeCompositorFileOutputItem.md#bpy.types.NodeCompositorFileOutputItem.format "bpy.types.NodeCompositorFileOutputItem.format")
  * [`BakeSettings.image_settings`](../B/bpy.types.BakeSettings.md#bpy.types.BakeSettings.image_settings "bpy.types.BakeSettings.image_settings")

| 

  * [`RenderSettings.image_settings`](../R/bpy.types.RenderSettings.md#bpy.types.RenderSettings.image_settings "bpy.types.RenderSettings.image_settings")
  * [`UILayout.template_image_settings`](../U/bpy.types.UILayout.md#bpy.types.UILayout.template_image_settings "bpy.types.UILayout.template_image_settings")
  * [`UILayout.template_image_views`](../U/bpy.types.UILayout.md#bpy.types.UILayout.template_image_views "bpy.types.UILayout.template_image_views")

  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
