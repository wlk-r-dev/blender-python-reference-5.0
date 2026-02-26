# PoseBoneConstraints(bpy_struct)

base class — [[bpy_struct]]

_class _bpy.types.PoseBoneConstraints(_bpy_struct_)
    

Collection of pose bone constraints

active
    

Active PoseChannel constraint

Type:
    

[[Constraint]]

new(_type_)
    

Add a constraint to this object

Parameters:
    

**type** (enum in [Constraint Type Items](../../bpy_types_enum_items/constraint_type_items.md#rna-enum-constraint-type-items)) – Constraint type to add

Returns:
    

New constraint

Return type:
    

[[Constraint]]

remove(_constraint_)
    

Remove a constraint from this object

Parameters:
    

**constraint** ([[Constraint]], (never None)) – Removed constraint

move(_from_index_ , _to_index_)
    

Move a constraint to a different position

Parameters:
    

  * **from_index** (_int in_ _[__-inf_ _,__inf_ _]_) – From Index, Index to move

  * **to_index** (_int in_ _[__-inf_ _,__inf_ _]_) – To Index, Target index


copy(_constraint_)
    

Add a new constraint that is a copy of the given one

Parameters:
    

**constraint** ([[Constraint]], (never None)) – Constraint to copy - may belong to a different object

Returns:
    

New constraint

Return type:
    

[[Constraint]]

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

  * [[PoseBone.constraints]]

| 


  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
