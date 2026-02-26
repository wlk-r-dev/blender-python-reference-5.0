# MovieTrackingSettings(bpy_struct)

base class — [[bpy_struct]]

_class _bpy.types.MovieTrackingSettings(_bpy_struct_)
    

Match moving settings

clean_action
    

Cleanup action to execute

  * `SELECT` Select – Select unclean tracks.

  * `DELETE_TRACK` Delete Track – Delete unclean tracks.

  * `DELETE_SEGMENTS` Delete Segments – Delete unclean segments of tracks.


Type:
    

enum in [`'SELECT'`, `'DELETE_TRACK'`, `'DELETE_SEGMENTS'`], default `'SELECT'`

clean_error
    

Effect on tracks which have a larger re-projection error

Type:
    

float in [0, inf], default 0.0

clean_frames
    

Effect on tracks which are tracked less than the specified amount of frames

Type:
    

int in [0, inf], default 0

default_correlation_min
    

Default minimum value of correlation between matched pattern and reference that is still treated as successful tracking

Type:
    

float in [0, 1], default 0.0

default_frames_limit
    

Every tracking cycle, this number of frames are tracked

Type:
    

int in [0, 32767], default 0

default_margin
    

Default distance from image boundary at which marker stops tracking

Type:
    

int in [0, 300], default 0

default_motion_model
    

Default motion model to use for tracking

  * `Perspective` Perspective – Search for markers that are perspectively deformed (homography) between frames.

  * `Affine` Affine – Search for markers that are affine-deformed (t, r, k, and skew) between frames.

  * `LocRotScale` Location, Rotation & Scale – Search for markers that are translated, rotated, and scaled between frames.

  * `LocScale` Location & Scale – Search for markers that are translated and scaled between frames.

  * `LocRot` Location & Rotation – Search for markers that are translated and rotated between frames.

  * `Loc` Location – Search for markers that are translated between frames.


Type:
    

enum in [`'Perspective'`, `'Affine'`, `'LocRotScale'`, `'LocScale'`, `'LocRot'`, `'Loc'`], default `'Loc'`

default_pattern_match
    

Track pattern from given frame when tracking marker to next frame

  * `KEYFRAME` Keyframe – Track pattern from keyframe to next frame.

  * `PREV_FRAME` Previous frame – Track pattern from current frame to next frame.


Type:
    

enum in [`'KEYFRAME'`, `'PREV_FRAME'`], default `'KEYFRAME'`

default_pattern_size
    

Size of pattern area for newly created tracks

Type:
    

int in [5, 1000], default 0

default_search_size
    

Size of search area for newly created tracks

Type:
    

int in [5, 1000], default 0

default_weight
    

Influence of newly created track on a final solution

Type:
    

float in [0, 1], default 0.0

distance
    

Distance between two bundles used for scene scaling

Type:
    

float in [-inf, inf], default 1.0

object_distance
    

Distance between two bundles used for object scaling

Type:
    

float in [0.001, 10000], default 1.0

refine_intrinsics_focal_length
    

Refine focal length during camera solving

Type:
    

boolean, default False

refine_intrinsics_principal_point
    

Refine principal point during camera solving

Type:
    

boolean, default False

refine_intrinsics_radial_distortion
    

Refine radial coefficients of distortion model during camera solving

Type:
    

boolean, default False

refine_intrinsics_tangential_distortion
    

Refine tangential coefficients of distortion model during camera solving

Type:
    

boolean, default False

speed
    

Limit speed of tracking to make visual feedback easier (this does not affect the tracking quality)

  * `FASTEST` Fastest – Track as fast as possible.

  * `DOUBLE` Double – Track with double speed.

  * `REALTIME` Realtime – Track with realtime speed.

  * `HALF` Half – Track with half of realtime speed.

  * `QUARTER` Quarter – Track with quarter of realtime speed.


Type:
    

enum in [`'FASTEST'`, `'DOUBLE'`, `'REALTIME'`, `'HALF'`, `'QUARTER'`], default `'FASTEST'`

use_default_blue_channel
    

Use blue channel from footage for tracking

Type:
    

boolean, default False

use_default_brute
    

Use a brute-force translation-only initialization when tracking

Type:
    

boolean, default False

use_default_green_channel
    

Use green channel from footage for tracking

Type:
    

boolean, default False

use_default_mask
    

Use a Grease Pencil data-block as a mask to use only specified areas of pattern when tracking

Type:
    

boolean, default False

use_default_normalization
    

Normalize light intensities while tracking (slower)

Type:
    

boolean, default False

use_default_red_channel
    

Use red channel from footage for tracking

Type:
    

boolean, default False

use_keyframe_selection
    

Automatically select keyframes when solving camera/object motion

Type:
    

boolean, default False

use_tripod_solver
    

Use special solver to track a stable camera position, such as a tripod

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

  * [[MovieTracking.settings]]

| 


  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
