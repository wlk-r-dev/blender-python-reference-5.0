# Node(bpy_struct)

base class — [[bpy_struct]]

subclasses — [[NodeCustomGroup]], [[NodeInternal]]

_class _bpy.types.Node(_bpy_struct_)
    

Node in a node tree

bl_description
    

Type:
    

string, default “”, (never None)

bl_height_default
    

Type:
    

float in [0, inf], default 0.0

bl_height_max
    

Type:
    

float in [0, inf], default 0.0

bl_height_min
    

Type:
    

float in [0, inf], default 0.0

bl_icon
    

The node icon

Type:
    

enum in [Icon Items](../../bpy_types_enum_items/icon_items.md#rna-enum-icon-items), default `'NODE'`

bl_idname
    

Type:
    

string, default “”, (never None)

bl_label
    

The node label

Type:
    

string, default “”, (never None)

bl_static_type
    

Legacy unique node type identifier, redundant with bl_idname property

Type:
    

string, default “”, (readonly, never None)

bl_width_default
    

Type:
    

float in [0, inf], default 0.0

bl_width_max
    

Type:
    

float in [0, inf], default 0.0

bl_width_min
    

Type:
    

float in [0, inf], default 0.0

color
    

Custom color of the node body

Type:
    

[[mathutils.Color]] of 3 items in [0, 1], default (0.0, 0.0, 0.0)

color_tag
    

Node header color tag

  * `NONE` None – Default color tag for new nodes and node groups.

  * `ATTRIBUTE` Attribute.

  * `COLOR` Color.

  * `CONVERTER` Converter.

  * `DISTORT` Distort.

  * `FILTER` Filter.

  * `GEOMETRY` Geometry.

  * `INPUT` Input.

  * `MATTE` Matte.

  * `OUTPUT` Output.

  * `SCRIPT` Script.

  * `SHADER` Shader.

  * `TEXTURE` Texture.

  * `VECTOR` Vector.

  * `PATTERN` Pattern.

  * `INTERFACE` Interface.

  * `GROUP` Group.


Type:
    

enum in [`'NONE'`, `'ATTRIBUTE'`, `'COLOR'`, `'CONVERTER'`, `'DISTORT'`, `'FILTER'`, `'GEOMETRY'`, `'INPUT'`, `'MATTE'`, `'OUTPUT'`, `'SCRIPT'`, `'SHADER'`, `'TEXTURE'`, `'VECTOR'`, `'PATTERN'`, `'INTERFACE'`, `'GROUP'`], default `'NONE'`, (readonly)

dimensions
    

Absolute bounding box dimensions of the node

Type:
    

[[mathutils.Vector]] of 2 items in [-inf, inf], default (0.0, 0.0), (readonly)

height
    

Height of the node

Type:
    

float in [-inf, inf], default 0.0

hide
    

Type:
    

boolean, default False

inputs
    

Type:
    

[[NodeInputs]] [[bpy_prop_collection]] of [[NodeSocket]], (readonly)

internal_links
    

Internal input-to-output connections for muting

Type:
    

[[bpy_prop_collection]] of [[NodeLink]], (readonly)

label
    

Optional custom node label

Type:
    

string, default “”, (never None)

location
    

Location of the node within its parent frame

Type:
    

[[mathutils.Vector]] of 2 items in [-1e+06, 1e+06], default (0.0, 0.0)

location_absolute
    

Location of the node in the entire canvas

Type:
    

[[mathutils.Vector]] of 2 items in [-1e+06, 1e+06], default (0.0, 0.0)

mute
    

Type:
    

boolean, default False

name
    

Unique node identifier

Type:
    

string, default “”, (never None)

outputs
    

Type:
    

[[NodeOutputs]] [[bpy_prop_collection]] of [[NodeSocket]], (readonly)

parent
    

Parent this node is attached to

Type:
    

`Node`

select
    

Node selection state

Type:
    

boolean, default False

show_options
    

Type:
    

boolean, default False

show_preview
    

Type:
    

boolean, default False

show_texture
    

Display node in viewport textured shading mode

Type:
    

boolean, default False

type
    

Legacy unique node type identifier, redundant with bl_idname property

Type:
    

string, default “”, (readonly, never None)

use_custom_color
    

Use custom color for the node

Type:
    

boolean, default False

warning_propagation
    

The kinds of messages that should be propagated from this node to the parent group node

Type:
    

enum in [`'ALL'`, `'NONE'`, `'ERRORS'`, `'ERRORS_AND_WARNINGS'`], default `'ALL'`

width
    

Width of the node

Type:
    

float in [-inf, inf], default 0.0

bl_system_properties_get(_*_ , _do_create =False_)
    

DEBUG ONLY. Internal access to runtime-defined RNA data storage, intended solely for testing and debugging purposes. Do not access it in regular scripting work, and in particular, do not assume that it contains writable data

Parameters:
    

**do_create** (_boolean_ _,__(__optional_ _)_) – Ensure that system properties are created if they do not exist yet

Returns:
    

The system properties root container, or None if there are no system properties stored in this data yet, and its creation was not requested

Return type:
    

[[PropertyGroup]]

socket_value_update(_context_)
    

Update after property changes

_classmethod _is_registered_node_type()
    

True if a registered node type

Returns:
    

Result

Return type:
    

boolean

_classmethod _poll(_node_tree_)
    

If non-null output is returned, the node type can be added to the tree

Parameters:
    

**node_tree** ([[NodeTree]]) – Node Tree

Return type:
    

boolean

poll_instance(_node_tree_)
    

If non-null output is returned, the node can be added to the tree

Parameters:
    

**node_tree** ([[NodeTree]]) – Node Tree

Return type:
    

boolean

update()
    

Update on node graph topology changes (adding or removing nodes and links)

insert_link(_link_)
    

Handle creation of a link to or from the node

Parameters:
    

**link** ([[NodeLink]], (never None)) – Link, Node link that will be inserted

init(_context_)
    

Initialize a new instance of this node

copy(_node_)
    

Initialize a new instance of this node from an existing node

Parameters:
    

**node** (`Node`, (never None)) – Node, Existing node to copy

free()
    

Clean up node on removal

draw_buttons(_context_ , _layout_)
    

Draw node buttons

Parameters:
    

**layout** ([[UILayout]], (never None)) – Layout, Layout in the UI

draw_buttons_ext(_context_ , _layout_)
    

Draw node buttons in the sidebar

Parameters:
    

**layout** ([[UILayout]], (never None)) – Layout, Layout in the UI

draw_label()
    

Returns a dynamic label string

Returns:
    

Label

Return type:
    

string, (never None)

debug_zone_body_lazy_function_graph()
    

Get the internal lazy-function graph for the body of this zone

Returns:
    

Dot Graph, Graph in dot format

Return type:
    

string

debug_zone_lazy_function_graph()
    

Get the internal lazy-function graph for this zone

Returns:
    

Dot Graph, Graph in dot format

Return type:
    

string

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

  * [[bpy.context.active_node]]
  * [[bpy.context.selected_nodes]]
  * [[bpy.context.texture_node]]
  * [[GeometryNodeForeachGeometryElementInput.paired_output]]
  * [[GeometryNodeMenuSwitch.enum_definition]]
  * [[GeometryNodeRepeatInput.paired_output]]
  * [[GeometryNodeSimulationInput.paired_output]]
  * `Node.copy`
  * `Node.parent`
  * [[NodeClosureInput.paired_output]]
  * [[NodeLink.from_node]]
  * [[NodeLink.to_node]]
  * [[NodeSocket.draw]]
  * [[NodeSocket.draw_color]]
  * [[NodeSocket.node]]
  * [[NodeSocketStandard.draw]]
  * [[NodeSocketStandard.draw_color]]
  * [[NodeTree.nodes]]
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
  * [[Nodes.active]]
  * [[Nodes.new]]
  * [[Nodes.remove]]
  * [[NodesModifierBake.node]]
  * [[RenderEngine.update_script_node]]
  * [[SpaceNodeEditorPath.append]]
  * [[UILayout.template_node_inputs]]
  * [[UILayout.template_node_link]]
  * [[UILayout.template_node_view]]

  
---|---
  *[*]: Keyword-only parameters separator (PEP 3102)
  *[/]: Positional-only parameter separator (PEP 570)
