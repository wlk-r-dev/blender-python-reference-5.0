# MovieTrackingStabilization(bpy_struct)

base class — [[bpy_struct]]

_class _bpy.types.MovieTrackingStabilization(_bpy_struct_)
    

2D stabilization based on tracking markers

active_rotation_track_index
    

Index of active track in rotation stabilization tracks list

Type:
    

int in [-inf, inf], default 0

active_track_index
    

Index of active track in translation stabilization tracks list

Type:
    

int in [-inf, inf], default 0

anchor_frame
    

Reference point to anchor stabilization (other frames will be adjusted relative to this frame’s position)

Type:
    

int in [0, 1048574], default 0

filter_type
    

Interpolation to use for sub-pixel shifts and rotations due to stabilization

  * `NEAREST` Nearest – No interpolation, use nearest neighbor pixel.

  * `BILINEAR` Bilinear – Simple interpolation between adjacent pixels.

  * `BICUBIC` Bicubic – High quality pixel interpolation.


Type:
    

enum in [`'NEAREST'`, `'BILINEAR'`, `'BICUBIC'`], default `'NEAREST'`

influence_location
    

Influence of stabilization algorithm on footage location

Type:
    

float in [0, 1], default 0.0

influence_rotation
    

Influence of stabilization algorithm on footage rotation

Type:
    

float in [0, 1], default 0.0

influence_scale
    

Influence of stabilization algorithm on footage scale

Type:
    

float in [0, 1], default 0.0

rotation_tracks
    

Collection of tracks used for 2D stabilization (translation)

Type:
    

[[bpy_prop_collection]] of [[MovieTrackingTrack]], (readonly)

scale_max
    

Limit the amount of automatic scaling

Type:
    

float in [0, 10], default 0.0

show_tracks_expanded
    

Show UI list of tracks participating in stabilization

Type:
    

boolean, default False

target_position
    

Known relative offset of original shot, will be subtracted (e.g. for panning shot, can be animated)

Type:
    

[[mathutils.Vector]] of 2 items in [-inf, inf], default (0.0, 0.0)

target_rotation
    

Rotation present on original shot, will be compensated (e.g. for deliberate tilting)

Type:
    

float in [-inf, inf], default 0.0

target_scale
    

Explicitly scale resulting frame to compensate zoom of original shot

Type:
    

float in [1.192e-07, inf], default 0.0

tracks
    

Collection of tracks used for 2D stabilization (translation)

Type:
    

[[bpy_prop_collection]] of [[MovieTrackingTrack]], (readonly)

use_2d_stabilization
    

Use 2D stabilization for footage

Type:
    

boolean, default False

use_autoscale
    

Automatically scale footage to cover unfilled areas when stabilizing

Type:
    

boolean, default False

use_stabilize_rotation
    

Stabilize detected rotation around center of frame

Type:
    

boolean, default False

use_stabilize_scale
    

Compensate any scale changes relative to center of rotation

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

  * [[MovieTracking.stabilization]]

| 


  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
