# NodeTreeInterfaceSocketVectorTranslation(NodeTreeInterfaceSocket)

base classes — [[bpy_struct]], [[NodeTreeInterfaceItem]], [[NodeTreeInterfaceSocket]]

_class _bpy.types.NodeTreeInterfaceSocketVectorTranslation(_NodeTreeInterfaceSocket_)
    

3D vector socket of a node

default_value
    

Input value used for unconnected socket

Type:
    

[[mathutils.Vector]] of 3 items in [-inf, inf], default (0.0, 0.0, 0.0)

dimensions
    

Dimensions of the vector socket

Type:
    

int in [2, 4], default 0

max_value
    

Maximum value

Type:
    

float in [-inf, inf], default 0.0

min_value
    

Minimum value

Type:
    

float in [-inf, inf], default 0.0

subtype
    

Subtype of the default value

Type:
    

enum in [`'DEFAULT'`], default `'DEFAULT'`

draw(_context_ , _layout_)
    

Draw interface socket settings

Parameters:
    

**layout** ([[UILayout]], (never None)) – Layout, Layout in the UI

init_socket(_node_ , _socket_ , _data_path_)
    

Initialize a node socket instance

Parameters:
    

  * **node** ([[Node]], (never None)) – Node, Node of the socket to initialize

  * **socket** ([[NodeSocket]], (never None)) – Socket, Socket to initialize

  * **data_path** (_string_ _,__(__never None_ _)_) – Data Path, Path to specialized socket data


from_socket(_node_ , _socket_)
    

Setup template parameters from an existing socket

Parameters:
    

  * **node** ([[Node]], (never None)) – Node, Node of the original socket

  * **socket** ([[NodeSocket]], (never None)) – Socket, Original socket


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
  * [[NodeTreeInterfaceItem.position]]
  * [[NodeTreeInterfaceItem.index]]
  * [[NodeTreeInterfaceSocket.name]]
  * [[NodeTreeInterfaceSocket.identifier]]
  * [[NodeTreeInterfaceSocket.description]]
  * [[NodeTreeInterfaceSocket.socket_type]]
  * [[NodeTreeInterfaceSocket.in_out]]
  * [[NodeTreeInterfaceSocket.hide_value]]
  * [[NodeTreeInterfaceSocket.hide_in_modifier]]

| 

  * [[NodeTreeInterfaceSocket.force_non_field]]
  * [[NodeTreeInterfaceSocket.is_inspect_output]]
  * [[NodeTreeInterfaceSocket.is_panel_toggle]]
  * [[NodeTreeInterfaceSocket.layer_selection_field]]
  * [[NodeTreeInterfaceSocket.menu_expanded]]
  * [[NodeTreeInterfaceSocket.optional_label]]
  * [[NodeTreeInterfaceSocket.attribute_domain]]
  * [[NodeTreeInterfaceSocket.default_attribute_name]]
  * [[NodeTreeInterfaceSocket.structure_type]]
  * [[NodeTreeInterfaceSocket.default_input]]
  * [[NodeTreeInterfaceSocket.bl_socket_idname]]

  
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
  * [[bpy_struct.keyframe_insert]]
  * [[bpy_struct.keys]]
  * [[bpy_struct.path_from_id]]

| 

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
  * [[NodeTreeInterfaceSocket.bl_system_properties_get]]
  * [[NodeTreeInterfaceSocket.draw]]
  * [[NodeTreeInterfaceSocket.init_socket]]
  * [[NodeTreeInterfaceSocket.from_socket]]
  * [[NodeTreeInterfaceSocket.bl_rna_get_subclass]]
  * [[NodeTreeInterfaceSocket.bl_rna_get_subclass_py]]

  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
