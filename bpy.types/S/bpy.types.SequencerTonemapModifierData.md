# SequencerTonemapModifierData(StripModifier)

base classes — [[bpy_struct]], [[StripModifier]]

_class _bpy.types.SequencerTonemapModifierData(_StripModifier_)
    

Tone mapping modifier

adaptation
    

If 0, global; if 1, based on pixel intensity

Type:
    

float in [0, 1], default 0.0

contrast
    

Set to 0 to use estimate from input image

Type:
    

float in [0, 1], default 0.0

correction
    

If 0, same for all channels; if 1, each independent

Type:
    

float in [0, 1], default 0.0

gamma
    

If not used, set to 1

Type:
    

float in [0.001, 3], default 0.0

intensity
    

If less than zero, darkens image; otherwise, makes it brighter

Type:
    

float in [-8, 8], default 0.0

key
    

The value the average luminance is mapped to

Type:
    

float in [0, 1], default 0.0

offset
    

Normally always 1, but can be used as an extra control to alter the brightness curve

Type:
    

float in [0.001, 10], default 0.0

open_mask_input_panel
    

Type:
    

boolean, default False

tonemap_type
    

Tone mapping algorithm

Type:
    

enum in [`'RD_PHOTORECEPTOR'`, `'RH_SIMPLE'`], default `'RH_SIMPLE'`

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
