# Sculpt(Paint)

base classes — [`bpy_struct`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct "bpy.types.bpy_struct"), [`Paint`](../P/bpy.types.Paint.md#bpy.types.Paint "bpy.types.Paint")

_class _bpy.types.Sculpt(_Paint_)
    

automasking_boundary_edges_propagation_steps
    

Distance where boundary edge automasking is going to protect vertices from the fully masked edge

Type:
    

int in [1, 20], default 1

automasking_cavity_blur_steps
    

The number of times the cavity mask is blurred

Type:
    

int in [0, 25], default 0

automasking_cavity_curve
    

Curve used for the sensitivity

Type:
    

[`CurveMapping`](../C/bpy.types.CurveMapping.md#bpy.types.CurveMapping "bpy.types.CurveMapping"), (readonly)

automasking_cavity_curve_op
    

Curve used for the sensitivity

Type:
    

[`CurveMapping`](../C/bpy.types.CurveMapping.md#bpy.types.CurveMapping "bpy.types.CurveMapping"), (readonly)

automasking_cavity_factor
    

The contrast of the cavity mask

Type:
    

float in [0, 5], default 1.0

automasking_start_normal_falloff
    

Extend the angular range with a falloff gradient

Type:
    

float in [0.0001, 1], default 0.25

automasking_start_normal_limit
    

The range of angles that will be affected

Type:
    

float in [0.0001, 3.14159], default 0.349066

automasking_view_normal_falloff
    

Extend the angular range with a falloff gradient

Type:
    

float in [0.0001, 1], default 0.25

automasking_view_normal_limit
    

The range of angles that will be affected

Type:
    

float in [0.0001, 3.14159], default 1.5708

constant_detail_resolution
    

Maximum edge length for dynamic topology sculpting (as divisor of Blender unit - higher value means smaller edge length)

Type:
    

float in [0.0001, inf], default 3.0

detail_percent
    

Maximum edge length for dynamic topology sculpting (in brush percentage)

Type:
    

float in [0.5, 100], default 25.0

detail_refine_method
    

In dynamic-topology mode, how to add or remove mesh detail

  * `SUBDIVIDE` Subdivide Edges – Subdivide long edges to add mesh detail where needed.

  * `COLLAPSE` Collapse Edges – Collapse short edges to remove mesh detail where possible.

  * `SUBDIVIDE_COLLAPSE` Subdivide Collapse – Both subdivide long edges and collapse short edges to refine mesh detail.


Type:
    

enum in [`'SUBDIVIDE'`, `'COLLAPSE'`, `'SUBDIVIDE_COLLAPSE'`], default `'SUBDIVIDE_COLLAPSE'`

detail_size
    

Maximum edge length for dynamic topology sculpting (in pixels)

Type:
    

float in [0.5, 40], default 12.0

detail_type_method
    

In dynamic-topology mode, how mesh detail size is calculated

  * `RELATIVE` Relative Detail – Mesh detail is relative to the brush size and detail size.

  * `CONSTANT` Constant Detail – Mesh detail is constant in world space according to detail size.

  * `BRUSH` Brush Detail – Mesh detail is relative to brush size.

  * `MANUAL` Manual Detail – Mesh detail does not change on each stroke, only when using Flood Fill.


Type:
    

enum in [`'RELATIVE'`, `'CONSTANT'`, `'BRUSH'`, `'MANUAL'`], default `'RELATIVE'`

gravity
    

Amount of gravity after each dab

Type:
    

float in [0, 1], default 0.0

gravity_object
    

Object whose Z axis defines orientation of gravity

Type:
    

[`Object`](../O/bpy.types.Object.md#bpy.types.Object "bpy.types.Object")

lock_x
    

Disallow changes to the X axis of vertices

Type:
    

boolean, default False

lock_y
    

Disallow changes to the Y axis of vertices

Type:
    

boolean, default False

lock_z
    

Disallow changes to the Z axis of vertices

Type:
    

boolean, default False

symmetrize_direction
    

Source and destination for symmetrize operator

Type:
    

enum in [Symmetrize Direction Items](../../bpy_types_enum_items/symmetrize_direction_items.md#rna-enum-symmetrize-direction-items), default `'NEGATIVE_X'`

transform_mode
    

How the transformation is going to be applied to the target

  * `ALL_VERTICES` All Vertices – Applies the transformation to all vertices in the mesh.

  * `RADIUS_ELASTIC` Elastic – Applies the transformation simulating elasticity using the radius of the cursor.


Type:
    

enum in [`'ALL_VERTICES'`, `'RADIUS_ELASTIC'`], default `'ALL_VERTICES'`

use_automasking_boundary_edges
    

Do not affect non manifold boundary edges

Type:
    

boolean, default False

use_automasking_boundary_face_sets
    

Do not affect vertices that belong to a Face Set boundary

Type:
    

boolean, default False

use_automasking_cavity
    

Do not affect vertices on peaks, based on the surface curvature

Type:
    

boolean, default False

use_automasking_cavity_inverted
    

Do not affect vertices within crevices, based on the surface curvature

Type:
    

boolean, default False

use_automasking_custom_cavity_curve
    

Use custom curve

Type:
    

boolean, default False

use_automasking_face_sets
    

Affect only vertices that share Face Sets with the active vertex

Type:
    

boolean, default False

use_automasking_start_normal
    

Affect only vertices with a similar normal to where the stroke starts

Type:
    

boolean, default False

use_automasking_topology
    

Affect only vertices connected to the active vertex under the brush

Type:
    

boolean, default False

use_automasking_view_normal
    

Affect only vertices with a normal that faces the viewer

Type:
    

boolean, default False

use_automasking_view_occlusion
    

Only affect vertices that are not occluded by other faces (slower performance)

Type:
    

boolean, default False

use_deform_only
    

Use only deformation modifiers (temporary disable all constructive modifiers except multi-resolution)

Type:
    

boolean, default False

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
  * [`Paint.brush`](../P/bpy.types.Paint.md#bpy.types.Paint.brush "bpy.types.Paint.brush")
  * [`Paint.brush_asset_reference`](../P/bpy.types.Paint.md#bpy.types.Paint.brush_asset_reference "bpy.types.Paint.brush_asset_reference")
  * [`Paint.eraser_brush`](../P/bpy.types.Paint.md#bpy.types.Paint.eraser_brush "bpy.types.Paint.eraser_brush")
  * [`Paint.eraser_brush_asset_reference`](../P/bpy.types.Paint.md#bpy.types.Paint.eraser_brush_asset_reference "bpy.types.Paint.eraser_brush_asset_reference")
  * [`Paint.palette`](../P/bpy.types.Paint.md#bpy.types.Paint.palette "bpy.types.Paint.palette")
  * [`Paint.show_brush`](../P/bpy.types.Paint.md#bpy.types.Paint.show_brush "bpy.types.Paint.show_brush")
  * [`Paint.show_brush_on_surface`](../P/bpy.types.Paint.md#bpy.types.Paint.show_brush_on_surface "bpy.types.Paint.show_brush_on_surface")
  * [`Paint.show_low_resolution`](../P/bpy.types.Paint.md#bpy.types.Paint.show_low_resolution "bpy.types.Paint.show_low_resolution")
  * [`Paint.use_sculpt_delay_updates`](../P/bpy.types.Paint.md#bpy.types.Paint.use_sculpt_delay_updates "bpy.types.Paint.use_sculpt_delay_updates")
  * [`Paint.use_symmetry_x`](../P/bpy.types.Paint.md#bpy.types.Paint.use_symmetry_x "bpy.types.Paint.use_symmetry_x")
  * [`Paint.use_symmetry_y`](../P/bpy.types.Paint.md#bpy.types.Paint.use_symmetry_y "bpy.types.Paint.use_symmetry_y")

| 

  * [`Paint.use_symmetry_z`](../P/bpy.types.Paint.md#bpy.types.Paint.use_symmetry_z "bpy.types.Paint.use_symmetry_z")
  * [`Paint.use_symmetry_feather`](../P/bpy.types.Paint.md#bpy.types.Paint.use_symmetry_feather "bpy.types.Paint.use_symmetry_feather")
  * [`Paint.cavity_curve`](../P/bpy.types.Paint.md#bpy.types.Paint.cavity_curve "bpy.types.Paint.cavity_curve")
  * [`Paint.use_cavity`](../P/bpy.types.Paint.md#bpy.types.Paint.use_cavity "bpy.types.Paint.use_cavity")
  * [`Paint.tile_offset`](../P/bpy.types.Paint.md#bpy.types.Paint.tile_offset "bpy.types.Paint.tile_offset")
  * [`Paint.tile_x`](../P/bpy.types.Paint.md#bpy.types.Paint.tile_x "bpy.types.Paint.tile_x")
  * [`Paint.tile_y`](../P/bpy.types.Paint.md#bpy.types.Paint.tile_y "bpy.types.Paint.tile_y")
  * [`Paint.tile_z`](../P/bpy.types.Paint.md#bpy.types.Paint.tile_z "bpy.types.Paint.tile_z")
  * [`Paint.show_strength_curve`](../P/bpy.types.Paint.md#bpy.types.Paint.show_strength_curve "bpy.types.Paint.show_strength_curve")
  * [`Paint.show_size_curve`](../P/bpy.types.Paint.md#bpy.types.Paint.show_size_curve "bpy.types.Paint.show_size_curve")
  * [`Paint.show_jitter_curve`](../P/bpy.types.Paint.md#bpy.types.Paint.show_jitter_curve "bpy.types.Paint.show_jitter_curve")
  * [`Paint.unified_paint_settings`](../P/bpy.types.Paint.md#bpy.types.Paint.unified_paint_settings "bpy.types.Paint.unified_paint_settings")

  
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
  * [`Paint.bl_rna_get_subclass`](../P/bpy.types.Paint.md#bpy.types.Paint.bl_rna_get_subclass "bpy.types.Paint.bl_rna_get_subclass")
  * [`Paint.bl_rna_get_subclass_py`](../P/bpy.types.Paint.md#bpy.types.Paint.bl_rna_get_subclass_py "bpy.types.Paint.bl_rna_get_subclass_py")

  
---|---  
  
## References

  * [`ToolSettings.sculpt`](../T/bpy.types.ToolSettings.md#bpy.types.ToolSettings.sculpt "bpy.types.ToolSettings.sculpt")

| 


  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
