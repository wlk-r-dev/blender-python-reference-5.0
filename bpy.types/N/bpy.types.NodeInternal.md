# NodeInternal(Node)

base classes — [`bpy_struct`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct "bpy.types.bpy_struct"), [`Node`](bpy.types.Node.md#bpy.types.Node "bpy.types.Node")

subclasses — [`CompositorNode`](../C/bpy.types.CompositorNode.md#bpy.types.CompositorNode "bpy.types.CompositorNode"), [`FunctionNode`](../F/bpy.types.FunctionNode.md#bpy.types.FunctionNode "bpy.types.FunctionNode"), [`GeometryNode`](../G/bpy.types.GeometryNode.md#bpy.types.GeometryNode "bpy.types.GeometryNode"), [`NodeClosureInput`](bpy.types.NodeClosureInput.md#bpy.types.NodeClosureInput "bpy.types.NodeClosureInput"), [`NodeClosureOutput`](bpy.types.NodeClosureOutput.md#bpy.types.NodeClosureOutput "bpy.types.NodeClosureOutput"), [`NodeCombineBundle`](bpy.types.NodeCombineBundle.md#bpy.types.NodeCombineBundle "bpy.types.NodeCombineBundle"), [`NodeEnableOutput`](bpy.types.NodeEnableOutput.md#bpy.types.NodeEnableOutput "bpy.types.NodeEnableOutput"), [`NodeEvaluateClosure`](bpy.types.NodeEvaluateClosure.md#bpy.types.NodeEvaluateClosure "bpy.types.NodeEvaluateClosure"), [`NodeFrame`](bpy.types.NodeFrame.md#bpy.types.NodeFrame "bpy.types.NodeFrame"), [`NodeGroup`](bpy.types.NodeGroup.md#bpy.types.NodeGroup "bpy.types.NodeGroup"), [`NodeGroupInput`](bpy.types.NodeGroupInput.md#bpy.types.NodeGroupInput "bpy.types.NodeGroupInput"), [`NodeGroupOutput`](bpy.types.NodeGroupOutput.md#bpy.types.NodeGroupOutput "bpy.types.NodeGroupOutput"), [`NodeJoinBundle`](bpy.types.NodeJoinBundle.md#bpy.types.NodeJoinBundle "bpy.types.NodeJoinBundle"), [`NodeReroute`](bpy.types.NodeReroute.md#bpy.types.NodeReroute "bpy.types.NodeReroute"), [`NodeSeparateBundle`](bpy.types.NodeSeparateBundle.md#bpy.types.NodeSeparateBundle "bpy.types.NodeSeparateBundle"), [`ShaderNode`](../S/bpy.types.ShaderNode.md#bpy.types.ShaderNode "bpy.types.ShaderNode"), [`TextureNode`](../T/bpy.types.TextureNode.md#bpy.types.TextureNode "bpy.types.TextureNode")

_class _bpy.types.NodeInternal(_Node_)
    

_classmethod _poll(_node_tree_)
    

If non-null output is returned, the node type can be added to the tree

Parameters:
    

**node_tree** ([`NodeTree`](bpy.types.NodeTree.md#bpy.types.NodeTree "bpy.types.NodeTree")) – Node Tree

Return type:
    

boolean

poll_instance(_node_tree_)
    

If non-null output is returned, the node can be added to the tree

Parameters:
    

**node_tree** ([`NodeTree`](bpy.types.NodeTree.md#bpy.types.NodeTree "bpy.types.NodeTree")) – Node Tree

Return type:
    

boolean

update()
    

Update on node graph topology changes (adding or removing nodes and links)

draw_buttons(_context_ , _layout_)
    

Draw node buttons

Parameters:
    

**layout** ([`UILayout`](../U/bpy.types.UILayout.md#bpy.types.UILayout "bpy.types.UILayout"), (never None)) – Layout, Layout in the UI

draw_buttons_ext(_context_ , _layout_)
    

Draw node buttons in the sidebar

Parameters:
    

**layout** ([`UILayout`](../U/bpy.types.UILayout.md#bpy.types.UILayout "bpy.types.UILayout"), (never None)) – Layout, Layout in the UI

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
  * [`Node.type`](bpy.types.Node.md#bpy.types.Node.type "bpy.types.Node.type")
  * [`Node.location`](bpy.types.Node.md#bpy.types.Node.location "bpy.types.Node.location")
  * [`Node.location_absolute`](bpy.types.Node.md#bpy.types.Node.location_absolute "bpy.types.Node.location_absolute")
  * [`Node.width`](bpy.types.Node.md#bpy.types.Node.width "bpy.types.Node.width")
  * [`Node.height`](bpy.types.Node.md#bpy.types.Node.height "bpy.types.Node.height")
  * [`Node.dimensions`](bpy.types.Node.md#bpy.types.Node.dimensions "bpy.types.Node.dimensions")
  * [`Node.name`](bpy.types.Node.md#bpy.types.Node.name "bpy.types.Node.name")
  * [`Node.label`](bpy.types.Node.md#bpy.types.Node.label "bpy.types.Node.label")
  * [`Node.inputs`](bpy.types.Node.md#bpy.types.Node.inputs "bpy.types.Node.inputs")
  * [`Node.outputs`](bpy.types.Node.md#bpy.types.Node.outputs "bpy.types.Node.outputs")
  * [`Node.internal_links`](bpy.types.Node.md#bpy.types.Node.internal_links "bpy.types.Node.internal_links")
  * [`Node.parent`](bpy.types.Node.md#bpy.types.Node.parent "bpy.types.Node.parent")
  * [`Node.warning_propagation`](bpy.types.Node.md#bpy.types.Node.warning_propagation "bpy.types.Node.warning_propagation")
  * [`Node.use_custom_color`](bpy.types.Node.md#bpy.types.Node.use_custom_color "bpy.types.Node.use_custom_color")
  * [`Node.color`](bpy.types.Node.md#bpy.types.Node.color "bpy.types.Node.color")
  * [`Node.color_tag`](bpy.types.Node.md#bpy.types.Node.color_tag "bpy.types.Node.color_tag")

| 

  * [`Node.select`](bpy.types.Node.md#bpy.types.Node.select "bpy.types.Node.select")
  * [`Node.show_options`](bpy.types.Node.md#bpy.types.Node.show_options "bpy.types.Node.show_options")
  * [`Node.show_preview`](bpy.types.Node.md#bpy.types.Node.show_preview "bpy.types.Node.show_preview")
  * [`Node.hide`](bpy.types.Node.md#bpy.types.Node.hide "bpy.types.Node.hide")
  * [`Node.mute`](bpy.types.Node.md#bpy.types.Node.mute "bpy.types.Node.mute")
  * [`Node.show_texture`](bpy.types.Node.md#bpy.types.Node.show_texture "bpy.types.Node.show_texture")
  * [`Node.bl_idname`](bpy.types.Node.md#bpy.types.Node.bl_idname "bpy.types.Node.bl_idname")
  * [`Node.bl_label`](bpy.types.Node.md#bpy.types.Node.bl_label "bpy.types.Node.bl_label")
  * [`Node.bl_description`](bpy.types.Node.md#bpy.types.Node.bl_description "bpy.types.Node.bl_description")
  * [`Node.bl_icon`](bpy.types.Node.md#bpy.types.Node.bl_icon "bpy.types.Node.bl_icon")
  * [`Node.bl_static_type`](bpy.types.Node.md#bpy.types.Node.bl_static_type "bpy.types.Node.bl_static_type")
  * [`Node.bl_width_default`](bpy.types.Node.md#bpy.types.Node.bl_width_default "bpy.types.Node.bl_width_default")
  * [`Node.bl_width_min`](bpy.types.Node.md#bpy.types.Node.bl_width_min "bpy.types.Node.bl_width_min")
  * [`Node.bl_width_max`](bpy.types.Node.md#bpy.types.Node.bl_width_max "bpy.types.Node.bl_width_max")
  * [`Node.bl_height_default`](bpy.types.Node.md#bpy.types.Node.bl_height_default "bpy.types.Node.bl_height_default")
  * [`Node.bl_height_min`](bpy.types.Node.md#bpy.types.Node.bl_height_min "bpy.types.Node.bl_height_min")
  * [`Node.bl_height_max`](bpy.types.Node.md#bpy.types.Node.bl_height_max "bpy.types.Node.bl_height_max")

  
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
  * [`bpy_struct.path_from_module`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.path_from_module "bpy.types.bpy_struct.path_from_module")
  * [`bpy_struct.path_resolve`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.path_resolve "bpy.types.bpy_struct.path_resolve")
  * [`bpy_struct.pop`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.pop "bpy.types.bpy_struct.pop")
  * [`bpy_struct.property_overridable_library_set`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.property_overridable_library_set "bpy.types.bpy_struct.property_overridable_library_set")
  * [`bpy_struct.property_unset`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.property_unset "bpy.types.bpy_struct.property_unset")

| 

  * [`bpy_struct.rna_ancestors`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.rna_ancestors "bpy.types.bpy_struct.rna_ancestors")
  * [`bpy_struct.type_recast`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.type_recast "bpy.types.bpy_struct.type_recast")
  * [`bpy_struct.values`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.values "bpy.types.bpy_struct.values")
  * [`Node.bl_system_properties_get`](bpy.types.Node.md#bpy.types.Node.bl_system_properties_get "bpy.types.Node.bl_system_properties_get")
  * [`Node.socket_value_update`](bpy.types.Node.md#bpy.types.Node.socket_value_update "bpy.types.Node.socket_value_update")
  * [`Node.is_registered_node_type`](bpy.types.Node.md#bpy.types.Node.is_registered_node_type "bpy.types.Node.is_registered_node_type")
  * [`Node.poll`](bpy.types.Node.md#bpy.types.Node.poll "bpy.types.Node.poll")
  * [`Node.poll_instance`](bpy.types.Node.md#bpy.types.Node.poll_instance "bpy.types.Node.poll_instance")
  * [`Node.update`](bpy.types.Node.md#bpy.types.Node.update "bpy.types.Node.update")
  * [`Node.insert_link`](bpy.types.Node.md#bpy.types.Node.insert_link "bpy.types.Node.insert_link")
  * [`Node.init`](bpy.types.Node.md#bpy.types.Node.init "bpy.types.Node.init")
  * [`Node.copy`](bpy.types.Node.md#bpy.types.Node.copy "bpy.types.Node.copy")
  * [`Node.free`](bpy.types.Node.md#bpy.types.Node.free "bpy.types.Node.free")
  * [`Node.draw_buttons`](bpy.types.Node.md#bpy.types.Node.draw_buttons "bpy.types.Node.draw_buttons")
  * [`Node.draw_buttons_ext`](bpy.types.Node.md#bpy.types.Node.draw_buttons_ext "bpy.types.Node.draw_buttons_ext")
  * [`Node.draw_label`](bpy.types.Node.md#bpy.types.Node.draw_label "bpy.types.Node.draw_label")
  * [`Node.debug_zone_body_lazy_function_graph`](bpy.types.Node.md#bpy.types.Node.debug_zone_body_lazy_function_graph "bpy.types.Node.debug_zone_body_lazy_function_graph")
  * [`Node.debug_zone_lazy_function_graph`](bpy.types.Node.md#bpy.types.Node.debug_zone_lazy_function_graph "bpy.types.Node.debug_zone_lazy_function_graph")
  * [`Node.poll`](bpy.types.Node.md#bpy.types.Node.poll "bpy.types.Node.poll")
  * [`Node.bl_rna_get_subclass`](bpy.types.Node.md#bpy.types.Node.bl_rna_get_subclass "bpy.types.Node.bl_rna_get_subclass")
  * [`Node.bl_rna_get_subclass_py`](bpy.types.Node.md#bpy.types.Node.bl_rna_get_subclass_py "bpy.types.Node.bl_rna_get_subclass_py")

  
---|---  
  
## References

  * [`GeometryNodeForeachGeometryElementInput.pair_with_output`](../G/bpy.types.GeometryNodeForeachGeometryElementInput.md#bpy.types.GeometryNodeForeachGeometryElementInput.pair_with_output "bpy.types.GeometryNodeForeachGeometryElementInput.pair_with_output")
  * [`GeometryNodeRepeatInput.pair_with_output`](../G/bpy.types.GeometryNodeRepeatInput.md#bpy.types.GeometryNodeRepeatInput.pair_with_output "bpy.types.GeometryNodeRepeatInput.pair_with_output")

| 

  * [`GeometryNodeSimulationInput.pair_with_output`](../G/bpy.types.GeometryNodeSimulationInput.md#bpy.types.GeometryNodeSimulationInput.pair_with_output "bpy.types.GeometryNodeSimulationInput.pair_with_output")
  * [`NodeClosureInput.pair_with_output`](bpy.types.NodeClosureInput.md#bpy.types.NodeClosureInput.pair_with_output "bpy.types.NodeClosureInput.pair_with_output")

  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
