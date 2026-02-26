# XrEventData(bpy_struct)

base class — [[bpy_struct]]

_class _bpy.types.XrEventData(_bpy_struct_)
    

XR Data for Window Manager Event

action
    

XR action name

Type:
    

string, default “”, (readonly, never None)

action_set
    

XR action set name

Type:
    

string, default “”, (readonly, never None)

bimanual
    

Whether bimanual interaction is occurring

Type:
    

boolean, default False, (readonly)

controller_location
    

Location of the action’s corresponding controller aim in world space

Type:
    

[[mathutils.Vector]] of 3 items in [-inf, inf], default (0.0, 0.0, 0.0), (readonly)

controller_location_other
    

Controller aim location of the other user path for bimanual actions

Type:
    

[[mathutils.Vector]] of 3 items in [-inf, inf], default (0.0, 0.0, 0.0), (readonly)

controller_rotation
    

Rotation of the action’s corresponding controller aim in world space

Type:
    

[[mathutils.Quaternion]] rotation of 4 items in [-inf, inf], default (0.0, 0.0, 0.0, 0.0), (readonly)

controller_rotation_other
    

Controller aim rotation of the other user path for bimanual actions

Type:
    

[[mathutils.Quaternion]] rotation of 4 items in [-inf, inf], default (0.0, 0.0, 0.0, 0.0), (readonly)

float_threshold
    

Input threshold for float/2D vector actions

Type:
    

float in [-inf, inf], default 0.0, (readonly)

state
    

XR action values corresponding to type

Type:
    

float array of 2 items in [-inf, inf], default (0.0, 0.0), (readonly)

state_other
    

State of the other user path for bimanual actions

Type:
    

float array of 2 items in [-inf, inf], default (0.0, 0.0), (readonly)

type
    

XR action type

  * `FLOAT` Float – Float action, representing either a digital or analog button.

  * `VECTOR2D` Vector2D – 2D float vector action, representing a thumbstick or trackpad.

  * `POSE` Pose – 3D pose action, representing a controller’s location and rotation.

  * `VIBRATION` Vibration – Haptic vibration output action, to be applied with a duration, frequency, and amplitude.


Type:
    

enum in [`'FLOAT'`, `'VECTOR2D'`, `'POSE'`, `'VIBRATION'`], default `'FLOAT'`, (readonly)

user_path
    

User path of the action. E.g. “/user/hand/left”

Type:
    

string, default “”, (readonly, never None)

user_path_other
    

Other user path, for bimanual actions. E.g. “/user/hand/right”

Type:
    

string, default “”, (readonly, never None)

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

  * [[Event.xr]]

| 


  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
