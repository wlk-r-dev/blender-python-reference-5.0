# ClampToConstraint(Constraint)

base classes — [[bpy_struct]], [[Constraint]]

_class _bpy.types.ClampToConstraint(_Constraint_)
    

Constrain an object’s location to the nearest point along the target path

main_axis
    

Main axis of movement

Type:
    

enum in [`'CLAMPTO_AUTO'`, `'CLAMPTO_X'`, `'CLAMPTO_Y'`, `'CLAMPTO_Z'`], default `'CLAMPTO_AUTO'`

target
    

Target Object (Curves only)

Type:
    

[[Object]]

use_cyclic
    

Treat curve as cyclic curve (no clamping to curve bounding box)

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
  * [[Constraint.name]]
  * [[Constraint.type]]
  * [[Constraint.is_override_data]]
  * [[Constraint.owner_space]]
  * [[Constraint.target_space]]
  * [[Constraint.space_object]]
  * [[Constraint.space_subtarget]]

| 

  * [[Constraint.mute]]
  * [[Constraint.enabled]]
  * [[Constraint.show_expanded]]
  * [[Constraint.is_valid]]
  * [[Constraint.active]]
  * [[Constraint.influence]]
  * [[Constraint.error_location]]
  * [[Constraint.error_rotation]]

  
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
  * [[Constraint.bl_rna_get_subclass]]
  * [[Constraint.bl_rna_get_subclass_py]]

  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
