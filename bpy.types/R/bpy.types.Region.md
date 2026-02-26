# Region(bpy_struct)

base class — [`bpy_struct`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct "bpy.types.bpy_struct")

_class _bpy.types.Region(_bpy_struct_)
    

Region in a subdivided screen area

active_panel_category
    

The current active panel category, may be Null if the region does not support this feature (NOTE: these categories are generated at runtime, so list may be empty at initialization, before any drawing took place)

  * `UNSUPPORTED` Not Supported – This region does not support panel categories.


Type:
    

enum in [`'UNSUPPORTED'`], default `'UNSUPPORTED'`

alignment
    

Alignment of the region within the area

  * `NONE` None – Don’t use any fixed alignment, fill available space.

  * `TOP` Top.

  * `BOTTOM` Bottom.

  * `LEFT` Left.

  * `RIGHT` Right.

  * `HORIZONTAL_SPLIT` Horizontal Split.

  * `VERTICAL_SPLIT` Vertical Split.

  * `FLOAT` Float – Region floats on screen, does not use any fixed alignment.

  * `QUAD_SPLIT` Quad Split – Region is split horizontally and vertically.


Type:
    

enum in [`'NONE'`, `'TOP'`, `'BOTTOM'`, `'LEFT'`, `'RIGHT'`, `'HORIZONTAL_SPLIT'`, `'VERTICAL_SPLIT'`, `'FLOAT'`, `'QUAD_SPLIT'`], default `'NONE'`, (readonly)

data
    

Region specific data (the type depends on the region type)

Type:
    

[`AnyType`](../A/bpy.types.AnyType.md#bpy.types.AnyType "bpy.types.AnyType"), (readonly)

height
    

Region height

Type:
    

int in [0, 32767], default 0, (readonly)

type
    

Type of this region

Type:
    

enum in [Region Type Items](../../bpy_types_enum_items/region_type_items.md#rna-enum-region-type-items), default `'WINDOW'`, (readonly)

view2d
    

2D view of the region

Type:
    

[`View2D`](../V/bpy.types.View2D.md#bpy.types.View2D "bpy.types.View2D"), (readonly, never None)

width
    

Region width

Type:
    

int in [0, 32767], default 0, (readonly)

x
    

The window relative vertical location of the region

Type:
    

int in [-inf, inf], default 0, (readonly)

y
    

The window relative horizontal location of the region

Type:
    

int in [-inf, inf], default 0, (readonly)

tag_redraw()
    

tag_redraw

tag_refresh_ui()
    

tag_refresh_ui

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

  * [`Area.regions`](../A/bpy.types.Area.md#bpy.types.Area.regions "bpy.types.Area.regions")
  * [`Context.region`](../C/bpy.types.Context.md#bpy.types.Context.region "bpy.types.Context.region")

| 

  * [`Context.region_popup`](../C/bpy.types.Context.md#bpy.types.Context.region_popup "bpy.types.Context.region_popup")

  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
