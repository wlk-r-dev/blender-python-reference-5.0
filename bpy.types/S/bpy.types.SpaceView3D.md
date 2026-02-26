# SpaceView3D(Space)

base classes — [[bpy_struct]], [[Space]]

_class _bpy.types.SpaceView3D(_Space_)
    

3D View space data

camera
    

Active camera used in this view (when unlocked from the scene’s active camera)

Type:
    

[[Object]]

clip_end
    

3D View far clipping distance

Type:
    

float in [1e-06, inf], default 1000.0

clip_start
    

3D View near clipping distance (perspective view only)

Type:
    

float in [1e-06, inf], default 0.01

icon_from_show_object_viewport
    

Type:
    

int in [-inf, inf], default 0, (readonly)

lens
    

Viewport lens angle

Type:
    

float in [1, 250], default 50.0

local_view
    

Display an isolated subset of objects, apart from the scene visibility

Type:
    

`SpaceView3D`, (readonly)

lock_bone
    

3D View center is locked to this bone’s position

Type:
    

string, default “”, (never None)

lock_camera
    

Enable view navigation within the camera view

Type:
    

boolean, default False

lock_cursor
    

3D View center is locked to the cursor’s position

Type:
    

boolean, default False

lock_object
    

3D View center is locked to this object’s position

Type:
    

[[Object]]

mirror_xr_session
    

Synchronize the viewer perspective of virtual reality sessions with this 3D viewport

Type:
    

boolean, default False

overlay
    

Settings for display of overlays in the 3D viewport

Type:
    

[[View3DOverlay]], (readonly, never None)

region_3d
    

3D region for this space. When the space is in quad view, the camera region

Type:
    

[[RegionView3D]], (readonly)

region_quadviews
    

3D regions (the third one defines quad view settings, the fourth one is same as ‘region_3d’)

Type:
    

[[bpy_prop_collection]] of [[RegionView3D]], (readonly)

render_border_max_x
    

Maximum X value for the render region

Type:
    

float in [0, 1], default 0.0

render_border_max_y
    

Maximum Y value for the render region

Type:
    

float in [0, 1], default 0.0

render_border_min_x
    

Minimum X value for the render region

Type:
    

float in [0, 1], default 0.0

render_border_min_y
    

Minimum Y value for the render region

Type:
    

float in [0, 1], default 0.0

shading
    

Settings for shading in the 3D viewport

Type:
    

[[View3DShading]], (readonly, never None)

show_bundle_names
    

Show names for reconstructed tracks objects

Type:
    

boolean, default False

show_camera_path
    

Show reconstructed camera path

Type:
    

boolean, default False

show_gizmo
    

Show gizmos of all types

Type:
    

boolean, default True

show_gizmo_camera_dof_distance
    

Gizmo to adjust camera focus distance (depends on limits display)

Type:
    

boolean, default False

show_gizmo_camera_lens
    

Gizmo to adjust camera focal length or orthographic scale

Type:
    

boolean, default False

show_gizmo_context
    

Context sensitive gizmos for the active item

Type:
    

boolean, default True

show_gizmo_empty_force_field
    

Gizmo to adjust the force field

Type:
    

boolean, default False

show_gizmo_empty_image
    

Gizmo to adjust image size and position

Type:
    

boolean, default False

show_gizmo_light_look_at
    

Gizmo to adjust the direction of the light

Type:
    

boolean, default False

show_gizmo_light_size
    

Gizmo to adjust spot and area size

Type:
    

boolean, default False

show_gizmo_modifier
    

Gizmos for the active modifier

Type:
    

boolean, default True

show_gizmo_navigate
    

Viewport navigation gizmo

Type:
    

boolean, default True

show_gizmo_object_rotate
    

Gizmo to adjust rotation

Type:
    

boolean, default False

show_gizmo_object_scale
    

Gizmo to adjust scale

Type:
    

boolean, default False

show_gizmo_object_translate
    

Gizmo to adjust location

Type:
    

boolean, default False

show_gizmo_tool
    

Active tool gizmo

Type:
    

boolean, default True

show_object_select_armature
    

Allow selection of armatures

Type:
    

boolean, default True

show_object_select_camera
    

Allow selection of cameras

Type:
    

boolean, default True

show_object_select_curve
    

Allow selection of curves

Type:
    

boolean, default True

show_object_select_curves
    

Allow selection of hair curves

Type:
    

boolean, default True

show_object_select_empty
    

Allow selection of empties

Type:
    

boolean, default True

show_object_select_font
    

Allow selection of text objects

Type:
    

boolean, default True

show_object_select_grease_pencil
    

Allow selection of Grease Pencil objects

Type:
    

boolean, default True

show_object_select_lattice
    

Allow selection of lattices

Type:
    

boolean, default True

show_object_select_light
    

Allow selection of lights

Type:
    

boolean, default True

show_object_select_light_probe
    

Allow selection of light probes

Type:
    

boolean, default True

show_object_select_mesh
    

Allow selection of mesh objects

Type:
    

boolean, default True

show_object_select_meta
    

Allow selection of metaballs

Type:
    

boolean, default True

show_object_select_pointcloud
    

Allow selection of point clouds

Type:
    

boolean, default True

show_object_select_speaker
    

Allow selection of speakers

Type:
    

boolean, default True

show_object_select_surf
    

Allow selection of surfaces

Type:
    

boolean, default True

show_object_select_volume
    

Allow selection of volumes

Type:
    

boolean, default True

