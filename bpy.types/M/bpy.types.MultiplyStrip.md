# MultiplyStrip(EffectStrip)

base classes — [[bpy_struct]], [[Strip]], [[EffectStrip]]

_class _bpy.types.MultiplyStrip(_EffectStrip_)
    

Multiply Strip

input_1
    

First input for the effect strip

Type:
    

[[Strip]], (never None)

input_2
    

Second input for the effect strip

Type:
    

[[Strip]], (never None)

input_count
    

Type:
    

int in [0, inf], default 0, (readonly)

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
  * [[Strip.frame_final_end]]
  * [[Strip.frame_offset_start]]
  * [[Strip.frame_offset_end]]
  * [[Strip.channel]]
  * [[Strip.use_linear_modifiers]]
  * [[Strip.blend_type]]
  * [[Strip.blend_alpha]]

| 

  * [[Strip.effect_fader]]
  * [[Strip.use_default_fade]]
  * [[Strip.color_tag]]
  * [[Strip.modifiers]]
  * [[Strip.show_retiming_keys]]
  * [[EffectStrip.use_deinterlace]]
  * [[EffectStrip.alpha_mode]]
  * [[EffectStrip.use_flip_x]]
  * [[EffectStrip.use_flip_y]]
  * [[EffectStrip.use_float]]
  * [[EffectStrip.use_reverse_frames]]
  * [[EffectStrip.color_multiply]]
  * [[EffectStrip.multiply_alpha]]
  * [[EffectStrip.color_saturation]]
  * [[EffectStrip.strobe]]
  * [[EffectStrip.transform]]
  * [[EffectStrip.crop]]
  * [[EffectStrip.use_proxy]]
  * [[EffectStrip.proxy]]

  
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
  * [[bpy_struct.path_resolve]]

| 

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
  * [[EffectStrip.bl_rna_get_subclass]]
  * [[EffectStrip.bl_rna_get_subclass_py]]

  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
