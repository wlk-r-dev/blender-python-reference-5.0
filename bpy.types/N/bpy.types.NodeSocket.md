# NodeSocket(bpy_struct)

base class — [[bpy_struct]]

subclasses — [[NodeSocketStandard]]

_class _bpy.types.NodeSocket(_bpy_struct_)
    

Input or output socket of a node

bl_idname
    

Type:
    

string, default “”, (never None)

bl_label
    

Label to display for the socket type in the UI

Type:
    

string, default “”, (never None)

bl_subtype_label
    

Label to display for the socket subtype in the UI

Type:
    

string, default “”, (never None)

description
    

Socket tooltip

Type:
    

string, default “”, (never None)

display_shape
    

Socket shape

Type:
    

enum in [`'CIRCLE'`, `'SQUARE'`, `'DIAMOND'`, `'CIRCLE_DOT'`, `'SQUARE_DOT'`, `'DIAMOND_DOT'`, `'LINE'`, `'VOLUME_GRID'`, `'LIST'`], default `'CIRCLE'`

enabled
    

Enable the socket

Type:
    

boolean, default False

hide
    

Hide the socket

Type:
    

boolean, default False

hide_value
    

Hide the socket input value

Type:
    

boolean, default False

identifier
    

Unique identifier for mapping sockets

Type:
    

string, default “”, (readonly, never None)

inferred_structure_type
    

Best known structure type of the socket. This may not match the socket shape, e.g. for unlinked input sockets

Type:
    

