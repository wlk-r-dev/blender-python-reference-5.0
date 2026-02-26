# MovieTrackingTrack(bpy_struct)

base class — [`bpy_struct`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct "bpy.types.bpy_struct")

_class _bpy.types.MovieTrackingTrack(_bpy_struct_)
    

Match-moving track data for tracking

annotation
    

Annotation data for this track

Type:
    

[`Annotation`](../A/bpy.types.Annotation.md#bpy.types.Annotation "bpy.types.Annotation")

average_error
    

Average error of re-projection

Type:
    

float in [-inf, inf], default 0.0, (readonly)

bundle
    

Position of bundle reconstructed from this track

Type:
    

[`mathutils.Vector`](mathutils.md#mathutils.Vector "mathutils.Vector") of 3 items in [-inf, inf], default (0.0, 0.0, 0.0), (readonly)

color
    

Color of the track in the Movie Clip Editor and the 3D viewport after a solve

Type:
    

[`mathutils.Color`](mathutils.md#mathutils.Color "mathutils.Color") of 3 items in [0, 1], default (0.0, 0.0, 0.0)

correlation_min
    

Minimal value of correlation between matched pattern and reference that is still treated as successful tracking

Type:
    

float in [0, 1], default 0.0

frames_limit
    

Every tracking cycle, this number of frames are tracked

Type:
    

int in [0, 32767], default 0

has_bundle
    

True if track has a valid bundle

Type:
    

boolean, default False, (readonly)

hide
    

Track is hidden

Type:
    

boolean, default False

lock
    

Track is locked and all changes to it are disabled

Type:
    

boolean, default False

margin
    

Distance from image boundary at which marker stops tracking

Type:
    

int in [0, 300], default 0

markers
    

Collection of markers in track

Type:
    

[`MovieTrackingMarkers`](bpy.types.MovieTrackingMarkers.md#bpy.types.MovieTrackingMarkers "bpy.types.MovieTrackingMarkers") [`bpy_prop_collection`](../_other/bpy.types.bpy_prop_collection.md#bpy.types.bpy_prop_collection "bpy.types.bpy_prop_collection") of [`MovieTrackingMarker`](bpy.types.MovieTrackingMarker.md#bpy.types.MovieTrackingMarker "bpy.types.MovieTrackingMarker"), (readonly)

motion_model
    

Default motion model to use for tracking

  * `Perspective` Perspective – Search for markers that are perspectively deformed (homography) between frames.

  * `Affine` Affine – Search for markers that are affine-deformed (t, r, k, and skew) between frames.

  * `LocRotScale` Location, Rotation & Scale – Search for markers that are translated, rotated, and scaled between frames.

  * `LocScale` Location & Scale – Search for markers that are translated and scaled between frames.

  * `LocRot` Location & Rotation – Search for markers that are translated and rotated between frames.

  * `Loc` Location – Search for markers that are translated between frames.


Type:
    

enum in [`'Perspective'`, `'Affine'`, `'LocRotScale'`, `'LocScale'`, `'LocRot'`, `'Loc'`], default `'Loc'`

name
    

Unique name of track

Type:
    

string, default “”, (never None)

offset
    

Offset of track from the parenting point

Type:
    

[`mathutils.Vector`](mathutils.md#mathutils.Vector "mathutils.Vector") of 2 items in [-inf, inf], default (0.0, 0.0)

pattern_match
    

Track pattern from given frame when tracking marker to next frame

  * `KEYFRAME` Keyframe – Track pattern from keyframe to next frame.

  * `PREV_FRAME` Previous frame – Track pattern from current frame to next frame.


Type:
    

enum in [`'KEYFRAME'`, `'PREV_FRAME'`], default `'KEYFRAME'`

select
    

Track is selected

Type:
    

boolean, default False

select_anchor
    

Track’s anchor point is selected

Type:
    

boolean, default False

select_pattern
    

Track’s pattern area is selected

Type:
    

boolean, default False

select_search
    

Track’s search area is selected

Type:
    

boolean, default False

use_alpha_preview
    

Apply track’s mask on displaying preview

Type:
    

boolean, default False

use_blue_channel
    

Use blue channel from footage for tracking

Type:
    

boolean, default False

use_brute
    

Use a brute-force translation only pre-track before refinement

Type:
    

boolean, default False

use_custom_color
    

Use custom color instead of theme-defined

Type:
    

boolean, default False

use_grayscale_preview
    

Display what the tracking algorithm sees in the preview

Type:
    

boolean, default False

use_green_channel
    

Use green channel from footage for tracking

Type:
    

boolean, default False

use_mask
    

Use a Grease Pencil data-block as a mask to use only specified areas of pattern when tracking

Type:
    

boolean, default False

use_normalization
    

Normalize light intensities while tracking (slower)

Type:
    

boolean, default False

use_red_channel
    

Use red channel from footage for tracking

Type:
    

boolean, default False

weight
    

Influence of this track on a final solution

Type:
    

float in [0, 1], default 0.0

weight_stab
    

Influence of this track on 2D stabilization

Type:
    

float in [0, 1], default 0.0

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

  * [`bpy.context.selected_movieclip_tracks`](../../bpy.context.md#bpy.context.selected_movieclip_tracks "bpy.context.selected_movieclip_tracks")
  * [`MovieTracking.tracks`](bpy.types.MovieTracking.md#bpy.types.MovieTracking.tracks "bpy.types.MovieTracking.tracks")
  * [`MovieTrackingObject.tracks`](bpy.types.MovieTrackingObject.md#bpy.types.MovieTrackingObject.tracks "bpy.types.MovieTrackingObject.tracks")
  * [`MovieTrackingObjectPlaneTracks.active`](bpy.types.MovieTrackingObjectPlaneTracks.md#bpy.types.MovieTrackingObjectPlaneTracks.active "bpy.types.MovieTrackingObjectPlaneTracks.active")
  * [`MovieTrackingObjectTracks.active`](bpy.types.MovieTrackingObjectTracks.md#bpy.types.MovieTrackingObjectTracks.active "bpy.types.MovieTrackingObjectTracks.active")
  * [`MovieTrackingObjectTracks.new`](bpy.types.MovieTrackingObjectTracks.md#bpy.types.MovieTrackingObjectTracks.new "bpy.types.MovieTrackingObjectTracks.new")

| 

  * [`MovieTrackingStabilization.rotation_tracks`](bpy.types.MovieTrackingStabilization.md#bpy.types.MovieTrackingStabilization.rotation_tracks "bpy.types.MovieTrackingStabilization.rotation_tracks")
  * [`MovieTrackingStabilization.tracks`](bpy.types.MovieTrackingStabilization.md#bpy.types.MovieTrackingStabilization.tracks "bpy.types.MovieTrackingStabilization.tracks")
  * [`MovieTrackingTracks.active`](bpy.types.MovieTrackingTracks.md#bpy.types.MovieTrackingTracks.active "bpy.types.MovieTrackingTracks.active")
  * [`MovieTrackingTracks.new`](bpy.types.MovieTrackingTracks.md#bpy.types.MovieTrackingTracks.new "bpy.types.MovieTrackingTracks.new")
  * [`UILayout.template_marker`](../U/bpy.types.UILayout.md#bpy.types.UILayout.template_marker "bpy.types.UILayout.template_marker")

  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
