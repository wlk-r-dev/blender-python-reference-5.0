# NodeSocketVectorTranslation4D(NodeSocketStandard)

base classes — [`bpy_struct`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct "bpy.types.bpy_struct"), [`NodeSocket`](bpy.types.NodeSocket.md#bpy.types.NodeSocket "bpy.types.NodeSocket"), [`NodeSocketStandard`](bpy.types.NodeSocketStandard.md#bpy.types.NodeSocketStandard "bpy.types.NodeSocketStandard")

_class _bpy.types.NodeSocketVectorTranslation4D(_NodeSocketStandard_)
    

3D vector socket of a node

default_value
    

Input value used for unconnected socket

Type:
    

[`mathutils.Vector`](mathutils.md#mathutils.Vector "mathutils.Vector") of 4 items in [-inf, inf], default (0.0, 0.0, 0.0, 0.0)

links
    

List of node links from or to this socket.

Type:
    

[`NodeLinks`](bpy.types.NodeLinks.md#bpy.types.NodeLinks "bpy.types.NodeLinks")

Note

Takes `O(len(nodetree.links))` time.

(readonly)

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
  * [`NodeSocket.name`](bpy.types.NodeSocket.md#bpy.types.NodeSocket.name "bpy.types.NodeSocket.name")
  * [`NodeSocket.label`](bpy.types.NodeSocket.md#bpy.types.NodeSocket.label "bpy.types.NodeSocket.label")
  * [`NodeSocket.identifier`](bpy.types.NodeSocket.md#bpy.types.NodeSocket.identifier "bpy.types.NodeSocket.identifier")
  * [`NodeSocket.description`](bpy.types.NodeSocket.md#bpy.types.NodeSocket.description "bpy.types.NodeSocket.description")
  * [`NodeSocket.is_output`](bpy.types.NodeSocket.md#bpy.types.NodeSocket.is_output "bpy.types.NodeSocket.is_output")
  * [`NodeSocket.select`](bpy.types.NodeSocket.md#bpy.types.NodeSocket.select "bpy.types.NodeSocket.select")
  * [`NodeSocket.hide`](bpy.types.NodeSocket.md#bpy.types.NodeSocket.hide "bpy.types.NodeSocket.hide")
  * [`NodeSocket.enabled`](bpy.types.NodeSocket.md#bpy.types.NodeSocket.enabled "bpy.types.NodeSocket.enabled")
  * [`NodeSocket.link_limit`](bpy.types.NodeSocket.md#bpy.types.NodeSocket.link_limit "bpy.types.NodeSocket.link_limit")
  * [`NodeSocket.is_linked`](bpy.types.NodeSocket.md#bpy.types.NodeSocket.is_linked "bpy.types.NodeSocket.is_linked")
  * [`NodeSocket.is_unavailable`](bpy.types.NodeSocket.md#bpy.types.NodeSocket.is_unavailable "bpy.types.NodeSocket.is_unavailable")
  * [`NodeSocket.is_multi_input`](bpy.types.NodeSocket.md#bpy.types.NodeSocket.is_multi_input "bpy.types.NodeSocket.is_multi_input")
  * [`NodeSocket.show_expanded`](bpy.types.NodeSocket.md#bpy.types.NodeSocket.show_expanded "bpy.types.NodeSocket.show_expanded")

| 

  * [`NodeSocket.is_inactive`](bpy.types.NodeSocket.md#bpy.types.NodeSocket.is_inactive "bpy.types.NodeSocket.is_inactive")
  * [`NodeSocket.is_icon_visible`](bpy.types.NodeSocket.md#bpy.types.NodeSocket.is_icon_visible "bpy.types.NodeSocket.is_icon_visible")
  * [`NodeSocket.hide_value`](bpy.types.NodeSocket.md#bpy.types.NodeSocket.hide_value "bpy.types.NodeSocket.hide_value")
  * [`NodeSocket.pin_gizmo`](bpy.types.NodeSocket.md#bpy.types.NodeSocket.pin_gizmo "bpy.types.NodeSocket.pin_gizmo")
  * [`NodeSocket.node`](bpy.types.NodeSocket.md#bpy.types.NodeSocket.node "bpy.types.NodeSocket.node")
  * [`NodeSocket.type`](bpy.types.NodeSocket.md#bpy.types.NodeSocket.type "bpy.types.NodeSocket.type")
  * [`NodeSocket.display_shape`](bpy.types.NodeSocket.md#bpy.types.NodeSocket.display_shape "bpy.types.NodeSocket.display_shape")
  * [`NodeSocket.inferred_structure_type`](bpy.types.NodeSocket.md#bpy.types.NodeSocket.inferred_structure_type "bpy.types.NodeSocket.inferred_structure_type")
  * [`NodeSocket.bl_idname`](bpy.types.NodeSocket.md#bpy.types.NodeSocket.bl_idname "bpy.types.NodeSocket.bl_idname")
  * [`NodeSocket.bl_label`](bpy.types.NodeSocket.md#bpy.types.NodeSocket.bl_label "bpy.types.NodeSocket.bl_label")
  * [`NodeSocket.bl_subtype_label`](bpy.types.NodeSocket.md#bpy.types.NodeSocket.bl_subtype_label "bpy.types.NodeSocket.bl_subtype_label")
  * [`NodeSocket.links`](bpy.types.NodeSocket.md#bpy.types.NodeSocket.links "bpy.types.NodeSocket.links")
  * [`NodeSocketStandard.links`](bpy.types.NodeSocketStandard.md#bpy.types.NodeSocketStandard.links "bpy.types.NodeSocketStandard.links")

  
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

| 

  * [`bpy_struct.pop`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.pop "bpy.types.bpy_struct.pop")
  * [`bpy_struct.property_overridable_library_set`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.property_overridable_library_set "bpy.types.bpy_struct.property_overridable_library_set")
  * [`bpy_struct.property_unset`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.property_unset "bpy.types.bpy_struct.property_unset")
  * [`bpy_struct.rna_ancestors`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.rna_ancestors "bpy.types.bpy_struct.rna_ancestors")
  * [`bpy_struct.type_recast`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.type_recast "bpy.types.bpy_struct.type_recast")
  * [`bpy_struct.values`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.values "bpy.types.bpy_struct.values")
  * [`NodeSocket.bl_system_properties_get`](bpy.types.NodeSocket.md#bpy.types.NodeSocket.bl_system_properties_get "bpy.types.NodeSocket.bl_system_properties_get")
  * [`NodeSocket.draw`](bpy.types.NodeSocket.md#bpy.types.NodeSocket.draw "bpy.types.NodeSocket.draw")
  * [`NodeSocket.draw_color`](bpy.types.NodeSocket.md#bpy.types.NodeSocket.draw_color "bpy.types.NodeSocket.draw_color")
  * [`NodeSocket.draw_color_simple`](bpy.types.NodeSocket.md#bpy.types.NodeSocket.draw_color_simple "bpy.types.NodeSocket.draw_color_simple")
  * [`NodeSocket.bl_rna_get_subclass`](bpy.types.NodeSocket.md#bpy.types.NodeSocket.bl_rna_get_subclass "bpy.types.NodeSocket.bl_rna_get_subclass")
  * [`NodeSocket.bl_rna_get_subclass_py`](bpy.types.NodeSocket.md#bpy.types.NodeSocket.bl_rna_get_subclass_py "bpy.types.NodeSocket.bl_rna_get_subclass_py")
  * [`NodeSocketStandard.draw`](bpy.types.NodeSocketStandard.md#bpy.types.NodeSocketStandard.draw "bpy.types.NodeSocketStandard.draw")
  * [`NodeSocketStandard.draw_color`](bpy.types.NodeSocketStandard.md#bpy.types.NodeSocketStandard.draw_color "bpy.types.NodeSocketStandard.draw_color")
  * [`NodeSocketStandard.draw_color_simple`](bpy.types.NodeSocketStandard.md#bpy.types.NodeSocketStandard.draw_color_simple "bpy.types.NodeSocketStandard.draw_color_simple")
  * [`NodeSocketStandard.bl_rna_get_subclass`](bpy.types.NodeSocketStandard.md#bpy.types.NodeSocketStandard.bl_rna_get_subclass "bpy.types.NodeSocketStandard.bl_rna_get_subclass")
  * [`NodeSocketStandard.bl_rna_get_subclass_py`](bpy.types.NodeSocketStandard.md#bpy.types.NodeSocketStandard.bl_rna_get_subclass_py "bpy.types.NodeSocketStandard.bl_rna_get_subclass_py")

  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
