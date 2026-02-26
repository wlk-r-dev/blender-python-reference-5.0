# NodeTreeInterfaceSocket(NodeTreeInterfaceItem)

base classes — [[bpy_struct]], [[NodeTreeInterfaceItem]]

subclasses — [[NodeTreeInterfaceSocketBool]], [[NodeTreeInterfaceSocketBundle]], [[NodeTreeInterfaceSocketClosure]], [[NodeTreeInterfaceSocketCollection]], [[NodeTreeInterfaceSocketColor]], [[NodeTreeInterfaceSocketFloat]], [[NodeTreeInterfaceSocketFloatAngle]], [[NodeTreeInterfaceSocketFloatColorTemperature]], [[NodeTreeInterfaceSocketFloatDistance]], [[NodeTreeInterfaceSocketFloatFactor]], [[NodeTreeInterfaceSocketFloatFrequency]], [[NodeTreeInterfaceSocketFloatPercentage]], [[NodeTreeInterfaceSocketFloatTime]], [[NodeTreeInterfaceSocketFloatTimeAbsolute]], [[NodeTreeInterfaceSocketFloatUnsigned]], [[NodeTreeInterfaceSocketFloatWavelength]], [[NodeTreeInterfaceSocketGeometry]], [[NodeTreeInterfaceSocketImage]], [[NodeTreeInterfaceSocketInt]], [[NodeTreeInterfaceSocketIntFactor]], [[NodeTreeInterfaceSocketIntPercentage]], [[NodeTreeInterfaceSocketIntUnsigned]], [[NodeTreeInterfaceSocketMaterial]], [[NodeTreeInterfaceSocketMatrix]], [[NodeTreeInterfaceSocketMenu]], [[NodeTreeInterfaceSocketObject]], [[NodeTreeInterfaceSocketRotation]], [[NodeTreeInterfaceSocketShader]], [[NodeTreeInterfaceSocketString]], [[NodeTreeInterfaceSocketStringFilePath]], [[NodeTreeInterfaceSocketTexture]], [[NodeTreeInterfaceSocketVector]], [[NodeTreeInterfaceSocketVector2D]], [[NodeTreeInterfaceSocketVector4D]], [[NodeTreeInterfaceSocketVectorAcceleration]], [[NodeTreeInterfaceSocketVectorAcceleration2D]], [[NodeTreeInterfaceSocketVectorAcceleration4D]], [[NodeTreeInterfaceSocketVectorDirection]], [[NodeTreeInterfaceSocketVectorDirection2D]], [[NodeTreeInterfaceSocketVectorDirection4D]], [[NodeTreeInterfaceSocketVectorEuler]], [[NodeTreeInterfaceSocketVectorEuler2D]], [[NodeTreeInterfaceSocketVectorEuler4D]], [[NodeTreeInterfaceSocketVectorFactor]], [[NodeTreeInterfaceSocketVectorFactor2D]], [[NodeTreeInterfaceSocketVectorFactor4D]], [[NodeTreeInterfaceSocketVectorPercentage]], [[NodeTreeInterfaceSocketVectorPercentage2D]], [[NodeTreeInterfaceSocketVectorPercentage4D]], [[NodeTreeInterfaceSocketVectorTranslation]], [[NodeTreeInterfaceSocketVectorTranslation2D]], [[NodeTreeInterfaceSocketVectorTranslation4D]], [[NodeTreeInterfaceSocketVectorVelocity]], [[NodeTreeInterfaceSocketVectorVelocity2D]], [[NodeTreeInterfaceSocketVectorVelocity4D]], [[NodeTreeInterfaceSocketVectorXYZ]], [[NodeTreeInterfaceSocketVectorXYZ2D]], [[NodeTreeInterfaceSocketVectorXYZ4D]]

_class _bpy.types.NodeTreeInterfaceSocket(_NodeTreeInterfaceItem_)
    

Declaration of a node socket

attribute_domain
    

Attribute domain used by the geometry nodes modifier to create an attribute output

Type:
    

