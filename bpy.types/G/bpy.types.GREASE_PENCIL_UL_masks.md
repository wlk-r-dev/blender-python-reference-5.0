# GREASE_PENCIL_UL_masks(UIList)

base classes — [`bpy_struct`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct "bpy.types.bpy_struct"), [`UIList`](../U/bpy.types.UIList.md#bpy.types.UIList "bpy.types.UIList")

_class _bpy.types.GREASE_PENCIL_UL_masks(_UIList_)
    

draw_item(__context_ , _layout_ , __data_ , _item_ , _icon_ , __active_data_ , __active_propname_ , __index_)
    

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
  * [`UIList.bl_idname`](../U/bpy.types.UIList.md#bpy.types.UIList.bl_idname "bpy.types.UIList.bl_idname")
  * [`UIList.list_id`](../U/bpy.types.UIList.md#bpy.types.UIList.list_id "bpy.types.UIList.list_id")
  * [`UIList.layout_type`](../U/bpy.types.UIList.md#bpy.types.UIList.layout_type "bpy.types.UIList.layout_type")
  * [`UIList.use_filter_show`](../U/bpy.types.UIList.md#bpy.types.UIList.use_filter_show "bpy.types.UIList.use_filter_show")
  * [`UIList.filter_name`](../U/bpy.types.UIList.md#bpy.types.UIList.filter_name "bpy.types.UIList.filter_name")

| 

  * [`UIList.use_filter_invert`](../U/bpy.types.UIList.md#bpy.types.UIList.use_filter_invert "bpy.types.UIList.use_filter_invert")
  * [`UIList.use_filter_sort_alpha`](../U/bpy.types.UIList.md#bpy.types.UIList.use_filter_sort_alpha "bpy.types.UIList.use_filter_sort_alpha")
  * [`UIList.use_filter_sort_reverse`](../U/bpy.types.UIList.md#bpy.types.UIList.use_filter_sort_reverse "bpy.types.UIList.use_filter_sort_reverse")
  * [`UIList.use_filter_sort_lock`](../U/bpy.types.UIList.md#bpy.types.UIList.use_filter_sort_lock "bpy.types.UIList.use_filter_sort_lock")
  * [`UIList.bitflag_filter_item`](../U/bpy.types.UIList.md#bpy.types.UIList.bitflag_filter_item "bpy.types.UIList.bitflag_filter_item")
  * [`UIList.bitflag_item_never_show`](../U/bpy.types.UIList.md#bpy.types.UIList.bitflag_item_never_show "bpy.types.UIList.bitflag_item_never_show")

  
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

| 

  * [`bpy_struct.path_resolve`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.path_resolve "bpy.types.bpy_struct.path_resolve")
  * [`bpy_struct.pop`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.pop "bpy.types.bpy_struct.pop")
  * [`bpy_struct.property_overridable_library_set`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.property_overridable_library_set "bpy.types.bpy_struct.property_overridable_library_set")
  * [`bpy_struct.property_unset`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.property_unset "bpy.types.bpy_struct.property_unset")
  * [`bpy_struct.rna_ancestors`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.rna_ancestors "bpy.types.bpy_struct.rna_ancestors")
  * [`bpy_struct.type_recast`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.type_recast "bpy.types.bpy_struct.type_recast")
  * [`bpy_struct.values`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.values "bpy.types.bpy_struct.values")
  * [`UIList.bl_system_properties_get`](../U/bpy.types.UIList.md#bpy.types.UIList.bl_system_properties_get "bpy.types.UIList.bl_system_properties_get")
  * [`UIList.draw_item`](../U/bpy.types.UIList.md#bpy.types.UIList.draw_item "bpy.types.UIList.draw_item")
  * [`UIList.draw_filter`](../U/bpy.types.UIList.md#bpy.types.UIList.draw_filter "bpy.types.UIList.draw_filter")
  * [`UIList.filter_items`](../U/bpy.types.UIList.md#bpy.types.UIList.filter_items "bpy.types.UIList.filter_items")
  * [`UIList.append`](../U/bpy.types.UIList.md#bpy.types.UIList.append "bpy.types.UIList.append")
  * [`UIList.is_extended`](../U/bpy.types.UIList.md#bpy.types.UIList.is_extended "bpy.types.UIList.is_extended")
  * [`UIList.prepend`](../U/bpy.types.UIList.md#bpy.types.UIList.prepend "bpy.types.UIList.prepend")
  * [`UIList.remove`](../U/bpy.types.UIList.md#bpy.types.UIList.remove "bpy.types.UIList.remove")
  * [`UIList.bl_rna_get_subclass`](../U/bpy.types.UIList.md#bpy.types.UIList.bl_rna_get_subclass "bpy.types.UIList.bl_rna_get_subclass")
  * [`UIList.bl_rna_get_subclass_py`](../U/bpy.types.UIList.md#bpy.types.UIList.bl_rna_get_subclass_py "bpy.types.UIList.bl_rna_get_subclass_py")

  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
