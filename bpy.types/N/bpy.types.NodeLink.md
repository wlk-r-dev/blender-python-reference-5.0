# NodeLink(bpy_struct)

base class — [[bpy_struct]]

_class _bpy.types.NodeLink(_bpy_struct_)
    

Link between nodes in a node tree

from_node
    

Type:
    

[[Node]], (readonly)

from_socket
    

Type:
    

[[NodeSocket]], (readonly)

is_hidden
    

Link is hidden due to invisible sockets

Type:
    

boolean, default False, (readonly)

is_muted
    

Link is muted and can be ignored

Type:
    

boolean, default False

is_valid
    

Link is valid

Type:
    

boolean, default False

multi_input_sort_id
    

Used to sort multiple links coming into the same input. The highest ID is at the top.

Type:
    

int in [0, inf], default 0, (readonly)

to_node
    

Type:
    

[[Node]], (readonly)

to_socket
    

Type:
    

[[NodeSocket]], (readonly)

swap_multi_input_sort_id(_other_)
    

Swap the order of two links connected to the same multi-input socket

Parameters:
    

**other** (`NodeLink`, (never None)) – Other, The other link. Must link to the same multi-input socket.

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

  * [[Node.insert_link]]
  * [[Node.internal_links]]
  * `NodeLink.swap_multi_input_sort_id`

| 

  * [[NodeLinks.new]]
  * [[NodeLinks.remove]]
  * [[NodeTree.links]]

  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