enum in [Attribute Domain Items](../../bpy_types_enum_items/attribute_domain_items.md#rna-enum-attribute-domain-items), default `'POINT'`

bl_socket_idname
    

Name of the socket type

Type:
    

string, default “”, (never None)

default_attribute_name
    

The attribute name used by default when the node group is used by a geometry nodes modifier

Type:
    

string, default “”, (never None)

default_input
    

Input to use when the socket is unconnected. Requires “Hide Value”.

  * `VALUE` Default Value – The node socket’s default value.

  * `INDEX` Index – The index from the context.

  * `ID_OR_INDEX` ID or Index – The “id” attribute if available, otherwise the index.

  * `NORMAL` Normal – The geometry’s normal direction.

  * `POSITION` Position – The position from the context.

  * `INSTANCE_TRANSFORM` Instance Transform – Transformation of each instance from the geometry context.

  * `HANDLE_LEFT` Left Handle – The left Bézier control point handle from the context.

  * `HANDLE_RIGHT` Right Handle – The right Bézier control point handle from the context.


Type:
    

enum in [`'VALUE'`, `'INDEX'`, `'ID_OR_INDEX'`, `'NORMAL'`, `'POSITION'`, `'INSTANCE_TRANSFORM'`, `'HANDLE_LEFT'`, `'HANDLE_RIGHT'`], default `'VALUE'`

description
    

Socket description

Type:
    

string, default “”, (never None)

force_non_field
    

Only allow single value inputs rather than field. Deprecated. Will be remove in 5.0.

Type:
    

boolean, default False

hide_in_modifier
    

Don’t show the input value in the geometry nodes modifier interface

Type:
    

boolean, default False

hide_value
    

Hide the socket input value even when the socket is not connected

Type:
    

boolean, default False

identifier
    

Unique identifier for mapping sockets

Type:
    

string, default “”, (readonly, never None)

in_out
    

Input or output socket type

  * `INPUT` Input – Generate a input node socket.

  * `OUTPUT` Output – Generate a output node socket.


Type:
    

enum in [`'INPUT'`, `'OUTPUT'`], default `'INPUT'`, (readonly)

is_inspect_output
    

Take link out of node group to connect to root tree output node

Type:
    

boolean, default False

is_panel_toggle
    

This socket is meant to be used as the toggle in its panel header

Type:
    

boolean, default False

layer_selection_field
    

Take Grease Pencil Layer or Layer Group as selection field

Type:
    

boolean, default False

menu_expanded
    

Draw the menu socket as an expanded drop-down menu

Type:
    

boolean, default False

name
    

Socket name

Type:
    

string, default “”, (never None)

optional_label
    

Indicate that the label of this socket is not necessary to understand its meaning. This may result in the label being skipped in some cases

Type:
    

boolean, default False

socket_type
    

Type of the socket generated by this interface item

Type:
    

enum in [`'DEFAULT'`], default `'DEFAULT'`

structure_type
    

What kind of higher order types are expected to flow through this socket

Type:
    

enum in [Node Socket Structure Type Items](../../bpy_types_enum_items/node_socket_structure_type_items.md#rna-enum-node-socket-structure-type-items), default `'AUTO'`

bl_system_properties_get(_*_ , _do_create =False_)
    

DEBUG ONLY. Internal access to runtime-defined RNA data storage, intended solely for testing and debugging purposes. Do not access it in regular scripting work, and in particular, do not assume that it contains writable data

Parameters:
    

**do_create** (_boolean_ _,__(__optional_ _)_) – Ensure that system properties are created if they do not exist yet

Returns:
    

The system properties root container, or None if there are no system properties stored in this data yet, and its creation was not requested

Return type:
    

[[PropertyGroup]]

draw(_context_ , _layout_)
    

Draw properties of the socket interface

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

  * [[NodeTreeInterface.new_socket]]

| 


  
---|---
  *[*]: Keyword-only parameters separator (PEP 3102)
  *[/]: Positional-only parameter separator (PEP 570)
