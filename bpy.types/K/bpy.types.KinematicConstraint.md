# KinematicConstraint(Constraint)

base classes — [`bpy_struct`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct "bpy.types.bpy_struct"), [`Constraint`](../C/bpy.types.Constraint.md#bpy.types.Constraint "bpy.types.Constraint")

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
    

[`Object`](../O/bpy.types.Object.md#bpy.types.Object "bpy.types.Object")

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
    

[`Object`](../O/bpy.types.Object.md#bpy.types.Object "bpy.types.Object")

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
    

[`bpy.types.Struct`](../S/bpy.types.Struct.md#bpy.types.Struct "bpy.types.Struct") subclass

_classmethod _bl_rna_get_subclass_py(_id_ , _default =None_, _/_)
    

Parameters:
    

**id** (_str_) – The RNA type identifier.

Returns:
    

The class or default when not found.

Return type:
    

type

## Inherited Properties

  * [`bpy_struct.id_data`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.id_data "bpy.types.bpy_struct.id_data")
  * [`Constraint.name`](../C/bpy.types.Constraint.md#bpy.types.Constraint.name "bpy.types.Constraint.name")
  * [`Constraint.type`](../C/bpy.types.Constraint.md#bpy.types.Constraint.type "bpy.types.Constraint.type")
  * [`Constraint.is_override_data`](../C/bpy.types.Constraint.md#bpy.types.Constraint.is_override_data "bpy.types.Constraint.is_override_data")
  * [`Constraint.owner_space`](../C/bpy.types.Constraint.md#bpy.types.Constraint.owner_space "bpy.types.Constraint.owner_space")
  * [`Constraint.target_space`](../C/bpy.types.Constraint.md#bpy.types.Constraint.target_space "bpy.types.Constraint.target_space")
  * [`Constraint.space_object`](../C/bpy.types.Constraint.md#bpy.types.Constraint.space_object "bpy.types.Constraint.space_object")
  * [`Constraint.space_subtarget`](../C/bpy.types.Constraint.md#bpy.types.Constraint.space_subtarget "bpy.types.Constraint.space_subtarget")

| 

  * [`Constraint.mute`](../C/bpy.types.Constraint.md#bpy.types.Constraint.mute "bpy.types.Constraint.mute")
  * [`Constraint.enabled`](../C/bpy.types.Constraint.md#bpy.types.Constraint.enabled "bpy.types.Constraint.enabled")
  * [`Constraint.show_expanded`](../C/bpy.types.Constraint.md#bpy.types.Constraint.show_expanded "bpy.types.Constraint.show_expanded")
  * [`Constraint.is_valid`](../C/bpy.types.Constraint.md#bpy.types.Constraint.is_valid "bpy.types.Constraint.is_valid")
  * [`Constraint.active`](../C/bpy.types.Constraint.md#bpy.types.Constraint.active "bpy.types.Constraint.active")
  * [`Constraint.influence`](../C/bpy.types.Constraint.md#bpy.types.Constraint.influence "bpy.types.Constraint.influence")
  * [`Constraint.error_location`](../C/bpy.types.Constraint.md#bpy.types.Constraint.error_location "bpy.types.Constraint.error_location")
  * [`Constraint.error_rotation`](../C/bpy.types.Constraint.md#bpy.types.Constraint.error_rotation "bpy.types.Constraint.error_rotation")

  
---|---  
  
## Inherited Functions

  * [`bpy_struct.as_pointer`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.as_pointer "bpy.types.bpy_struct.as_pointer")
  * [`bpy_struct.driver_add`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.driver_add "bpy.types.bpy_struct.driver_add")
  * [`bpy_struct.driver_remove`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.driver_remove "bpy.types.bpy_struct.driver_remove")
  * [`bpy_struct.get`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.get "bpy.types.bpy_struct.get")
  * [`bpy_struct.id_properties_clear`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.id_properties_clear "bpy.types.bpy_struct.id_properties_clear")
  * [`bpy_struct.id_properties_ensure`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.id_properties_ensure "bpy.types.bpy_struct.id_properties_ensure")
  * [`bpy_struct.id_properties_ui`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.id_properties_ui "bpy.types.bpy_struct.id_properties_ui")
  * [`bpy_struct.is_property_hidden`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.is_property_hidden "bpy.types.bpy_struct.is_property_hidden")
  * [`bpy_struct.is_property_overridable_library`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.is_property_overridable_library "bpy.types.bpy_struct.is_property_overridable_library")
  * [`bpy_struct.is_property_readonly`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.is_property_readonly "bpy.types.bpy_struct.is_property_readonly")
  * [`bpy_struct.is_property_set`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.is_property_set "bpy.types.bpy_struct.is_property_set")
  * [`bpy_struct.items`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.items "bpy.types.bpy_struct.items")
  * [`bpy_struct.keyframe_delete`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.keyframe_delete "bpy.types.bpy_struct.keyframe_delete")

| 

  * [`bpy_struct.keyframe_insert`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.keyframe_insert "bpy.types.bpy_struct.keyframe_insert")
  * [`bpy_struct.keys`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.keys "bpy.types.bpy_struct.keys")
  * [`bpy_struct.path_from_id`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.path_from_id "bpy.types.bpy_struct.path_from_id")
  * [`bpy_struct.path_from_module`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.path_from_module "bpy.types.bpy_struct.path_from_module")
  * [`bpy_struct.path_resolve`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.path_resolve "bpy.types.bpy_struct.path_resolve")
  * [`bpy_struct.pop`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.pop "bpy.types.bpy_struct.pop")
  * [`bpy_struct.property_overridable_library_set`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.property_overridable_library_set "bpy.types.bpy_struct.property_overridable_library_set")
  * [`bpy_struct.property_unset`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.property_unset "bpy.types.bpy_struct.property_unset")
  * [`bpy_struct.rna_ancestors`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.rna_ancestors "bpy.types.bpy_struct.rna_ancestors")
  * [`bpy_struct.type_recast`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.type_recast "bpy.types.bpy_struct.type_recast")
  * [`bpy_struct.values`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.values "bpy.types.bpy_struct.values")
  * [`Constraint.bl_rna_get_subclass`](../C/bpy.types.Constraint.md#bpy.types.Constraint.bl_rna_get_subclass "bpy.types.Constraint.bl_rna_get_subclass")
  * [`Constraint.bl_rna_get_subclass_py`](../C/bpy.types.Constraint.md#bpy.types.Constraint.bl_rna_get_subclass_py "bpy.types.Constraint.bl_rna_get_subclass_py")

  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
