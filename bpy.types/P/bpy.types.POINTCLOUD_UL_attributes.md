# POINTCLOUD_UL_attributes(UIList)

base classes — [[bpy_struct]], [[UIList]]

_class _bpy.types.POINTCLOUD_UL_attributes(_UIList_)
    

draw_item(__context_ , _layout_ , __data_ , _attribute_ , __icon_ , __active_data_ , __active_propname_ , __index_)
    

filter_items(__context_ , _data_ , _property_)
    

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
