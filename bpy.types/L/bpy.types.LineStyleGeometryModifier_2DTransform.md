# LineStyleGeometryModifier_2DTransform(LineStyleGeometryModifier)

base classes — [[bpy_struct]], [[LineStyleModifier]], [[LineStyleGeometryModifier]]

_class _bpy.types.LineStyleGeometryModifier_2DTransform(_LineStyleGeometryModifier_)
    

Apply two-dimensional scaling and rotation to stroke backbone geometry

angle
    

Rotation angle

Type:
    

float in [-inf, inf], default 0.0

expanded
    

True if the modifier tab is expanded

Type:
    

boolean, default False

pivot
    

Pivot of scaling and rotation operations

Type:
    

enum in [`'CENTER'`, `'START'`, `'END'`, `'PARAM'`, `'ABSOLUTE'`], default `'CENTER'`

pivot_u
    

Pivot in terms of the stroke point parameter u (0 <= u <= 1)

Type:
    

float in [0, 1], default 0.0

pivot_x
    

2D X coordinate of the absolute pivot

Type:
    

float in [-inf, inf], default 0.0

pivot_y
    

2D Y coordinate of the absolute pivot

Type:
    

float in [-inf, inf], default 0.0

scale_x
    

Scaling factor that is applied along the X axis

Type:
    

float in [-inf, inf], default 0.0

scale_y
    

Scaling factor that is applied along the Y axis

Type:
    

float in [-inf, inf], default 0.0

type
    

Type of the modifier

Type:
    

enum in [Linestyle Geometry Modifier Type Items](../../bpy_types_enum_items/linestyle_geometry_modifier_type_items.md#rna-enum-linestyle-geometry-modifier-type-items), default `'2D_OFFSET'`, (readonly)

use
    

Enable or disable this modifier during stroke rendering

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

  * [[LineStyleGeometryModifier.name]]

  
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

| 

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
  * [[LineStyleModifier.bl_rna_get_subclass]]
  * [[LineStyleModifier.bl_rna_get_subclass_py]]
  * [[LineStyleGeometryModifier.bl_rna_get_subclass]]
  * [[LineStyleGeometryModifier.bl_rna_get_subclass_py]]

  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
