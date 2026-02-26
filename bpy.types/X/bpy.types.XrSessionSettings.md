# XrSessionSettings(bpy_struct)

base class — [[bpy_struct]]

_class _bpy.types.XrSessionSettings(_bpy_struct_)
    

base_pose_angle
    

Rotation angle around the Z-Axis to apply the rotation deltas from the VR headset to

Type:
    

float in [-inf, inf], default 0.0

base_pose_location
    

Coordinates to apply translation deltas from the VR headset to

Type:
    

[[mathutils.Vector]] of 3 items in [-inf, inf], default (0.0, 0.0, 0.0)

base_pose_object
    

Object to take the location and rotation to which translation and rotation deltas from the VR headset will be applied to

Type:
    

[[Object]]

base_pose_type
    

Define where the location and rotation for the VR view come from, to which translation and rotation deltas from the VR headset will be applied to

  * `SCENE_CAMERA` Scene Camera – Follow the active scene camera to define the VR view’s base pose.

  * `OBJECT` Object – Follow the transformation of an object to define the VR view’s base pose.

  * `CUSTOM` Custom – Follow a custom transformation to define the VR view’s base pose.


Type:
    

enum in [`'SCENE_CAMERA'`, `'OBJECT'`, `'CUSTOM'`], default `'SCENE_CAMERA'`

base_scale
    

Uniform scale to apply to VR view

Type:
    

float in [1e-06, inf], default 1.0

clip_end
    

VR viewport far clipping distance

Type:
    

float in [1e-06, inf], default 0.0

clip_start
    

VR viewport near clipping distance

Type:
    

float in [1e-06, inf], default 0.0

controller_draw_style
    

Style to use when drawing VR controllers

  * `DARK` Dark – Draw dark controller.

  * `LIGHT` Light – Draw light controller.

  * `DARK_RAY` Dark + Ray – Draw dark controller with aiming axis ray.

  * `LIGHT_RAY` Light + Ray – Draw light controller with aiming axis ray.


Type:
    

enum in [`'DARK'`, `'LIGHT'`, `'DARK_RAY'`, `'LIGHT_RAY'`], default `'DARK'`

fly_speed
    

Fly speed in meters per second

Type:
    

float in [1e-06, inf], default 0.0

icon_from_show_object_viewport
    

Type:
    

int in [-inf, inf], default 0, (readonly)

shading
    

Type:
    

[[View3DShading]], (readonly, never None)

show_annotation
    

Show annotations for this view

Type:
    

boolean, default False

show_controllers
    

Show VR controllers (requires VR actions for controller poses)

Type:
    

boolean, default False

show_custom_overlays
    

Show custom VR overlays

Type:
    

boolean, default False

show_floor
    

Show the ground plane grid

Type:
    

boolean, default False

show_object_extras
    

Show object extras, including empties, lights, and cameras

Type:
    

boolean, default False

show_object_select_armature
    

Allow selection of armatures

Type:
    

boolean, default False

show_object_select_camera
    

Allow selection of cameras

Type:
    

boolean, default False

show_object_select_curve
    

Allow selection of curves

Type:
    

boolean, default False

show_object_select_curves
    

Allow selection of hair curves

Type:
    

boolean, default False

show_object_select_empty
    

Allow selection of empties

Type:
    

boolean, default False

show_object_select_font
    

Allow selection of text objects

Type:
    

boolean, default False

show_object_select_grease_pencil
    

Allow selection of Grease Pencil objects

Type:
    

boolean, default False

show_object_select_lattice
    

Allow selection of lattices

Type:
    

boolean, default False

show_object_select_light
    

Allow selection of lights

Type:
    

boolean, default False

show_object_select_light_probe
    

Allow selection of light probes

Type:
    

boolean, default False

show_object_select_mesh
    

Allow selection of mesh objects

Type:
    

boolean, default False

show_object_select_meta
    

Allow selection of metaballs

Type:
    

boolean, default False

show_object_select_pointcloud
    

Allow selection of point clouds

Type:
    

boolean, default False

show_object_select_speaker
    

Allow selection of speakers

Type:
    

boolean, default False

show_object_select_surf
    

Allow selection of surfaces

Type:
    

boolean, default False

show_object_select_volume
    

Allow selection of volumes

Type:
    

boolean, default False

show_object_viewport_armature
    

Show armatures

Type:
    

boolean, default False

show_object_viewport_camera
    

Show cameras

Type:
    

boolean, default False

show_object_viewport_curve
    

Show curves

Type:
    

boolean, default False

show_object_viewport_curves
    

Show hair curves

Type:
    

boolean, default False

show_object_viewport_empty
    

Show empties

Type:
    

boolean, default False

show_object_viewport_font
    

Show text objects

Type:
    

boolean, default False

show_object_viewport_grease_pencil
    

Show Grease Pencil objects

Type:
    

boolean, default False

show_object_viewport_lattice
    

Show lattices

Type:
    

boolean, default False

show_object_viewport_light
    

Show lights

Type:
    

boolean, default False

show_object_viewport_light_probe
    

Show light probes

Type:
    

boolean, default False

show_object_viewport_mesh
    

Show mesh objects

Type:
    

boolean, default False

show_object_viewport_meta
    

Show metaballs

Type:
    

boolean, default False

show_object_viewport_pointcloud
    

Show point clouds

Type:
    

boolean, default False

show_object_viewport_speaker
    

Show speakers

Type:
    

boolean, default False

show_object_viewport_surf
    

Show surfaces

Type:
    

boolean, default False

show_object_viewport_volume
    

Show volumes

Type:
    

boolean, default False

show_passthrough
    

Show the passthrough view

Type:
    

boolean, default False

show_selection
    

Show selection outlines

Type:
    

boolean, default False

use_absolute_tracking
    

Allow the VR tracking origin to be defined independently of the headset location

Type:
    

boolean, default False

use_positional_tracking
    

Allow VR headsets to affect the location in virtual space, in addition to the rotation

Type:
    

boolean, default False

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

  * [[WindowManager.xr_session_settings]]

| 


  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
