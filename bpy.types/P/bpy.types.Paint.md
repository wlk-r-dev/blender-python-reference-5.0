# Paint(bpy_struct)

base class — [[bpy_struct]]

subclasses — [[CurvesSculpt]], [[GpPaint]], [[GpSculptPaint]], [[GpVertexPaint]], [[GpWeightPaint]], [[ImagePaint]], [[Sculpt]], [[VertexPaint]]

_class _bpy.types.Paint(_bpy_struct_)
    

brush
    

Active brush

Type:
    

[[Brush]], (readonly)

brush_asset_reference
    

A weak reference to the matching brush asset, used e.g. to restore the last used brush on file load

Type:
    

[[AssetWeakReference]], (readonly)

cavity_curve
    

Editable cavity curve

Type:
    

[[CurveMapping]], (readonly, never None)

eraser_brush
    

Default eraser brush for quickly alternating with the main brush

Type:
    

[[Brush]]

eraser_brush_asset_reference
    

A weak reference to the matching brush asset, used e.g. to restore the last used brush on file load

Type:
    

[[AssetWeakReference]], (readonly)

palette
    

Active Palette

Type:
    

[[Palette]]

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
    

[[mathutils.Vector]] of 3 items in [0.01, inf], default (0.0, 0.0, 0.0)

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
    

[[UnifiedPaintSettings]], (readonly, never None)

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

| 


  
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

| 

  * [[bpy_struct.keyframe_delete]]
  * [[bpy_struct.keyframe_insert]]
  * [[bpy_struct.keys]]
  * [[bpy_struct.path_from_id]]
  * [[bpy_struct.path_from_module]]
  * [[bpy_struct.path_resolve]]
  * [[bpy_struct.pop]]
  * [[bpy_struct.property_overridable_library_set]]
  * [[bpy_struct.property_unset]]
  * [[bpy_struct.rna_ancestors]]
  * [[bpy_struct.type_recast]]
  * [[bpy_struct.values]]

  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
