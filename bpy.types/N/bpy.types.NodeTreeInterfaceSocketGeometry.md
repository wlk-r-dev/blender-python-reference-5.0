# NodeTreeInterfaceSocketGeometry(NodeTreeInterfaceSocket)

base classes — [`bpy_struct`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct "bpy.types.bpy_struct"), [`NodeTreeInterfaceItem`](bpy.types.NodeTreeInterfaceItem.md#bpy.types.NodeTreeInterfaceItem "bpy.types.NodeTreeInterfaceItem"), [`NodeTreeInterfaceSocket`](bpy.types.NodeTreeInterfaceSocket.md#bpy.types.NodeTreeInterfaceSocket "bpy.types.NodeTreeInterfaceSocket")

_class _bpy.types.NodeTreeInterfaceSocketGeometry(_NodeTreeInterfaceSocket_)
    

Geometry socket of a node

draw(_context_ , _layout_)
    

Draw interface socket settings

Parameters:
    

**layout** ([`UILayout`](../U/bpy.types.UILayout.md#bpy.types.UILayout "bpy.types.UILayout"), (never None)) – Layout, Layout in the UI

init_socket(_node_ , _socket_ , _data_path_)
    

Initialize a node socket instance

Parameters:
    

  * **node** ([`Node`](bpy.types.Node.md#bpy.types.Node "bpy.types.Node"), (never None)) – Node, Node of the socket to initialize

  * **socket** ([`NodeSocket`](bpy.types.NodeSocket.md#bpy.types.NodeSocket "bpy.types.NodeSocket"), (never None)) – Socket, Socket to initialize

  * **data_path** (_string_ _,__(__never None_ _)_) – Data Path, Path to specialized socket data


from_socket(_node_ , _socket_)
    

Setup template parameters from an existing socket

Parameters:
    

  * **node** ([`Node`](bpy.types.Node.md#bpy.types.Node "bpy.types.Node"), (never None)) – Node, Node of the original socket

  * **socket** ([`NodeSocket`](bpy.types.NodeSocket.md#bpy.types.NodeSocket "bpy.types.NodeSocket"), (never None)) – Socket, Original socket


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
  * [`NodeTreeInterfaceItem.item_type`](bpy.types.NodeTreeInterfaceItem.md#bpy.types.NodeTreeInterfaceItem.item_type "bpy.types.NodeTreeInterfaceItem.item_type")
  * [`NodeTreeInterfaceItem.parent`](bpy.types.NodeTreeInterfaceItem.md#bpy.types.NodeTreeInterfaceItem.parent "bpy.types.NodeTreeInterfaceItem.parent")
  * [`NodeTreeInterfaceItem.position`](bpy.types.NodeTreeInterfaceItem.md#bpy.types.NodeTreeInterfaceItem.position "bpy.types.NodeTreeInterfaceItem.position")
  * [`NodeTreeInterfaceItem.index`](bpy.types.NodeTreeInterfaceItem.md#bpy.types.NodeTreeInterfaceItem.index "bpy.types.NodeTreeInterfaceItem.index")
  * [`NodeTreeInterfaceSocket.name`](bpy.types.NodeTreeInterfaceSocket.md#bpy.types.NodeTreeInterfaceSocket.name "bpy.types.NodeTreeInterfaceSocket.name")
  * [`NodeTreeInterfaceSocket.identifier`](bpy.types.NodeTreeInterfaceSocket.md#bpy.types.NodeTreeInterfaceSocket.identifier "bpy.types.NodeTreeInterfaceSocket.identifier")
  * [`NodeTreeInterfaceSocket.description`](bpy.types.NodeTreeInterfaceSocket.md#bpy.types.NodeTreeInterfaceSocket.description "bpy.types.NodeTreeInterfaceSocket.description")
  * [`NodeTreeInterfaceSocket.socket_type`](bpy.types.NodeTreeInterfaceSocket.md#bpy.types.NodeTreeInterfaceSocket.socket_type "bpy.types.NodeTreeInterfaceSocket.socket_type")
  * [`NodeTreeInterfaceSocket.in_out`](bpy.types.NodeTreeInterfaceSocket.md#bpy.types.NodeTreeInterfaceSocket.in_out "bpy.types.NodeTreeInterfaceSocket.in_out")
  * [`NodeTreeInterfaceSocket.hide_value`](bpy.types.NodeTreeInterfaceSocket.md#bpy.types.NodeTreeInterfaceSocket.hide_value "bpy.types.NodeTreeInterfaceSocket.hide_value")
  * [`NodeTreeInterfaceSocket.hide_in_modifier`](bpy.types.NodeTreeInterfaceSocket.md#bpy.types.NodeTreeInterfaceSocket.hide_in_modifier "bpy.types.NodeTreeInterfaceSocket.hide_in_modifier")

| 

  * [`NodeTreeInterfaceSocket.force_non_field`](bpy.types.NodeTreeInterfaceSocket.md#bpy.types.NodeTreeInterfaceSocket.force_non_field "bpy.types.NodeTreeInterfaceSocket.force_non_field")
  * [`NodeTreeInterfaceSocket.is_inspect_output`](bpy.types.NodeTreeInterfaceSocket.md#bpy.types.NodeTreeInterfaceSocket.is_inspect_output "bpy.types.NodeTreeInterfaceSocket.is_inspect_output")
  * [`NodeTreeInterfaceSocket.is_panel_toggle`](bpy.types.NodeTreeInterfaceSocket.md#bpy.types.NodeTreeInterfaceSocket.is_panel_toggle "bpy.types.NodeTreeInterfaceSocket.is_panel_toggle")
  * [`NodeTreeInterfaceSocket.layer_selection_field`](bpy.types.NodeTreeInterfaceSocket.md#bpy.types.NodeTreeInterfaceSocket.layer_selection_field "bpy.types.NodeTreeInterfaceSocket.layer_selection_field")
  * [`NodeTreeInterfaceSocket.menu_expanded`](bpy.types.NodeTreeInterfaceSocket.md#bpy.types.NodeTreeInterfaceSocket.menu_expanded "bpy.types.NodeTreeInterfaceSocket.menu_expanded")
  * [`NodeTreeInterfaceSocket.optional_label`](bpy.types.NodeTreeInterfaceSocket.md#bpy.types.NodeTreeInterfaceSocket.optional_label "bpy.types.NodeTreeInterfaceSocket.optional_label")
  * [`NodeTreeInterfaceSocket.attribute_domain`](bpy.types.NodeTreeInterfaceSocket.md#bpy.types.NodeTreeInterfaceSocket.attribute_domain "bpy.types.NodeTreeInterfaceSocket.attribute_domain")
  * [`NodeTreeInterfaceSocket.default_attribute_name`](bpy.types.NodeTreeInterfaceSocket.md#bpy.types.NodeTreeInterfaceSocket.default_attribute_name "bpy.types.NodeTreeInterfaceSocket.default_attribute_name")
  * [`NodeTreeInterfaceSocket.structure_type`](bpy.types.NodeTreeInterfaceSocket.md#bpy.types.NodeTreeInterfaceSocket.structure_type "bpy.types.NodeTreeInterfaceSocket.structure_type")
  * [`NodeTreeInterfaceSocket.default_input`](bpy.types.NodeTreeInterfaceSocket.md#bpy.types.NodeTreeInterfaceSocket.default_input "bpy.types.NodeTreeInterfaceSocket.default_input")
  * [`NodeTreeInterfaceSocket.bl_socket_idname`](bpy.types.NodeTreeInterfaceSocket.md#bpy.types.NodeTreeInterfaceSocket.bl_socket_idname "bpy.types.NodeTreeInterfaceSocket.bl_socket_idname")

  
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
  * [`bpy_struct.keyframe_delete`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.keyframe_delete "bpy.types.bpy_struct.keyframe_delete")
  * [`bpy_struct.keyframe_insert`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.keyframe_insert "bpy.types.bpy_struct.keyframe_insert")
  * [`bpy_struct.keys`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.keys "bpy.types.bpy_struct.keys")
  * [`bpy_struct.path_from_id`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.path_from_id "bpy.types.bpy_struct.path_from_id")

| 

  * [`bpy_struct.path_from_module`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.path_from_module "bpy.types.bpy_struct.path_from_module")
  * [`bpy_struct.path_resolve`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.path_resolve "bpy.types.bpy_struct.path_resolve")
  * [`bpy_struct.pop`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.pop "bpy.types.bpy_struct.pop")
  * [`bpy_struct.property_overridable_library_set`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.property_overridable_library_set "bpy.types.bpy_struct.property_overridable_library_set")
  * [`bpy_struct.property_unset`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.property_unset "bpy.types.bpy_struct.property_unset")
  * [`bpy_struct.rna_ancestors`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.rna_ancestors "bpy.types.bpy_struct.rna_ancestors")
  * [`bpy_struct.type_recast`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.type_recast "bpy.types.bpy_struct.type_recast")
  * [`bpy_struct.values`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.values "bpy.types.bpy_struct.values")
  * [`NodeTreeInterfaceItem.bl_rna_get_subclass`](bpy.types.NodeTreeInterfaceItem.md#bpy.types.NodeTreeInterfaceItem.bl_rna_get_subclass "bpy.types.NodeTreeInterfaceItem.bl_rna_get_subclass")
  * [`NodeTreeInterfaceItem.bl_rna_get_subclass_py`](bpy.types.NodeTreeInterfaceItem.md#bpy.types.NodeTreeInterfaceItem.bl_rna_get_subclass_py "bpy.types.NodeTreeInterfaceItem.bl_rna_get_subclass_py")
  * [`NodeTreeInterfaceSocket.bl_system_properties_get`](bpy.types.NodeTreeInterfaceSocket.md#bpy.types.NodeTreeInterfaceSocket.bl_system_properties_get "bpy.types.NodeTreeInterfaceSocket.bl_system_properties_get")
  * [`NodeTreeInterfaceSocket.draw`](bpy.types.NodeTreeInterfaceSocket.md#bpy.types.NodeTreeInterfaceSocket.draw "bpy.types.NodeTreeInterfaceSocket.draw")
  * [`NodeTreeInterfaceSocket.init_socket`](bpy.types.NodeTreeInterfaceSocket.md#bpy.types.NodeTreeInterfaceSocket.init_socket "bpy.types.NodeTreeInterfaceSocket.init_socket")
  * [`NodeTreeInterfaceSocket.from_socket`](bpy.types.NodeTreeInterfaceSocket.md#bpy.types.NodeTreeInterfaceSocket.from_socket "bpy.types.NodeTreeInterfaceSocket.from_socket")
  * [`NodeTreeInterfaceSocket.bl_rna_get_subclass`](bpy.types.NodeTreeInterfaceSocket.md#bpy.types.NodeTreeInterfaceSocket.bl_rna_get_subclass "bpy.types.NodeTreeInterfaceSocket.bl_rna_get_subclass")
  * [`NodeTreeInterfaceSocket.bl_rna_get_subclass_py`](bpy.types.NodeTreeInterfaceSocket.md#bpy.types.NodeTreeInterfaceSocket.bl_rna_get_subclass_py "bpy.types.NodeTreeInterfaceSocket.bl_rna_get_subclass_py")

  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
