# PoseBone(bpy_struct)

base class — [`bpy_struct`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct "bpy.types.bpy_struct")

_class _bpy.types.PoseBone(_bpy_struct_)
    

Channel defining pose data for a bone in a Pose

bbone_curveinx
    

X-axis handle offset for start of the B-Bone’s curve, adjusts curvature

Type:
    

float in [-inf, inf], default 0.0

bbone_curveinz
    

Z-axis handle offset for start of the B-Bone’s curve, adjusts curvature

Type:
    

float in [-inf, inf], default 0.0

bbone_curveoutx
    

X-axis handle offset for end of the B-Bone’s curve, adjusts curvature

Type:
    

float in [-inf, inf], default 0.0

bbone_curveoutz
    

Z-axis handle offset for end of the B-Bone’s curve, adjusts curvature

Type:
    

float in [-inf, inf], default 0.0

bbone_custom_handle_end
    

Bone that serves as the end handle for the B-Bone curve

Type:
    

`PoseBone`, (readonly)

bbone_custom_handle_start
    

Bone that serves as the start handle for the B-Bone curve

Type:
    

`PoseBone`, (readonly)

bbone_easein
    

Length of first Bézier Handle (for B-Bones only)

Type:
    

float in [-inf, inf], default 0.0

bbone_easeout
    

Length of second Bézier Handle (for B-Bones only)

Type:
    

float in [-inf, inf], default 0.0

bbone_rollin
    

Roll offset for the start of the B-Bone, adjusts twist

Type:
    

float in [-inf, inf], default 0.0

bbone_rollout
    

Roll offset for the end of the B-Bone, adjusts twist

Type:
    

float in [-inf, inf], default 0.0

bbone_scalein
    

Scale factors for the start of the B-Bone, adjusts thickness (for tapering effects)

Type:
    

