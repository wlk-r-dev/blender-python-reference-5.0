# SpaceSequenceEditor(Space)

base classes — [[bpy_struct]], [[Space]]

_class _bpy.types.SpaceSequenceEditor(_Space_)
    

Sequence editor space data

annotation
    

Annotation data for this Preview region

Type:
    

[[Annotation]]

cache_overlay
    

Settings for display of overlays

Type:
    

[[SequencerCacheOverlay]], (readonly, never None)

cursor_location
    

2D cursor location for this view

Type:
    

[[mathutils.Vector]] of 2 items in [-inf, inf], default (0.0, 0.0)

display_channel
    

Preview all channels less than or equal to this value. 0 shows every channel, and negative values climb that many meta-strip levels if applicable, showing every channel there.

Type:
    

int in [-5, 128], default 0

display_mode
    

View mode to use for displaying sequencer output

Type:
    

enum in [`'IMAGE'`, `'WAVEFORM'`, `'RGB_PARADE'`, `'VECTOR_SCOPE'`, `'HISTOGRAM'`], default `'IMAGE'`

overlay_frame_type
    

Overlay display method

  * `RECTANGLE` Rectangle – Show rectangle area overlay.

  * `REFERENCE` Reference – Show reference frame only.

  * `CURRENT` Current – Show current frame only.


Type:
    

enum in [`'RECTANGLE'`, `'REFERENCE'`, `'CURRENT'`], default `'RECTANGLE'`

preview_channels
    

Channels of the preview to display

  * `COLOR_ALPHA` Color & Alpha – Display image with RGB colors and alpha transparency.

  * `COLOR` Color – Display image with RGB colors.


Type:
    

enum in [`'COLOR_ALPHA'`, `'COLOR'`], default `'COLOR'`

preview_overlay
    

Settings for display of overlays

Type:
    

[[SequencerPreviewOverlay]], (readonly, never None)

proxy_render_size
    

Display preview using full resolution or different proxy resolutions

Type:
    

enum in [`'NONE'`, `'SCENE'`, `'PROXY_25'`, `'PROXY_50'`, `'PROXY_75'`, `'PROXY_100'`], default `'SCENE'`

show_frames
    

Display frames rather than seconds

Type:
    

boolean, default False

show_gizmo
    

Show gizmos of all types

Type:
    

boolean, default False

show_gizmo_context
    

Context sensitive gizmos for the active item

Type:
    

boolean, default False

show_gizmo_navigate
    

Viewport navigation gizmo

Type:
    

boolean, default False

show_gizmo_tool
    

Active tool gizmo

Type:
    

boolean, default False

show_markers
    

If any exists, show markers in a separate row at the bottom of the editor

Type:
    

boolean, default False

show_overexposed
    

Show overexposed areas with zebra stripes

Type:
    

int in [0, 110], default 0

show_overlays
    

Type:
    

boolean, default False

show_region_channels
    

Type:
    

boolean, default False

show_region_footer
    

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

show_seconds
    

Show timing as a timecode instead of frames

Type:
    

boolean, default False

show_transform_preview
    

Show a preview of the start or end frame of a strip while transforming its respective handle

Type:
    

boolean, default False

timeline_overlay
    

Settings for display of overlays

Type:
    

[[SequencerTimelineOverlay]], (readonly, never None)

use_clamp_view
    

Limit timeline height to maximum used channel slot

Type:
    

boolean, default False

use_marker_sync
    

Transform markers as well as strips

Type:
    

boolean, default False

use_proxies
    

Use optimized files for faster scrubbing when available

Type:
    

boolean, default False

use_zoom_to_fit
    

Automatically zoom preview image to make it fully fit the region

Type:
    

boolean, default False

view_type
    

Type of the Sequencer view (sequencer, preview or both)

Type:
    

enum in [Space Sequencer View Type Items](../../bpy_types_enum_items/space_sequencer_view_type_items.md#rna-enum-space-sequencer-view-type-items), default `'SEQUENCER'`

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
  *[/]: Positional-only parameter separator (PEP 570)
