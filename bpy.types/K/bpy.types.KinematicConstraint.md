# KinematicConstraint(Constraint)

base classes — [[bpy_struct]], [[Constraint]]

_class _bpy.types.KinematicConstraint(_Constraint_)
    

Inverse Kinematics

chain_count
    

How many bones are included in the IK effect - 0 uses all bones

Type:
    

int in [0, 255], default 0

distance
    

Radius of limiting sphere

Type:
    

float in [0, 100], default 0.0

ik_type
    

Type:
    

enum in [`'COPY_POSE'`, `'DISTANCE'`], default `'COPY_POSE'`

iterations
    

Maximum number of solving iterations

Type:
    

int in [0, 10000], default 0

limit_mode
    

Distances in relation to sphere of influence to allow

  * `LIMITDIST_INSIDE` Inside – The object is constrained inside a virtual sphere around the target object, with a radius defined by the limit distance.

  * `LIMITDIST_OUTSIDE` Outside – The object is constrained outside a virtual sphere around the target object, with a radius defined by the limit distance.

  * `LIMITDIST_ONSURFACE` On Surface – The object is constrained on the surface of a virtual sphere around the target object, with a radius defined by the limit distance.


Type:
    

enum in [`'LIMITDIST_INSIDE'`, `'LIMITDIST_OUTSIDE'`, `'LIMITDIST_ONSURFACE'`], default `'LIMITDIST_INSIDE'`

lock_location_x
    

Constraint position along X axis

Type:
    

boolean, default False

lock_location_y
    

Constraint position along Y axis

Type:
    

boolean, default False

lock_location_z
    

Constraint position along Z axis

Type:
    

boolean, default False

lock_rotation_x
    

Constraint rotation along X axis

Type:
    

boolean, default False

lock_rotation_y
    

Constraint rotation along Y axis

Type:
    

boolean, default False

lock_rotation_z
    

Constraint rotation along Z axis

Type:
    

boolean, default False

orient_weight
    

For Tree-IK: Weight of orientation control for this target

Type:
    

float in [0.01, 1], default 0.0

pole_angle
    

Pole rotation offset

Type:
    

float in [-3.14159, 3.14159], default 0.0

pole_subtarget
    

Type:
    

string, default “”, (never None)

pole_target
    

Object for pole rotation

Type:
    

[[Object]]

reference_axis
    

Constraint axis Lock options relative to Bone or Target reference

Type:
    

enum in [`'BONE'`, `'TARGET'`], default `'BONE'`

subtarget
    

Armature bone, mesh or lattice vertex group, …

Type:
    

string, default “”, (never None)

target
    

Target object

Type:
    

[[Object]]

use_location
    

Chain follows position of target

Type:
    

boolean, default False

use_rotation
    

Chain follows rotation of target

Type:
    

boolean, default False

use_stretch
    

Enable IK Stretching

Type:
    

boolean, default False

use_tail
    

Include bone’s tail as last element in chain

Type:
    

boolean, default False

weight
    

For Tree-IK: Weight of position control for this target

Type:
    

float in [0.01, 1], default 0.0

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
  * [[Constraint.name]]
  * [[Constraint.type]]
  * [[Constraint.is_override_data]]
  * [[Constraint.owner_space]]
  * [[Constraint.target_space]]
  * [[Constraint.space_object]]
  * [[Constraint.space_subtarget]]

| 

  * [[Constraint.mute]]
  * [[Constraint.enabled]]
  * [[Constraint.show_expanded]]
  * [[Constraint.is_valid]]
  * [[Constraint.active]]
  * [[Constraint.influence]]
  * [[Constraint.error_location]]
  * [[Constraint.error_rotation]]

  
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

| 

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
  * [[Constraint.bl_rna_get_subclass]]
  * [[Constraint.bl_rna_get_subclass_py]]

  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