[`mathutils.Vector`](mathutils.md#mathutils.Vector "mathutils.Vector") of 3 items in [-inf, inf], default (1.0, 1.0, 1.0)

bbone_scaleout
    

Scale factors for the end of the B-Bone, adjusts thickness (for tapering effects)

Type:
    

[`mathutils.Vector`](mathutils.md#mathutils.Vector "mathutils.Vector") of 3 items in [-inf, inf], default (1.0, 1.0, 1.0)

bone
    

Bone associated with this PoseBone

Type:
    

[`Bone`](../B/bpy.types.Bone.md#bpy.types.Bone "bpy.types.Bone"), (readonly, never None)

child
    

Child of this pose bone

Type:
    

`PoseBone`, (readonly)

color
    

Type:
    

[`BoneColor`](../B/bpy.types.BoneColor.md#bpy.types.BoneColor "bpy.types.BoneColor"), (readonly)

constraints
    

Constraints that act on this pose channel

Type:
    

[`PoseBoneConstraints`](bpy.types.PoseBoneConstraints.md#bpy.types.PoseBoneConstraints "bpy.types.PoseBoneConstraints") [`bpy_prop_collection`](../_other/bpy.types.bpy_prop_collection.md#bpy.types.bpy_prop_collection "bpy.types.bpy_prop_collection") of [`Constraint`](../C/bpy.types.Constraint.md#bpy.types.Constraint "bpy.types.Constraint"), (readonly)

custom_shape
    

Object that defines custom display shape for this bone

Type:
    

[`Object`](../O/bpy.types.Object.md#bpy.types.Object "bpy.types.Object")

custom_shape_rotation_euler
    

Adjust the rotation of the custom shape

Type:
    

[`mathutils.Euler`](mathutils.md#mathutils.Euler "mathutils.Euler") rotation of 3 items in [-inf, inf], default (0.0, 0.0, 0.0)

custom_shape_scale_xyz
    

Adjust the size of the custom shape

Type:
    

[`mathutils.Vector`](mathutils.md#mathutils.Vector "mathutils.Vector") of 3 items in [-inf, inf], default (1.0, 1.0, 1.0)

custom_shape_transform
    

Bone that defines the display transform of this custom shape

Type:
    

`PoseBone`

custom_shape_translation
    

Adjust the location of the custom shape

Type:
    

[`mathutils.Vector`](mathutils.md#mathutils.Vector "mathutils.Vector") of 3 items in [-inf, inf], default (0.0, 0.0, 0.0)

custom_shape_wire_width
    

Adjust the line thickness of custom shapes

Type:
    

float in [1, 16], default 0.0

head
    

Location of head of the channel’s bone

Type:
    

[`mathutils.Vector`](mathutils.md#mathutils.Vector "mathutils.Vector") of 3 items in [-inf, inf], default (0.0, 0.0, 0.0), (readonly)

hide
    

Bone is not visible except for Edit Mode

Type:
    

boolean, default False

ik_linear_weight
    

Weight of scale constraint for IK

Type:
    

float in [0, 1], default 0.0

ik_max_x
    

Maximum angles for IK Limit

Type:
    

float in [0, 3.14159], default 0.0

ik_max_y
    

Maximum angles for IK Limit

Type:
    

float in [0, 3.14159], default 0.0

ik_max_z
    

Maximum angles for IK Limit

Type:
    

float in [0, 3.14159], default 0.0

ik_min_x
    

Minimum angles for IK Limit

Type:
    

float in [-3.14159, 0], default 0.0

ik_min_y
    

Minimum angles for IK Limit

Type:
    

float in [-3.14159, 0], default 0.0

ik_min_z
    

Minimum angles for IK Limit

Type:
    

float in [-3.14159, 0], default 0.0

ik_rotation_weight
    

Weight of rotation constraint for IK

Type:
    

float in [0, 1], default 0.0

ik_stiffness_x
    

IK stiffness around the X axis

Type:
    

float in [0, 0.99], default 0.0

ik_stiffness_y
    

IK stiffness around the Y axis

Type:
    

float in [0, 0.99], default 0.0

ik_stiffness_z
    

IK stiffness around the Z axis

Type:
    

float in [0, 0.99], default 0.0

ik_stretch
    

Allow scaling of the bone for IK

Type:
    

float in [0, 1], default 0.0

is_in_ik_chain
    

Is part of an IK chain

Type:
    

boolean, default False, (readonly)

length
    

Length of the bone

Type:
    

float in [-inf, inf], default 0.0, (readonly)

location
    

Type:
    

[`mathutils.Vector`](mathutils.md#mathutils.Vector "mathutils.Vector") of 3 items in [-inf, inf], default (0.0, 0.0, 0.0)

lock_ik_x
    

Disallow movement around the X axis

Type:
    

boolean, default False

lock_ik_y
    

Disallow movement around the Y axis

Type:
    

boolean, default False

lock_ik_z
    

Disallow movement around the Z axis

Type:
    

boolean, default False

lock_location
    

Lock editing of location when transforming

Type:
    

boolean array of 3 items, default (False, False, False)

lock_rotation
    

Lock editing of rotation when transforming

Type:
    

boolean array of 3 items, default (False, False, False)

lock_rotation_w
    

Lock editing of ‘angle’ component of four-component rotations when transforming

Type:
    

boolean, default False

lock_rotations_4d
    

Lock editing of four component rotations by components (instead of as Eulers)

Type:
    

boolean, default False

lock_scale
    

Lock editing of scale when transforming

Type:
    

boolean array of 3 items, default (False, False, False)

matrix
    

Final 4×4 matrix after constraints and drivers are applied, in the armature object space

Type:
    

[`mathutils.Matrix`](mathutils.md#mathutils.Matrix "mathutils.Matrix") of 4 * 4 items in [-inf, inf], default ((0.0, 0.0, 0.0, 0.0), (0.0, 0.0, 0.0, 0.0), (0.0, 0.0, 0.0, 0.0), (0.0, 0.0, 0.0, 0.0))

matrix_basis
    

Alternative access to location/scale/rotation relative to the parent and own rest bone

Type:
    

[`mathutils.Matrix`](mathutils.md#mathutils.Matrix "mathutils.Matrix") of 4 * 4 items in [-inf, inf], default ((0.0, 0.0, 0.0, 0.0), (0.0, 0.0, 0.0, 0.0), (0.0, 0.0, 0.0, 0.0), (0.0, 0.0, 0.0, 0.0))

matrix_channel
    

4×4 matrix of the bone’s location/rotation/scale channels (including animation and drivers) and the effect of bone constraints

Type:
    

[`mathutils.Matrix`](mathutils.md#mathutils.Matrix "mathutils.Matrix") of 4 * 4 items in [-inf, inf], default ((0.0, 0.0, 0.0, 0.0), (0.0, 0.0, 0.0, 0.0), (0.0, 0.0, 0.0, 0.0), (0.0, 0.0, 0.0, 0.0)), (readonly)

motion_path
    

Motion Path for this element

Type:
    

[`MotionPath`](../M/bpy.types.MotionPath.md#bpy.types.MotionPath "bpy.types.MotionPath"), (readonly)

name
    

Type:
    

string, default “”, (never None)

parent
    

Parent of this pose bone

Type:
    

`PoseBone`, (readonly)

rotation_axis_angle
    

Angle of Rotation for Axis-Angle rotation representation

Type:
    

float array of 4 items in [-inf, inf], default (0.0, 0.0, 1.0, 0.0)

rotation_euler
    

Rotation in Eulers

Type:
    

[`mathutils.Euler`](mathutils.md#mathutils.Euler "mathutils.Euler") rotation of 3 items in [-inf, inf], default (0.0, 0.0, 0.0)

rotation_mode
    

The kind of rotation to apply, values from other rotation modes are not used

Type:
    

enum in [Object Rotation Mode Items](../../bpy_types_enum_items/object_rotation_mode_items.md#rna-enum-object-rotation-mode-items), default `'QUATERNION'`

rotation_quaternion
    

Rotation in Quaternions

Type:
    

[`mathutils.Quaternion`](mathutils.md#mathutils.Quaternion "mathutils.Quaternion") rotation of 4 items in [-inf, inf], default (1.0, 0.0, 0.0, 0.0)

scale
    

Type:
    

[`mathutils.Vector`](mathutils.md#mathutils.Vector "mathutils.Vector") of 3 items in [-inf, inf], default (1.0, 1.0, 1.0)

select
    

Bone is selected in Pose Mode

Type:
    

boolean, default False

tail
    

Location of tail of the channel’s bone

Type:
    

[`mathutils.Vector`](mathutils.md#mathutils.Vector "mathutils.Vector") of 3 items in [-inf, inf], default (0.0, 0.0, 0.0), (readonly)

use_custom_shape_bone_size
    

Scale the custom object by the bone length

Type:
    

boolean, default False

use_ik_limit_x
    

Limit movement around the X axis

Type:
    

boolean, default False

use_ik_limit_y
    

Limit movement around the Y axis

Type:
    

boolean, default False

use_ik_limit_z
    

Limit movement around the Z axis

Type:
    

boolean, default False

use_ik_linear_control
    

Apply channel size as IK constraint if stretching is enabled

Type:
    

boolean, default False

use_ik_rotation_control
    

Apply channel rotation as IK constraint

Type:
    

boolean, default False

use_transform_around_custom_shape
    

Transform the bone as if it was a child of the Custom Shape Transform bone. This can be useful when combining shape-key and armature deformations.

Type:
    

boolean, default False

use_transform_at_custom_shape
    

The location and orientation of the Custom Shape Transform bone will be used for transform gizmos and for other transform operators in the 3D Viewport. When disabled, the 3D Viewport will still use the actual bone transform for these, even when the custom bone shape transform is overridden.

Type:
    

boolean, default False

basename
    

The name of this bone before any `.` character.

(readonly)

center
    

The midpoint between the head and the tail.

(readonly)

children
    

(readonly)

children_recursive
    

A list of all children from this bone.

Note

Takes `O(len(bones)**2)` time.

(readonly)

children_recursive_basename
    

Returns a chain of children with the same base name as this bone. Only direct chains are supported, forks caused by multiple children with matching base names will terminate the function and not be returned.

Note

Takes `O(len(bones)**2)` time.

(readonly)

parent_recursive
    

A list of parents, starting with the immediate parent.

(readonly)

vector
    

The direction this bone is pointing. Utility function for (tail - head)

(readonly)

x_axis
    

Vector pointing down the x-axis of the bone.

(readonly)

y_axis
    

Vector pointing down the y-axis of the bone.

(readonly)

z_axis
    

Vector pointing down the z-axis of the bone.

(readonly)

bl_system_properties_get(_*_ , _do_create =False_)
    

DEBUG ONLY. Internal access to runtime-defined RNA data storage, intended solely for testing and debugging purposes. Do not access it in regular scripting work, and in particular, do not assume that it contains writable data

Parameters:
    

**do_create** (_boolean_ _,__(__optional_ _)_) – Ensure that system properties are created if they do not exist yet

Returns:
    

The system properties root container, or None if there are no system properties stored in this data yet, and its creation was not requested

Return type:
    

[`PropertyGroup`](bpy.types.PropertyGroup.md#bpy.types.PropertyGroup "bpy.types.PropertyGroup")

evaluate_envelope(_point_)
    

Calculate bone envelope at given point

Parameters:
    

**point** ([`mathutils.Vector`](mathutils.md#mathutils.Vector "mathutils.Vector") of 3 items in [-inf, inf]) – Point, Position in 3d space to evaluate

Returns:
    

Factor, Envelope factor

Return type:
    

float in [-inf, inf]

bbone_segment_index(_point_)
    

Retrieve the index and blend factor of the B-Bone segments based on vertex position

Parameters:
    

**point** ([`mathutils.Vector`](mathutils.md#mathutils.Vector "mathutils.Vector") of 3 items in [-inf, inf]) – Point, Vertex position in armature pose space

Returns:
    

`index`, The index of the first segment joint affecting the point, int in [-inf, inf]

`blend_next`, The blend factor between the given and the following joint, float in [-inf, inf]

Return type:
    

(int in [-inf, inf], float in [-inf, inf])

bbone_segment_matrix(_index_ , _*_ , _rest =False_)
    

Retrieve the matrix of the joint between B-Bone segments if available

Parameters:
    

  * **index** (_int in_ _[__0_ _,__inf_ _]_) – Index of the segment endpoint

  * **rest** (_boolean_ _,__(__optional_ _)_) – Return the rest pose matrix


Returns:
    

The resulting matrix in bone local space

Return type:
    

[`mathutils.Matrix`](mathutils.md#mathutils.Matrix "mathutils.Matrix") of 4 * 4 items in [-inf, inf]

This example shows how to use B-Bone segment matrices to emulate deformation produced by the Armature modifier or constraint when assigned to the given bone (without Preserve Volume). The coordinates are processed in armature Pose space:
    
    
    def bbone_deform_matrix(pose_bone, point):
        index, blend_next = pose_bone.bbone_segment_index(point)
    
        rest1 = pose_bone.bbone_segment_matrix(index, rest=True)
        pose1 = pose_bone.bbone_segment_matrix(index, rest=False)
        deform1 = pose1 @ rest1.inverted()
    
        # `bbone_segment_index` ensures that index + 1 is always valid
        rest2 = pose_bone.bbone_segment_matrix(index + 1, rest=True)
        pose2 = pose_bone.bbone_segment_matrix(index + 1, rest=False)
        deform2 = pose2 @ rest2.inverted()
    
        deform = deform1 * (1 - blend_next) + deform2 * blend_next
    
        return pose_bone.matrix @ deform @ pose_bone.bone.matrix_local.inverted()
    
    
    # Armature modifier deforming vertices:
    mesh = bpy.data.objects["Mesh"]
    pose_bone = bpy.data.objects["Armature"].pose.bones["Bone"]
    
    for vertex in mesh.data.vertices:
        vertex.co = bbone_deform_matrix(pose_bone, vertex.co) @ vertex.co
    
    # Armature constraint modifying an object transform:
    empty = bpy.data.objects["Empty"]
    matrix = empty.matrix_world
    
    empty.matrix_world = bbone_deform_matrix(pose_bone, matrix.translation) @ matrix
    

compute_bbone_handles(_*_ , _rest =False_, _ease =False_, _offsets =False_)
    

Retrieve the vectors and rolls coming from B-Bone custom handles

Parameters:
    

  * **rest** (_boolean_ _,__(__optional_ _)_) – Return the rest pose state

  * **ease** (_boolean_ _,__(__optional_ _)_) – Apply scale from ease values

  * **offsets** (_boolean_ _,__(__optional_ _)_) – Apply roll and curve offsets from bone properties


Returns:
    

`handle1`, The direction vector of the start handle in bone local space, [`mathutils.Vector`](mathutils.md#mathutils.Vector "mathutils.Vector") of 3 items in [-inf, inf]

`roll1`, Roll of the start handle, float in [-inf, inf]

`handle2`, The direction vector of the end handle in bone local space, [`mathutils.Vector`](mathutils.md#mathutils.Vector "mathutils.Vector") of 3 items in [-inf, inf]

`roll2`, Roll of the end handle, float in [-inf, inf]

Return type:
    

([`mathutils.Vector`](mathutils.md#mathutils.Vector "mathutils.Vector") of 3 items in [-inf, inf], float in [-inf, inf], [`mathutils.Vector`](mathutils.md#mathutils.Vector "mathutils.Vector") of 3 items in [-inf, inf], float in [-inf, inf])

parent_index(_parent_test_)
    

The same as ‘bone in other_bone.parent_recursive’ but saved generating a list.

translate(_vec_)
    

Utility function to add _vec_ to the head and tail of this bone.

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

| 


  
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

| 

  * [`bpy_struct.keyframe_delete`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.keyframe_delete "bpy.types.bpy_struct.keyframe_delete")
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

  
---|---  
  
## References

  * [`bpy.context.active_pose_bone`](../../bpy.context.md#bpy.context.active_pose_bone "bpy.context.active_pose_bone")
  * [`bpy.context.pose_bone`](../../bpy.context.md#bpy.context.pose_bone "bpy.context.pose_bone")
  * [`bpy.context.selected_pose_bones`](../../bpy.context.md#bpy.context.selected_pose_bones "bpy.context.selected_pose_bones")
  * [`bpy.context.selected_pose_bones_from_active_object`](../../bpy.context.md#bpy.context.selected_pose_bones_from_active_object "bpy.context.selected_pose_bones_from_active_object")
  * [`bpy.context.visible_pose_bones`](../../bpy.context.md#bpy.context.visible_pose_bones "bpy.context.visible_pose_bones")
  * [`Object.convert_space`](../O/bpy.types.Object.md#bpy.types.Object.convert_space "bpy.types.Object.convert_space")

| 

  * [`Pose.bones`](bpy.types.Pose.md#bpy.types.Pose.bones "bpy.types.Pose.bones")
  * `PoseBone.bbone_custom_handle_end`
  * `PoseBone.bbone_custom_handle_start`
  * `PoseBone.child`
  * `PoseBone.custom_shape_transform`
  * `PoseBone.parent`

  
---|---
  *[*]: Keyword-only parameters separator (PEP 3102)
  *[/]: Positional-only parameter separator (PEP 570)
