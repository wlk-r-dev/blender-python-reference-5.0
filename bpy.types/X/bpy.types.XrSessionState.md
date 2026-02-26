# XrSessionState(bpy_struct)

base class — [[bpy_struct]]

_class _bpy.types.XrSessionState(_bpy_struct_)
    

Runtime state information about the VR session

actionmaps
    

Type:
    

[[XrActionMaps]] [[bpy_prop_collection]] of [[XrActionMap]], (readonly)

active_actionmap
    

Type:
    

int in [-inf, inf], default 0

navigation_location
    

Location offset to apply to base pose when determining viewer location

Type:
    

[[mathutils.Vector]] of 3 items in [-inf, inf], default (0.0, 0.0, 0.0)

navigation_rotation
    

Rotation offset to apply to base pose when determining viewer rotation

Type:
    

[[mathutils.Quaternion]] rotation of 4 items in [-inf, inf], default (0.0, 0.0, 0.0, 0.0)

navigation_scale
    

Additional scale multiplier to apply to base scale when determining viewer scale

Type:
    

float in [-inf, inf], default 0.0

selected_actionmap
    

Type:
    

int in [-inf, inf], default 0

viewer_pose_location
    

Last known location of the viewer pose (center between the eyes) in world space

Type:
    

[[mathutils.Vector]] of 3 items in [-inf, inf], default (0.0, 0.0, 0.0), (readonly)

viewer_pose_rotation
    

Last known rotation of the viewer pose (center between the eyes) in world space

Type:
    

[[mathutils.Quaternion]] rotation of 4 items in [-inf, inf], default (0.0, 0.0, 0.0, 0.0), (readonly)

_classmethod _is_running(_context_)
    

Query if the VR session is currently running

Returns:
    

Result

Return type:
    

boolean

_classmethod _reset_to_base_pose(_context_)
    

Force resetting of position and rotation deltas

_classmethod _action_set_create(_context_ , _actionmap_)
    

Create a VR action set

Returns:
    

Result

Return type:
    

boolean

_classmethod _action_create(_context_ , _actionmap_ , _actionmap_item_)
    

Create a VR action

Returns:
    

Result

Return type:
    

boolean

_classmethod _action_binding_create(_context_ , _actionmap_ , _actionmap_item_ , _actionmap_binding_)
    

Create a VR action binding

Returns:
    

Result

Return type:
    

boolean

_classmethod _active_action_set_set(_context_ , _action_set_)
    

Set the active VR action set

Parameters:
    

**action_set** (_string_ _,__(__never None_ _)_) – Action Set, Action set name

Returns:
    

Result

Return type:
    

boolean

_classmethod _controller_pose_actions_set(_context_ , _action_set_ , _grip_action_ , _aim_action_)
    

Set the actions that determine the VR controller poses

Parameters:
    

  * **action_set** (_string_ _,__(__never None_ _)_) – Action Set, Action set name

  * **grip_action** (_string_ _,__(__never None_ _)_) – Grip Action, Name of the action representing the controller grips

  * **aim_action** (_string_ _,__(__never None_ _)_) – Aim Action, Name of the action representing the controller aims


Returns:
    

Result

Return type:
    

boolean

_classmethod _action_state_get(_context_ , _action_set_name_ , _action_name_ , _user_path_)
    

Get the current state of a VR action

Parameters:
    

  * **action_set_name** (_string_ _,__(__never None_ _)_) – Action Set, Action set name

  * **action_name** (_string_ _,__(__never None_ _)_) – Action, Action name

  * **user_path** (_string_ _,__(__never None_ _)_) – User Path, OpenXR user path


Returns:
    

Action State, Current state of the VR action. Second float value is only set for 2D vector type actions.

Return type:
    

float array of 2 items in [-inf, inf], (never None)

_classmethod _haptic_action_apply(_context_ , _action_set_name_ , _action_name_ , _user_path_ , _duration_ , _frequency_ , _amplitude_)
    

Apply a VR haptic action

Parameters:
    

  * **action_set_name** (_string_ _,__(__never None_ _)_) – Action Set, Action set name

  * **action_name** (_string_ _,__(__never None_ _)_) – Action, Action name

  * **user_path** (_string_ _,__(__never None_ _)_) – User Path, Optional OpenXR user path. If not set, the action will be applied to all paths.

  * **duration** (_float in_ _[__0_ _,__inf_ _]_) – Duration, Haptic duration in seconds. 0.0 is the minimum supported duration.

  * **frequency** (_float in_ _[__0_ _,__inf_ _]_) – Frequency, Frequency of the haptic vibration in hertz. 0.0 specifies the OpenXR runtime’s default frequency.

  * **amplitude** (_float in_ _[__0_ _,__1_ _]_) – Amplitude, Haptic amplitude, ranging from 0.0 to 1.0


Returns:
    

Result

Return type:
    

boolean

_classmethod _haptic_action_stop(_context_ , _action_set_name_ , _action_name_ , _user_path_)
    

Stop a VR haptic action

Parameters:
    

  * **action_set_name** (_string_ _,__(__never None_ _)_) – Action Set, Action set name

  * **action_name** (_string_ _,__(__never None_ _)_) – Action, Action name

  * **user_path** (_string_ _,__(__never None_ _)_) – User Path, Optional OpenXR user path. If not set, the action will be stopped for all paths.


_classmethod _controller_grip_location_get(_context_ , _index_)
    

Get the last known controller grip location in world space

Parameters:
    

**index** (_int in_ _[__0_ _,__255_ _]_) – Index, Controller index

Returns:
    

Location, Controller grip location

Return type:
    

[[mathutils.Vector]] of 3 items in [-inf, inf], (never None)

_classmethod _controller_grip_rotation_get(_context_ , _index_)
    

Get the last known controller grip rotation (quaternion) in world space

Parameters:
    

**index** (_int in_ _[__0_ _,__255_ _]_) – Index, Controller index

Returns:
    

Rotation, Controller grip quaternion rotation

Return type:
    

[[mathutils.Quaternion]] rotation of 4 items in [-inf, inf], (never None)

_classmethod _controller_aim_location_get(_context_ , _index_)
    

Get the last known controller aim location in world space

Parameters:
    

**index** (_int in_ _[__0_ _,__255_ _]_) – Index, Controller index

Returns:
    

Location, Controller aim location

Return type:
    

[[mathutils.Vector]] of 3 items in [-inf, inf], (never None)

_classmethod _controller_aim_rotation_get(_context_ , _index_)
    

Get the last known controller aim rotation (quaternion) in world space

Parameters:
    

**index** (_int in_ _[__0_ _,__255_ _]_) – Index, Controller index

Returns:
    

Rotation, Controller aim quaternion rotation

Return type:
    

[[mathutils.Quaternion]] rotation of 4 items in [-inf, inf], (never None)

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

  * [[WindowManager.xr_session_state]]
  * [[XrActionMaps.find]]
  * [[XrActionMaps.new]]

| 

  * [[XrActionMaps.new_from_actionmap]]
  * [[XrActionMaps.remove]]

  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
