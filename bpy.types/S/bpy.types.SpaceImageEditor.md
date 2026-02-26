# SpaceImageEditor(Space)

base classes — [[bpy_struct]], [[Space]]

_class _bpy.types.SpaceImageEditor(_Space_)
    

Image and UV editor space data

annotation
    

Annotation data for this space

Type:
    

[[Annotation]]

blend_factor
    

Overlay blending factor of rasterized mask

Type:
    

float in [0, 1], default 0.0

cursor_location
    

2D cursor location for this view

Type:
    

[[mathutils.Vector]] of 2 items in [-inf, inf], default (0.0, 0.0)

display_channels
    

Channels of the image to display

  * `COLOR_ALPHA` Color & Alpha – Display image with RGB colors and alpha transparency.

  * `COLOR` Color – Display image with RGB colors.

  * `ALPHA` Alpha – Display alpha transparency channel.

  * `Z_BUFFER` Z-Buffer – Display Z-buffer associated with image (mapped from camera clip start to end).

  * `RED` Red.

  * `GREEN` Green.

  * `BLUE` Blue.


Type:
    

enum in [`'COLOR_ALPHA'`, `'COLOR'`, `'ALPHA'`, `'Z_BUFFER'`, `'RED'`, `'GREEN'`, `'BLUE'`], default `'COLOR'`

image
    

Image displayed and edited in this space

Type:
    

[[Image]]

image_user
    

Parameters defining which layer, pass and frame of the image is displayed

Type:
    

[[ImageUser]], (readonly, never None)

mask
    

Mask displayed and edited in this space

Type:
    

[[Mask]]

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
    

enum in [Space Image Mode All Items](../../bpy_types_enum_items/space_image_mode_all_items.md#rna-enum-space-image-mode-all-items), default `'VIEW'`

overlay
    

Settings for display of overlays in the UV/Image editor

Type:
    

[[SpaceImageOverlay]], (readonly, never None)

pivot_point
    

Rotation/Scaling Pivot

  * `BOUNDING_BOX_CENTER` Bounding Box Center – Pivot around bounding box center of selected object(s).

  * `CURSOR` 3D Cursor – Pivot around the 3D cursor.

  * `INDIVIDUAL_ORIGINS` Individual Origins – Pivot around each object’s own origin.

  * `MEDIAN_POINT` Median Point – Pivot around the median point of selected objects.

  * `ACTIVE_ELEMENT` Active Element – Pivot around active object.


Type:
    

enum in [`'BOUNDING_BOX_CENTER'`, `'CURSOR'`, `'INDIVIDUAL_ORIGINS'`, `'MEDIAN_POINT'`, `'ACTIVE_ELEMENT'`], default `'BOUNDING_BOX_CENTER'`

sample_histogram
    

Sampled colors along line

Type:
    

[[Histogram]], (readonly)

scopes
    

Scopes to visualize image statistics

Type:
    

[[Scopes]], (readonly)

show_annotation
    

Show annotations for this view

Type:
    

boolean, default False

show_gizmo
    

Show gizmos of all types

Type:
    

boolean, default False

show_gizmo_navigate
    

Viewport navigation gizmo

Type:
    

boolean, default False

show_mask_overlay
    

Type:
    

boolean, default False

show_mask_spline
    

Type:
    

boolean, default False

show_maskedit
    

Show Mask editing related properties

Type:
    

boolean, default False, (readonly)

show_paint
    

Show paint related properties

Type:
    

boolean, default False, (readonly)

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

show_render
    

Show render related properties

Type:
    

boolean, default False, (readonly)

show_repeat
    

Display the image repeated outside of the main view

Type:
    

boolean, default False

show_sequencer_scene
    

Display the render result for the sequencer scene instead of the active scene

Type:
    

boolean, default False

show_stereo_3d
    

Display the image in Stereo 3D

Type:
    

boolean, default False

show_uvedit
    

Show UV editing related properties

Type:
    

boolean, default False, (readonly)

ui_mode
    

Editing context being displayed

  * `VIEW` View – Inspect images or render results.

  * `PAINT` Paint – Paint images in 2D.

  * `MASK` Mask – View and edit masks.


Type:
    

enum in [`'VIEW'`, `'PAINT'`, `'MASK'`], default `'VIEW'`

use_image_pin
    

Display current image regardless of object selection

Type:
    

boolean, default False

use_realtime_update
    

Update other affected window spaces automatically to reflect changes during interactive operations such as transform

Type:
    

boolean, default False

uv_editor
    

UV editor settings

Type:
    

[[SpaceUVEditor]], (readonly, never None)

zoom
    

Zoom factor

Type:
    

float array of 2 items in [-inf, inf], default (0.0, 0.0), (readonly)

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
