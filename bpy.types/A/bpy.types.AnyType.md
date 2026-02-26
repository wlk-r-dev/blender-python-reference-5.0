# AnyType(bpy_struct)

base class — [`bpy_struct`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct "bpy.types.bpy_struct")

_class _bpy.types.AnyType(_bpy_struct_)
    

RNA type used for pointers to any possible data

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

  * [`bpy.context.property`](../../bpy.context.md#bpy.context.property "bpy.context.property")
  * [`BoneCollection.assign`](../B/bpy.types.BoneCollection.md#bpy.types.BoneCollection.assign "bpy.types.BoneCollection.assign")
  * [`BoneCollection.unassign`](../B/bpy.types.BoneCollection.md#bpy.types.BoneCollection.unassign "bpy.types.BoneCollection.unassign")
  * [`FCurve.update_autoflags`](../F/bpy.types.FCurve.md#bpy.types.FCurve.update_autoflags "bpy.types.FCurve.update_autoflags")
  * [`Gizmo.target_set_prop`](../G/bpy.types.Gizmo.md#bpy.types.Gizmo.target_set_prop "bpy.types.Gizmo.target_set_prop")
  * [`KeyingSetInfo.generate`](../K/bpy.types.KeyingSetInfo.md#bpy.types.KeyingSetInfo.generate "bpy.types.KeyingSetInfo.generate")
  * [`Region.data`](../R/bpy.types.Region.md#bpy.types.Region.data "bpy.types.Region.data")
  * [`UILayout.context_pointer_set`](../U/bpy.types.UILayout.md#bpy.types.UILayout.context_pointer_set "bpy.types.UILayout.context_pointer_set")
  * [`UILayout.enum_item_description`](../U/bpy.types.UILayout.md#bpy.types.UILayout.enum_item_description "bpy.types.UILayout.enum_item_description")
  * [`UILayout.enum_item_icon`](../U/bpy.types.UILayout.md#bpy.types.UILayout.enum_item_icon "bpy.types.UILayout.enum_item_icon")
  * [`UILayout.enum_item_name`](../U/bpy.types.UILayout.md#bpy.types.UILayout.enum_item_name "bpy.types.UILayout.enum_item_name")
  * [`UILayout.icon`](../U/bpy.types.UILayout.md#bpy.types.UILayout.icon "bpy.types.UILayout.icon")
  * [`UILayout.panel_prop`](../U/bpy.types.UILayout.md#bpy.types.UILayout.panel_prop "bpy.types.UILayout.panel_prop")
  * [`UILayout.prop`](../U/bpy.types.UILayout.md#bpy.types.UILayout.prop "bpy.types.UILayout.prop")
  * [`UILayout.prop_decorator`](../U/bpy.types.UILayout.md#bpy.types.UILayout.prop_decorator "bpy.types.UILayout.prop_decorator")
  * [`UILayout.prop_enum`](../U/bpy.types.UILayout.md#bpy.types.UILayout.prop_enum "bpy.types.UILayout.prop_enum")
  * [`UILayout.prop_menu_enum`](../U/bpy.types.UILayout.md#bpy.types.UILayout.prop_menu_enum "bpy.types.UILayout.prop_menu_enum")
  * [`UILayout.prop_search`](../U/bpy.types.UILayout.md#bpy.types.UILayout.prop_search "bpy.types.UILayout.prop_search")
  * [`UILayout.prop_search`](../U/bpy.types.UILayout.md#bpy.types.UILayout.prop_search "bpy.types.UILayout.prop_search")
  * [`UILayout.prop_tabs_enum`](../U/bpy.types.UILayout.md#bpy.types.UILayout.prop_tabs_enum "bpy.types.UILayout.prop_tabs_enum")
  * [`UILayout.prop_tabs_enum`](../U/bpy.types.UILayout.md#bpy.types.UILayout.prop_tabs_enum "bpy.types.UILayout.prop_tabs_enum")
  * [`UILayout.prop_with_menu`](../U/bpy.types.UILayout.md#bpy.types.UILayout.prop_with_menu "bpy.types.UILayout.prop_with_menu")
  * [`UILayout.prop_with_popover`](../U/bpy.types.UILayout.md#bpy.types.UILayout.prop_with_popover "bpy.types.UILayout.prop_with_popover")
  * [`UILayout.props_enum`](../U/bpy.types.UILayout.md#bpy.types.UILayout.props_enum "bpy.types.UILayout.props_enum")
  * [`UILayout.template_ID`](../U/bpy.types.UILayout.md#bpy.types.UILayout.template_ID "bpy.types.UILayout.template_ID")
  * [`UILayout.template_ID_preview`](../U/bpy.types.UILayout.md#bpy.types.UILayout.template_ID_preview "bpy.types.UILayout.template_ID_preview")
  * [`UILayout.template_ID_tabs`](../U/bpy.types.UILayout.md#bpy.types.UILayout.template_ID_tabs "bpy.types.UILayout.template_ID_tabs")
  * [`UILayout.template_any_ID`](../U/bpy.types.UILayout.md#bpy.types.UILayout.template_any_ID "bpy.types.UILayout.template_any_ID")
  * [`UILayout.template_cache_file`](../U/bpy.types.UILayout.md#bpy.types.UILayout.template_cache_file "bpy.types.UILayout.template_cache_file")
  * [`UILayout.template_cache_file_layers`](../U/bpy.types.UILayout.md#bpy.types.UILayout.template_cache_file_layers "bpy.types.UILayout.template_cache_file_layers")
  * [`UILayout.template_cache_file_time_settings`](../U/bpy.types.UILayout.md#bpy.types.UILayout.template_cache_file_time_settings "bpy.types.UILayout.template_cache_file_time_settings")
  * [`UILayout.template_cache_file_velocity`](../U/bpy.types.UILayout.md#bpy.types.UILayout.template_cache_file_velocity "bpy.types.UILayout.template_cache_file_velocity")
  * [`UILayout.template_color_picker`](../U/bpy.types.UILayout.md#bpy.types.UILayout.template_color_picker "bpy.types.UILayout.template_color_picker")

| 

  * [`UILayout.template_color_ramp`](../U/bpy.types.UILayout.md#bpy.types.UILayout.template_color_ramp "bpy.types.UILayout.template_color_ramp")
  * [`UILayout.template_colormanaged_view_settings`](../U/bpy.types.UILayout.md#bpy.types.UILayout.template_colormanaged_view_settings "bpy.types.UILayout.template_colormanaged_view_settings")
  * [`UILayout.template_colorspace_settings`](../U/bpy.types.UILayout.md#bpy.types.UILayout.template_colorspace_settings "bpy.types.UILayout.template_colorspace_settings")
  * [`UILayout.template_component_menu`](../U/bpy.types.UILayout.md#bpy.types.UILayout.template_component_menu "bpy.types.UILayout.template_component_menu")
  * [`UILayout.template_curve_mapping`](../U/bpy.types.UILayout.md#bpy.types.UILayout.template_curve_mapping "bpy.types.UILayout.template_curve_mapping")
  * [`UILayout.template_curveprofile`](../U/bpy.types.UILayout.md#bpy.types.UILayout.template_curveprofile "bpy.types.UILayout.template_curveprofile")
  * [`UILayout.template_greasepencil_color`](../U/bpy.types.UILayout.md#bpy.types.UILayout.template_greasepencil_color "bpy.types.UILayout.template_greasepencil_color")
  * [`UILayout.template_histogram`](../U/bpy.types.UILayout.md#bpy.types.UILayout.template_histogram "bpy.types.UILayout.template_histogram")
  * [`UILayout.template_icon_view`](../U/bpy.types.UILayout.md#bpy.types.UILayout.template_icon_view "bpy.types.UILayout.template_icon_view")
  * [`UILayout.template_image`](../U/bpy.types.UILayout.md#bpy.types.UILayout.template_image "bpy.types.UILayout.template_image")
  * [`UILayout.template_layers`](../U/bpy.types.UILayout.md#bpy.types.UILayout.template_layers "bpy.types.UILayout.template_layers")
  * [`UILayout.template_layers`](../U/bpy.types.UILayout.md#bpy.types.UILayout.template_layers "bpy.types.UILayout.template_layers")
  * [`UILayout.template_light_linking_collection`](../U/bpy.types.UILayout.md#bpy.types.UILayout.template_light_linking_collection "bpy.types.UILayout.template_light_linking_collection")
  * [`UILayout.template_list`](../U/bpy.types.UILayout.md#bpy.types.UILayout.template_list "bpy.types.UILayout.template_list")
  * [`UILayout.template_list`](../U/bpy.types.UILayout.md#bpy.types.UILayout.template_list "bpy.types.UILayout.template_list")
  * [`UILayout.template_marker`](../U/bpy.types.UILayout.md#bpy.types.UILayout.template_marker "bpy.types.UILayout.template_marker")
  * [`UILayout.template_matrix`](../U/bpy.types.UILayout.md#bpy.types.UILayout.template_matrix "bpy.types.UILayout.template_matrix")
  * [`UILayout.template_movieclip`](../U/bpy.types.UILayout.md#bpy.types.UILayout.template_movieclip "bpy.types.UILayout.template_movieclip")
  * [`UILayout.template_movieclip_information`](../U/bpy.types.UILayout.md#bpy.types.UILayout.template_movieclip_information "bpy.types.UILayout.template_movieclip_information")
  * [`UILayout.template_palette`](../U/bpy.types.UILayout.md#bpy.types.UILayout.template_palette "bpy.types.UILayout.template_palette")
  * [`UILayout.template_path_builder`](../U/bpy.types.UILayout.md#bpy.types.UILayout.template_path_builder "bpy.types.UILayout.template_path_builder")
  * [`UILayout.template_search`](../U/bpy.types.UILayout.md#bpy.types.UILayout.template_search "bpy.types.UILayout.template_search")
  * [`UILayout.template_search`](../U/bpy.types.UILayout.md#bpy.types.UILayout.template_search "bpy.types.UILayout.template_search")
  * [`UILayout.template_search_preview`](../U/bpy.types.UILayout.md#bpy.types.UILayout.template_search_preview "bpy.types.UILayout.template_search_preview")
  * [`UILayout.template_search_preview`](../U/bpy.types.UILayout.md#bpy.types.UILayout.template_search_preview "bpy.types.UILayout.template_search_preview")
  * [`UILayout.template_track`](../U/bpy.types.UILayout.md#bpy.types.UILayout.template_track "bpy.types.UILayout.template_track")
  * [`UILayout.template_vectorscope`](../U/bpy.types.UILayout.md#bpy.types.UILayout.template_vectorscope "bpy.types.UILayout.template_vectorscope")
  * [`UILayout.template_waveform`](../U/bpy.types.UILayout.md#bpy.types.UILayout.template_waveform "bpy.types.UILayout.template_waveform")
  * [`UIList.draw_item`](../U/bpy.types.UIList.md#bpy.types.UIList.draw_item "bpy.types.UIList.draw_item")
  * [`UIList.draw_item`](../U/bpy.types.UIList.md#bpy.types.UIList.draw_item "bpy.types.UIList.draw_item")
  * [`UIList.draw_item`](../U/bpy.types.UIList.md#bpy.types.UIList.draw_item "bpy.types.UIList.draw_item")
  * [`UIList.filter_items`](../U/bpy.types.UIList.md#bpy.types.UIList.filter_items "bpy.types.UIList.filter_items")

  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
