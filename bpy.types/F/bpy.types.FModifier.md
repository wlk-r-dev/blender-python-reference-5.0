# FModifier(bpy_struct)

base class — [[bpy_struct]]

subclasses — [[FModifierCycles]], [[FModifierEnvelope]], [[FModifierFunctionGenerator]], [[FModifierGenerator]], [[FModifierLimits]], [[FModifierNoise]], [[FModifierStepped]]

_class _bpy.types.FModifier(_bpy_struct_)
    

Modifier for values of F-Curve

active
    

F-Curve modifier will show settings in the editor

Type:
    

boolean, default False

blend_in
    

Number of frames from start frame for influence to take effect

Type:
    

float in [-inf, inf], default 0.0

blend_out
    

Number of frames from end frame for influence to fade out

Type:
    

float in [-inf, inf], default 0.0

frame_end
    

Frame that modifier’s influence ends (if Restrict Frame Range is in use)

Type:
    

float in [-inf, inf], default 0.0

frame_start
    

Frame that modifier’s influence starts (if Restrict Frame Range is in use)

Type:
    

float in [-inf, inf], default 0.0

influence
    

Amount of influence F-Curve Modifier will have when not fading in/out

Type:
    

float in [0, 1], default 1.0

is_valid
    

F-Curve Modifier has invalid settings and will not be evaluated

Type:
    

boolean, default False, (readonly)

mute
    

Enable F-Curve modifier evaluation

Type:
    

boolean, default False

name
    

F-Curve Modifier name

Type:
    

string, default “”, (never None)

show_expanded
    

F-Curve Modifier’s panel is expanded in UI

Type:
    

boolean, default False

type
    

F-Curve Modifier Type

Type:
    

enum in [Fmodifier Type Items](../../bpy_types_enum_items/fmodifier_type_items.md#rna-enum-fmodifier-type-items), default `'NULL'`, (readonly)

use_influence
    

F-Curve Modifier’s effects will be tempered by a default factor

Type:
    

boolean, default False

use_restricted_range
    

F-Curve Modifier is only applied for the specified frame range to help mask off effects in order to chain them

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

  * [[FCurve.modifiers]]
  * [[FCurveModifiers.active]]
  * [[FCurveModifiers.new]]

| 

  * [[FCurveModifiers.remove]]
  * [[NlaStrip.modifiers]]

  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
