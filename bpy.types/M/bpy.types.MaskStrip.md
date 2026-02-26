# MaskStrip(Strip)

base classes — [[bpy_struct]], [[Strip]]

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
    

[[StripCrop]], (readonly)

mask
    

Mask that this strip uses

Type:
    

[[Mask]]

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
    

[[StripTransform]], (readonly)

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
    

[[bpy.types.Struct]] subclass

_classmethod _bl_rna_get_subclass_py(_id_ , _default =None_, _/_)
    

Parameters:
    

**id** (_str_) – The RNA type identifier.

Returns:
    

The class or default when not found.

Return type:
    

type

## Inherited Properties

  * [[bpy_struct.id_data]]
  * [[Strip.name]]
  * [[Strip.type]]
  * [[Strip.select]]
  * [[Strip.select_left_handle]]
  * [[Strip.select_right_handle]]
  * [[Strip.mute]]
  * [[Strip.lock]]
  * [[Strip.frame_final_duration]]
  * [[Strip.frame_duration]]
  * [[Strip.frame_start]]
  * [[Strip.frame_final_start]]

| 

  * [[Strip.frame_final_end]]
  * [[Strip.frame_offset_start]]
  * [[Strip.frame_offset_end]]
  * [[Strip.channel]]
  * [[Strip.use_linear_modifiers]]
  * [[Strip.blend_type]]
  * [[Strip.blend_alpha]]
  * [[Strip.effect_fader]]
  * [[Strip.use_default_fade]]
  * [[Strip.color_tag]]
  * [[Strip.modifiers]]
  * [[Strip.show_retiming_keys]]

  
---|---  
  
## Inherited Functions

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

| 

  * [[bpy_struct.path_resolve]]
  * [[bpy_struct.pop]]
  * [[bpy_struct.property_overridable_library_set]]
  * [[bpy_struct.property_unset]]
  * [[bpy_struct.rna_ancestors]]
  * [[bpy_struct.type_recast]]
  * [[bpy_struct.values]]
  * [[Strip.bl_system_properties_get]]
  * [[Strip.strip_elem_from_frame]]
  * [[Strip.swap]]
  * [[Strip.move_to_meta]]
  * [[Strip.parent_meta]]
  * [[Strip.invalidate_cache]]
  * [[Strip.split]]
  * [[Strip.bl_rna_get_subclass]]
  * [[Strip.bl_rna_get_subclass_py]]

  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
