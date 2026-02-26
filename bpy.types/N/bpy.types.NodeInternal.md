# NodeInternal(Node)

base classes — [[bpy_struct]], [[Node]]

subclasses — [[CompositorNode]], [[FunctionNode]], [[GeometryNode]], [[NodeClosureInput]], [[NodeClosureOutput]], [[NodeCombineBundle]], [[NodeEnableOutput]], [[NodeEvaluateClosure]], [[NodeFrame]], [[NodeGroup]], [[NodeGroupInput]], [[NodeGroupOutput]], [[NodeJoinBundle]], [[NodeReroute]], [[NodeSeparateBundle]], [[ShaderNode]], [[TextureNode]]

_class _bpy.types.NodeInternal(_Node_)
    

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

draw_buttons(_context_ , _layout_)
    

Draw node buttons

Parameters:
    

**layout** ([[UILayout]], (never None)) – Layout, Layout in the UI

draw_buttons_ext(_context_ , _layout_)
    

Draw node buttons in the sidebar

Parameters:
    

**layout** ([[UILayout]], (never None)) – Layout, Layout in the UI

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
  * [[Node.type]]
  * [[Node.location]]
  * [[Node.location_absolute]]
  * [[Node.width]]
  * [[Node.height]]
  * [[Node.dimensions]]
  * [[Node.name]]
  * [[Node.label]]
  * [[Node.inputs]]
  * [[Node.outputs]]
  * [[Node.internal_links]]
  * [[Node.parent]]
  * [[Node.warning_propagation]]
  * [[Node.use_custom_color]]
  * [[Node.color]]
  * [[Node.color_tag]]

| 

  * [[Node.select]]
  * [[Node.show_options]]
  * [[Node.show_preview]]
  * [[Node.hide]]
  * [[Node.mute]]
  * [[Node.show_texture]]
  * [[Node.bl_idname]]
  * [[Node.bl_label]]
  * [[Node.bl_description]]
  * [[Node.bl_icon]]
  * [[Node.bl_static_type]]
  * [[Node.bl_width_default]]
  * [[Node.bl_width_min]]
  * [[Node.bl_width_max]]
  * [[Node.bl_height_default]]
  * [[Node.bl_height_min]]
  * [[Node.bl_height_max]]

  
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
  * [[bpy_struct.path_from_module]]
  * [[bpy_struct.path_resolve]]
  * [[bpy_struct.pop]]
  * [[bpy_struct.property_overridable_library_set]]
  * [[bpy_struct.property_unset]]

| 

  * [[bpy_struct.rna_ancestors]]
  * [[bpy_struct.type_recast]]
  * [[bpy_struct.values]]
  * [[Node.bl_system_properties_get]]
  * [[Node.socket_value_update]]
  * [[Node.is_registered_node_type]]
  * [[Node.poll]]
  * [[Node.poll_instance]]
  * [[Node.update]]
  * [[Node.insert_link]]
  * [[Node.init]]
  * [[Node.copy]]
  * [[Node.free]]
  * [[Node.draw_buttons]]
  * [[Node.draw_buttons_ext]]
  * [[Node.draw_label]]
  * [[Node.debug_zone_body_lazy_function_graph]]
  * [[Node.debug_zone_lazy_function_graph]]
  * [[Node.poll]]
  * [[Node.bl_rna_get_subclass]]
  * [[Node.bl_rna_get_subclass_py]]

  
---|---  
  
## References

  * [[GeometryNodeForeachGeometryElementInput.pair_with_output]]
  * [[GeometryNodeRepeatInput.pair_with_output]]

| 

  * [[GeometryNodeSimulationInput.pair_with_output]]
  * [[NodeClosureInput.pair_with_output]]

  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
