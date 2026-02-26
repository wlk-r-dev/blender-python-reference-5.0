# VIEW3D_AST_brush_gpencil_weight(AssetShelf)

base classes — [`bpy_struct`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct "bpy.types.bpy_struct"), [`AssetShelf`](../A/bpy.types.AssetShelf.md#bpy.types.AssetShelf "bpy.types.AssetShelf")

_class _bpy.types.VIEW3D_AST_brush_gpencil_weight(_AssetShelf_)
    

_classmethod _brush_type_poll(_context_ , _asset_)
    

_static _draw_popup_selector(_layout_ , _context_ , _brush_ , _show_name =True_)
    

_static _get_shelf_name_from_context(_context_)
    

_classmethod _has_tool_with_brush_type(_context_ , _brush_type_)
    

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
  * [`AssetShelf.bl_idname`](../A/bpy.types.AssetShelf.md#bpy.types.AssetShelf.bl_idname "bpy.types.AssetShelf.bl_idname")
  * [`AssetShelf.bl_space_type`](../A/bpy.types.AssetShelf.md#bpy.types.AssetShelf.bl_space_type "bpy.types.AssetShelf.bl_space_type")
  * [`AssetShelf.bl_options`](../A/bpy.types.AssetShelf.md#bpy.types.AssetShelf.bl_options "bpy.types.AssetShelf.bl_options")
  * [`AssetShelf.bl_activate_operator`](../A/bpy.types.AssetShelf.md#bpy.types.AssetShelf.bl_activate_operator "bpy.types.AssetShelf.bl_activate_operator")
  * [`AssetShelf.bl_drag_operator`](../A/bpy.types.AssetShelf.md#bpy.types.AssetShelf.bl_drag_operator "bpy.types.AssetShelf.bl_drag_operator")
  * [`AssetShelf.bl_default_preview_size`](../A/bpy.types.AssetShelf.md#bpy.types.AssetShelf.bl_default_preview_size "bpy.types.AssetShelf.bl_default_preview_size")
  * [`AssetShelf.filter_action`](../A/bpy.types.AssetShelf.md#bpy.types.AssetShelf.filter_action "bpy.types.AssetShelf.filter_action")
  * [`AssetShelf.filter_armature`](../A/bpy.types.AssetShelf.md#bpy.types.AssetShelf.filter_armature "bpy.types.AssetShelf.filter_armature")
  * [`AssetShelf.filter_brush`](../A/bpy.types.AssetShelf.md#bpy.types.AssetShelf.filter_brush "bpy.types.AssetShelf.filter_brush")
  * [`AssetShelf.filter_camera`](../A/bpy.types.AssetShelf.md#bpy.types.AssetShelf.filter_camera "bpy.types.AssetShelf.filter_camera")
  * [`AssetShelf.filter_cachefile`](../A/bpy.types.AssetShelf.md#bpy.types.AssetShelf.filter_cachefile "bpy.types.AssetShelf.filter_cachefile")
  * [`AssetShelf.filter_curve`](../A/bpy.types.AssetShelf.md#bpy.types.AssetShelf.filter_curve "bpy.types.AssetShelf.filter_curve")
  * [`AssetShelf.filter_annotations`](../A/bpy.types.AssetShelf.md#bpy.types.AssetShelf.filter_annotations "bpy.types.AssetShelf.filter_annotations")
  * [`AssetShelf.filter_grease_pencil`](../A/bpy.types.AssetShelf.md#bpy.types.AssetShelf.filter_grease_pencil "bpy.types.AssetShelf.filter_grease_pencil")
  * [`AssetShelf.filter_group`](../A/bpy.types.AssetShelf.md#bpy.types.AssetShelf.filter_group "bpy.types.AssetShelf.filter_group")
  * [`AssetShelf.filter_curves`](../A/bpy.types.AssetShelf.md#bpy.types.AssetShelf.filter_curves "bpy.types.AssetShelf.filter_curves")
  * [`AssetShelf.filter_image`](../A/bpy.types.AssetShelf.md#bpy.types.AssetShelf.filter_image "bpy.types.AssetShelf.filter_image")
  * [`AssetShelf.filter_light`](../A/bpy.types.AssetShelf.md#bpy.types.AssetShelf.filter_light "bpy.types.AssetShelf.filter_light")
  * [`AssetShelf.filter_light_probe`](../A/bpy.types.AssetShelf.md#bpy.types.AssetShelf.filter_light_probe "bpy.types.AssetShelf.filter_light_probe")
  * [`AssetShelf.filter_linestyle`](../A/bpy.types.AssetShelf.md#bpy.types.AssetShelf.filter_linestyle "bpy.types.AssetShelf.filter_linestyle")
  * [`AssetShelf.filter_lattice`](../A/bpy.types.AssetShelf.md#bpy.types.AssetShelf.filter_lattice "bpy.types.AssetShelf.filter_lattice")
  * [`AssetShelf.filter_material`](../A/bpy.types.AssetShelf.md#bpy.types.AssetShelf.filter_material "bpy.types.AssetShelf.filter_material")

| 

  * [`AssetShelf.filter_metaball`](../A/bpy.types.AssetShelf.md#bpy.types.AssetShelf.filter_metaball "bpy.types.AssetShelf.filter_metaball")
  * [`AssetShelf.filter_movie_clip`](../A/bpy.types.AssetShelf.md#bpy.types.AssetShelf.filter_movie_clip "bpy.types.AssetShelf.filter_movie_clip")
  * [`AssetShelf.filter_mesh`](../A/bpy.types.AssetShelf.md#bpy.types.AssetShelf.filter_mesh "bpy.types.AssetShelf.filter_mesh")
  * [`AssetShelf.filter_mask`](../A/bpy.types.AssetShelf.md#bpy.types.AssetShelf.filter_mask "bpy.types.AssetShelf.filter_mask")
  * [`AssetShelf.filter_node_tree`](../A/bpy.types.AssetShelf.md#bpy.types.AssetShelf.filter_node_tree "bpy.types.AssetShelf.filter_node_tree")
  * [`AssetShelf.filter_object`](../A/bpy.types.AssetShelf.md#bpy.types.AssetShelf.filter_object "bpy.types.AssetShelf.filter_object")
  * [`AssetShelf.filter_particle_settings`](../A/bpy.types.AssetShelf.md#bpy.types.AssetShelf.filter_particle_settings "bpy.types.AssetShelf.filter_particle_settings")
  * [`AssetShelf.filter_palette`](../A/bpy.types.AssetShelf.md#bpy.types.AssetShelf.filter_palette "bpy.types.AssetShelf.filter_palette")
  * [`AssetShelf.filter_paint_curve`](../A/bpy.types.AssetShelf.md#bpy.types.AssetShelf.filter_paint_curve "bpy.types.AssetShelf.filter_paint_curve")
  * [`AssetShelf.filter_pointcloud`](../A/bpy.types.AssetShelf.md#bpy.types.AssetShelf.filter_pointcloud "bpy.types.AssetShelf.filter_pointcloud")
  * [`AssetShelf.filter_scene`](../A/bpy.types.AssetShelf.md#bpy.types.AssetShelf.filter_scene "bpy.types.AssetShelf.filter_scene")
  * [`AssetShelf.filter_speaker`](../A/bpy.types.AssetShelf.md#bpy.types.AssetShelf.filter_speaker "bpy.types.AssetShelf.filter_speaker")
  * [`AssetShelf.filter_sound`](../A/bpy.types.AssetShelf.md#bpy.types.AssetShelf.filter_sound "bpy.types.AssetShelf.filter_sound")
  * [`AssetShelf.filter_texture`](../A/bpy.types.AssetShelf.md#bpy.types.AssetShelf.filter_texture "bpy.types.AssetShelf.filter_texture")
  * [`AssetShelf.filter_text`](../A/bpy.types.AssetShelf.md#bpy.types.AssetShelf.filter_text "bpy.types.AssetShelf.filter_text")
  * [`AssetShelf.filter_font`](../A/bpy.types.AssetShelf.md#bpy.types.AssetShelf.filter_font "bpy.types.AssetShelf.filter_font")
  * [`AssetShelf.filter_volume`](../A/bpy.types.AssetShelf.md#bpy.types.AssetShelf.filter_volume "bpy.types.AssetShelf.filter_volume")
  * [`AssetShelf.filter_world`](../A/bpy.types.AssetShelf.md#bpy.types.AssetShelf.filter_world "bpy.types.AssetShelf.filter_world")
  * [`AssetShelf.filter_work_space`](../A/bpy.types.AssetShelf.md#bpy.types.AssetShelf.filter_work_space "bpy.types.AssetShelf.filter_work_space")
  * [`AssetShelf.asset_library_reference`](../A/bpy.types.AssetShelf.md#bpy.types.AssetShelf.asset_library_reference "bpy.types.AssetShelf.asset_library_reference")
  * [`AssetShelf.show_names`](../A/bpy.types.AssetShelf.md#bpy.types.AssetShelf.show_names "bpy.types.AssetShelf.show_names")
  * [`AssetShelf.preview_size`](../A/bpy.types.AssetShelf.md#bpy.types.AssetShelf.preview_size "bpy.types.AssetShelf.preview_size")
  * [`AssetShelf.search_filter`](../A/bpy.types.AssetShelf.md#bpy.types.AssetShelf.search_filter "bpy.types.AssetShelf.search_filter")

  
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

| 

  * [`bpy_struct.path_from_id`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.path_from_id "bpy.types.bpy_struct.path_from_id")
  * [`bpy_struct.path_from_module`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.path_from_module "bpy.types.bpy_struct.path_from_module")
  * [`bpy_struct.path_resolve`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.path_resolve "bpy.types.bpy_struct.path_resolve")
  * [`bpy_struct.pop`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.pop "bpy.types.bpy_struct.pop")
  * [`bpy_struct.property_overridable_library_set`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.property_overridable_library_set "bpy.types.bpy_struct.property_overridable_library_set")
  * [`bpy_struct.property_unset`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.property_unset "bpy.types.bpy_struct.property_unset")
  * [`bpy_struct.rna_ancestors`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.rna_ancestors "bpy.types.bpy_struct.rna_ancestors")
  * [`bpy_struct.type_recast`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.type_recast "bpy.types.bpy_struct.type_recast")
  * [`bpy_struct.values`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.values "bpy.types.bpy_struct.values")
  * [`AssetShelf.poll`](../A/bpy.types.AssetShelf.md#bpy.types.AssetShelf.poll "bpy.types.AssetShelf.poll")
  * [`AssetShelf.asset_poll`](../A/bpy.types.AssetShelf.md#bpy.types.AssetShelf.asset_poll "bpy.types.AssetShelf.asset_poll")
  * [`AssetShelf.get_active_asset`](../A/bpy.types.AssetShelf.md#bpy.types.AssetShelf.get_active_asset "bpy.types.AssetShelf.get_active_asset")
  * [`AssetShelf.draw_context_menu`](../A/bpy.types.AssetShelf.md#bpy.types.AssetShelf.draw_context_menu "bpy.types.AssetShelf.draw_context_menu")
  * [`AssetShelf.bl_rna_get_subclass`](../A/bpy.types.AssetShelf.md#bpy.types.AssetShelf.bl_rna_get_subclass "bpy.types.AssetShelf.bl_rna_get_subclass")
  * [`AssetShelf.bl_rna_get_subclass_py`](../A/bpy.types.AssetShelf.md#bpy.types.AssetShelf.bl_rna_get_subclass_py "bpy.types.AssetShelf.bl_rna_get_subclass_py")

  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
