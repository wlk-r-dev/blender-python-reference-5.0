# Space(bpy_struct)

base class — [`bpy_struct`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct "bpy.types.bpy_struct")

subclasses — [`SpaceClipEditor`](bpy.types.SpaceClipEditor.md#bpy.types.SpaceClipEditor "bpy.types.SpaceClipEditor"), [`SpaceConsole`](bpy.types.SpaceConsole.md#bpy.types.SpaceConsole "bpy.types.SpaceConsole"), [`SpaceDopeSheetEditor`](bpy.types.SpaceDopeSheetEditor.md#bpy.types.SpaceDopeSheetEditor "bpy.types.SpaceDopeSheetEditor"), [`SpaceFileBrowser`](bpy.types.SpaceFileBrowser.md#bpy.types.SpaceFileBrowser "bpy.types.SpaceFileBrowser"), [`SpaceGraphEditor`](bpy.types.SpaceGraphEditor.md#bpy.types.SpaceGraphEditor "bpy.types.SpaceGraphEditor"), [`SpaceImageEditor`](bpy.types.SpaceImageEditor.md#bpy.types.SpaceImageEditor "bpy.types.SpaceImageEditor"), [`SpaceInfo`](bpy.types.SpaceInfo.md#bpy.types.SpaceInfo "bpy.types.SpaceInfo"), [`SpaceNLA`](bpy.types.SpaceNLA.md#bpy.types.SpaceNLA "bpy.types.SpaceNLA"), [`SpaceNodeEditor`](bpy.types.SpaceNodeEditor.md#bpy.types.SpaceNodeEditor "bpy.types.SpaceNodeEditor"), [`SpaceOutliner`](bpy.types.SpaceOutliner.md#bpy.types.SpaceOutliner "bpy.types.SpaceOutliner"), [`SpacePreferences`](bpy.types.SpacePreferences.md#bpy.types.SpacePreferences "bpy.types.SpacePreferences"), [`SpaceProperties`](bpy.types.SpaceProperties.md#bpy.types.SpaceProperties "bpy.types.SpaceProperties"), [`SpaceSequenceEditor`](bpy.types.SpaceSequenceEditor.md#bpy.types.SpaceSequenceEditor "bpy.types.SpaceSequenceEditor"), [`SpaceSpreadsheet`](bpy.types.SpaceSpreadsheet.md#bpy.types.SpaceSpreadsheet "bpy.types.SpaceSpreadsheet"), [`SpaceTextEditor`](bpy.types.SpaceTextEditor.md#bpy.types.SpaceTextEditor "bpy.types.SpaceTextEditor"), [`SpaceView3D`](bpy.types.SpaceView3D.md#bpy.types.SpaceView3D "bpy.types.SpaceView3D")

_class _bpy.types.Space(_bpy_struct_)
    

Space data for a screen area

show_locked_time
    

Synchronize the visible timeline range with other time-based editors

Type:
    

boolean, default False

show_region_header
    

Type:
    

boolean, default False

type
    

Space data type

Type:
    

enum in [Space Type Items](../../bpy_types_enum_items/space_type_items.md#rna-enum-space-type-items), default `'EMPTY'`, (readonly)

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

_classmethod _draw_handler_add(_callback_ , _args_ , _region_type_ , _draw_type_)
    

Add a new draw handler to this space type. It will be called every time the specified region in the space type will be drawn. Note: All arguments are positional only for now.

Parameters:
    

  * **callback** (_Callable_ _[__...__,__Any_ _]_) – A function that will be called when the region is drawn. It gets the specified arguments as input, it’s return value is ignored.

  * **args** (_tuple_ _[__Any_ _,__...__]_) – Arguments that will be passed to the callback.

  * **region_type** (_str_) – The region type the callback draws in; usually `WINDOW`. ([`bpy.types.Region.type`](../R/bpy.types.Region.md#bpy.types.Region.type "bpy.types.Region.type"))

  * **draw_type** (_str_) – Usually `POST_PIXEL` for 2D drawing and `POST_VIEW` for 3D drawing. In some cases `PRE_VIEW` can be used. `BACKDROP` can be used for backdrops in the node editor.


Returns:
    

Handler that can be removed later on.

Return type:
    

object

_classmethod _draw_handler_remove(_handler_ , _region_type_)
    

Remove a draw handler that was added previously.

Parameters:
    

  * **handler** (_object_) – The draw handler that should be removed.

  * **region_type** (_str_) – Region type the callback was added to.


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

  * [`Area.spaces`](../A/bpy.types.Area.md#bpy.types.Area.spaces "bpy.types.Area.spaces")
  * [`AreaSpaces.active`](../A/bpy.types.AreaSpaces.md#bpy.types.AreaSpaces.active "bpy.types.AreaSpaces.active")

| 

  * [`Context.space_data`](../C/bpy.types.Context.md#bpy.types.Context.space_data "bpy.types.Context.space_data")

  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
