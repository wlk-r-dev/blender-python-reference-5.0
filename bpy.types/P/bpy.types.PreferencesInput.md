# PreferencesInput(bpy_struct)

base class — [`bpy_struct`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct "bpy.types.bpy_struct")

_class _bpy.types.PreferencesInput(_bpy_struct_)
    

Settings for input devices

drag_threshold
    

Number of pixels to drag before a drag event is triggered for keyboard and other non mouse/tablet input (otherwise click events are detected)

Type:
    

int in [1, 255], default 30

drag_threshold_mouse
    

Number of pixels to drag before a drag event is triggered for mouse/trackpad input (otherwise click events are detected)

Type:
    

int in [1, 255], default 3

drag_threshold_tablet
    

Number of pixels to drag before a drag event is triggered for tablet input (otherwise click events are detected)

Type:
    

int in [1, 255], default 10

invert_mouse_zoom
    

Invert the axis of mouse movement for zooming

Type:
    

boolean, default False

invert_zoom_wheel
    

Swap the Mouse Wheel zoom direction

Type:
    

boolean, default False

mouse_double_click_time
    

Time/delay (in ms) for a double click

Type:
    

int in [1, 1000], default 350

mouse_emulate_3_button_modifier
    

Hold this modifier to emulate the middle mouse button

Type:
    

enum in [`'ALT'`, `'OSKEY'`], default `'ALT'`

move_threshold
    

Number of pixels to before the cursor is considered to have moved (used for cycling selected items on successive clicks)

Type:
    

int in [0, 255], default 2

navigation_mode
    

Which method to use for viewport navigation

Type:
    

