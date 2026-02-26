# FCurveKeyframePoints(bpy_struct)

base class — [[bpy_struct]]

_class _bpy.types.FCurveKeyframePoints(_bpy_struct_)
    

Collection of keyframe points

insert(_frame_ , _value_ , _*_ , _options ={}_, _keyframe_type ='KEYFRAME'_)
    

Add a keyframe point to a F-Curve

Parameters:
    

  * **frame** (_float in_ _[__-inf_ _,__inf_ _]_) – X Value of this keyframe point

  * **value** (_float in_ _[__-inf_ _,__inf_ _]_) – Y Value of this keyframe point

  * **options** (enum set in {`'REPLACE'`, `'NEEDED'`, `'FAST'`}, (optional)) – 

Keyframe options

    * `REPLACE` Replace – Don’t add any new keyframes, but just replace existing ones.

    * `NEEDED` Needed – Only adds keyframes that are needed.

    * `FAST` Fast – Fast keyframe insertion to avoid recalculating the curve each time.

  * **keyframe_type** (enum in [Beztriple Keyframe Type Items](../../bpy_types_enum_items/beztriple_keyframe_type_items.md#rna-enum-beztriple-keyframe-type-items), (optional)) – Type of keyframe to insert


Returns:
    

Newly created keyframe

Return type:
    

[[Keyframe]]

add(_count_)
    

Add a keyframe point to a F-Curve

Parameters:
    

**count** (_int in_ _[__0_ _,__inf_ _]_) – Number, Number of points to add to the spline

remove(_keyframe_ , _*_ , _fast =False_)
    

Remove keyframe from an F-Curve

Parameters:
    

  * **keyframe** ([[Keyframe]], (never None)) – Keyframe to remove

  * **fast** (_boolean_ _,__(__optional_ _)_) – Fast, Fast keyframe removal to avoid recalculating the curve each time


clear()
    

Remove all keyframes from an F-Curve

sort()
    

Ensure all keyframe points are chronologically sorted

deduplicate()
    

Ensure there are no duplicate keys. Assumes that the points have already been sorted

handles_recalc()
    

Update handles after modifications to the keyframe points, to update things like auto-clamping

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

  * [[FCurve.keyframe_points]]

| 


  
---|---
  *[*]: Keyword-only parameters separator (PEP 3102)
  *[/]: Positional-only parameter separator (PEP 570)
