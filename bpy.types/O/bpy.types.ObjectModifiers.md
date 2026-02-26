# ObjectModifiers(bpy_struct)

base class — [[bpy_struct]]

_class _bpy.types.ObjectModifiers(_bpy_struct_)
    

Collection of object modifiers

active
    

The active modifier in the list

Type:
    

[[Modifier]]

new(_name_ , _type_)
    

Add a new modifier

Parameters:
    

  * **name** (_string_ _,__(__never None_ _)_) – New name for the modifier

  * **type** (enum in [Object Modifier Type Items](../../bpy_types_enum_items/object_modifier_type_items.md#rna-enum-object-modifier-type-items)) – Modifier type to add


Returns:
    

Newly created modifier

Return type:
    

[[Modifier]]

remove(_modifier_)
    

Remove an existing modifier from the object

Parameters:
    

**modifier** ([[Modifier]], (never None)) – Modifier to remove

clear()
    

Remove all modifiers from the object

move(_from_index_ , _to_index_)
    

Move a modifier to a different position

Parameters:
    

  * **from_index** (_int in_ _[__-inf_ _,__inf_ _]_) – From Index, Index to move

  * **to_index** (_int in_ _[__-inf_ _,__inf_ _]_) – To Index, Target index


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

  * [[Object.modifiers]]

| 


  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
