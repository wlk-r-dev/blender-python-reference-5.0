# NodeOutputs(bpy_struct)

base class — [[bpy_struct]]

_class _bpy.types.NodeOutputs(_bpy_struct_)
    

Collection of Node Sockets

new(_type_ , _name_ , _*_ , _identifier =''_, _use_multi_input =False_)
    

Add a socket to this node

Parameters:
    

  * **type** (_string_ _,__(__never None_ _)_) – Type, Data type

  * **name** (_string_ _,__(__never None_ _)_) – Name

  * **identifier** (_string_ _,__(__optional_ _,__never None_ _)_) – Identifier, Unique socket identifier

  * **use_multi_input** (_boolean_ _,__(__optional_ _)_) – Make the socket multi-input (valid for inputs only)


Returns:
    

New socket

Return type:
    

[[NodeSocket]]

remove(_socket_)
    

Remove a socket from this node

Parameters:
    

**socket** ([[NodeSocket]]) – The socket to remove

clear()
    

Remove all sockets from this node

move(_from_index_ , _to_index_)
    

Move a socket to another position

Parameters:
    

  * **from_index** (_int in_ _[__0_ _,__inf_ _]_) – From Index, Index of the socket to move

  * **to_index** (_int in_ _[__0_ _,__inf_ _]_) – To Index, Target index for the socket


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

  * [[Node.outputs]]

| 


  
---|---
  *[*]: Keyword-only parameters separator (PEP 3102)
  *[/]: Positional-only parameter separator (PEP 570)
