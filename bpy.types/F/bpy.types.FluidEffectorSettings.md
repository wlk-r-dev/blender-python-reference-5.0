# FluidEffectorSettings(bpy_struct)

base class — [[bpy_struct]]

_class _bpy.types.FluidEffectorSettings(_bpy_struct_)
    

Smoke collision settings

effector_type
    

Change type of effector in the simulation

  * `COLLISION` Collision – Create collision object.

  * `GUIDE` Guide – Create guide object.


Type:
    

enum in [`'COLLISION'`, `'GUIDE'`], default `'COLLISION'`

guide_mode
    

How to create guiding velocities

  * `MAXIMUM` Maximize – Compare velocities from previous frame with new velocities from current frame and keep the maximum.

  * `MINIMUM` Minimize – Compare velocities from previous frame with new velocities from current frame and keep the minimum.

  * `OVERRIDE` Override – Always write new guide velocities for every frame (each frame only contains current velocities from guiding objects).

  * `AVERAGED` Averaged – Take average of velocities from previous frame and new velocities from current frame.


Type:
    

enum in [`'MAXIMUM'`, `'MINIMUM'`, `'OVERRIDE'`, `'AVERAGED'`], default `'OVERRIDE'`

subframes
    

Number of additional samples to take between frames to improve quality of fast moving effector objects

Type:
    

int in [0, 200], default 0

surface_distance
    

Additional distance around mesh surface to consider as effector

Type:
    

float in [0, 10], default 0.0

use_effector
    

Control when to apply the effector

Type:
    

boolean, default True

use_plane_init
    

Treat this object as a planar, unclosed mesh

Type:
    

boolean, default False

velocity_factor
    

Multiplier of obstacle velocity

Type:
    

float in [-100, 100], default 1.0

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

  * [[FluidModifier.effector_settings]]

| 


  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
