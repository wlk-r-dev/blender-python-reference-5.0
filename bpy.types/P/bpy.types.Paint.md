# Paint(bpy_struct)

base class — [`bpy_struct`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct "bpy.types.bpy_struct")

subclasses — [`CurvesSculpt`](../C/bpy.types.CurvesSculpt.md#bpy.types.CurvesSculpt "bpy.types.CurvesSculpt"), [`GpPaint`](../G/bpy.types.GpPaint.md#bpy.types.GpPaint "bpy.types.GpPaint"), [`GpSculptPaint`](../G/bpy.types.GpSculptPaint.md#bpy.types.GpSculptPaint "bpy.types.GpSculptPaint"), [`GpVertexPaint`](../G/bpy.types.GpVertexPaint.md#bpy.types.GpVertexPaint "bpy.types.GpVertexPaint"), [`GpWeightPaint`](../G/bpy.types.GpWeightPaint.md#bpy.types.GpWeightPaint "bpy.types.GpWeightPaint"), [`ImagePaint`](../I/bpy.types.ImagePaint.md#bpy.types.ImagePaint "bpy.types.ImagePaint"), [`Sculpt`](../S/bpy.types.Sculpt.md#bpy.types.Sculpt "bpy.types.Sculpt"), [`VertexPaint`](../V/bpy.types.VertexPaint.md#bpy.types.VertexPaint "bpy.types.VertexPaint")

_class _bpy.types.Paint(_bpy_struct_)
    

brush
    

Active brush

Type:
    

[`Brush`](../B/bpy.types.Brush.md#bpy.types.Brush "bpy.types.Brush"), (readonly)

brush_asset_reference
    

A weak reference to the matching brush asset, used e.g. to restore the last used brush on file load

Type:
    

[`AssetWeakReference`](../A/bpy.types.AssetWeakReference.md#bpy.types.AssetWeakReference "bpy.types.AssetWeakReference"), (readonly)

cavity_curve
    

Editable cavity curve

Type:
    

[`CurveMapping`](../C/bpy.types.CurveMapping.md#bpy.types.CurveMapping "bpy.types.CurveMapping"), (readonly, never None)

eraser_brush
    

Default eraser brush for quickly alternating with the main brush

Type:
    

[`Brush`](../B/bpy.types.Brush.md#bpy.types.Brush "bpy.types.Brush")

eraser_brush_asset_reference
    

A weak reference to the matching brush asset, used e.g. to restore the last used brush on file load

Type:
    

[`AssetWeakReference`](../A/bpy.types.AssetWeakReference.md#bpy.types.AssetWeakReference "bpy.types.AssetWeakReference"), (readonly)

palette
    

Active Palette

Type:
    

[`Palette`](bpy.types.Palette.md#bpy.types.Palette "bpy.types.Palette")

show_brush
    

Type:
    

boolean, default False

show_brush_on_surface
    

Type:
    

boolean, default False

show_jitter_curve
    

Type:
    

boolean, default False

show_low_resolution
    

For multires, show low resolution while navigating the view

Type:
    

boolean, default False

show_size_curve
    

Type:
    

boolean, default False

show_strength_curve
    

Type:
    

boolean, default False

tile_offset
    

Stride at which tiled strokes are copied

Type:
    

[`mathutils.Vector`](mathutils.md#mathutils.Vector "mathutils.Vector") of 3 items in [0.01, inf], default (0.0, 0.0, 0.0)

tile_x
    

Tile along X axis

Type:
    

boolean, default False

tile_y
    

Tile along Y axis

Type:
    

boolean, default False

tile_z
    

Tile along Z axis

Type:
    

boolean, default False

unified_paint_settings
    

Type:
    

[`UnifiedPaintSettings`](../U/bpy.types.UnifiedPaintSettings.md#bpy.types.UnifiedPaintSettings "bpy.types.UnifiedPaintSettings"), (readonly, never None)

use_cavity
    

Mask painting according to mesh geometry cavity

Type:
    

boolean, default False

use_sculpt_delay_updates
    

Update the geometry when it enters the view, providing faster view navigation

Type:
    

boolean, default False

use_symmetry_feather
    

Reduce the strength of the brush where it overlaps symmetrical daubs

Type:
    

boolean, default False

use_symmetry_x
    

Mirror brush across the X axis

Type:
    

boolean, default False

use_symmetry_y
    

Mirror brush across the Y axis

Type:
    

boolean, default False

use_symmetry_z
    

Mirror brush across the Z axis

Type:
    

boolean, default False

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
  *[/]: Positional-only parameter separator (PEP 570)
