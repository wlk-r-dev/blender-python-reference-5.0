# BoidState(bpy_struct)

base class — [[bpy_struct]]

_class _bpy.types.BoidState(_bpy_struct_)
    

Boid state for boid physics

active_boid_rule
    

Type:
    

[[BoidRule]], (readonly)

active_boid_rule_index
    

Type:
    

int in [0, inf], default 0

falloff
    

Type:
    

float in [0, 10], default 0.0

name
    

Boid state name

Type:
    

string, default “”, (never None)

rule_fuzzy
    

Type:
    

float in [0, 1], default 0.0

rules
    

Type:
    

[[bpy_prop_collection]] of [[BoidRule]], (readonly)

ruleset_type
    

How the rules in the list are evaluated

  * `FUZZY` Fuzzy – Rules are gone through top to bottom (only the first rule which effect is above fuzziness threshold is evaluated).

  * `RANDOM` Random – A random rule is selected for each boid.

  * `AVERAGE` Average – All rules are averaged.


Type:
    

enum in [`'FUZZY'`, `'RANDOM'`, `'AVERAGE'`], default `'FUZZY'`

volume
    

Type:
    

float in [0, 100], default 0.0

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

  * [[BoidSettings.states]]

| 


  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
