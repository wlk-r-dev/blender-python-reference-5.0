# Spline(bpy_struct)

base class — [[bpy_struct]]

_class _bpy.types.Spline(_bpy_struct_)
    

Element of a curve, either NURBS, Bézier or Polyline or a character with text objects

bezier_points
    

Collection of points for Bézier curves only

Type:
    

[[SplineBezierPoints]] [[bpy_prop_collection]] of [[BezierSplinePoint]], (readonly)

character_index
    

Location of this character in the text data (only for text curves)

Type:
    

int in [0, inf], default 0, (readonly)

hide
    

Hide this curve in Edit mode

Type:
    

boolean, default False

material_index
    

Material slot index of this curve

Type:
    

int in [0, 32767], default 0

order_u
    

NURBS order in the U direction. Higher values make each point influence a greater area, but have worse performance.

Type:
    

int in [2, 64], default 0

order_v
    

NURBS order in the V direction. Higher values make each point influence a greater area, but have worse performance.

Type:
    

int in [2, 64], default 0

point_count_u
    

Total number points for the curve or surface in the U direction

Type:
    

int in [0, inf], default 0, (readonly)

point_count_v
    

Total number points for the surface on the V direction

Type:
    

int in [0, inf], default 0, (readonly)

points
    

Collection of points that make up this poly or nurbs spline

Type:
    

[[SplinePoints]] [[bpy_prop_collection]] of [[SplinePoint]], (readonly)

radius_interpolation
    

The type of radius interpolation for Bézier curves

Type:
    

enum in [`'LINEAR'`, `'CARDINAL'`, `'BSPLINE'`, `'EASE'`], default `'LINEAR'`

resolution_u
    

Curve or Surface subdivisions per segment

Type:
    

int in [1, 1024], default 0

resolution_v
    

Surface subdivisions per segment

Type:
    

int in [1, 1024], default 0

tilt_interpolation
    

The type of tilt interpolation for 3D, Bézier curves

Type:
    

enum in [`'LINEAR'`, `'CARDINAL'`, `'BSPLINE'`, `'EASE'`], default `'LINEAR'`

type
    

The interpolation type for this curve element

Type:
    

enum in [`'POLY'`, `'BEZIER'`, `'NURBS'`], default `'POLY'`

use_bezier_u
    

Make this nurbs curve or surface act like a Bézier spline in the U direction

Type:
    

boolean, default False

use_bezier_v
    

Make this nurbs surface act like a Bézier spline in the V direction

Type:
    

boolean, default False

use_cyclic_u
    

Make this curve or surface a closed loop in the U direction

Type:
    

boolean, default False

use_cyclic_v
    

Make this surface a closed loop in the V direction

Type:
    

boolean, default False

use_endpoint_u
    

Make this nurbs curve or surface meet the endpoints in the U direction

Type:
    

boolean, default False

use_endpoint_v
    

Make this nurbs surface meet the endpoints in the V direction

Type:
    

boolean, default False

use_smooth
    

Smooth the normals of the surface or beveled curve

Type:
    

boolean, default False

calc_length(_*_ , _resolution =0_)
    

Calculate spline length

Parameters:
    

**resolution** (_int in_ _[__0_ _,__1024_ _]__,__(__optional_ _)_) – Resolution, Spline resolution to be used, 0 defaults to the resolution_u

Returns:
    

Length, Length of the polygonaly approximated spline

Return type:
    

float in [0, inf]

valid_message(_direction_)
    

Return the message

Parameters:
    

**direction** (_int in_ _[__0_ _,__1_ _]_) – Direction, The direction where 0-1 maps to U-V

Returns:
    

Return value, The message or an empty string when there is no error

Return type:
    

string

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
  
## References

  * [[Curve.splines]]
  * [[CurveSplines.active]]

| 

  * [[CurveSplines.new]]
  * [[CurveSplines.remove]]

  
---|---
  *[*]: Keyword-only parameters separator (PEP 3102)
  *[/]: Positional-only parameter separator (PEP 570)
