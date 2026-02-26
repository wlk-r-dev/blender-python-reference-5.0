# Pose(bpy_struct)

base class — [[bpy_struct]]

_class _bpy.types.Pose(_bpy_struct_)
    

A collection of pose channels, including settings for animating bones

animation_visualization
    

Animation data for this data-block

Type:
    

[[AnimViz]], (readonly, never None)

bones
    

Individual pose bones for the armature

Type:
    

[[bpy_prop_collection]] of [[PoseBone]], (readonly)

ik_param
    

Parameters for IK solver

Type:
    

[[IKParam]], (readonly)

ik_solver
    

Selection of IK solver for IK chain

  * `LEGACY` Standard – Original IK solver.

  * `ITASC` iTaSC – Multi constraint, stateful IK solver.


Type:
    

enum in [`'LEGACY'`, `'ITASC'`], default `'LEGACY'`

use_auto_ik
    

Add temporary IK constraints while grabbing bones in Pose Mode

Type:
    

boolean, default False

use_mirror_relative
    

Apply relative transformations in X-mirror mode (not supported with Auto IK)

Type:
    

boolean, default False

use_mirror_x
    

Apply changes to matching bone on opposite side of X-Axis

Type:
    

boolean, default False

_classmethod _apply_pose_from_action(_action_ , _*_ , _evaluation_time =0.0_)
    

Apply the given action to this pose by evaluating it at a specific time. Only updates the pose of selected bones, or all bones if none are selected.

Parameters:
    

  * **action** ([[Action]]) – Action, The Action containing the pose

  * **evaluation_time** (_float in_ _[__-inf_ _,__inf_ _]__,__(__optional_ _)_) – Evaluation Time, Time at which the given action is evaluated to obtain the pose


_classmethod _blend_pose_from_action(_action_ , _*_ , _blend_factor =1.0_, _evaluation_time =0.0_)
    

Blend the given action into this pose by evaluating it at a specific time. Only updates the pose of selected bones, or all bones if none are selected.

Parameters:
    

  * **action** ([[Action]]) – Action, The Action containing the pose

  * **blend_factor** (_float in_ _[__0_ _,__1_ _]__,__(__optional_ _)_) – Blend Factor, How much the given Action affects the final pose

  * **evaluation_time** (_float in_ _[__-inf_ _,__inf_ _]__,__(__optional_ _)_) – Evaluation Time, Time at which the given action is evaluated to obtain the pose


_classmethod _backup_create(_action_)
    

Create a backup of the current pose. Only those bones that are animated in the Action are backed up. The object owns the backup, and each object can have only one backup at a time. When you no longer need it, it must be freed use `backup_clear()`.

Parameters:
    

**action** ([[Action]]) – Action, An Action with animation data for the bones. Only the animated bones will be included in the backup.

_classmethod _backup_restore()
    

Restore the previously made pose backup. This can be called multiple times. See `Pose.backup_create()` for more info.

Returns:
    

`True` when the backup was restored, `False` if there was no backup to restore

Return type:
    

boolean

_classmethod _backup_clear()
    

Free a previously made pose backup. See `Pose.backup_create()` for more info.

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

  * [[Object.pose]]

| 


  
---|---
  *[*]: Keyword-only parameters separator (PEP 3102)
  *[/]: Positional-only parameter separator (PEP 570)
