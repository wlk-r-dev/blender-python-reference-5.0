# NodeTree(ID)

## Poll Function

The `NodeTree.poll` function determines if a node tree is visible in the given context (similar to how [`Panel.poll`](../P/bpy.types.Panel.md#bpy.types.Panel.poll "bpy.types.Panel.poll") and [`Menu.poll`](../M/bpy.types.Menu.md#bpy.types.Menu.poll "bpy.types.Menu.poll") define visibility). If it returns False, the node tree type will not be selectable in the node editor.

A typical condition for shader nodes would be to check the active render engine of the scene and only show nodes of the renderer they are designed for.
    
    
    import bpy
    
    
    class CyclesNodeTree(bpy.types.NodeTree):
        """ This operator is only visible when Cycles is the selected render engine"""
        bl_label = "Cycles Node Tree"
        bl_icon = 'NONE'
    
        @classmethod
        def poll(cls, context):
            return context.scene.render.engine == 'CYCLES'
    
    
    bpy.utils.register_class(CyclesNodeTree)
    

base classes — [`bpy_struct`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct "bpy.types.bpy_struct"), [`ID`](../I/bpy.types.ID.md#bpy.types.ID "bpy.types.ID")

subclasses — [`CompositorNodeTree`](../C/bpy.types.CompositorNodeTree.md#bpy.types.CompositorNodeTree "bpy.types.CompositorNodeTree"), [`GeometryNodeTree`](../G/bpy.types.GeometryNodeTree.md#bpy.types.GeometryNodeTree "bpy.types.GeometryNodeTree"), [`ShaderNodeTree`](../S/bpy.types.ShaderNodeTree.md#bpy.types.ShaderNodeTree "bpy.types.ShaderNodeTree"), [`TextureNodeTree`](../T/bpy.types.TextureNodeTree.md#bpy.types.TextureNodeTree "bpy.types.TextureNodeTree")

_class _bpy.types.NodeTree(_ID_)
    

Node tree consisting of linked nodes used for shading, textures and compositing

animation_data
    

Animation data for this data-block

Type:
    

[`AnimData`](../A/bpy.types.AnimData.md#bpy.types.AnimData "bpy.types.AnimData"), (readonly)

annotation
    

Annotation data

Type:
    

[`Annotation`](../A/bpy.types.Annotation.md#bpy.types.Annotation "bpy.types.Annotation")

bl_description
    

Type:
    

string, default “”, (never None)

bl_icon
    

The node tree icon

Type:
    

enum in [Icon Items](../../bpy_types_enum_items/icon_items.md#rna-enum-icon-items), default `'NODETREE'`

bl_idname
    

Type:
    

string, default “”, (never None)

bl_label
    

The node tree label

Type:
    

string, default “”, (never None)

bl_use_group_interface
    

Determines the visibility of some UI elements related to node groups

Type:
    

boolean, default True

color_tag
    

Color tag of the node group which influences the header color

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
    

enum in [`'NONE'`, `'ATTRIBUTE'`, `'COLOR'`, `'CONVERTER'`, `'DISTORT'`, `'FILTER'`, `'GEOMETRY'`, `'INPUT'`, `'MATTE'`, `'OUTPUT'`, `'SCRIPT'`, `'SHADER'`, `'TEXTURE'`, `'VECTOR'`, `'PATTERN'`, `'INTERFACE'`, `'GROUP'`], default `'NONE'`

default_group_node_width
    

The width for newly created group nodes

Type:
    

int in [60, 700], default 140

description
    

Description of the node tree

Type:
    

string, default “”, (never None)

interface
    

Interface declaration for this node tree

Type:
    

[`NodeTreeInterface`](bpy.types.NodeTreeInterface.md#bpy.types.NodeTreeInterface "bpy.types.NodeTreeInterface"), (readonly)

links
    

Type:
    

[`NodeLinks`](bpy.types.NodeLinks.md#bpy.types.NodeLinks "bpy.types.NodeLinks") [`bpy_prop_collection`](../_other/bpy.types.bpy_prop_collection.md#bpy.types.bpy_prop_collection "bpy.types.bpy_prop_collection") of [`NodeLink`](bpy.types.NodeLink.md#bpy.types.NodeLink "bpy.types.NodeLink"), (readonly)

nodes
    

Type:
    

[`Nodes`](bpy.types.Nodes.md#bpy.types.Nodes "bpy.types.Nodes") [`bpy_prop_collection`](../_other/bpy.types.bpy_prop_collection.md#bpy.types.bpy_prop_collection "bpy.types.bpy_prop_collection") of [`Node`](bpy.types.Node.md#bpy.types.Node "bpy.types.Node"), (readonly)

type
    

Node Tree type (deprecated, bl_idname is the actual node tree type identifier)

  * `UNDEFINED` Undefined – Undefined type of nodes (can happen e.g. when a linked node tree goes missing).

  * `CUSTOM` Custom – Custom nodes.

  * `SHADER` Shader – Shader nodes.

  * `TEXTURE` Texture – Texture nodes.

  * `COMPOSITING` Compositing – Compositing nodes.

  * `GEOMETRY` Geometry – Geometry nodes.


Type:
    

enum in [`'UNDEFINED'`, `'CUSTOM'`, `'SHADER'`, `'TEXTURE'`, `'COMPOSITING'`, `'GEOMETRY'`], default `'SHADER'`, (readonly)

view_center
    

The current location (offset) of the view for this Node Tree

Type:
    

[`mathutils.Vector`](mathutils.md#mathutils.Vector "mathutils.Vector") of 2 items in [-inf, inf], default (0.0, 0.0), (readonly)

interface_update(_context_)
    

Updated node group interface

contains_tree(_sub_tree_)
    

Check if the node tree contains another. Used to avoid creating recursive node groups.

Parameters:
    

**sub_tree** (`NodeTree`, (never None)) – Node Tree, Node tree for recursive check

Returns:
    

contained

Return type:
    

boolean

_classmethod _poll(_context_)
    

Check visibility in the editor

Return type:
    

boolean

update()
    

Update on editor changes

_classmethod _get_from_context(_context_)
    

Get a node tree from the context

Returns:
    

`result_1`, Active node tree from context, `NodeTree`

`result_2`, ID data-block that owns the node tree, [`ID`](../I/bpy.types.ID.md#bpy.types.ID "bpy.types.ID")

`result_3`, Original ID data-block selected from the context, [`ID`](../I/bpy.types.ID.md#bpy.types.ID "bpy.types.ID")

Return type:
    

(`NodeTree`, [`ID`](../I/bpy.types.ID.md#bpy.types.ID "bpy.types.ID"), [`ID`](../I/bpy.types.ID.md#bpy.types.ID "bpy.types.ID"))

_classmethod _valid_socket_type(_idname_)
    

Check if the socket type is valid for the node tree

Parameters:
    

**idname** (_string_ _,__(__never None_ _)_) – Socket Type, Identifier of the socket type

Return type:
    

boolean

debug_lazy_function_graph()
    

Get the internal lazy-function graph for this node tree

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
    

[`bpy.types.Struct`](../S/bpy.types.Struct.md#bpy.types.Struct "bpy.types.Struct") subclass

_classmethod _bl_rna_get_subclass_py(_id_ , _default =None_, _/_)
    

Parameters:
    

**id** (_str_) – The RNA type identifier.

Returns:
    

The class or default when not found.

Return type:
    

type

### Inherited Properties

  * [`bpy_struct.id_data`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.id_data "bpy.types.bpy_struct.id_data")
  * [`ID.name`](../I/bpy.types.ID.md#bpy.types.ID.name "bpy.types.ID.name")
  * [`ID.name_full`](../I/bpy.types.ID.md#bpy.types.ID.name_full "bpy.types.ID.name_full")
  * [`ID.id_type`](../I/bpy.types.ID.md#bpy.types.ID.id_type "bpy.types.ID.id_type")
  * [`ID.session_uid`](../I/bpy.types.ID.md#bpy.types.ID.session_uid "bpy.types.ID.session_uid")
  * [`ID.is_evaluated`](../I/bpy.types.ID.md#bpy.types.ID.is_evaluated "bpy.types.ID.is_evaluated")
  * [`ID.original`](../I/bpy.types.ID.md#bpy.types.ID.original "bpy.types.ID.original")
  * [`ID.users`](../I/bpy.types.ID.md#bpy.types.ID.users "bpy.types.ID.users")
  * [`ID.use_fake_user`](../I/bpy.types.ID.md#bpy.types.ID.use_fake_user "bpy.types.ID.use_fake_user")
  * [`ID.use_extra_user`](../I/bpy.types.ID.md#bpy.types.ID.use_extra_user "bpy.types.ID.use_extra_user")
  * [`ID.is_embedded_data`](../I/bpy.types.ID.md#bpy.types.ID.is_embedded_data "bpy.types.ID.is_embedded_data")

| 

  * [`ID.is_linked_packed`](../I/bpy.types.ID.md#bpy.types.ID.is_linked_packed "bpy.types.ID.is_linked_packed")
  * [`ID.is_missing`](../I/bpy.types.ID.md#bpy.types.ID.is_missing "bpy.types.ID.is_missing")
  * [`ID.is_runtime_data`](../I/bpy.types.ID.md#bpy.types.ID.is_runtime_data "bpy.types.ID.is_runtime_data")
  * [`ID.is_editable`](../I/bpy.types.ID.md#bpy.types.ID.is_editable "bpy.types.ID.is_editable")
  * [`ID.tag`](../I/bpy.types.ID.md#bpy.types.ID.tag "bpy.types.ID.tag")
  * [`ID.is_library_indirect`](../I/bpy.types.ID.md#bpy.types.ID.is_library_indirect "bpy.types.ID.is_library_indirect")
  * [`ID.library`](../I/bpy.types.ID.md#bpy.types.ID.library "bpy.types.ID.library")
  * [`ID.library_weak_reference`](../I/bpy.types.ID.md#bpy.types.ID.library_weak_reference "bpy.types.ID.library_weak_reference")
  * [`ID.asset_data`](../I/bpy.types.ID.md#bpy.types.ID.asset_data "bpy.types.ID.asset_data")
  * [`ID.override_library`](../I/bpy.types.ID.md#bpy.types.ID.override_library "bpy.types.ID.override_library")
  * [`ID.preview`](../I/bpy.types.ID.md#bpy.types.ID.preview "bpy.types.ID.preview")

  
---|---  
  
### Inherited Functions

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
  * [`bpy_struct.path_from_module`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.path_from_module "bpy.types.bpy_struct.path_from_module")
  * [`bpy_struct.path_resolve`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.path_resolve "bpy.types.bpy_struct.path_resolve")
  * [`bpy_struct.pop`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.pop "bpy.types.bpy_struct.pop")
  * [`bpy_struct.property_overridable_library_set`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.property_overridable_library_set "bpy.types.bpy_struct.property_overridable_library_set")
  * [`bpy_struct.property_unset`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.property_unset "bpy.types.bpy_struct.property_unset")
  * [`bpy_struct.rna_ancestors`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.rna_ancestors "bpy.types.bpy_struct.rna_ancestors")

| 

  * [`bpy_struct.type_recast`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.type_recast "bpy.types.bpy_struct.type_recast")
  * [`bpy_struct.values`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.values "bpy.types.bpy_struct.values")
  * [`ID.bl_system_properties_get`](../I/bpy.types.ID.md#bpy.types.ID.bl_system_properties_get "bpy.types.ID.bl_system_properties_get")
  * [`ID.rename`](../I/bpy.types.ID.md#bpy.types.ID.rename "bpy.types.ID.rename")
  * [`ID.evaluated_get`](../I/bpy.types.ID.md#bpy.types.ID.evaluated_get "bpy.types.ID.evaluated_get")
  * [`ID.copy`](../I/bpy.types.ID.md#bpy.types.ID.copy "bpy.types.ID.copy")
  * [`ID.asset_mark`](../I/bpy.types.ID.md#bpy.types.ID.asset_mark "bpy.types.ID.asset_mark")
  * [`ID.asset_clear`](../I/bpy.types.ID.md#bpy.types.ID.asset_clear "bpy.types.ID.asset_clear")
  * [`ID.asset_generate_preview`](../I/bpy.types.ID.md#bpy.types.ID.asset_generate_preview "bpy.types.ID.asset_generate_preview")
  * [`ID.override_create`](../I/bpy.types.ID.md#bpy.types.ID.override_create "bpy.types.ID.override_create")
  * [`ID.override_hierarchy_create`](../I/bpy.types.ID.md#bpy.types.ID.override_hierarchy_create "bpy.types.ID.override_hierarchy_create")
  * [`ID.user_clear`](../I/bpy.types.ID.md#bpy.types.ID.user_clear "bpy.types.ID.user_clear")
  * [`ID.user_remap`](../I/bpy.types.ID.md#bpy.types.ID.user_remap "bpy.types.ID.user_remap")
  * [`ID.make_local`](../I/bpy.types.ID.md#bpy.types.ID.make_local "bpy.types.ID.make_local")
  * [`ID.user_of_id`](../I/bpy.types.ID.md#bpy.types.ID.user_of_id "bpy.types.ID.user_of_id")
  * [`ID.animation_data_create`](../I/bpy.types.ID.md#bpy.types.ID.animation_data_create "bpy.types.ID.animation_data_create")
  * [`ID.animation_data_clear`](../I/bpy.types.ID.md#bpy.types.ID.animation_data_clear "bpy.types.ID.animation_data_clear")
  * [`ID.update_tag`](../I/bpy.types.ID.md#bpy.types.ID.update_tag "bpy.types.ID.update_tag")
  * [`ID.preview_ensure`](../I/bpy.types.ID.md#bpy.types.ID.preview_ensure "bpy.types.ID.preview_ensure")
  * [`ID.bl_rna_get_subclass`](../I/bpy.types.ID.md#bpy.types.ID.bl_rna_get_subclass "bpy.types.ID.bl_rna_get_subclass")
  * [`ID.bl_rna_get_subclass_py`](../I/bpy.types.ID.md#bpy.types.ID.bl_rna_get_subclass_py "bpy.types.ID.bl_rna_get_subclass_py")

  
---|---  
  
### References

  * [`BlendData.node_groups`](../B/bpy.types.BlendData.md#bpy.types.BlendData.node_groups "bpy.types.BlendData.node_groups")
  * [`BlendDataNodeTrees.new`](../B/bpy.types.BlendDataNodeTrees.md#bpy.types.BlendDataNodeTrees.new "bpy.types.BlendDataNodeTrees.new")
  * [`BlendDataNodeTrees.remove`](../B/bpy.types.BlendDataNodeTrees.md#bpy.types.BlendDataNodeTrees.remove "bpy.types.BlendDataNodeTrees.remove")
  * [`CompositorNodeCustomGroup.node_tree`](../C/bpy.types.CompositorNodeCustomGroup.md#bpy.types.CompositorNodeCustomGroup.node_tree "bpy.types.CompositorNodeCustomGroup.node_tree")
  * [`CompositorNodeGroup.node_tree`](../C/bpy.types.CompositorNodeGroup.md#bpy.types.CompositorNodeGroup.node_tree "bpy.types.CompositorNodeGroup.node_tree")
  * [`EvaluateClosureNodeViewerPathElem.source_node_tree`](../E/bpy.types.EvaluateClosureNodeViewerPathElem.md#bpy.types.EvaluateClosureNodeViewerPathElem.source_node_tree "bpy.types.EvaluateClosureNodeViewerPathElem.source_node_tree")
  * [`FreestyleLineStyle.node_tree`](../F/bpy.types.FreestyleLineStyle.md#bpy.types.FreestyleLineStyle.node_tree "bpy.types.FreestyleLineStyle.node_tree")
  * [`GeometryNodeCustomGroup.node_tree`](../G/bpy.types.GeometryNodeCustomGroup.md#bpy.types.GeometryNodeCustomGroup.node_tree "bpy.types.GeometryNodeCustomGroup.node_tree")
  * [`GeometryNodeGroup.node_tree`](../G/bpy.types.GeometryNodeGroup.md#bpy.types.GeometryNodeGroup.node_tree "bpy.types.GeometryNodeGroup.node_tree")
  * [`Light.node_tree`](../L/bpy.types.Light.md#bpy.types.Light.node_tree "bpy.types.Light.node_tree")
  * [`Material.node_tree`](../M/bpy.types.Material.md#bpy.types.Material.node_tree "bpy.types.Material.node_tree")
  * [`Node.poll`](bpy.types.Node.md#bpy.types.Node.poll "bpy.types.Node.poll")
  * [`Node.poll_instance`](bpy.types.Node.md#bpy.types.Node.poll_instance "bpy.types.Node.poll_instance")
  * [`NodeCustomGroup.node_tree`](bpy.types.NodeCustomGroup.md#bpy.types.NodeCustomGroup.node_tree "bpy.types.NodeCustomGroup.node_tree")
  * [`NodeGroup.node_tree`](bpy.types.NodeGroup.md#bpy.types.NodeGroup.node_tree "bpy.types.NodeGroup.node_tree")
  * [`NodeInternal.poll`](bpy.types.NodeInternal.md#bpy.types.NodeInternal.poll "bpy.types.NodeInternal.poll")
  * [`NodeInternal.poll_instance`](bpy.types.NodeInternal.md#bpy.types.NodeInternal.poll_instance "bpy.types.NodeInternal.poll_instance")
  * `NodeTree.contains_tree`

| 

  * `NodeTree.get_from_context`
  * [`NodeTreePath.node_tree`](bpy.types.NodeTreePath.md#bpy.types.NodeTreePath.node_tree "bpy.types.NodeTreePath.node_tree")
  * [`NodesModifier.node_group`](bpy.types.NodesModifier.md#bpy.types.NodesModifier.node_group "bpy.types.NodesModifier.node_group")
  * [`Scene.compositing_node_group`](../S/bpy.types.Scene.md#bpy.types.Scene.compositing_node_group "bpy.types.Scene.compositing_node_group")
  * [`SequencerCompositorModifierData.node_group`](../S/bpy.types.SequencerCompositorModifierData.md#bpy.types.SequencerCompositorModifierData.node_group "bpy.types.SequencerCompositorModifierData.node_group")
  * [`ShaderNodeCustomGroup.node_tree`](../S/bpy.types.ShaderNodeCustomGroup.md#bpy.types.ShaderNodeCustomGroup.node_tree "bpy.types.ShaderNodeCustomGroup.node_tree")
  * [`ShaderNodeGroup.node_tree`](../S/bpy.types.ShaderNodeGroup.md#bpy.types.ShaderNodeGroup.node_tree "bpy.types.ShaderNodeGroup.node_tree")
  * [`SpaceNodeEditor.edit_tree`](../S/bpy.types.SpaceNodeEditor.md#bpy.types.SpaceNodeEditor.edit_tree "bpy.types.SpaceNodeEditor.edit_tree")
  * [`SpaceNodeEditor.node_tree`](../S/bpy.types.SpaceNodeEditor.md#bpy.types.SpaceNodeEditor.node_tree "bpy.types.SpaceNodeEditor.node_tree")
  * [`SpaceNodeEditor.selected_node_group`](../S/bpy.types.SpaceNodeEditor.md#bpy.types.SpaceNodeEditor.selected_node_group "bpy.types.SpaceNodeEditor.selected_node_group")
  * [`SpaceNodeEditorPath.append`](../S/bpy.types.SpaceNodeEditorPath.md#bpy.types.SpaceNodeEditorPath.append "bpy.types.SpaceNodeEditorPath.append")
  * [`SpaceNodeEditorPath.start`](../S/bpy.types.SpaceNodeEditorPath.md#bpy.types.SpaceNodeEditorPath.start "bpy.types.SpaceNodeEditorPath.start")
  * [`Texture.node_tree`](../T/bpy.types.Texture.md#bpy.types.Texture.node_tree "bpy.types.Texture.node_tree")
  * [`TextureNodeGroup.node_tree`](../T/bpy.types.TextureNodeGroup.md#bpy.types.TextureNodeGroup.node_tree "bpy.types.TextureNodeGroup.node_tree")
  * [`UILayout.template_node_link`](../U/bpy.types.UILayout.md#bpy.types.UILayout.template_node_link "bpy.types.UILayout.template_node_link")
  * [`UILayout.template_node_view`](../U/bpy.types.UILayout.md#bpy.types.UILayout.template_node_view "bpy.types.UILayout.template_node_view")
  * [`World.node_tree`](../W/bpy.types.World.md#bpy.types.World.node_tree "bpy.types.World.node_tree")

  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
