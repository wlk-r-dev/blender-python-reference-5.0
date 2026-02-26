# NodeTreeInterfacePanel(NodeTreeInterfaceItem)

base classes — [[bpy_struct]], [[NodeTreeInterfaceItem]]

_class _bpy.types.NodeTreeInterfacePanel(_NodeTreeInterfaceItem_)
    

Declaration of a node panel

default_closed
    

Panel is closed by default on new nodes

Type:
    

boolean, default False

description
    

Panel description

Type:
    

string, default “”, (never None)

interface_items
    

Items in the node panel

Type:
    

[[bpy_prop_collection]] of [[NodeTreeInterfaceItem]], (readonly)

name
    

Panel name

Type:
    

string, default “”, (never None)

persistent_uid
    

Unique identifier for this panel within this node tree

Type:
    

int in [-inf, inf], default 0, (readonly)

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
  * [[NodeTreeInterfaceItem.item_type]]
  * [[NodeTreeInterfaceItem.parent]]

| 

  * [[NodeTreeInterfaceItem.position]]
  * [[NodeTreeInterfaceItem.index]]

  
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
  * [[NodeTreeInterfaceItem.bl_rna_get_subclass]]
  * [[NodeTreeInterfaceItem.bl_rna_get_subclass_py]]

  
---|---  
  
## References

  * [[NodeTreeInterface.move_to_parent]]
  * [[NodeTreeInterface.new_panel]]

| 

  * [[NodeTreeInterface.new_socket]]
  * [[NodeTreeInterfaceItem.parent]]

  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
