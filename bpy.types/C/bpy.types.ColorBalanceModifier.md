# ColorBalanceModifier(StripModifier)

base classes — [[bpy_struct]], [[StripModifier]]

_class _bpy.types.ColorBalanceModifier(_StripModifier_)
    

Color balance modifier for sequence strip

color_balance
    

Type:
    

[[StripColorBalanceData]], (readonly)

color_multiply
    

Multiply the intensity of each pixel

Type:
    

float in [0, 20], default 1.0

open_mask_input_panel
    

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
  * [[StripModifier.name]]
  * [[StripModifier.type]]
  * [[StripModifier.mute]]
  * [[StripModifier.enable]]
  * [[StripModifier.show_expanded]]

| 

  * [[StripModifier.input_mask_type]]
  * [[StripModifier.mask_time]]
  * [[StripModifier.input_mask_strip]]
  * [[StripModifier.input_mask_id]]
  * [[StripModifier.is_active]]

  
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

| 

  * [[bpy_struct.keyframe_insert]]
  * [[bpy_struct.keys]]
  * [[bpy_struct.path_from_id]]
  * [[bpy_struct.path_from_module]]
  * [[bpy_struct.path_resolve]]
  * [[bpy_struct.pop]]
  * [[bpy_struct.property_overridable_library_set]]
  * [[bpy_struct.property_unset]]
  * [[bpy_struct.rna_ancestors]]
  * [[bpy_struct.type_recast]]
  * [[bpy_struct.values]]
  * [[StripModifier.bl_rna_get_subclass]]
  * [[StripModifier.bl_rna_get_subclass_py]]

  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
