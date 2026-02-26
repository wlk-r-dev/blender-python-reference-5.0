# Constraint(bpy_struct)

base class — [[bpy_struct]]

subclasses — [[ActionConstraint]], [[ArmatureConstraint]], [[CameraSolverConstraint]], [[ChildOfConstraint]], [[ClampToConstraint]], [[CopyLocationConstraint]], [[CopyRotationConstraint]], [[CopyScaleConstraint]], [[CopyTransformsConstraint]], [[DampedTrackConstraint]], [[FloorConstraint]], [[FollowPathConstraint]], [[FollowTrackConstraint]], [[GeometryAttributeConstraint]], [[KinematicConstraint]], [[LimitDistanceConstraint]], [[LimitLocationConstraint]], [[LimitRotationConstraint]], [[LimitScaleConstraint]], [[LockedTrackConstraint]], [[MaintainVolumeConstraint]], [[ObjectSolverConstraint]], [[PivotConstraint]], [[ShrinkwrapConstraint]], [[SplineIKConstraint]], [[StretchToConstraint]], [[TrackToConstraint]], [[TransformCacheConstraint]], [[TransformConstraint]]

_class _bpy.types.Constraint(_bpy_struct_)
    

Constraint modifying the transformation of objects and bones

active
    

Constraint is the one being edited

Type:
    

boolean, default False

enabled
    

Use the results of this constraint

Type:
    

boolean, default False

error_location
    

Amount of residual error in Blender space unit for constraints that work on position

Type:
    

float in [-inf, inf], default 0.0, (readonly)

error_rotation
    

Amount of residual error in radians for constraints that work on orientation

Type:
    

float in [-inf, inf], default 0.0, (readonly)

influence
    

Amount of influence constraint will have on the final solution

Type:
    

float in [0, 1], default 0.0

is_override_data
    

In a local override object, whether this constraint comes from the linked reference object, or is local to the override

Type:
    

boolean, default False, (readonly)

is_valid
    

Constraint has valid settings and can be evaluated

Type:
    

boolean, default False, (readonly)

mute
    

Enable/Disable Constraint

Type:
    

boolean, default False

name
    

Constraint name

Type:
    

string, default “”, (never None)

owner_space
    

Space that owner is evaluated in

  * `WORLD` World Space – The constraint is applied relative to the world coordinate system.

  * `CUSTOM` Custom Space – The constraint is applied in local space of a custom object/bone/vertex group.

  * `POSE` Pose Space – The constraint is applied in Pose Space, the object transformation is ignored.

  * `LOCAL_WITH_PARENT` Local With Parent – The constraint is applied relative to the rest pose local coordinate system of the bone, thus including the parent-induced transformation.

  * `LOCAL` Local Space – The constraint is applied relative to the local coordinate system of the object.


Type:
    

enum in [`'WORLD'`, `'CUSTOM'`, `'POSE'`, `'LOCAL_WITH_PARENT'`, `'LOCAL'`], default `'WORLD'`

show_expanded
    

Constraint’s panel is expanded in UI

Type:
    

boolean, default False

space_object
    

Object for Custom Space

Type:
    

[[Object]]

space_subtarget
    

Armature bone, mesh or lattice vertex group, …

Type:
    

string, default “”, (never None)

target_space
    

Space that target is evaluated in

  * `WORLD` World Space – The transformation of the target is evaluated relative to the world coordinate system.

  * `CUSTOM` Custom Space – The transformation of the target is evaluated relative to a custom object/bone/vertex group.

  * `POSE` Pose Space – The transformation of the target is only evaluated in the Pose Space, the target armature object transformation is ignored.

  * `LOCAL_WITH_PARENT` Local With Parent – The transformation of the target bone is evaluated relative to its rest pose local coordinate system, thus including the parent-induced transformation.

  * `LOCAL` Local Space – The transformation of the target is evaluated relative to its local coordinate system.

  * `LOCAL_OWNER_ORIENT` Local Space (Owner Orientation) – The transformation of the target bone is evaluated relative to its local coordinate system, followed by a correction for the difference in target and owner rest pose orientations. When applied as local transform to the owner produces the same global motion as the target if the parents are still in rest pose..


Type:
    

enum in [`'WORLD'`, `'CUSTOM'`, `'POSE'`, `'LOCAL_WITH_PARENT'`, `'LOCAL'`, `'LOCAL_OWNER_ORIENT'`], default `'WORLD'`

type
    

Type:
    

enum in [Constraint Type Items](../../bpy_types_enum_items/constraint_type_items.md#rna-enum-constraint-type-items), default `'CAMERA_SOLVER'`, (readonly)

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

  * [[Object.constraints]]
  * [[ObjectConstraints.active]]
  * [[ObjectConstraints.copy]]
  * [[ObjectConstraints.copy]]
  * [[ObjectConstraints.new]]
  * [[ObjectConstraints.remove]]
  * [[Panel.custom_data]]

| 

  * [[PoseBone.constraints]]
  * [[PoseBoneConstraints.active]]
  * [[PoseBoneConstraints.copy]]
  * [[PoseBoneConstraints.copy]]
  * [[PoseBoneConstraints.new]]
  * [[PoseBoneConstraints.remove]]
  * [[UILayout.template_constraint_header]]

  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
