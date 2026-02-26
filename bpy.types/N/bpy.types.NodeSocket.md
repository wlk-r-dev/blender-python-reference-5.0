# NodeSocket(bpy_struct)

base class — [`bpy_struct`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct "bpy.types.bpy_struct")

subclasses — [`NodeSocketStandard`](bpy.types.NodeSocketStandard.md#bpy.types.NodeSocketStandard "bpy.types.NodeSocketStandard")

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
    

[`Node`](bpy.types.Node.md#bpy.types.Node "bpy.types.Node"), (readonly)

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
    

[`NodeLinks`](bpy.types.NodeLinks.md#bpy.types.NodeLinks "bpy.types.NodeLinks")

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
    

[`PropertyGroup`](../P/bpy.types.PropertyGroup.md#bpy.types.PropertyGroup "bpy.types.PropertyGroup")

draw(_context_ , _layout_ , _node_ , _text_)
    

Draw socket

Parameters:
    

  * **layout** ([`UILayout`](../U/bpy.types.UILayout.md#bpy.types.UILayout "bpy.types.UILayout"), (never None)) – Layout, Layout in the UI

  * **node** ([`Node`](bpy.types.Node.md#bpy.types.Node "bpy.types.Node"), (never None)) – Node, Node the socket belongs to

  * **text** (_string_ _,__(__never None_ _)_) – Text, Text label to draw alongside properties


draw_color(_context_ , _node_)
    

Color of the socket icon

Parameters:
    

**node** ([`Node`](bpy.types.Node.md#bpy.types.Node "bpy.types.Node"), (never None)) – Node, Node the socket belongs to

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

  * [`Node.inputs`](bpy.types.Node.md#bpy.types.Node.inputs "bpy.types.Node.inputs")
  * [`Node.outputs`](bpy.types.Node.md#bpy.types.Node.outputs "bpy.types.Node.outputs")
  * [`NodeInputs.new`](bpy.types.NodeInputs.md#bpy.types.NodeInputs.new "bpy.types.NodeInputs.new")
  * [`NodeInputs.remove`](bpy.types.NodeInputs.md#bpy.types.NodeInputs.remove "bpy.types.NodeInputs.remove")
  * [`NodeLink.from_socket`](bpy.types.NodeLink.md#bpy.types.NodeLink.from_socket "bpy.types.NodeLink.from_socket")
  * [`NodeLink.to_socket`](bpy.types.NodeLink.md#bpy.types.NodeLink.to_socket "bpy.types.NodeLink.to_socket")
  * [`NodeLinks.new`](bpy.types.NodeLinks.md#bpy.types.NodeLinks.new "bpy.types.NodeLinks.new")
  * [`NodeLinks.new`](bpy.types.NodeLinks.md#bpy.types.NodeLinks.new "bpy.types.NodeLinks.new")
  * [`NodeOutputs.new`](bpy.types.NodeOutputs.md#bpy.types.NodeOutputs.new "bpy.types.NodeOutputs.new")
  * [`NodeOutputs.remove`](bpy.types.NodeOutputs.md#bpy.types.NodeOutputs.remove "bpy.types.NodeOutputs.remove")
  * [`NodeTreeInterfaceSocket.from_socket`](bpy.types.NodeTreeInterfaceSocket.md#bpy.types.NodeTreeInterfaceSocket.from_socket "bpy.types.NodeTreeInterfaceSocket.from_socket")
  * [`NodeTreeInterfaceSocket.init_socket`](bpy.types.NodeTreeInterfaceSocket.md#bpy.types.NodeTreeInterfaceSocket.init_socket "bpy.types.NodeTreeInterfaceSocket.init_socket")
  * [`NodeTreeInterfaceSocketBool.from_socket`](bpy.types.NodeTreeInterfaceSocketBool.md#bpy.types.NodeTreeInterfaceSocketBool.from_socket "bpy.types.NodeTreeInterfaceSocketBool.from_socket")
  * [`NodeTreeInterfaceSocketBool.init_socket`](bpy.types.NodeTreeInterfaceSocketBool.md#bpy.types.NodeTreeInterfaceSocketBool.init_socket "bpy.types.NodeTreeInterfaceSocketBool.init_socket")
  * [`NodeTreeInterfaceSocketBundle.from_socket`](bpy.types.NodeTreeInterfaceSocketBundle.md#bpy.types.NodeTreeInterfaceSocketBundle.from_socket "bpy.types.NodeTreeInterfaceSocketBundle.from_socket")
  * [`NodeTreeInterfaceSocketBundle.init_socket`](bpy.types.NodeTreeInterfaceSocketBundle.md#bpy.types.NodeTreeInterfaceSocketBundle.init_socket "bpy.types.NodeTreeInterfaceSocketBundle.init_socket")
  * [`NodeTreeInterfaceSocketClosure.from_socket`](bpy.types.NodeTreeInterfaceSocketClosure.md#bpy.types.NodeTreeInterfaceSocketClosure.from_socket "bpy.types.NodeTreeInterfaceSocketClosure.from_socket")
  * [`NodeTreeInterfaceSocketClosure.init_socket`](bpy.types.NodeTreeInterfaceSocketClosure.md#bpy.types.NodeTreeInterfaceSocketClosure.init_socket "bpy.types.NodeTreeInterfaceSocketClosure.init_socket")
  * [`NodeTreeInterfaceSocketCollection.from_socket`](bpy.types.NodeTreeInterfaceSocketCollection.md#bpy.types.NodeTreeInterfaceSocketCollection.from_socket "bpy.types.NodeTreeInterfaceSocketCollection.from_socket")
  * [`NodeTreeInterfaceSocketCollection.init_socket`](bpy.types.NodeTreeInterfaceSocketCollection.md#bpy.types.NodeTreeInterfaceSocketCollection.init_socket "bpy.types.NodeTreeInterfaceSocketCollection.init_socket")
  * [`NodeTreeInterfaceSocketColor.from_socket`](bpy.types.NodeTreeInterfaceSocketColor.md#bpy.types.NodeTreeInterfaceSocketColor.from_socket "bpy.types.NodeTreeInterfaceSocketColor.from_socket")
  * [`NodeTreeInterfaceSocketColor.init_socket`](bpy.types.NodeTreeInterfaceSocketColor.md#bpy.types.NodeTreeInterfaceSocketColor.init_socket "bpy.types.NodeTreeInterfaceSocketColor.init_socket")
  * [`NodeTreeInterfaceSocketFloat.from_socket`](bpy.types.NodeTreeInterfaceSocketFloat.md#bpy.types.NodeTreeInterfaceSocketFloat.from_socket "bpy.types.NodeTreeInterfaceSocketFloat.from_socket")
  * [`NodeTreeInterfaceSocketFloat.init_socket`](bpy.types.NodeTreeInterfaceSocketFloat.md#bpy.types.NodeTreeInterfaceSocketFloat.init_socket "bpy.types.NodeTreeInterfaceSocketFloat.init_socket")
  * [`NodeTreeInterfaceSocketFloatAngle.from_socket`](bpy.types.NodeTreeInterfaceSocketFloatAngle.md#bpy.types.NodeTreeInterfaceSocketFloatAngle.from_socket "bpy.types.NodeTreeInterfaceSocketFloatAngle.from_socket")
  * [`NodeTreeInterfaceSocketFloatAngle.init_socket`](bpy.types.NodeTreeInterfaceSocketFloatAngle.md#bpy.types.NodeTreeInterfaceSocketFloatAngle.init_socket "bpy.types.NodeTreeInterfaceSocketFloatAngle.init_socket")
  * [`NodeTreeInterfaceSocketFloatColorTemperature.from_socket`](bpy.types.NodeTreeInterfaceSocketFloatColorTemperature.md#bpy.types.NodeTreeInterfaceSocketFloatColorTemperature.from_socket "bpy.types.NodeTreeInterfaceSocketFloatColorTemperature.from_socket")
  * [`NodeTreeInterfaceSocketFloatColorTemperature.init_socket`](bpy.types.NodeTreeInterfaceSocketFloatColorTemperature.md#bpy.types.NodeTreeInterfaceSocketFloatColorTemperature.init_socket "bpy.types.NodeTreeInterfaceSocketFloatColorTemperature.init_socket")
  * [`NodeTreeInterfaceSocketFloatDistance.from_socket`](bpy.types.NodeTreeInterfaceSocketFloatDistance.md#bpy.types.NodeTreeInterfaceSocketFloatDistance.from_socket "bpy.types.NodeTreeInterfaceSocketFloatDistance.from_socket")
  * [`NodeTreeInterfaceSocketFloatDistance.init_socket`](bpy.types.NodeTreeInterfaceSocketFloatDistance.md#bpy.types.NodeTreeInterfaceSocketFloatDistance.init_socket "bpy.types.NodeTreeInterfaceSocketFloatDistance.init_socket")
  * [`NodeTreeInterfaceSocketFloatFactor.from_socket`](bpy.types.NodeTreeInterfaceSocketFloatFactor.md#bpy.types.NodeTreeInterfaceSocketFloatFactor.from_socket "bpy.types.NodeTreeInterfaceSocketFloatFactor.from_socket")
  * [`NodeTreeInterfaceSocketFloatFactor.init_socket`](bpy.types.NodeTreeInterfaceSocketFloatFactor.md#bpy.types.NodeTreeInterfaceSocketFloatFactor.init_socket "bpy.types.NodeTreeInterfaceSocketFloatFactor.init_socket")
  * [`NodeTreeInterfaceSocketFloatFrequency.from_socket`](bpy.types.NodeTreeInterfaceSocketFloatFrequency.md#bpy.types.NodeTreeInterfaceSocketFloatFrequency.from_socket "bpy.types.NodeTreeInterfaceSocketFloatFrequency.from_socket")
  * [`NodeTreeInterfaceSocketFloatFrequency.init_socket`](bpy.types.NodeTreeInterfaceSocketFloatFrequency.md#bpy.types.NodeTreeInterfaceSocketFloatFrequency.init_socket "bpy.types.NodeTreeInterfaceSocketFloatFrequency.init_socket")
  * [`NodeTreeInterfaceSocketFloatPercentage.from_socket`](bpy.types.NodeTreeInterfaceSocketFloatPercentage.md#bpy.types.NodeTreeInterfaceSocketFloatPercentage.from_socket "bpy.types.NodeTreeInterfaceSocketFloatPercentage.from_socket")
  * [`NodeTreeInterfaceSocketFloatPercentage.init_socket`](bpy.types.NodeTreeInterfaceSocketFloatPercentage.md#bpy.types.NodeTreeInterfaceSocketFloatPercentage.init_socket "bpy.types.NodeTreeInterfaceSocketFloatPercentage.init_socket")
  * [`NodeTreeInterfaceSocketFloatTime.from_socket`](bpy.types.NodeTreeInterfaceSocketFloatTime.md#bpy.types.NodeTreeInterfaceSocketFloatTime.from_socket "bpy.types.NodeTreeInterfaceSocketFloatTime.from_socket")
  * [`NodeTreeInterfaceSocketFloatTime.init_socket`](bpy.types.NodeTreeInterfaceSocketFloatTime.md#bpy.types.NodeTreeInterfaceSocketFloatTime.init_socket "bpy.types.NodeTreeInterfaceSocketFloatTime.init_socket")
  * [`NodeTreeInterfaceSocketFloatTimeAbsolute.from_socket`](bpy.types.NodeTreeInterfaceSocketFloatTimeAbsolute.md#bpy.types.NodeTreeInterfaceSocketFloatTimeAbsolute.from_socket "bpy.types.NodeTreeInterfaceSocketFloatTimeAbsolute.from_socket")
  * [`NodeTreeInterfaceSocketFloatTimeAbsolute.init_socket`](bpy.types.NodeTreeInterfaceSocketFloatTimeAbsolute.md#bpy.types.NodeTreeInterfaceSocketFloatTimeAbsolute.init_socket "bpy.types.NodeTreeInterfaceSocketFloatTimeAbsolute.init_socket")
  * [`NodeTreeInterfaceSocketFloatUnsigned.from_socket`](bpy.types.NodeTreeInterfaceSocketFloatUnsigned.md#bpy.types.NodeTreeInterfaceSocketFloatUnsigned.from_socket "bpy.types.NodeTreeInterfaceSocketFloatUnsigned.from_socket")
  * [`NodeTreeInterfaceSocketFloatUnsigned.init_socket`](bpy.types.NodeTreeInterfaceSocketFloatUnsigned.md#bpy.types.NodeTreeInterfaceSocketFloatUnsigned.init_socket "bpy.types.NodeTreeInterfaceSocketFloatUnsigned.init_socket")
  * [`NodeTreeInterfaceSocketFloatWavelength.from_socket`](bpy.types.NodeTreeInterfaceSocketFloatWavelength.md#bpy.types.NodeTreeInterfaceSocketFloatWavelength.from_socket "bpy.types.NodeTreeInterfaceSocketFloatWavelength.from_socket")
  * [`NodeTreeInterfaceSocketFloatWavelength.init_socket`](bpy.types.NodeTreeInterfaceSocketFloatWavelength.md#bpy.types.NodeTreeInterfaceSocketFloatWavelength.init_socket "bpy.types.NodeTreeInterfaceSocketFloatWavelength.init_socket")
  * [`NodeTreeInterfaceSocketGeometry.from_socket`](bpy.types.NodeTreeInterfaceSocketGeometry.md#bpy.types.NodeTreeInterfaceSocketGeometry.from_socket "bpy.types.NodeTreeInterfaceSocketGeometry.from_socket")
  * [`NodeTreeInterfaceSocketGeometry.init_socket`](bpy.types.NodeTreeInterfaceSocketGeometry.md#bpy.types.NodeTreeInterfaceSocketGeometry.init_socket "bpy.types.NodeTreeInterfaceSocketGeometry.init_socket")
  * [`NodeTreeInterfaceSocketImage.from_socket`](bpy.types.NodeTreeInterfaceSocketImage.md#bpy.types.NodeTreeInterfaceSocketImage.from_socket "bpy.types.NodeTreeInterfaceSocketImage.from_socket")
  * [`NodeTreeInterfaceSocketImage.init_socket`](bpy.types.NodeTreeInterfaceSocketImage.md#bpy.types.NodeTreeInterfaceSocketImage.init_socket "bpy.types.NodeTreeInterfaceSocketImage.init_socket")
  * [`NodeTreeInterfaceSocketInt.from_socket`](bpy.types.NodeTreeInterfaceSocketInt.md#bpy.types.NodeTreeInterfaceSocketInt.from_socket "bpy.types.NodeTreeInterfaceSocketInt.from_socket")
  * [`NodeTreeInterfaceSocketInt.init_socket`](bpy.types.NodeTreeInterfaceSocketInt.md#bpy.types.NodeTreeInterfaceSocketInt.init_socket "bpy.types.NodeTreeInterfaceSocketInt.init_socket")
  * [`NodeTreeInterfaceSocketIntFactor.from_socket`](bpy.types.NodeTreeInterfaceSocketIntFactor.md#bpy.types.NodeTreeInterfaceSocketIntFactor.from_socket "bpy.types.NodeTreeInterfaceSocketIntFactor.from_socket")
  * [`NodeTreeInterfaceSocketIntFactor.init_socket`](bpy.types.NodeTreeInterfaceSocketIntFactor.md#bpy.types.NodeTreeInterfaceSocketIntFactor.init_socket "bpy.types.NodeTreeInterfaceSocketIntFactor.init_socket")
  * [`NodeTreeInterfaceSocketIntPercentage.from_socket`](bpy.types.NodeTreeInterfaceSocketIntPercentage.md#bpy.types.NodeTreeInterfaceSocketIntPercentage.from_socket "bpy.types.NodeTreeInterfaceSocketIntPercentage.from_socket")
  * [`NodeTreeInterfaceSocketIntPercentage.init_socket`](bpy.types.NodeTreeInterfaceSocketIntPercentage.md#bpy.types.NodeTreeInterfaceSocketIntPercentage.init_socket "bpy.types.NodeTreeInterfaceSocketIntPercentage.init_socket")
  * [`NodeTreeInterfaceSocketIntUnsigned.from_socket`](bpy.types.NodeTreeInterfaceSocketIntUnsigned.md#bpy.types.NodeTreeInterfaceSocketIntUnsigned.from_socket "bpy.types.NodeTreeInterfaceSocketIntUnsigned.from_socket")
  * [`NodeTreeInterfaceSocketIntUnsigned.init_socket`](bpy.types.NodeTreeInterfaceSocketIntUnsigned.md#bpy.types.NodeTreeInterfaceSocketIntUnsigned.init_socket "bpy.types.NodeTreeInterfaceSocketIntUnsigned.init_socket")
  * [`NodeTreeInterfaceSocketMaterial.from_socket`](bpy.types.NodeTreeInterfaceSocketMaterial.md#bpy.types.NodeTreeInterfaceSocketMaterial.from_socket "bpy.types.NodeTreeInterfaceSocketMaterial.from_socket")
  * [`NodeTreeInterfaceSocketMaterial.init_socket`](bpy.types.NodeTreeInterfaceSocketMaterial.md#bpy.types.NodeTreeInterfaceSocketMaterial.init_socket "bpy.types.NodeTreeInterfaceSocketMaterial.init_socket")
  * [`NodeTreeInterfaceSocketMatrix.from_socket`](bpy.types.NodeTreeInterfaceSocketMatrix.md#bpy.types.NodeTreeInterfaceSocketMatrix.from_socket "bpy.types.NodeTreeInterfaceSocketMatrix.from_socket")
  * [`NodeTreeInterfaceSocketMatrix.init_socket`](bpy.types.NodeTreeInterfaceSocketMatrix.md#bpy.types.NodeTreeInterfaceSocketMatrix.init_socket "bpy.types.NodeTreeInterfaceSocketMatrix.init_socket")
  * [`NodeTreeInterfaceSocketMenu.from_socket`](bpy.types.NodeTreeInterfaceSocketMenu.md#bpy.types.NodeTreeInterfaceSocketMenu.from_socket "bpy.types.NodeTreeInterfaceSocketMenu.from_socket")
  * [`NodeTreeInterfaceSocketMenu.init_socket`](bpy.types.NodeTreeInterfaceSocketMenu.md#bpy.types.NodeTreeInterfaceSocketMenu.init_socket "bpy.types.NodeTreeInterfaceSocketMenu.init_socket")
  * [`NodeTreeInterfaceSocketObject.from_socket`](bpy.types.NodeTreeInterfaceSocketObject.md#bpy.types.NodeTreeInterfaceSocketObject.from_socket "bpy.types.NodeTreeInterfaceSocketObject.from_socket")
  * [`NodeTreeInterfaceSocketObject.init_socket`](bpy.types.NodeTreeInterfaceSocketObject.md#bpy.types.NodeTreeInterfaceSocketObject.init_socket "bpy.types.NodeTreeInterfaceSocketObject.init_socket")
  * [`NodeTreeInterfaceSocketRotation.from_socket`](bpy.types.NodeTreeInterfaceSocketRotation.md#bpy.types.NodeTreeInterfaceSocketRotation.from_socket "bpy.types.NodeTreeInterfaceSocketRotation.from_socket")

| 

  * [`NodeTreeInterfaceSocketRotation.init_socket`](bpy.types.NodeTreeInterfaceSocketRotation.md#bpy.types.NodeTreeInterfaceSocketRotation.init_socket "bpy.types.NodeTreeInterfaceSocketRotation.init_socket")
  * [`NodeTreeInterfaceSocketShader.from_socket`](bpy.types.NodeTreeInterfaceSocketShader.md#bpy.types.NodeTreeInterfaceSocketShader.from_socket "bpy.types.NodeTreeInterfaceSocketShader.from_socket")
  * [`NodeTreeInterfaceSocketShader.init_socket`](bpy.types.NodeTreeInterfaceSocketShader.md#bpy.types.NodeTreeInterfaceSocketShader.init_socket "bpy.types.NodeTreeInterfaceSocketShader.init_socket")
  * [`NodeTreeInterfaceSocketString.from_socket`](bpy.types.NodeTreeInterfaceSocketString.md#bpy.types.NodeTreeInterfaceSocketString.from_socket "bpy.types.NodeTreeInterfaceSocketString.from_socket")
  * [`NodeTreeInterfaceSocketString.init_socket`](bpy.types.NodeTreeInterfaceSocketString.md#bpy.types.NodeTreeInterfaceSocketString.init_socket "bpy.types.NodeTreeInterfaceSocketString.init_socket")
  * [`NodeTreeInterfaceSocketStringFilePath.from_socket`](bpy.types.NodeTreeInterfaceSocketStringFilePath.md#bpy.types.NodeTreeInterfaceSocketStringFilePath.from_socket "bpy.types.NodeTreeInterfaceSocketStringFilePath.from_socket")
  * [`NodeTreeInterfaceSocketStringFilePath.init_socket`](bpy.types.NodeTreeInterfaceSocketStringFilePath.md#bpy.types.NodeTreeInterfaceSocketStringFilePath.init_socket "bpy.types.NodeTreeInterfaceSocketStringFilePath.init_socket")
  * [`NodeTreeInterfaceSocketTexture.from_socket`](bpy.types.NodeTreeInterfaceSocketTexture.md#bpy.types.NodeTreeInterfaceSocketTexture.from_socket "bpy.types.NodeTreeInterfaceSocketTexture.from_socket")
  * [`NodeTreeInterfaceSocketTexture.init_socket`](bpy.types.NodeTreeInterfaceSocketTexture.md#bpy.types.NodeTreeInterfaceSocketTexture.init_socket "bpy.types.NodeTreeInterfaceSocketTexture.init_socket")
  * [`NodeTreeInterfaceSocketVector.from_socket`](bpy.types.NodeTreeInterfaceSocketVector.md#bpy.types.NodeTreeInterfaceSocketVector.from_socket "bpy.types.NodeTreeInterfaceSocketVector.from_socket")
  * [`NodeTreeInterfaceSocketVector.init_socket`](bpy.types.NodeTreeInterfaceSocketVector.md#bpy.types.NodeTreeInterfaceSocketVector.init_socket "bpy.types.NodeTreeInterfaceSocketVector.init_socket")
  * [`NodeTreeInterfaceSocketVector2D.from_socket`](bpy.types.NodeTreeInterfaceSocketVector2D.md#bpy.types.NodeTreeInterfaceSocketVector2D.from_socket "bpy.types.NodeTreeInterfaceSocketVector2D.from_socket")
  * [`NodeTreeInterfaceSocketVector2D.init_socket`](bpy.types.NodeTreeInterfaceSocketVector2D.md#bpy.types.NodeTreeInterfaceSocketVector2D.init_socket "bpy.types.NodeTreeInterfaceSocketVector2D.init_socket")
  * [`NodeTreeInterfaceSocketVector4D.from_socket`](bpy.types.NodeTreeInterfaceSocketVector4D.md#bpy.types.NodeTreeInterfaceSocketVector4D.from_socket "bpy.types.NodeTreeInterfaceSocketVector4D.from_socket")
  * [`NodeTreeInterfaceSocketVector4D.init_socket`](bpy.types.NodeTreeInterfaceSocketVector4D.md#bpy.types.NodeTreeInterfaceSocketVector4D.init_socket "bpy.types.NodeTreeInterfaceSocketVector4D.init_socket")
  * [`NodeTreeInterfaceSocketVectorAcceleration.from_socket`](bpy.types.NodeTreeInterfaceSocketVectorAcceleration.md#bpy.types.NodeTreeInterfaceSocketVectorAcceleration.from_socket "bpy.types.NodeTreeInterfaceSocketVectorAcceleration.from_socket")
  * [`NodeTreeInterfaceSocketVectorAcceleration.init_socket`](bpy.types.NodeTreeInterfaceSocketVectorAcceleration.md#bpy.types.NodeTreeInterfaceSocketVectorAcceleration.init_socket "bpy.types.NodeTreeInterfaceSocketVectorAcceleration.init_socket")
  * [`NodeTreeInterfaceSocketVectorAcceleration2D.from_socket`](bpy.types.NodeTreeInterfaceSocketVectorAcceleration2D.md#bpy.types.NodeTreeInterfaceSocketVectorAcceleration2D.from_socket "bpy.types.NodeTreeInterfaceSocketVectorAcceleration2D.from_socket")
  * [`NodeTreeInterfaceSocketVectorAcceleration2D.init_socket`](bpy.types.NodeTreeInterfaceSocketVectorAcceleration2D.md#bpy.types.NodeTreeInterfaceSocketVectorAcceleration2D.init_socket "bpy.types.NodeTreeInterfaceSocketVectorAcceleration2D.init_socket")
  * [`NodeTreeInterfaceSocketVectorAcceleration4D.from_socket`](bpy.types.NodeTreeInterfaceSocketVectorAcceleration4D.md#bpy.types.NodeTreeInterfaceSocketVectorAcceleration4D.from_socket "bpy.types.NodeTreeInterfaceSocketVectorAcceleration4D.from_socket")
  * [`NodeTreeInterfaceSocketVectorAcceleration4D.init_socket`](bpy.types.NodeTreeInterfaceSocketVectorAcceleration4D.md#bpy.types.NodeTreeInterfaceSocketVectorAcceleration4D.init_socket "bpy.types.NodeTreeInterfaceSocketVectorAcceleration4D.init_socket")
  * [`NodeTreeInterfaceSocketVectorDirection.from_socket`](bpy.types.NodeTreeInterfaceSocketVectorDirection.md#bpy.types.NodeTreeInterfaceSocketVectorDirection.from_socket "bpy.types.NodeTreeInterfaceSocketVectorDirection.from_socket")
  * [`NodeTreeInterfaceSocketVectorDirection.init_socket`](bpy.types.NodeTreeInterfaceSocketVectorDirection.md#bpy.types.NodeTreeInterfaceSocketVectorDirection.init_socket "bpy.types.NodeTreeInterfaceSocketVectorDirection.init_socket")
  * [`NodeTreeInterfaceSocketVectorDirection2D.from_socket`](bpy.types.NodeTreeInterfaceSocketVectorDirection2D.md#bpy.types.NodeTreeInterfaceSocketVectorDirection2D.from_socket "bpy.types.NodeTreeInterfaceSocketVectorDirection2D.from_socket")
  * [`NodeTreeInterfaceSocketVectorDirection2D.init_socket`](bpy.types.NodeTreeInterfaceSocketVectorDirection2D.md#bpy.types.NodeTreeInterfaceSocketVectorDirection2D.init_socket "bpy.types.NodeTreeInterfaceSocketVectorDirection2D.init_socket")
  * [`NodeTreeInterfaceSocketVectorDirection4D.from_socket`](bpy.types.NodeTreeInterfaceSocketVectorDirection4D.md#bpy.types.NodeTreeInterfaceSocketVectorDirection4D.from_socket "bpy.types.NodeTreeInterfaceSocketVectorDirection4D.from_socket")
  * [`NodeTreeInterfaceSocketVectorDirection4D.init_socket`](bpy.types.NodeTreeInterfaceSocketVectorDirection4D.md#bpy.types.NodeTreeInterfaceSocketVectorDirection4D.init_socket "bpy.types.NodeTreeInterfaceSocketVectorDirection4D.init_socket")
  * [`NodeTreeInterfaceSocketVectorEuler.from_socket`](bpy.types.NodeTreeInterfaceSocketVectorEuler.md#bpy.types.NodeTreeInterfaceSocketVectorEuler.from_socket "bpy.types.NodeTreeInterfaceSocketVectorEuler.from_socket")
  * [`NodeTreeInterfaceSocketVectorEuler.init_socket`](bpy.types.NodeTreeInterfaceSocketVectorEuler.md#bpy.types.NodeTreeInterfaceSocketVectorEuler.init_socket "bpy.types.NodeTreeInterfaceSocketVectorEuler.init_socket")
  * [`NodeTreeInterfaceSocketVectorEuler2D.from_socket`](bpy.types.NodeTreeInterfaceSocketVectorEuler2D.md#bpy.types.NodeTreeInterfaceSocketVectorEuler2D.from_socket "bpy.types.NodeTreeInterfaceSocketVectorEuler2D.from_socket")
  * [`NodeTreeInterfaceSocketVectorEuler2D.init_socket`](bpy.types.NodeTreeInterfaceSocketVectorEuler2D.md#bpy.types.NodeTreeInterfaceSocketVectorEuler2D.init_socket "bpy.types.NodeTreeInterfaceSocketVectorEuler2D.init_socket")
  * [`NodeTreeInterfaceSocketVectorEuler4D.from_socket`](bpy.types.NodeTreeInterfaceSocketVectorEuler4D.md#bpy.types.NodeTreeInterfaceSocketVectorEuler4D.from_socket "bpy.types.NodeTreeInterfaceSocketVectorEuler4D.from_socket")
  * [`NodeTreeInterfaceSocketVectorEuler4D.init_socket`](bpy.types.NodeTreeInterfaceSocketVectorEuler4D.md#bpy.types.NodeTreeInterfaceSocketVectorEuler4D.init_socket "bpy.types.NodeTreeInterfaceSocketVectorEuler4D.init_socket")
  * [`NodeTreeInterfaceSocketVectorFactor.from_socket`](bpy.types.NodeTreeInterfaceSocketVectorFactor.md#bpy.types.NodeTreeInterfaceSocketVectorFactor.from_socket "bpy.types.NodeTreeInterfaceSocketVectorFactor.from_socket")
  * [`NodeTreeInterfaceSocketVectorFactor.init_socket`](bpy.types.NodeTreeInterfaceSocketVectorFactor.md#bpy.types.NodeTreeInterfaceSocketVectorFactor.init_socket "bpy.types.NodeTreeInterfaceSocketVectorFactor.init_socket")
  * [`NodeTreeInterfaceSocketVectorFactor2D.from_socket`](bpy.types.NodeTreeInterfaceSocketVectorFactor2D.md#bpy.types.NodeTreeInterfaceSocketVectorFactor2D.from_socket "bpy.types.NodeTreeInterfaceSocketVectorFactor2D.from_socket")
  * [`NodeTreeInterfaceSocketVectorFactor2D.init_socket`](bpy.types.NodeTreeInterfaceSocketVectorFactor2D.md#bpy.types.NodeTreeInterfaceSocketVectorFactor2D.init_socket "bpy.types.NodeTreeInterfaceSocketVectorFactor2D.init_socket")
  * [`NodeTreeInterfaceSocketVectorFactor4D.from_socket`](bpy.types.NodeTreeInterfaceSocketVectorFactor4D.md#bpy.types.NodeTreeInterfaceSocketVectorFactor4D.from_socket "bpy.types.NodeTreeInterfaceSocketVectorFactor4D.from_socket")
  * [`NodeTreeInterfaceSocketVectorFactor4D.init_socket`](bpy.types.NodeTreeInterfaceSocketVectorFactor4D.md#bpy.types.NodeTreeInterfaceSocketVectorFactor4D.init_socket "bpy.types.NodeTreeInterfaceSocketVectorFactor4D.init_socket")
  * [`NodeTreeInterfaceSocketVectorPercentage.from_socket`](bpy.types.NodeTreeInterfaceSocketVectorPercentage.md#bpy.types.NodeTreeInterfaceSocketVectorPercentage.from_socket "bpy.types.NodeTreeInterfaceSocketVectorPercentage.from_socket")
  * [`NodeTreeInterfaceSocketVectorPercentage.init_socket`](bpy.types.NodeTreeInterfaceSocketVectorPercentage.md#bpy.types.NodeTreeInterfaceSocketVectorPercentage.init_socket "bpy.types.NodeTreeInterfaceSocketVectorPercentage.init_socket")
  * [`NodeTreeInterfaceSocketVectorPercentage2D.from_socket`](bpy.types.NodeTreeInterfaceSocketVectorPercentage2D.md#bpy.types.NodeTreeInterfaceSocketVectorPercentage2D.from_socket "bpy.types.NodeTreeInterfaceSocketVectorPercentage2D.from_socket")
  * [`NodeTreeInterfaceSocketVectorPercentage2D.init_socket`](bpy.types.NodeTreeInterfaceSocketVectorPercentage2D.md#bpy.types.NodeTreeInterfaceSocketVectorPercentage2D.init_socket "bpy.types.NodeTreeInterfaceSocketVectorPercentage2D.init_socket")
  * [`NodeTreeInterfaceSocketVectorPercentage4D.from_socket`](bpy.types.NodeTreeInterfaceSocketVectorPercentage4D.md#bpy.types.NodeTreeInterfaceSocketVectorPercentage4D.from_socket "bpy.types.NodeTreeInterfaceSocketVectorPercentage4D.from_socket")
  * [`NodeTreeInterfaceSocketVectorPercentage4D.init_socket`](bpy.types.NodeTreeInterfaceSocketVectorPercentage4D.md#bpy.types.NodeTreeInterfaceSocketVectorPercentage4D.init_socket "bpy.types.NodeTreeInterfaceSocketVectorPercentage4D.init_socket")
  * [`NodeTreeInterfaceSocketVectorTranslation.from_socket`](bpy.types.NodeTreeInterfaceSocketVectorTranslation.md#bpy.types.NodeTreeInterfaceSocketVectorTranslation.from_socket "bpy.types.NodeTreeInterfaceSocketVectorTranslation.from_socket")
  * [`NodeTreeInterfaceSocketVectorTranslation.init_socket`](bpy.types.NodeTreeInterfaceSocketVectorTranslation.md#bpy.types.NodeTreeInterfaceSocketVectorTranslation.init_socket "bpy.types.NodeTreeInterfaceSocketVectorTranslation.init_socket")
  * [`NodeTreeInterfaceSocketVectorTranslation2D.from_socket`](bpy.types.NodeTreeInterfaceSocketVectorTranslation2D.md#bpy.types.NodeTreeInterfaceSocketVectorTranslation2D.from_socket "bpy.types.NodeTreeInterfaceSocketVectorTranslation2D.from_socket")
  * [`NodeTreeInterfaceSocketVectorTranslation2D.init_socket`](bpy.types.NodeTreeInterfaceSocketVectorTranslation2D.md#bpy.types.NodeTreeInterfaceSocketVectorTranslation2D.init_socket "bpy.types.NodeTreeInterfaceSocketVectorTranslation2D.init_socket")
  * [`NodeTreeInterfaceSocketVectorTranslation4D.from_socket`](bpy.types.NodeTreeInterfaceSocketVectorTranslation4D.md#bpy.types.NodeTreeInterfaceSocketVectorTranslation4D.from_socket "bpy.types.NodeTreeInterfaceSocketVectorTranslation4D.from_socket")
  * [`NodeTreeInterfaceSocketVectorTranslation4D.init_socket`](bpy.types.NodeTreeInterfaceSocketVectorTranslation4D.md#bpy.types.NodeTreeInterfaceSocketVectorTranslation4D.init_socket "bpy.types.NodeTreeInterfaceSocketVectorTranslation4D.init_socket")
  * [`NodeTreeInterfaceSocketVectorVelocity.from_socket`](bpy.types.NodeTreeInterfaceSocketVectorVelocity.md#bpy.types.NodeTreeInterfaceSocketVectorVelocity.from_socket "bpy.types.NodeTreeInterfaceSocketVectorVelocity.from_socket")
  * [`NodeTreeInterfaceSocketVectorVelocity.init_socket`](bpy.types.NodeTreeInterfaceSocketVectorVelocity.md#bpy.types.NodeTreeInterfaceSocketVectorVelocity.init_socket "bpy.types.NodeTreeInterfaceSocketVectorVelocity.init_socket")
  * [`NodeTreeInterfaceSocketVectorVelocity2D.from_socket`](bpy.types.NodeTreeInterfaceSocketVectorVelocity2D.md#bpy.types.NodeTreeInterfaceSocketVectorVelocity2D.from_socket "bpy.types.NodeTreeInterfaceSocketVectorVelocity2D.from_socket")
  * [`NodeTreeInterfaceSocketVectorVelocity2D.init_socket`](bpy.types.NodeTreeInterfaceSocketVectorVelocity2D.md#bpy.types.NodeTreeInterfaceSocketVectorVelocity2D.init_socket "bpy.types.NodeTreeInterfaceSocketVectorVelocity2D.init_socket")
  * [`NodeTreeInterfaceSocketVectorVelocity4D.from_socket`](bpy.types.NodeTreeInterfaceSocketVectorVelocity4D.md#bpy.types.NodeTreeInterfaceSocketVectorVelocity4D.from_socket "bpy.types.NodeTreeInterfaceSocketVectorVelocity4D.from_socket")
  * [`NodeTreeInterfaceSocketVectorVelocity4D.init_socket`](bpy.types.NodeTreeInterfaceSocketVectorVelocity4D.md#bpy.types.NodeTreeInterfaceSocketVectorVelocity4D.init_socket "bpy.types.NodeTreeInterfaceSocketVectorVelocity4D.init_socket")
  * [`NodeTreeInterfaceSocketVectorXYZ.from_socket`](bpy.types.NodeTreeInterfaceSocketVectorXYZ.md#bpy.types.NodeTreeInterfaceSocketVectorXYZ.from_socket "bpy.types.NodeTreeInterfaceSocketVectorXYZ.from_socket")
  * [`NodeTreeInterfaceSocketVectorXYZ.init_socket`](bpy.types.NodeTreeInterfaceSocketVectorXYZ.md#bpy.types.NodeTreeInterfaceSocketVectorXYZ.init_socket "bpy.types.NodeTreeInterfaceSocketVectorXYZ.init_socket")
  * [`NodeTreeInterfaceSocketVectorXYZ2D.from_socket`](bpy.types.NodeTreeInterfaceSocketVectorXYZ2D.md#bpy.types.NodeTreeInterfaceSocketVectorXYZ2D.from_socket "bpy.types.NodeTreeInterfaceSocketVectorXYZ2D.from_socket")
  * [`NodeTreeInterfaceSocketVectorXYZ2D.init_socket`](bpy.types.NodeTreeInterfaceSocketVectorXYZ2D.md#bpy.types.NodeTreeInterfaceSocketVectorXYZ2D.init_socket "bpy.types.NodeTreeInterfaceSocketVectorXYZ2D.init_socket")
  * [`NodeTreeInterfaceSocketVectorXYZ4D.from_socket`](bpy.types.NodeTreeInterfaceSocketVectorXYZ4D.md#bpy.types.NodeTreeInterfaceSocketVectorXYZ4D.from_socket "bpy.types.NodeTreeInterfaceSocketVectorXYZ4D.from_socket")
  * [`NodeTreeInterfaceSocketVectorXYZ4D.init_socket`](bpy.types.NodeTreeInterfaceSocketVectorXYZ4D.md#bpy.types.NodeTreeInterfaceSocketVectorXYZ4D.init_socket "bpy.types.NodeTreeInterfaceSocketVectorXYZ4D.init_socket")
  * [`UILayout.template_node_link`](../U/bpy.types.UILayout.md#bpy.types.UILayout.template_node_link "bpy.types.UILayout.template_node_link")
  * [`UILayout.template_node_view`](../U/bpy.types.UILayout.md#bpy.types.UILayout.template_node_view "bpy.types.UILayout.template_node_view")

  
---|---
  *[*]: Keyword-only parameters separator (PEP 3102)
  *[/]: Positional-only parameter separator (PEP 570)
