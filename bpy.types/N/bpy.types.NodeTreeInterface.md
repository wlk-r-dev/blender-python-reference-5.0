# NodeTreeInterface(bpy_struct)

base class — [`bpy_struct`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct "bpy.types.bpy_struct")

_class _bpy.types.NodeTreeInterface(_bpy_struct_)
    

Declaration of sockets and ui panels of a node group

active
    

Active item

Type:
    

[`NodeTreeInterfaceItem`](bpy.types.NodeTreeInterfaceItem.md#bpy.types.NodeTreeInterfaceItem "bpy.types.NodeTreeInterfaceItem")

active_index
    

Index of the active item

Type:
    

int in [0, inf], default 0

items_tree
    

Items in the node interface

Type:
    

[`bpy_prop_collection`](../_other/bpy.types.bpy_prop_collection.md#bpy.types.bpy_prop_collection "bpy.types.bpy_prop_collection") of [`NodeTreeInterfaceItem`](bpy.types.NodeTreeInterfaceItem.md#bpy.types.NodeTreeInterfaceItem "bpy.types.NodeTreeInterfaceItem"), (readonly)

new_socket(_name_ , _*_ , _description =''_, _in_out ='INPUT'_, _socket_type ='DEFAULT'_, _parent =None_)
    

Add a new socket to the interface

Parameters:
    

  * **name** (_string_ _,__(__never None_ _)_) – Name, Name of the socket

  * **description** (_string_ _,__(__optional_ _,__never None_ _)_) – Description, Description of the socket

  * **in_out** (enum in [`'INPUT'`, `'OUTPUT'`], (optional)) – 

Input/Output Type, Create an input or output socket

    * `INPUT` Input – Generate a input node socket.

    * `OUTPUT` Output – Generate a output node socket.

  * **socket_type** (enum in [`'DEFAULT'`], (optional)) – Socket Type, Type of socket generated on nodes

  * **parent** ([`NodeTreeInterfacePanel`](bpy.types.NodeTreeInterfacePanel.md#bpy.types.NodeTreeInterfacePanel "bpy.types.NodeTreeInterfacePanel"), (optional)) – Parent, Panel to add the socket in


Returns:
    

Socket, New socket

Return type:
    

[`NodeTreeInterfaceSocket`](bpy.types.NodeTreeInterfaceSocket.md#bpy.types.NodeTreeInterfaceSocket "bpy.types.NodeTreeInterfaceSocket")

new_panel(_name_ , _*_ , _description =''_, _default_closed =False_)
    

Add a new panel to the interface

Parameters:
    

  * **name** (_string_ _,__(__never None_ _)_) – Name, Name of the new panel

  * **description** (_string_ _,__(__optional_ _,__never None_ _)_) – Description, Description of the panel

  * **default_closed** (_boolean_ _,__(__optional_ _)_) – Default Closed, Panel is closed by default on new nodes


Returns:
    

Panel, New panel

Return type:
    

[`NodeTreeInterfacePanel`](bpy.types.NodeTreeInterfacePanel.md#bpy.types.NodeTreeInterfacePanel "bpy.types.NodeTreeInterfacePanel")

copy(_item_)
    

Add a copy of an item to the interface

Parameters:
    

**item** ([`NodeTreeInterfaceItem`](bpy.types.NodeTreeInterfaceItem.md#bpy.types.NodeTreeInterfaceItem "bpy.types.NodeTreeInterfaceItem"), (never None)) – Item, Item to copy

Returns:
    

Item Copy, Copy of the item

Return type:
    

[`NodeTreeInterfaceItem`](bpy.types.NodeTreeInterfaceItem.md#bpy.types.NodeTreeInterfaceItem "bpy.types.NodeTreeInterfaceItem")

remove(_item_ , _*_ , _move_content_to_parent =True_)
    

Remove an item from the interface

Parameters:
    

  * **item** ([`NodeTreeInterfaceItem`](bpy.types.NodeTreeInterfaceItem.md#bpy.types.NodeTreeInterfaceItem "bpy.types.NodeTreeInterfaceItem"), (never None)) – Item, The item to remove

  * **move_content_to_parent** (_boolean_ _,__(__optional_ _)_) – Move Content, If the item is a panel, move the contents to the parent instead of deleting it


clear()
    

Remove all items from the interface

move(_item_ , _to_position_)
    

Move an item to another position

Parameters:
    

  * **item** ([`NodeTreeInterfaceItem`](bpy.types.NodeTreeInterfaceItem.md#bpy.types.NodeTreeInterfaceItem "bpy.types.NodeTreeInterfaceItem"), (never None)) – Item, The item to move

  * **to_position** (_int in_ _[__0_ _,__inf_ _]_) – To Position, Target position for the item in its current panel


move_to_parent(_item_ , _parent_ , _to_position_)
    

Move an item to a new panel and/or position.

Parameters:
    

  * **item** ([`NodeTreeInterfaceItem`](bpy.types.NodeTreeInterfaceItem.md#bpy.types.NodeTreeInterfaceItem "bpy.types.NodeTreeInterfaceItem"), (never None)) – Item, The item to move

  * **parent** ([`NodeTreeInterfacePanel`](bpy.types.NodeTreeInterfacePanel.md#bpy.types.NodeTreeInterfacePanel "bpy.types.NodeTreeInterfacePanel")) – Parent, New parent of the item

  * **to_position** (_int in_ _[__0_ _,__inf_ _]_) – To Position, Target position for the item in the new parent panel


_classmethod _bl_rna_get_subclass(_id_ , _default =None_, _/_)
    

Parameters:
    

**id** (_str_) – The RNA type identifier.

Returns:
    

The RNA type or default when not found.

Return type:
    

[`bpy.types.Struct`](../S/bpy.types.Struct.md#bpy.types.Struct "bpy.types.Struct") subclass

_classmethod _bl_rna_get_subclass_py(_id_ , _default =None_, _/_)
    

Parameters:
    

**id** (_str_) – The RNA type identifier.

Returns:
    

The class or default when not found.

Return type:
    

type

## Inherited Properties

  * [`bpy_struct.id_data`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.id_data "bpy.types.bpy_struct.id_data")

| 


  
---|---  
  
## Inherited Functions

  * [`bpy_struct.as_pointer`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.as_pointer "bpy.types.bpy_struct.as_pointer")
  * [`bpy_struct.driver_add`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.driver_add "bpy.types.bpy_struct.driver_add")
  * [`bpy_struct.driver_remove`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.driver_remove "bpy.types.bpy_struct.driver_remove")
  * [`bpy_struct.get`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.get "bpy.types.bpy_struct.get")
  * [`bpy_struct.id_properties_clear`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.id_properties_clear "bpy.types.bpy_struct.id_properties_clear")
  * [`bpy_struct.id_properties_ensure`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.id_properties_ensure "bpy.types.bpy_struct.id_properties_ensure")
  * [`bpy_struct.id_properties_ui`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.id_properties_ui "bpy.types.bpy_struct.id_properties_ui")
  * [`bpy_struct.is_property_hidden`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.is_property_hidden "bpy.types.bpy_struct.is_property_hidden")
  * [`bpy_struct.is_property_overridable_library`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.is_property_overridable_library "bpy.types.bpy_struct.is_property_overridable_library")
  * [`bpy_struct.is_property_readonly`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.is_property_readonly "bpy.types.bpy_struct.is_property_readonly")
  * [`bpy_struct.is_property_set`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.is_property_set "bpy.types.bpy_struct.is_property_set")
  * [`bpy_struct.items`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.items "bpy.types.bpy_struct.items")

| 

  * [`bpy_struct.keyframe_delete`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.keyframe_delete "bpy.types.bpy_struct.keyframe_delete")
  * [`bpy_struct.keyframe_insert`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.keyframe_insert "bpy.types.bpy_struct.keyframe_insert")
  * [`bpy_struct.keys`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.keys "bpy.types.bpy_struct.keys")
  * [`bpy_struct.path_from_id`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.path_from_id "bpy.types.bpy_struct.path_from_id")
  * [`bpy_struct.path_from_module`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.path_from_module "bpy.types.bpy_struct.path_from_module")
  * [`bpy_struct.path_resolve`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.path_resolve "bpy.types.bpy_struct.path_resolve")
  * [`bpy_struct.pop`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.pop "bpy.types.bpy_struct.pop")
  * [`bpy_struct.property_overridable_library_set`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.property_overridable_library_set "bpy.types.bpy_struct.property_overridable_library_set")
  * [`bpy_struct.property_unset`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.property_unset "bpy.types.bpy_struct.property_unset")
  * [`bpy_struct.rna_ancestors`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.rna_ancestors "bpy.types.bpy_struct.rna_ancestors")
  * [`bpy_struct.type_recast`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.type_recast "bpy.types.bpy_struct.type_recast")
  * [`bpy_struct.values`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.values "bpy.types.bpy_struct.values")

  
---|---  
  
## References

  * [`NodeTree.interface`](bpy.types.NodeTree.md#bpy.types.NodeTree.interface "bpy.types.NodeTree.interface")

| 

  * [`UILayout.template_node_tree_interface`](../U/bpy.types.UILayout.md#bpy.types.UILayout.template_node_tree_interface "bpy.types.UILayout.template_node_tree_interface")

  
---|---
  *[*]: Keyword-only parameters separator (PEP 3102)
  *[/]: Positional-only parameter separator (PEP 570)
