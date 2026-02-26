# NodeTreeInterfaceItem(bpy_struct)

base class — [[bpy_struct]]

subclasses — [[NodeTreeInterfacePanel]], [[NodeTreeInterfaceSocket]]

_class _bpy.types.NodeTreeInterfaceItem(_bpy_struct_)
    

Item in a node tree interface

index
    

Global index of the item among all items in the interface

Type:
    

int in [-1, inf], default 0, (readonly)

item_type
    

Type of interface item

Type:
    

enum in [Node Tree Interface Item Type Items](../../bpy_types_enum_items/node_tree_interface_item_type_items.md#rna-enum-node-tree-interface-item-type-items), default `'PANEL'`, (readonly)

parent
    

Panel that contains the item

Type:
    

[[NodeTreeInterfacePanel]], (readonly)

position
    

Position of the item in its parent panel

Type:
    

int in [-1, inf], default 0, (readonly)

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

  * [[NodeTreeInterface.active]]
  * [[NodeTreeInterface.copy]]
  * [[NodeTreeInterface.copy]]
  * [[NodeTreeInterface.items_tree]]

| 

  * [[NodeTreeInterface.move]]
  * [[NodeTreeInterface.move_to_parent]]
  * [[NodeTreeInterface.remove]]
  * [[NodeTreeInterfacePanel.interface_items]]

  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