show_object_viewport_armature
    

Show armatures

Type:
    

boolean, default True

show_object_viewport_camera
    

Show cameras

Type:
    

boolean, default True

show_object_viewport_curve
    

Show curves

Type:
    

boolean, default True

show_object_viewport_curves
    

Show hair curves

Type:
    

boolean, default True

show_object_viewport_empty
    

Show empties

Type:
    

boolean, default True

show_object_viewport_font
    

Show text objects

Type:
    

boolean, default True

show_object_viewport_grease_pencil
    

Show Grease Pencil objects

Type:
    

boolean, default True

show_object_viewport_lattice
    

Show lattices

Type:
    

boolean, default True

show_object_viewport_light
    

Show lights

Type:
    

boolean, default True

show_object_viewport_light_probe
    

Show light probes

Type:
    

boolean, default True

show_object_viewport_mesh
    

Show mesh objects

Type:
    

boolean, default True

show_object_viewport_meta
    

Show metaballs

Type:
    

boolean, default True

show_object_viewport_pointcloud
    

Show point clouds

Type:
    

boolean, default True

show_object_viewport_speaker
    

Show speakers

Type:
    

boolean, default True

show_object_viewport_surf
    

Show surfaces

Type:
    

boolean, default True

show_object_viewport_volume
    

Show volumes

Type:
    

boolean, default True

show_reconstruction
    

Display reconstruction data from active movie clip

Type:
    

boolean, default True

show_region_asset_shelf
    

Display a region with assets that may currently be relevant (such as brushes in paint modes, or poses in Pose Mode)

Type:
    

boolean, default False

show_region_hud
    

Type:
    

boolean, default False

show_region_tool_header
    

Type:
    

boolean, default False

show_region_toolbar
    

Type:
    

boolean, default False

show_region_ui
    

Type:
    

boolean, default False

show_stereo_3d_cameras
    

Show the left and right cameras

Type:
    

boolean, default False

show_stereo_3d_convergence_plane
    

Show the stereo 3D convergence plane

Type:
    

boolean, default True

show_stereo_3d_volume
    

Show the stereo 3D frustum volume

Type:
    

boolean, default False

show_viewer
    

Display non-final geometry from viewer nodes

Type:
    

boolean, default True

stereo_3d_camera
    

Type:
    

enum in [`'LEFT'`, `'RIGHT'`, `'S3D'`], default `'S3D'`

stereo_3d_convergence_plane_alpha
    

Opacity (alpha) of the convergence plane

Type:
    

float in [0, 1], default 0.15

stereo_3d_eye
    

Current stereo eye being displayed

Type:
    

enum in [`'LEFT_EYE'`, `'RIGHT_EYE'`], default `'LEFT_EYE'`, (readonly)

stereo_3d_volume_alpha
    

Opacity (alpha) of the cameras’ frustum volume

Type:
    

float in [0, 1], default 0.05

tracks_display_size
    

Display size of tracks from reconstructed data

Type:
    

float in [0, inf], default 0.2

tracks_display_type
    

Viewport display style for tracks

Type:
    

enum in [`'PLAIN_AXES'`, `'ARROWS'`, `'SINGLE_ARROW'`, `'CIRCLE'`, `'CUBE'`, `'SPHERE'`, `'CONE'`], default `'PLAIN_AXES'`

use_local_camera
    

Use a local camera in this view, rather than scene’s active camera

Type:
    

boolean, default False

use_local_collections
    

Display a different set of collections in this viewport

Type:
    

boolean, default False

use_render_border
    

Use a region within the frame size for rendered viewport (when not viewing through the camera)

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

_classmethod _draw_handler_add(_callback_ , _args_ , _region_type_ , _draw_type_)
    

Add a new draw handler to this space type. It will be called every time the specified region in the space type will be drawn. Note: All arguments are positional only for now.

Parameters:
    

  * **callback** (_Callable_ _[__...__,__Any_ _]_) – A function that will be called when the region is drawn. It gets the specified arguments as input, it’s return value is ignored.

  * **args** (_tuple_ _[__Any_ _,__...__]_) – Arguments that will be passed to the callback.

  * **region_type** (_str_) – The region type the callback draws in; usually `WINDOW`. ([[bpy.types.Region.type]])

  * **draw_type** (_str_) – Usually `POST_PIXEL` for 2D drawing and `POST_VIEW` for 3D drawing. In some cases `PRE_VIEW` can be used. `BACKDROP` can be used for backdrops in the node editor.


Returns:
    

Handler that can be removed later on.

Return type:
    

object

_classmethod _draw_handler_remove(_handler_ , _region_type_)
    

Remove a draw handler that was added previously.

Parameters:
    

  * **handler** (_object_) – The draw handler that should be removed.

  * **region_type** (_str_) – Region type the callback was added to.


## Inherited Properties

  * [[bpy_struct.id_data]]
  * [[Space.type]]

| 

  * [[Space.show_locked_time]]
  * [[Space.show_region_header]]

  
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
  * [[bpy_struct.keyframe_insert]]

| 

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
  * [[Space.bl_rna_get_subclass]]
  * [[Space.bl_rna_get_subclass_py]]
  * [[Space.draw_handler_add]]
  * [[Space.draw_handler_remove]]

  
---|---  
  
## References

  * [[Object.local_view_get]]
  * [[Object.local_view_set]]
  * [[Object.visible_get]]

| 

  * [[Object.visible_in_viewport_get]]
  * `SpaceView3D.local_view`

  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
