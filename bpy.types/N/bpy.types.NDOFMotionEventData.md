# NDOFMotionEventData(bpy_struct)

base class — [[bpy_struct]]

_class _bpy.types.NDOFMotionEventData(_bpy_struct_)
    

NDOF motion data for window manager events

progress
    

Indicates the gesture phase

Type:
    

enum in [`'STARTING'`, `'IN_PROGRESS'`, `'FINISHING'`], default `'STARTING'`, (readonly)

rotation
    

Axis-angle rotation of this motion event. The vector magnitude is the angle where 1.0 represents 360 degrees. The angle is typically scaled by the time-delta before use.

Type:
    

[[mathutils.Vector]] of 3 items in [-inf, inf], default (0.0, 0.0, 0.0), (readonly)

time_delta
    

Time since previous motion event (in seconds)

Type:
    

float in [-inf, inf], default 0.0, (readonly)

translation
    

The translation of this motion event. The range on each axis is [-1 to 1], before being multiplied by the sensitivity preference. This is typically scaled by the time-delta before use.

Type:
    

[[mathutils.Vector]] of 3 items in [-inf, inf], default (0.0, 0.0, 0.0), (readonly)

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

  * [[Event.ndof_motion]]

| 


  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
