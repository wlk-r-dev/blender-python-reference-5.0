# MaskSpline(bpy_struct)

base class — [[bpy_struct]]

_class _bpy.types.MaskSpline(_bpy_struct_)
    

Single spline used for defining mask shape

offset_mode
    

The method used for calculating the feather offset

  * `EVEN` Even – Calculate even feather offset.

  * `SMOOTH` Smooth – Calculate feather offset as a second curve.


Type:
    

enum in [`'EVEN'`, `'SMOOTH'`], default `'EVEN'`

points
    

Collection of points

Type:
    

[[MaskSplinePoints]] [[bpy_prop_collection]] of [[MaskSplinePoint]], (readonly)

use_cyclic
    

Make this spline a closed loop

Type:
    

boolean, default False

use_fill
    

Make this spline filled

Type:
    

boolean, default False

use_self_intersection_check
    

Prevent feather from self-intersections

Type:
    

boolean, default False

weight_interpolation
    

The type of weight interpolation for spline

Type:
    

enum in [`'LINEAR'`, `'EASE'`], default `'LINEAR'`

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

  * [[MaskLayer.splines]]
  * [[MaskSplines.active]]

| 

  * [[MaskSplines.new]]
  * [[MaskSplines.remove]]

  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
