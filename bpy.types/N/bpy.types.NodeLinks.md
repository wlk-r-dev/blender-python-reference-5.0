# NodeLinks(bpy_struct)

base class — [[bpy_struct]]

_class _bpy.types.NodeLinks(_bpy_struct_)
    

Collection of Node Links

new(_input_ , _output_ , _*_ , _verify_limits =True_, _handle_dynamic_sockets =False_)
    

Add a node link to this node tree

Parameters:
    

  * **input** ([[NodeSocket]], (never None)) – The input socket

  * **output** ([[NodeSocket]], (never None)) – The output socket

  * **verify_limits** (_boolean_ _,__(__optional_ _)_) – Verify Limits, Remove existing links if connection limit is exceeded

  * **handle_dynamic_sockets** (_boolean_ _,__(__optional_ _)_) – Handle Dynamic Sockets, Handle node specific features like virtual sockets


Returns:
    

New node link

Return type:
    

[[NodeLink]]

remove(_link_)
    

remove a node link from the node tree

Parameters:
    

**link** ([[NodeLink]], (never None)) – The node link to remove

clear()
    

remove all node links from the node tree

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

  * [[NodeTree.links]]

| 


  
---|---
  *[*]: Keyword-only parameters separator (PEP 3102)
  *[/]: Positional-only parameter separator (PEP 570)
