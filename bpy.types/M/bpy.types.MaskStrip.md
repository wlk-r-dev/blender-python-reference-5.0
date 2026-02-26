# MaskStrip(Strip)

base classes — [`bpy_struct`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct "bpy.types.bpy_struct"), [`Strip`](../S/bpy.types.Strip.md#bpy.types.Strip "bpy.types.Strip")

_class _bpy.types.MaskStrip(_Strip_)
    

Sequence strip to load a video from a mask

alpha_mode
    

Representation of alpha information in the RGBA pixels

  * `STRAIGHT` Straight – RGB channels in transparent pixels are unaffected by the alpha channel.

  * `PREMUL` Premultiplied – RGB channels in transparent pixels are multiplied by the alpha channel.


Type:
    

enum in [`'STRAIGHT'`, `'PREMUL'`], default `'STRAIGHT'`

animation_offset_end
    

Animation end offset (trim end)

Type:
    

int in [0, inf], default 0

animation_offset_start
    

Animation start offset (trim start)

Type:
    

int in [0, inf], default 0

color_multiply
    

Type:
    

float in [0, 20], default 1.0

color_saturation
    

Adjust the intensity of the input’s color

Type:
    

float in [0, 20], default 1.0

crop
    

Type:
    

[`StripCrop`](../S/bpy.types.StripCrop.md#bpy.types.StripCrop "bpy.types.StripCrop"), (readonly)

mask
    

Mask that this strip uses

Type:
    

[`Mask`](bpy.types.Mask.md#bpy.types.Mask "bpy.types.Mask")

multiply_alpha
    

Multiply alpha along with color channels

Type:
    

boolean, default False

strobe
    

Only display every nth frame

Type:
    

float in [1, 30], default 0.0

transform
    

Type:
    

[`StripTransform`](../S/bpy.types.StripTransform.md#bpy.types.StripTransform "bpy.types.StripTransform"), (readonly)

use_deinterlace
    

Remove fields from video movies

Type:
    

boolean, default False

use_flip_x
    

Flip on the X axis

Type:
    

boolean, default False

use_flip_y
    

Flip on the Y axis

Type:
    

boolean, default False

use_float
    

Convert input to float data

Type:
    

boolean, default False

use_reverse_frames
    

Reverse frame order

Type:
    

boolean, default False

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
  * [`Strip.name`](../S/bpy.types.Strip.md#bpy.types.Strip.name "bpy.types.Strip.name")
  * [`Strip.type`](../S/bpy.types.Strip.md#bpy.types.Strip.type "bpy.types.Strip.type")
  * [`Strip.select`](../S/bpy.types.Strip.md#bpy.types.Strip.select "bpy.types.Strip.select")
  * [`Strip.select_left_handle`](../S/bpy.types.Strip.md#bpy.types.Strip.select_left_handle "bpy.types.Strip.select_left_handle")
  * [`Strip.select_right_handle`](../S/bpy.types.Strip.md#bpy.types.Strip.select_right_handle "bpy.types.Strip.select_right_handle")
  * [`Strip.mute`](../S/bpy.types.Strip.md#bpy.types.Strip.mute "bpy.types.Strip.mute")
  * [`Strip.lock`](../S/bpy.types.Strip.md#bpy.types.Strip.lock "bpy.types.Strip.lock")
  * [`Strip.frame_final_duration`](../S/bpy.types.Strip.md#bpy.types.Strip.frame_final_duration "bpy.types.Strip.frame_final_duration")
  * [`Strip.frame_duration`](../S/bpy.types.Strip.md#bpy.types.Strip.frame_duration "bpy.types.Strip.frame_duration")
  * [`Strip.frame_start`](../S/bpy.types.Strip.md#bpy.types.Strip.frame_start "bpy.types.Strip.frame_start")
  * [`Strip.frame_final_start`](../S/bpy.types.Strip.md#bpy.types.Strip.frame_final_start "bpy.types.Strip.frame_final_start")

| 

  * [`Strip.frame_final_end`](../S/bpy.types.Strip.md#bpy.types.Strip.frame_final_end "bpy.types.Strip.frame_final_end")
  * [`Strip.frame_offset_start`](../S/bpy.types.Strip.md#bpy.types.Strip.frame_offset_start "bpy.types.Strip.frame_offset_start")
  * [`Strip.frame_offset_end`](../S/bpy.types.Strip.md#bpy.types.Strip.frame_offset_end "bpy.types.Strip.frame_offset_end")
  * [`Strip.channel`](../S/bpy.types.Strip.md#bpy.types.Strip.channel "bpy.types.Strip.channel")
  * [`Strip.use_linear_modifiers`](../S/bpy.types.Strip.md#bpy.types.Strip.use_linear_modifiers "bpy.types.Strip.use_linear_modifiers")
  * [`Strip.blend_type`](../S/bpy.types.Strip.md#bpy.types.Strip.blend_type "bpy.types.Strip.blend_type")
  * [`Strip.blend_alpha`](../S/bpy.types.Strip.md#bpy.types.Strip.blend_alpha "bpy.types.Strip.blend_alpha")
  * [`Strip.effect_fader`](../S/bpy.types.Strip.md#bpy.types.Strip.effect_fader "bpy.types.Strip.effect_fader")
  * [`Strip.use_default_fade`](../S/bpy.types.Strip.md#bpy.types.Strip.use_default_fade "bpy.types.Strip.use_default_fade")
  * [`Strip.color_tag`](../S/bpy.types.Strip.md#bpy.types.Strip.color_tag "bpy.types.Strip.color_tag")
  * [`Strip.modifiers`](../S/bpy.types.Strip.md#bpy.types.Strip.modifiers "bpy.types.Strip.modifiers")
  * [`Strip.show_retiming_keys`](../S/bpy.types.Strip.md#bpy.types.Strip.show_retiming_keys "bpy.types.Strip.show_retiming_keys")

  
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
  * [`bpy_struct.keyframe_delete`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.keyframe_delete "bpy.types.bpy_struct.keyframe_delete")
  * [`bpy_struct.keyframe_insert`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.keyframe_insert "bpy.types.bpy_struct.keyframe_insert")
  * [`bpy_struct.keys`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.keys "bpy.types.bpy_struct.keys")
  * [`bpy_struct.path_from_id`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.path_from_id "bpy.types.bpy_struct.path_from_id")
  * [`bpy_struct.path_from_module`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.path_from_module "bpy.types.bpy_struct.path_from_module")

| 

  * [`bpy_struct.path_resolve`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.path_resolve "bpy.types.bpy_struct.path_resolve")
  * [`bpy_struct.pop`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.pop "bpy.types.bpy_struct.pop")
  * [`bpy_struct.property_overridable_library_set`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.property_overridable_library_set "bpy.types.bpy_struct.property_overridable_library_set")
  * [`bpy_struct.property_unset`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.property_unset "bpy.types.bpy_struct.property_unset")
  * [`bpy_struct.rna_ancestors`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.rna_ancestors "bpy.types.bpy_struct.rna_ancestors")
  * [`bpy_struct.type_recast`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.type_recast "bpy.types.bpy_struct.type_recast")
  * [`bpy_struct.values`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.values "bpy.types.bpy_struct.values")
  * [`Strip.bl_system_properties_get`](../S/bpy.types.Strip.md#bpy.types.Strip.bl_system_properties_get "bpy.types.Strip.bl_system_properties_get")
  * [`Strip.strip_elem_from_frame`](../S/bpy.types.Strip.md#bpy.types.Strip.strip_elem_from_frame "bpy.types.Strip.strip_elem_from_frame")
  * [`Strip.swap`](../S/bpy.types.Strip.md#bpy.types.Strip.swap "bpy.types.Strip.swap")
  * [`Strip.move_to_meta`](../S/bpy.types.Strip.md#bpy.types.Strip.move_to_meta "bpy.types.Strip.move_to_meta")
  * [`Strip.parent_meta`](../S/bpy.types.Strip.md#bpy.types.Strip.parent_meta "bpy.types.Strip.parent_meta")
  * [`Strip.invalidate_cache`](../S/bpy.types.Strip.md#bpy.types.Strip.invalidate_cache "bpy.types.Strip.invalidate_cache")
  * [`Strip.split`](../S/bpy.types.Strip.md#bpy.types.Strip.split "bpy.types.Strip.split")
  * [`Strip.bl_rna_get_subclass`](../S/bpy.types.Strip.md#bpy.types.Strip.bl_rna_get_subclass "bpy.types.Strip.bl_rna_get_subclass")
  * [`Strip.bl_rna_get_subclass_py`](../S/bpy.types.Strip.md#bpy.types.Strip.bl_rna_get_subclass_py "bpy.types.Strip.bl_rna_get_subclass_py")

  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