enum in [Navigation Mode Items](../../bpy_types_enum_items/navigation_mode_items.md#rna-enum-navigation-mode-items), default `'WALK'`

ndof_deadzone
    

Threshold of initial movement needed from the device’s rest position

Type:
    

float in [0, 1], default 0.0

ndof_fly_helicopter
    

Device up/down directly controls the Z position of the 3D viewport

Type:
    

boolean, default False

ndof_fly_speed_auto
    

Automatically adjusts fly navigation speed based on the distance of objects near the center of the viewport, making it easier to navigate complex scenes. Speed is recalculated each time movement starts.

Type:
    

boolean, default False

ndof_lock_camera_pan_zoom
    

Pan/zoom the camera view instead of leaving the camera view when orbiting

Type:
    

boolean, default True

ndof_lock_horizon
    

Lock Horizon forces the horizon to be kept leveled as it currently is

Type:
    

boolean, default True

ndof_navigation_mode
    

3D Mouse Navigation Mode

  * `OBJECT` Object – This mode is like reaching into the screen and holding the model in your hand. Push the 3D Mouse cap left, and the model moves left. Push right and the model moves right.

  * `FLY` Fly – Enables using the 3D Mouse as if it is a camera. Push into the scene and the camera moves forward into the scene. You are entering the scene as if flying around in it. This also inverts pan & zoom for 2D views.


Type:
    

enum in [`'OBJECT'`, `'FLY'`], default `'OBJECT'`

ndof_orbit_center_auto
    

Auto sets the orbit center dynamically. When the complete model is in view, the center of volume of the whole model is used as the rotation point. When you move closer, the orbit center will be set on an object close to your center of the view.

Type:
    

boolean, default True

ndof_orbit_center_selected
    

Selected Item forces the orbit center to only take the currently selected objects into account.

Type:
    

boolean, default False

ndof_panx_invert_axis
    

Type:
    

boolean, default False

ndof_pany_invert_axis
    

Type:
    

boolean, default False

ndof_panz_invert_axis
    

Type:
    

boolean, default False

ndof_rotation_sensitivity
    

Overall sensitivity of the 3D Mouse for rotation

Type:
    

float in [0.01, 40], default 4.0

ndof_rotx_invert_axis
    

Type:
    

boolean, default False

ndof_roty_invert_axis
    

Type:
    

boolean, default False

ndof_rotz_invert_axis
    

Type:
    

boolean, default False

ndof_show_guide_orbit_axis
    

Display the center and axis during rotation

Type:
    

boolean, default False

ndof_show_guide_orbit_center
    

Display the orbit center during rotation

Type:
    

boolean, default True

ndof_translation_sensitivity
    

Overall sensitivity of the 3D Mouse for translation

Type:
    

float in [0.01, 40], default 4.0

ndof_zoom_direction
    

Which axis of the 3D Mouse cap zooms the view

  * `NDOF_ZOOM_FORWARD` Forward/Backward – Zoom by pulling the 3D Mouse cap upwards or pushing the cap downwards.

  * `NDOF_ZOOM_UP` Up/Down – Zoom by pulling the 3D Mouse cap upwards or pushing the cap downwards.


Type:
    

enum in [`'NDOF_ZOOM_FORWARD'`, `'NDOF_ZOOM_UP'`], default `'NDOF_ZOOM_FORWARD'`

pressure_softness
    

Adjusts softness of the low pressure response onset using a gamma curve

Type:
    

float in [-inf, inf], default 0.0

pressure_threshold_max
    

Raw input pressure value that is interpreted as 100% by Blender

Type:
    

float in [0, 1], default 1.0

tablet_api
    

Select the tablet API to use for pressure sensitivity (may require restarting Blender for changes to take effect)

  * `AUTOMATIC` Automatic – Automatically choose Wintab or Windows Ink depending on the device.

  * `WINDOWS_INK` Windows Ink – Use native Windows Ink API, for modern tablet and pen devices. Requires Windows 8 or newer..

  * `WINTAB` Wintab – Use Wintab driver for older tablets and Windows versions.


Type:
    

enum in [`'AUTOMATIC'`, `'WINDOWS_INK'`, `'WINTAB'`], default `'AUTOMATIC'`

touchpad_scroll_direction
    

Scroll direction (Wayland only)

  * `TRADITIONAL` Traditional – Traditional scroll direction.

  * `NATURAL` Natural – Natural scroll direction.


Type:
    

enum in [`'TRADITIONAL'`, `'NATURAL'`], default `'TRADITIONAL'`

use_auto_perspective
    

Automatically switch between orthographic and perspective when changing from top/front/side views

Type:
    

boolean, default True

use_drag_immediately
    

Moving things with a mouse drag confirms when releasing the button

Type:
    

boolean, default True

use_emulate_numpad
    

Main 1 to 0 keys act as the numpad ones (useful for laptops)

Type:
    

boolean, default False

use_mouse_continuous
    

Let the mouse wrap around the view boundaries so mouse movements are not limited by the screen size (used by transform, dragging of UI controls, etc.)

Type:
    

boolean, default True

use_mouse_depth_navigate
    

Use the depth under the mouse to improve view pan/rotate/zoom functionality

Type:
    

boolean, default False

use_mouse_emulate_3_button
    

Emulate Middle Mouse with Alt+Left Mouse

Type:
    

boolean, default False

use_multitouch_gestures
    

Use multi-touch gestures for navigation with touchpad, instead of scroll wheel emulation

Type:
    

boolean, default True

use_numeric_input_advanced
    

When entering numbers while transforming, default to advanced mode for full math expression evaluation

Type:
    

boolean, default False

use_rotate_around_active
    

Use selection as the pivot point

Type:
    

boolean, default False

use_zoom_to_mouse
    

Zoom in towards the mouse pointer’s position in the 3D view, rather than the 2D window center

Type:
    

boolean, default False

view_rotate_method
    

Orbit method in the viewport

  * `TURNTABLE` Turntable – Turntable keeps the Z-axis upright while orbiting.

  * `TRACKBALL` Trackball – Trackball allows you to tumble your view at any angle.


Type:
    

enum in [`'TURNTABLE'`, `'TRACKBALL'`], default `'TURNTABLE'`

view_rotate_sensitivity_trackball
    

Scale trackball orbit sensitivity

Type:
    

float in [0.1, 10], default 1.0

view_rotate_sensitivity_turntable
    

Rotation amount per pixel to control how fast the viewport orbits

Type:
    

float in [1.74533e-05, 0.261799], default 0.00698132

view_zoom_axis
    

Axis of mouse movement to zoom in or out on

  * `VERTICAL` Vertical – Zoom in and out based on vertical mouse movement.

  * `HORIZONTAL` Horizontal – Zoom in and out based on horizontal mouse movement.


Type:
    

enum in [`'VERTICAL'`, `'HORIZONTAL'`], default `'VERTICAL'`

view_zoom_method
    

Which style to use for viewport scaling

  * `CONTINUE` Continue – Continuous zooming. The zoom direction and speed depends on how far along the set Zoom Axis the mouse has moved..

  * `DOLLY` Dolly – Zoom in and out based on mouse movement along the set Zoom Axis.

  * `SCALE` Scale – Zoom in and out as if you are scaling the view, mouse movements relative to center.


Type:
    

enum in [`'CONTINUE'`, `'DOLLY'`, `'SCALE'`], default `'DOLLY'`

walk_navigation
    

Settings for walk navigation mode

Type:
    

[`WalkNavigation`](../W/bpy.types.WalkNavigation.md#bpy.types.WalkNavigation "bpy.types.WalkNavigation"), (readonly, never None)

xr_navigation
    

Settings for navigation in XR

Type:
    

[`XrNavigation`](../X/bpy.types.XrNavigation.md#bpy.types.XrNavigation "bpy.types.XrNavigation"), (readonly, never None)

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

  * [`Preferences.inputs`](bpy.types.Preferences.md#bpy.types.Preferences.inputs "bpy.types.Preferences.inputs")

| 


  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
