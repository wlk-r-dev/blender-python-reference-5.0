# GeometryNodeSetID(GeometryNode)

base classes — [`bpy_struct`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct "bpy.types.bpy_struct"), [`Node`](../N/bpy.types.Node.md#bpy.types.Node "bpy.types.Node"), [`NodeInternal`](../N/bpy.types.NodeInternal.md#bpy.types.NodeInternal "bpy.types.NodeInternal"), [`GeometryNode`](bpy.types.GeometryNode.md#bpy.types.GeometryNode "bpy.types.GeometryNode")

_class _bpy.types.GeometryNodeSetID(_GeometryNode_)
    

Set the id attribute on the input geometry, mainly used internally for randomizing

_classmethod _is_registered_node_type()
    

True if a registered node type

Returns:
    

Result

Return type:
    

boolean

_classmethod _input_template(_index_)
    

Input socket template

Parameters:
    

**index** (_int in_ _[__0_ _,__inf_ _]_) – Index

Returns:
    

result

Return type:
    

[`NodeInternalSocketTemplate`](../N/bpy.types.NodeInternalSocketTemplate.md#bpy.types.NodeInternalSocketTemplate "bpy.types.NodeInternalSocketTemplate")

_classmethod _output_template(_index_)
    

Output socket template

Parameters:
    

**index** (_int in_ _[__0_ _,__inf_ _]_) – Index

Returns:
    

result

Return type:
    

[`NodeInternalSocketTemplate`](../N/bpy.types.NodeInternalSocketTemplate.md#bpy.types.NodeInternalSocketTemplate "bpy.types.NodeInternalSocketTemplate")

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
  * [`Node.type`](../N/bpy.types.Node.md#bpy.types.Node.type "bpy.types.Node.type")
  * [`Node.location`](../N/bpy.types.Node.md#bpy.types.Node.location "bpy.types.Node.location")
  * [`Node.location_absolute`](../N/bpy.types.Node.md#bpy.types.Node.location_absolute "bpy.types.Node.location_absolute")
  * [`Node.width`](../N/bpy.types.Node.md#bpy.types.Node.width "bpy.types.Node.width")
  * [`Node.height`](../N/bpy.types.Node.md#bpy.types.Node.height "bpy.types.Node.height")
  * [`Node.dimensions`](../N/bpy.types.Node.md#bpy.types.Node.dimensions "bpy.types.Node.dimensions")
  * [`Node.name`](../N/bpy.types.Node.md#bpy.types.Node.name "bpy.types.Node.name")
  * [`Node.label`](../N/bpy.types.Node.md#bpy.types.Node.label "bpy.types.Node.label")
  * [`Node.inputs`](../N/bpy.types.Node.md#bpy.types.Node.inputs "bpy.types.Node.inputs")
  * [`Node.outputs`](../N/bpy.types.Node.md#bpy.types.Node.outputs "bpy.types.Node.outputs")
  * [`Node.internal_links`](../N/bpy.types.Node.md#bpy.types.Node.internal_links "bpy.types.Node.internal_links")
  * [`Node.parent`](../N/bpy.types.Node.md#bpy.types.Node.parent "bpy.types.Node.parent")
  * [`Node.warning_propagation`](../N/bpy.types.Node.md#bpy.types.Node.warning_propagation "bpy.types.Node.warning_propagation")
  * [`Node.use_custom_color`](../N/bpy.types.Node.md#bpy.types.Node.use_custom_color "bpy.types.Node.use_custom_color")
  * [`Node.color`](../N/bpy.types.Node.md#bpy.types.Node.color "bpy.types.Node.color")
  * [`Node.color_tag`](../N/bpy.types.Node.md#bpy.types.Node.color_tag "bpy.types.Node.color_tag")

| 

  * [`Node.select`](../N/bpy.types.Node.md#bpy.types.Node.select "bpy.types.Node.select")
  * [`Node.show_options`](../N/bpy.types.Node.md#bpy.types.Node.show_options "bpy.types.Node.show_options")
  * [`Node.show_preview`](../N/bpy.types.Node.md#bpy.types.Node.show_preview "bpy.types.Node.show_preview")
  * [`Node.hide`](../N/bpy.types.Node.md#bpy.types.Node.hide "bpy.types.Node.hide")
  * [`Node.mute`](../N/bpy.types.Node.md#bpy.types.Node.mute "bpy.types.Node.mute")
  * [`Node.show_texture`](../N/bpy.types.Node.md#bpy.types.Node.show_texture "bpy.types.Node.show_texture")
  * [`Node.bl_idname`](../N/bpy.types.Node.md#bpy.types.Node.bl_idname "bpy.types.Node.bl_idname")
  * [`Node.bl_label`](../N/bpy.types.Node.md#bpy.types.Node.bl_label "bpy.types.Node.bl_label")
  * [`Node.bl_description`](../N/bpy.types.Node.md#bpy.types.Node.bl_description "bpy.types.Node.bl_description")
  * [`Node.bl_icon`](../N/bpy.types.Node.md#bpy.types.Node.bl_icon "bpy.types.Node.bl_icon")
  * [`Node.bl_static_type`](../N/bpy.types.Node.md#bpy.types.Node.bl_static_type "bpy.types.Node.bl_static_type")
  * [`Node.bl_width_default`](../N/bpy.types.Node.md#bpy.types.Node.bl_width_default "bpy.types.Node.bl_width_default")
  * [`Node.bl_width_min`](../N/bpy.types.Node.md#bpy.types.Node.bl_width_min "bpy.types.Node.bl_width_min")
  * [`Node.bl_width_max`](../N/bpy.types.Node.md#bpy.types.Node.bl_width_max "bpy.types.Node.bl_width_max")
  * [`Node.bl_height_default`](../N/bpy.types.Node.md#bpy.types.Node.bl_height_default "bpy.types.Node.bl_height_default")
  * [`Node.bl_height_min`](../N/bpy.types.Node.md#bpy.types.Node.bl_height_min "bpy.types.Node.bl_height_min")
  * [`Node.bl_height_max`](../N/bpy.types.Node.md#bpy.types.Node.bl_height_max "bpy.types.Node.bl_height_max")

  
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
  * [`bpy_struct.rna_ancestors`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.rna_ancestors "bpy.types.bpy_struct.rna_ancestors")
  * [`bpy_struct.type_recast`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.type_recast "bpy.types.bpy_struct.type_recast")
  * [`bpy_struct.values`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.values "bpy.types.bpy_struct.values")
  * [`Node.bl_system_properties_get`](../N/bpy.types.Node.md#bpy.types.Node.bl_system_properties_get "bpy.types.Node.bl_system_properties_get")
  * [`Node.socket_value_update`](../N/bpy.types.Node.md#bpy.types.Node.socket_value_update "bpy.types.Node.socket_value_update")

| 

  * [`Node.is_registered_node_type`](../N/bpy.types.Node.md#bpy.types.Node.is_registered_node_type "bpy.types.Node.is_registered_node_type")
  * [`Node.poll`](../N/bpy.types.Node.md#bpy.types.Node.poll "bpy.types.Node.poll")
  * [`Node.poll_instance`](../N/bpy.types.Node.md#bpy.types.Node.poll_instance "bpy.types.Node.poll_instance")
  * [`Node.update`](../N/bpy.types.Node.md#bpy.types.Node.update "bpy.types.Node.update")
  * [`Node.insert_link`](../N/bpy.types.Node.md#bpy.types.Node.insert_link "bpy.types.Node.insert_link")
  * [`Node.init`](../N/bpy.types.Node.md#bpy.types.Node.init "bpy.types.Node.init")
  * [`Node.copy`](../N/bpy.types.Node.md#bpy.types.Node.copy "bpy.types.Node.copy")
  * [`Node.free`](../N/bpy.types.Node.md#bpy.types.Node.free "bpy.types.Node.free")
  * [`Node.draw_buttons`](../N/bpy.types.Node.md#bpy.types.Node.draw_buttons "bpy.types.Node.draw_buttons")
  * [`Node.draw_buttons_ext`](../N/bpy.types.Node.md#bpy.types.Node.draw_buttons_ext "bpy.types.Node.draw_buttons_ext")
  * [`Node.draw_label`](../N/bpy.types.Node.md#bpy.types.Node.draw_label "bpy.types.Node.draw_label")
  * [`Node.debug_zone_body_lazy_function_graph`](../N/bpy.types.Node.md#bpy.types.Node.debug_zone_body_lazy_function_graph "bpy.types.Node.debug_zone_body_lazy_function_graph")
  * [`Node.debug_zone_lazy_function_graph`](../N/bpy.types.Node.md#bpy.types.Node.debug_zone_lazy_function_graph "bpy.types.Node.debug_zone_lazy_function_graph")
  * [`Node.poll`](../N/bpy.types.Node.md#bpy.types.Node.poll "bpy.types.Node.poll")
  * [`Node.bl_rna_get_subclass`](../N/bpy.types.Node.md#bpy.types.Node.bl_rna_get_subclass "bpy.types.Node.bl_rna_get_subclass")
  * [`Node.bl_rna_get_subclass_py`](../N/bpy.types.Node.md#bpy.types.Node.bl_rna_get_subclass_py "bpy.types.Node.bl_rna_get_subclass_py")
  * [`NodeInternal.poll`](../N/bpy.types.NodeInternal.md#bpy.types.NodeInternal.poll "bpy.types.NodeInternal.poll")
  * [`NodeInternal.poll_instance`](../N/bpy.types.NodeInternal.md#bpy.types.NodeInternal.poll_instance "bpy.types.NodeInternal.poll_instance")
  * [`NodeInternal.update`](../N/bpy.types.NodeInternal.md#bpy.types.NodeInternal.update "bpy.types.NodeInternal.update")
  * [`NodeInternal.draw_buttons`](../N/bpy.types.NodeInternal.md#bpy.types.NodeInternal.draw_buttons "bpy.types.NodeInternal.draw_buttons")
  * [`NodeInternal.draw_buttons_ext`](../N/bpy.types.NodeInternal.md#bpy.types.NodeInternal.draw_buttons_ext "bpy.types.NodeInternal.draw_buttons_ext")
  * [`NodeInternal.bl_rna_get_subclass`](../N/bpy.types.NodeInternal.md#bpy.types.NodeInternal.bl_rna_get_subclass "bpy.types.NodeInternal.bl_rna_get_subclass")
  * [`NodeInternal.bl_rna_get_subclass_py`](../N/bpy.types.NodeInternal.md#bpy.types.NodeInternal.bl_rna_get_subclass_py "bpy.types.NodeInternal.bl_rna_get_subclass_py")
  * `GeometryNode.poll`
  * [`GeometryNode.bl_rna_get_subclass`](bpy.types.GeometryNode.md#bpy.types.GeometryNode.bl_rna_get_subclass "bpy.types.GeometryNode.bl_rna_get_subclass")
  * [`GeometryNode.bl_rna_get_subclass_py`](bpy.types.GeometryNode.md#bpy.types.GeometryNode.bl_rna_get_subclass_py "bpy.types.GeometryNode.bl_rna_get_subclass_py")

  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