enum in [Node Socket Structure Type Items](../../bpy_types_enum_items/node_socket_structure_type_items.md#rna-enum-node-socket-structure-type-items), default `'AUTO'`, (readonly)

is_icon_visible
    

Socket is drawn as interactive icon in the node editor

Type:
    

boolean, default False, (readonly)

is_inactive
    

Socket is grayed out because it has been detected to not have any effect on the output

Type:
    

boolean, default False, (readonly)

is_linked
    

True if the socket is connected

Type:
    

boolean, default False, (readonly)

is_multi_input
    

True if the socket can accept multiple ordered input links

Type:
    

boolean, default False, (readonly)

is_output
    

True if the socket is an output, otherwise input

Type:
    

boolean, default False, (readonly)

is_unavailable
    

True if the socket is unavailable

Type:
    

boolean, default False, (readonly)

label
    

Custom dynamic defined socket label

Type:
    

string, default “”, (readonly, never None)

link_limit
    

Max number of links allowed for this socket

Type:
    

int in [1, 4095], default 0

name
    

Socket name

Type:
    

string, default “”, (never None)

node
    

Node owning this socket

Type:
    

[[Node]], (readonly)

pin_gizmo
    

Keep gizmo visible even when the node is not selected

Type:
    

boolean, default False

select
    

True if the socket is selected

Type:
    

boolean, default False, (readonly)

show_expanded
    

Socket links are expanded in the user interface

Type:
    

boolean, default False

type
    

Data type

Type:
    

enum in [Node Socket Type Items](../../bpy_types_enum_items/node_socket_type_items.md#rna-enum-node-socket-type-items), default `'VALUE'`

links
    

List of node links from or to this socket.

Type:
    

[[NodeLinks]]

Note

Takes `O(len(nodetree.links))` time.

(readonly)

bl_system_properties_get(_*_ , _do_create =False_)
    

DEBUG ONLY. Internal access to runtime-defined RNA data storage, intended solely for testing and debugging purposes. Do not access it in regular scripting work, and in particular, do not assume that it contains writable data

Parameters:
    

**do_create** (_boolean_ _,__(__optional_ _)_) – Ensure that system properties are created if they do not exist yet

Returns:
    

The system properties root container, or None if there are no system properties stored in this data yet, and its creation was not requested

Return type:
    

[[PropertyGroup]]

draw(_context_ , _layout_ , _node_ , _text_)
    

Draw socket

Parameters:
    

  * **layout** ([[UILayout]], (never None)) – Layout, Layout in the UI

  * **node** ([[Node]], (never None)) – Node, Node the socket belongs to

  * **text** (_string_ _,__(__never None_ _)_) – Text, Text label to draw alongside properties


draw_color(_context_ , _node_)
    

Color of the socket icon

Parameters:
    

**node** ([[Node]], (never None)) – Node, Node the socket belongs to

Returns:
    

Color

Return type:
    

float array of 4 items in [0, 1]

_classmethod _draw_color_simple()
    

Color of the socket icon. Used to draw sockets in places where the socket does not belong to a node, like the node interface panel. Also used to draw node sockets if draw_color is not defined.

Returns:
    

Color

Return type:
    

float array of 4 items in [0, 1]

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

  * [[Node.inputs]]
  * [[Node.outputs]]
  * [[NodeInputs.new]]
  * [[NodeInputs.remove]]
  * [[NodeLink.from_socket]]
  * [[NodeLink.to_socket]]
  * [[NodeLinks.new]]
  * [[NodeLinks.new]]
  * [[NodeOutputs.new]]
  * [[NodeOutputs.remove]]
  * [[NodeTreeInterfaceSocket.from_socket]]
  * [[NodeTreeInterfaceSocket.init_socket]]
  * [[NodeTreeInterfaceSocketBool.from_socket]]
  * [[NodeTreeInterfaceSocketBool.init_socket]]
  * [[NodeTreeInterfaceSocketBundle.from_socket]]
  * [[NodeTreeInterfaceSocketBundle.init_socket]]
  * [[NodeTreeInterfaceSocketClosure.from_socket]]
  * [[NodeTreeInterfaceSocketClosure.init_socket]]
  * [[NodeTreeInterfaceSocketCollection.from_socket]]
  * [[NodeTreeInterfaceSocketCollection.init_socket]]
  * [[NodeTreeInterfaceSocketColor.from_socket]]
  * [[NodeTreeInterfaceSocketColor.init_socket]]
  * [[NodeTreeInterfaceSocketFloat.from_socket]]
  * [[NodeTreeInterfaceSocketFloat.init_socket]]
  * [[NodeTreeInterfaceSocketFloatAngle.from_socket]]
  * [[NodeTreeInterfaceSocketFloatAngle.init_socket]]
  * [[NodeTreeInterfaceSocketFloatColorTemperature.from_socket]]
  * [[NodeTreeInterfaceSocketFloatColorTemperature.init_socket]]
  * [[NodeTreeInterfaceSocketFloatDistance.from_socket]]
  * [[NodeTreeInterfaceSocketFloatDistance.init_socket]]
  * [[NodeTreeInterfaceSocketFloatFactor.from_socket]]
  * [[NodeTreeInterfaceSocketFloatFactor.init_socket]]
  * [[NodeTreeInterfaceSocketFloatFrequency.from_socket]]
  * [[NodeTreeInterfaceSocketFloatFrequency.init_socket]]
  * [[NodeTreeInterfaceSocketFloatPercentage.from_socket]]
  * [[NodeTreeInterfaceSocketFloatPercentage.init_socket]]
  * [[NodeTreeInterfaceSocketFloatTime.from_socket]]
  * [[NodeTreeInterfaceSocketFloatTime.init_socket]]
  * [[NodeTreeInterfaceSocketFloatTimeAbsolute.from_socket]]
  * [[NodeTreeInterfaceSocketFloatTimeAbsolute.init_socket]]
  * [[NodeTreeInterfaceSocketFloatUnsigned.from_socket]]
  * [[NodeTreeInterfaceSocketFloatUnsigned.init_socket]]
  * [[NodeTreeInterfaceSocketFloatWavelength.from_socket]]
  * [[NodeTreeInterfaceSocketFloatWavelength.init_socket]]
  * [[NodeTreeInterfaceSocketGeometry.from_socket]]
  * [[NodeTreeInterfaceSocketGeometry.init_socket]]
  * [[NodeTreeInterfaceSocketImage.from_socket]]
  * [[NodeTreeInterfaceSocketImage.init_socket]]
  * [[NodeTreeInterfaceSocketInt.from_socket]]
  * [[NodeTreeInterfaceSocketInt.init_socket]]
  * [[NodeTreeInterfaceSocketIntFactor.from_socket]]
  * [[NodeTreeInterfaceSocketIntFactor.init_socket]]
  * [[NodeTreeInterfaceSocketIntPercentage.from_socket]]
  * [[NodeTreeInterfaceSocketIntPercentage.init_socket]]
  * [[NodeTreeInterfaceSocketIntUnsigned.from_socket]]
  * [[NodeTreeInterfaceSocketIntUnsigned.init_socket]]
  * [[NodeTreeInterfaceSocketMaterial.from_socket]]
  * [[NodeTreeInterfaceSocketMaterial.init_socket]]
  * [[NodeTreeInterfaceSocketMatrix.from_socket]]
  * [[NodeTreeInterfaceSocketMatrix.init_socket]]
  * [[NodeTreeInterfaceSocketMenu.from_socket]]
  * [[NodeTreeInterfaceSocketMenu.init_socket]]
  * [[NodeTreeInterfaceSocketObject.from_socket]]
  * [[NodeTreeInterfaceSocketObject.init_socket]]
  * [[NodeTreeInterfaceSocketRotation.from_socket]]

| 

  * [[NodeTreeInterfaceSocketRotation.init_socket]]
  * [[NodeTreeInterfaceSocketShader.from_socket]]
  * [[NodeTreeInterfaceSocketShader.init_socket]]
  * [[NodeTreeInterfaceSocketString.from_socket]]
  * [[NodeTreeInterfaceSocketString.init_socket]]
  * [[NodeTreeInterfaceSocketStringFilePath.from_socket]]
  * [[NodeTreeInterfaceSocketStringFilePath.init_socket]]
  * [[NodeTreeInterfaceSocketTexture.from_socket]]
  * [[NodeTreeInterfaceSocketTexture.init_socket]]
  * [[NodeTreeInterfaceSocketVector.from_socket]]
  * [[NodeTreeInterfaceSocketVector.init_socket]]
  * [[NodeTreeInterfaceSocketVector2D.from_socket]]
  * [[NodeTreeInterfaceSocketVector2D.init_socket]]
  * [[NodeTreeInterfaceSocketVector4D.from_socket]]
  * [[NodeTreeInterfaceSocketVector4D.init_socket]]
  * [[NodeTreeInterfaceSocketVectorAcceleration.from_socket]]
  * [[NodeTreeInterfaceSocketVectorAcceleration.init_socket]]
  * [[NodeTreeInterfaceSocketVectorAcceleration2D.from_socket]]
  * [[NodeTreeInterfaceSocketVectorAcceleration2D.init_socket]]
  * [[NodeTreeInterfaceSocketVectorAcceleration4D.from_socket]]
  * [[NodeTreeInterfaceSocketVectorAcceleration4D.init_socket]]
  * [[NodeTreeInterfaceSocketVectorDirection.from_socket]]
  * [[NodeTreeInterfaceSocketVectorDirection.init_socket]]
  * [[NodeTreeInterfaceSocketVectorDirection2D.from_socket]]
  * [[NodeTreeInterfaceSocketVectorDirection2D.init_socket]]
  * [[NodeTreeInterfaceSocketVectorDirection4D.from_socket]]
  * [[NodeTreeInterfaceSocketVectorDirection4D.init_socket]]
  * [[NodeTreeInterfaceSocketVectorEuler.from_socket]]
  * [[NodeTreeInterfaceSocketVectorEuler.init_socket]]
  * [[NodeTreeInterfaceSocketVectorEuler2D.from_socket]]
  * [[NodeTreeInterfaceSocketVectorEuler2D.init_socket]]
  * [[NodeTreeInterfaceSocketVectorEuler4D.from_socket]]
  * [[NodeTreeInterfaceSocketVectorEuler4D.init_socket]]
  * [[NodeTreeInterfaceSocketVectorFactor.from_socket]]
  * [[NodeTreeInterfaceSocketVectorFactor.init_socket]]
  * [[NodeTreeInterfaceSocketVectorFactor2D.from_socket]]
  * [[NodeTreeInterfaceSocketVectorFactor2D.init_socket]]
  * [[NodeTreeInterfaceSocketVectorFactor4D.from_socket]]
  * [[NodeTreeInterfaceSocketVectorFactor4D.init_socket]]
  * [[NodeTreeInterfaceSocketVectorPercentage.from_socket]]
  * [[NodeTreeInterfaceSocketVectorPercentage.init_socket]]
  * [[NodeTreeInterfaceSocketVectorPercentage2D.from_socket]]
  * [[NodeTreeInterfaceSocketVectorPercentage2D.init_socket]]
  * [[NodeTreeInterfaceSocketVectorPercentage4D.from_socket]]
  * [[NodeTreeInterfaceSocketVectorPercentage4D.init_socket]]
  * [[NodeTreeInterfaceSocketVectorTranslation.from_socket]]
  * [[NodeTreeInterfaceSocketVectorTranslation.init_socket]]
  * [[NodeTreeInterfaceSocketVectorTranslation2D.from_socket]]
  * [[NodeTreeInterfaceSocketVectorTranslation2D.init_socket]]
  * [[NodeTreeInterfaceSocketVectorTranslation4D.from_socket]]
  * [[NodeTreeInterfaceSocketVectorTranslation4D.init_socket]]
  * [[NodeTreeInterfaceSocketVectorVelocity.from_socket]]
  * [[NodeTreeInterfaceSocketVectorVelocity.init_socket]]
  * [[NodeTreeInterfaceSocketVectorVelocity2D.from_socket]]
  * [[NodeTreeInterfaceSocketVectorVelocity2D.init_socket]]
  * [[NodeTreeInterfaceSocketVectorVelocity4D.from_socket]]
  * [[NodeTreeInterfaceSocketVectorVelocity4D.init_socket]]
  * [[NodeTreeInterfaceSocketVectorXYZ.from_socket]]
  * [[NodeTreeInterfaceSocketVectorXYZ.init_socket]]
  * [[NodeTreeInterfaceSocketVectorXYZ2D.from_socket]]
  * [[NodeTreeInterfaceSocketVectorXYZ2D.init_socket]]
  * [[NodeTreeInterfaceSocketVectorXYZ4D.from_socket]]
  * [[NodeTreeInterfaceSocketVectorXYZ4D.init_socket]]
  * [[UILayout.template_node_link]]
  * [[UILayout.template_node_view]]

  
---|---
  *[*]: Keyword-only parameters separator (PEP 3102)
  *[/]: Positional-only parameter separator (PEP 570)
