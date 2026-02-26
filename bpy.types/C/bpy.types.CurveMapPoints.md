# CurveMapPoints(bpy_struct)

base class — [[bpy_struct]]

_class _bpy.types.CurveMapPoints(_bpy_struct_)
    

Collection of Curve Map Points

new(_position_ , _value_)
    

Add point to CurveMap

Parameters:
    

  * **position** (_float in_ _[__-inf_ _,__inf_ _]_) – Position, Position to add point

  * **value** (_float in_ _[__-inf_ _,__inf_ _]_) – Value, Value of point


Returns:
    

New point

Return type:
    

[[CurveMapPoint]]

remove(_point_)
    

Delete point from CurveMap

Parameters:
    

**point** ([[CurveMapPoint]], (never None)) – PointElement to remove

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

  * [[CurveMap.points]]

| 


  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
