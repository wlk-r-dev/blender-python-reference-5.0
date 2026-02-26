# StripColorBalance(StripColorBalanceData)

base classes — [`bpy_struct`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct "bpy.types.bpy_struct"), [`StripColorBalanceData`](bpy.types.StripColorBalanceData.md#bpy.types.StripColorBalanceData "bpy.types.StripColorBalanceData")

_class _bpy.types.StripColorBalance(_StripColorBalanceData_)
    

Color balance parameters for a sequence strip

_classmethod _bl_rna_get_subclass(_id_ , _default =None_, _/_)
    

Parameters:
    

**id** (_str_) – The RNA type identifier.

Returns:
    

The RNA type or default when not found.

Return type:
    

[`bpy.types.Struct`](bpy.types.Struct.md#bpy.types.Struct "bpy.types.Struct") subclass

_classmethod _bl_rna_get_subclass_py(_id_ , _default =None_, _/_)
    

Parameters:
    

**id** (_str_) – The RNA type identifier.

Returns:
    

The class or default when not found.

Return type:
    

type

## Inherited Properties

  * [`bpy_struct.id_data`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.id_data "bpy.types.bpy_struct.id_data")
  * [`StripColorBalanceData.correction_method`](bpy.types.StripColorBalanceData.md#bpy.types.StripColorBalanceData.correction_method "bpy.types.StripColorBalanceData.correction_method")
  * [`StripColorBalanceData.lift`](bpy.types.StripColorBalanceData.md#bpy.types.StripColorBalanceData.lift "bpy.types.StripColorBalanceData.lift")
  * [`StripColorBalanceData.gamma`](bpy.types.StripColorBalanceData.md#bpy.types.StripColorBalanceData.gamma "bpy.types.StripColorBalanceData.gamma")
  * [`StripColorBalanceData.gain`](bpy.types.StripColorBalanceData.md#bpy.types.StripColorBalanceData.gain "bpy.types.StripColorBalanceData.gain")
  * [`StripColorBalanceData.slope`](bpy.types.StripColorBalanceData.md#bpy.types.StripColorBalanceData.slope "bpy.types.StripColorBalanceData.slope")
  * [`StripColorBalanceData.offset`](bpy.types.StripColorBalanceData.md#bpy.types.StripColorBalanceData.offset "bpy.types.StripColorBalanceData.offset")

| 

  * [`StripColorBalanceData.power`](bpy.types.StripColorBalanceData.md#bpy.types.StripColorBalanceData.power "bpy.types.StripColorBalanceData.power")
  * [`StripColorBalanceData.invert_lift`](bpy.types.StripColorBalanceData.md#bpy.types.StripColorBalanceData.invert_lift "bpy.types.StripColorBalanceData.invert_lift")
  * [`StripColorBalanceData.invert_gamma`](bpy.types.StripColorBalanceData.md#bpy.types.StripColorBalanceData.invert_gamma "bpy.types.StripColorBalanceData.invert_gamma")
  * [`StripColorBalanceData.invert_gain`](bpy.types.StripColorBalanceData.md#bpy.types.StripColorBalanceData.invert_gain "bpy.types.StripColorBalanceData.invert_gain")
  * [`StripColorBalanceData.invert_slope`](bpy.types.StripColorBalanceData.md#bpy.types.StripColorBalanceData.invert_slope "bpy.types.StripColorBalanceData.invert_slope")
  * [`StripColorBalanceData.invert_offset`](bpy.types.StripColorBalanceData.md#bpy.types.StripColorBalanceData.invert_offset "bpy.types.StripColorBalanceData.invert_offset")
  * [`StripColorBalanceData.invert_power`](bpy.types.StripColorBalanceData.md#bpy.types.StripColorBalanceData.invert_power "bpy.types.StripColorBalanceData.invert_power")

  
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

| 

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
  * [`StripColorBalanceData.bl_rna_get_subclass`](bpy.types.StripColorBalanceData.md#bpy.types.StripColorBalanceData.bl_rna_get_subclass "bpy.types.StripColorBalanceData.bl_rna_get_subclass")
  * [`StripColorBalanceData.bl_rna_get_subclass_py`](bpy.types.StripColorBalanceData.md#bpy.types.StripColorBalanceData.bl_rna_get_subclass_py "bpy.types.StripColorBalanceData.bl_rna_get_subclass_py")

  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
