# UI_UL_list(UIList)

base classes — [[bpy_struct]], [[UIList]]

_class _bpy.types.UI_UL_list(_UIList_)
    

_static _filter_items_by_name(_pattern_ , _bitflag_ , _items_ , _propname ='name'_, _flags =None_, _reverse =False_)
    

Set FILTER_ITEM for items which name matches filter_name one (case-insensitive). pattern is the filtering pattern. propname is the name of the string property to use for filtering. flags must be a list of integers the same length as items, or None! return a list of flags (based on given flags if not None), or an empty list if no flags were given and no filtering has been done.

_classmethod _sort_items_by_name(_items_ , _propname ='name'_)
    

Re-order items using their names (case-insensitive). propname is the name of the string property to use for sorting. return a list mapping org_idx -> new_idx, or an empty list if no sorting has been done.

_static _sort_items_helper(_sort_data_ , _key_ , _reverse =False_)
    

Common sorting utility. Returns a neworder list mapping org_idx -> new_idx. sort_data must be an (unordered) list of tuples [(org_idx, …), (org_idx, …), …]. key must be the same kind of callable you would use for sorted() builtin function. reverse will reverse the sorting!

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
  * [[UIList.bl_idname]]
  * [[UIList.list_id]]
  * [[UIList.layout_type]]
  * [[UIList.use_filter_show]]
  * [[UIList.filter_name]]

| 

  * [[UIList.use_filter_invert]]
  * [[UIList.use_filter_sort_alpha]]
  * [[UIList.use_filter_sort_reverse]]
  * [[UIList.use_filter_sort_lock]]
  * [[UIList.bitflag_filter_item]]
  * [[UIList.bitflag_item_never_show]]

  
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

| 

  * [[bpy_struct.path_resolve]]
  * [[bpy_struct.pop]]
  * [[bpy_struct.property_overridable_library_set]]
  * [[bpy_struct.property_unset]]
  * [[bpy_struct.rna_ancestors]]
  * [[bpy_struct.type_recast]]
  * [[bpy_struct.values]]
  * [[UIList.bl_system_properties_get]]
  * [[UIList.draw_item]]
  * [[UIList.draw_filter]]
  * [[UIList.filter_items]]
  * [[UIList.append]]
  * [[UIList.is_extended]]
  * [[UIList.prepend]]
  * [[UIList.remove]]
  * [[UIList.bl_rna_get_subclass]]
  * [[UIList.bl_rna_get_subclass_py]]

  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
