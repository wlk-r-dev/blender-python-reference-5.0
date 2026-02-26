# StripColorBalanceData(bpy_struct)

base class — [[bpy_struct]]

subclasses — [[StripColorBalance]]

_class _bpy.types.StripColorBalanceData(_bpy_struct_)
    

Color balance parameters for a sequence strip and its modifiers

correction_method
    

  * `LIFT_GAMMA_GAIN` Lift/Gamma/Gain.

  * `OFFSET_POWER_SLOPE` Offset/Power/Slope (ASC-CDL) – ASC-CDL standard color correction.


Type:
    

enum in [`'LIFT_GAMMA_GAIN'`, `'OFFSET_POWER_SLOPE'`], default `'LIFT_GAMMA_GAIN'`

gain
    

Color balance gain (highlights)

Type:
    

[[mathutils.Color]] of 3 items in [0, inf], default (1.0, 1.0, 1.0)

gamma
    

Color balance gamma (midtones)

Type:
    

[[mathutils.Color]] of 3 items in [0, inf], default (1.0, 1.0, 1.0)

invert_gain
    

Invert the gain color

Type:
    

boolean, default False

invert_gamma
    

Invert the gamma color

Type:
    

boolean, default False

invert_lift
    

Invert the lift color

Type:
    

boolean, default False

invert_offset
    

Invert the offset color

Type:
    

boolean, default False

invert_power
    

Invert the power color

Type:
    

boolean, default False

invert_slope
    

Invert the slope color

Type:
    

boolean, default False

lift
    

Color balance lift (shadows)

Type:
    

[[mathutils.Color]] of 3 items in [0, inf], default (1.0, 1.0, 1.0)

offset
    

Correction for entire tonal range

Type:
    

[[mathutils.Color]] of 3 items in [0, inf], default (1.0, 1.0, 1.0)

power
    

Correction for midtones

Type:
    

[[mathutils.Color]] of 3 items in [0, inf], default (1.0, 1.0, 1.0)

slope
    

Correction for highlights

Type:
    

[[mathutils.Color]] of 3 items in [0, inf], default (1.0, 1.0, 1.0)

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

| 


  
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

| 

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
  * [[bpy_struct.type_recast]]
  * [[bpy_struct.values]]

  
---|---  
  
## References

  * [[ColorBalanceModifier.color_balance]]

| 


  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
