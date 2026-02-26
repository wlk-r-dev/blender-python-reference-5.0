# BezierSplinePoint(bpy_struct)

base class — [[bpy_struct]]

_class _bpy.types.BezierSplinePoint(_bpy_struct_)
    

Bézier curve point with two handles

co
    

Coordinates of the control point

Type:
    

[[mathutils.Vector]] of 3 items in [-inf, inf], default (0.0, 0.0, 0.0)

handle_left
    

Coordinates of the first handle

Type:
    

[[mathutils.Vector]] of 3 items in [-inf, inf], default (0.0, 0.0, 0.0)

handle_left_type
    

Handle types

Type:
    

enum in [`'FREE'`, `'VECTOR'`, `'ALIGNED'`, `'AUTO'`], default `'FREE'`

handle_right
    

Coordinates of the second handle

Type:
    

[[mathutils.Vector]] of 3 items in [-inf, inf], default (0.0, 0.0, 0.0)

handle_right_type
    

Handle types

Type:
    

enum in [`'FREE'`, `'VECTOR'`, `'ALIGNED'`, `'AUTO'`], default `'FREE'`

hide
    

Visibility status

Type:
    

boolean, default False

radius
    

Radius for beveling

Type:
    

float in [0, inf], default 0.0

select_control_point
    

Control point selection status

Type:
    

boolean, default False

select_left_handle
    

Handle 1 selection status

Type:
    

boolean, default False

select_right_handle
    

Handle 2 selection status

Type:
    

boolean, default False

tilt
    

Tilt in 3D View

Type:
    

float in [-376.991, 376.991], default 0.0

weight_softbody
    

Softbody goal weight

Type:
    

float in [0.01, 100], default 0.0

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

  * [[Spline.bezier_points]]

| 


  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
