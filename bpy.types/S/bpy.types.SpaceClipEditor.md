# SpaceClipEditor(Space)

base classes — [`bpy_struct`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct "bpy.types.bpy_struct"), [`Space`](bpy.types.Space.md#bpy.types.Space "bpy.types.Space")

_class _bpy.types.SpaceClipEditor(_Space_)
    

Clip editor space data

annotation_source
    

Where the annotation comes from

  * `CLIP` Clip – Show annotation data-block which belongs to movie clip.

  * `TRACK` Track – Show annotation data-block which belongs to active track.


Type:
    

enum in [`'CLIP'`, `'TRACK'`], default `'CLIP'`

blend_factor
    

Overlay blending factor of rasterized mask

Type:
    

float in [0, 1], default 0.7

clip
    

Movie clip displayed and edited in this space

Type:
    

[`MovieClip`](../M/bpy.types.MovieClip.md#bpy.types.MovieClip "bpy.types.MovieClip")

clip_user
    

Parameters defining which frame of the movie clip is displayed

Type:
    

[`MovieClipUser`](../M/bpy.types.MovieClipUser.md#bpy.types.MovieClipUser "bpy.types.MovieClipUser"), (readonly, never None)

cursor_location
    

2D cursor location for this view

Type:
    

[`mathutils.Vector`](mathutils.md#mathutils.Vector "mathutils.Vector") of 2 items in [-inf, inf], default (0.0, 0.0)

lock_selection
    

Lock viewport to selected markers during playback

Type:
    

boolean, default False

lock_time_cursor
    

Lock curves view to time cursor during playback and tracking

Type:
    

boolean, default False

mask
    

Mask displayed and edited in this space

Type:
    

[`Mask`](../M/bpy.types.Mask.md#bpy.types.Mask "bpy.types.Mask")

mask_display_type
    

Display type for mask splines

  * `OUTLINE` Outline – Display white edges with black outline.

  * `DASH` Dash – Display dashed black-white edges.

  * `BLACK` Black – Display black edges.

  * `WHITE` White – Display white edges.


Type:
    

enum in [`'OUTLINE'`, `'DASH'`, `'BLACK'`, `'WHITE'`], default `'OUTLINE'`

mask_overlay_mode
    

Overlay mode of rasterized mask

  * `ALPHACHANNEL` Alpha Channel – Show alpha channel of the mask.

  * `COMBINED` Combined – Combine space background image with the mask.


Type:
    

enum in [`'ALPHACHANNEL'`, `'COMBINED'`], default `'ALPHACHANNEL'`

mode
    

Editing context being displayed

Type:
    

enum in [Clip Editor Mode Items](../../bpy_types_enum_items/clip_editor_mode_items.md#rna-enum-clip-editor-mode-items), default `'TRACKING'`

overlay
    

Settings for display of overlays in the Movie Clip editor

Type:
    

[`SpaceClipOverlay`](bpy.types.SpaceClipOverlay.md#bpy.types.SpaceClipOverlay "bpy.types.SpaceClipOverlay"), (readonly, never None)

path_length
    

Length of displaying path, in frames

Type:
    

int in [0, inf], default 20

pivot_point
    

Pivot center for rotation/scaling

  * `BOUNDING_BOX_CENTER` Bounding Box Center – Pivot around bounding box center of selected object(s).

  * `CURSOR` 2D Cursor – Pivot around the 2D cursor.

  * `INDIVIDUAL_ORIGINS` Individual Origins – Pivot around each object’s own origin.

  * `MEDIAN_POINT` Median Point – Pivot around the median point of selected objects.


Type:
    

enum in [`'BOUNDING_BOX_CENTER'`, `'CURSOR'`, `'INDIVIDUAL_ORIGINS'`, `'MEDIAN_POINT'`], default `'MEDIAN_POINT'`

scopes
    

Scopes to visualize movie clip statistics

Type:
    

[`MovieClipScopes`](../M/bpy.types.MovieClipScopes.md#bpy.types.MovieClipScopes "bpy.types.MovieClipScopes"), (readonly)

show_annotation
    

Show annotations for this view

Type:
    

boolean, default True

show_blue_channel
    

Show blue channel in the frame

Type:
    

boolean, default True

show_bundles
    

Show projection of 3D markers into footage

Type:
    

boolean, default False

show_disabled
    

Show disabled tracks from the footage

Type:
    

boolean, default True

show_filters
    

Show filters for graph editor

Type:
    

boolean, default False

show_gizmo
    

Show gizmos of all types

Type:
    

boolean, default True

show_gizmo_navigate
    

Viewport navigation gizmo

Type:
    

boolean, default True

show_graph_frames
    

Show curve for per-frame average error (camera motion should be solved first)

Type:
    

boolean, default True

show_graph_hidden
    

Include channels from objects/bone that are not visible

Type:
    

boolean, default False

show_graph_only_selected
    

Only include channels relating to selected objects and data

Type:
    

boolean, default False

show_graph_tracks_error
    

Display the reprojection error curve for selected tracks

Type:
    

boolean, default False

show_graph_tracks_motion
    

Display speed curves for the selected tracks

Type:
    

boolean, default True

show_green_channel
    

Show green channel in the frame

Type:
    

boolean, default True

show_grid
    

Show grid showing lens distortion

Type:
    

boolean, default False

show_marker_pattern
    

Show pattern boundbox for markers

Type:
    

boolean, default True

show_marker_search
    

Show search boundbox for markers

Type:
    

boolean, default False

show_mask_overlay
    

Type:
    

boolean, default False

show_mask_spline
    

Type:
    

boolean, default True

show_metadata
    

Show metadata of clip

Type:
    

boolean, default False

show_names
    

Show track names and status

Type:
    

boolean, default False

show_red_channel
    

Show red channel in the frame

Type:
    

boolean, default True

show_region_channels
    

Type:
    

boolean, default False

show_region_hud
    

Type:
    

boolean, default False

show_region_toolbar
    

Type:
    

boolean, default False

show_region_ui
    

Type:
    

boolean, default False

show_seconds
    

Show timing as a timecode instead of frames

Type:
    

boolean, default False

show_stable
    

Show stable footage in editor (if stabilization is enabled)

Type:
    

boolean, default False

show_tiny_markers
    

Show markers in a more compact manner

Type:
    

boolean, default False

show_track_path
    

Show path of how track moves

Type:
    

boolean, default True

use_grayscale_preview
    

Display frame in grayscale mode

Type:
    

boolean, default False

use_manual_calibration
    

Use manual calibration helpers

Type:
    

boolean, default False

use_mute_footage
    

Mute footage and show black background instead

Type:
    

boolean, default False

view
    

Type of the clip editor view

  * `CLIP` Clip – Show editing clip preview.

  * `GRAPH` Graph – Show graph view for active element.

  * `DOPESHEET` Dope Sheet – Dope Sheet view for tracking data.


Type:
    

enum in [`'CLIP'`, `'GRAPH'`, `'DOPESHEET'`], default `'CLIP'`

zoom_percentage
    

Zoom percentage

Type:
    

float in [0.4, 80000], default 100.0

_classmethod _bl_rna_get_subclass(_id_ , _default =None_, _/_)
    

Parameters:
    

**id** (_str_) – The RNA type identifier.

Returns:
    

The RNA type or default when not found.

Return type:
    

[`bpy.types.Struct`](bpy.types.Struct.md#bpy.types.Struct "bpy.types.Struct") subclass

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

  * **region_type** (_str_) – The region type the callback draws in; usually `WINDOW`. ([`bpy.types.Region.type`](../R/bpy.types.Region.md#bpy.types.Region.type "bpy.types.Region.type"))

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

  * [`bpy_struct.id_data`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.id_data "bpy.types.bpy_struct.id_data")
  * [`Space.type`](bpy.types.Space.md#bpy.types.Space.type "bpy.types.Space.type")

| 

  * [`Space.show_locked_time`](bpy.types.Space.md#bpy.types.Space.show_locked_time "bpy.types.Space.show_locked_time")
  * [`Space.show_region_header`](bpy.types.Space.md#bpy.types.Space.show_region_header "bpy.types.Space.show_region_header")

  
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
  * [`bpy_struct.keyframe_delete`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.keyframe_delete "bpy.types.bpy_struct.keyframe_delete")
  * [`bpy_struct.keyframe_insert`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.keyframe_insert "bpy.types.bpy_struct.keyframe_insert")

| 

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
  * [`Space.bl_rna_get_subclass`](bpy.types.Space.md#bpy.types.Space.bl_rna_get_subclass "bpy.types.Space.bl_rna_get_subclass")
  * [`Space.bl_rna_get_subclass_py`](bpy.types.Space.md#bpy.types.Space.bl_rna_get_subclass_py "bpy.types.Space.bl_rna_get_subclass_py")
  * [`Space.draw_handler_add`](bpy.types.Space.md#bpy.types.Space.draw_handler_add "bpy.types.Space.draw_handler_add")
  * [`Space.draw_handler_remove`](bpy.types.Space.md#bpy.types.Space.draw_handler_remove "bpy.types.Space.draw_handler_remove")

  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
