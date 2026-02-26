# XrActionMapItem(bpy_struct)

base class — [[bpy_struct]]

_class _bpy.types.XrActionMapItem(_bpy_struct_)
    

bimanual
    

The action depends on the states/poses of both user paths

Type:
    

boolean, default False

bindings
    

Bindings for the action map item, mapping the action to an XR input

Type:
    

[[XrActionMapBindings]] [[bpy_prop_collection]] of [[XrActionMapBinding]], (readonly)

haptic_amplitude
    

Intensity of the haptic vibration, ranging from 0.0 to 1.0

Type:
    

float in [0, 1], default 0.0

haptic_duration
    

Haptic duration in seconds. 0.0 is the minimum supported duration.

Type:
    

float in [0, inf], default 0.0

haptic_frequency
    

Frequency of the haptic vibration in hertz. 0.0 specifies the OpenXR runtime’s default frequency.

Type:
    

float in [0, inf], default 0.0

haptic_match_user_paths
    

Apply haptics to the same user paths for the haptic action and this action

Type:
    

boolean, default False

haptic_mode
    

Haptic application mode

  * `PRESS` Press – Apply haptics on button press.

  * `RELEASE` Release – Apply haptics on button release.

  * `PRESS_RELEASE` Press Release – Apply haptics on button press and release.

  * `REPEAT` Repeat – Apply haptics repeatedly for the duration of the button press.


Type:
    

enum in [`'PRESS'`, `'RELEASE'`, `'PRESS_RELEASE'`, `'REPEAT'`], default `'PRESS'`

haptic_name
    

Name of the haptic action to apply when executing this action

Type:
    

string, default “”, (never None)

name
    

Name of the action map item

Type:
    

string, default “”, (never None)

op
    

Identifier of operator to call on action event

Type:
    

string, default “”, (never None)

op_mode
    

Operator execution mode

  * `PRESS` Press – Execute operator on button press (non-modal operators only).

  * `RELEASE` Release – Execute operator on button release (non-modal operators only).

  * `MODAL` Modal – Use modal execution (modal operators only).


Type:
    

enum in [`'PRESS'`, `'RELEASE'`, `'MODAL'`], default `'PRESS'`

op_name
    

Name of operator (translated) to call on action event

Type:
    

string, default “”, (readonly, never None)

op_properties
    

Properties to set when the operator is called

Type:
    

[[OperatorProperties]], (readonly)

pose_is_controller_aim
    

The action poses will be used for the VR controller aims

Type:
    

boolean, default False

pose_is_controller_grip
    

The action poses will be used for the VR controller grips

Type:
    

boolean, default False

selected_binding
    

Currently selected binding

Type:
    

int in [-32768, 32767], default 0

type
    

Action type

  * `FLOAT` Float – Float action, representing either a digital or analog button.

  * `VECTOR2D` Vector2D – 2D float vector action, representing a thumbstick or trackpad.

  * `POSE` Pose – 3D pose action, representing a controller’s location and rotation.

  * `VIBRATION` Vibration – Haptic vibration output action, to be applied with a duration, frequency, and amplitude.


Type:
    

enum in [`'FLOAT'`, `'VECTOR2D'`, `'POSE'`, `'VIBRATION'`], default `'FLOAT'`

user_paths
    

OpenXR user paths

Type:
    

[[XrUserPaths]] [[bpy_prop_collection]] of [[XrUserPath]], (readonly)

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

  * [[XrActionMap.actionmap_items]]
  * [[XrActionMapItems.find]]
  * [[XrActionMapItems.new]]
  * [[XrActionMapItems.new_from_item]]

| 

  * [[XrActionMapItems.new_from_item]]
  * [[XrActionMapItems.remove]]
  * [[XrSessionState.action_binding_create]]
  * [[XrSessionState.action_create]]

  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
