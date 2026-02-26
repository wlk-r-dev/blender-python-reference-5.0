# SpaceGraphEditor(Space)

base classes — [[bpy_struct]], [[Space]]

_class _bpy.types.SpaceGraphEditor(_Space_)
    

Graph Editor space data

cursor_position_x
    

Graph Editor 2D-Value cursor - X-Value component

Type:
    

float in [-inf, inf], default 0.0

cursor_position_y
    

Graph Editor 2D-Value cursor - Y-Value component

Type:
    

float in [-inf, inf], default 0.0

dopesheet
    

Settings for filtering animation data

Type:
    

[[DopeSheet]], (readonly)

has_ghost_curves
    

Graph Editor instance has some ghost curves stored

Type:
    

boolean, default False, (readonly)

mode
    

Editing context being displayed

Type:
    

enum in [Space Graph Mode Items](../../bpy_types_enum_items/space_graph_mode_items.md#rna-enum-space-graph-mode-items), default `'FCURVES'`

pivot_point
    

Pivot center for rotation/scaling

Type:
    

enum in [`'BOUNDING_BOX_CENTER'`, `'CURSOR'`, `'INDIVIDUAL_ORIGINS'`], default `'BOUNDING_BOX_CENTER'`

show_cursor
    

Show 2D cursor

Type:
    

boolean, default False

show_extrapolation
    

Type:
    

boolean, default False

show_handles
    

Show handles of Bézier control points

Type:
    

boolean, default False

show_markers
    

If any exists, show markers in a separate row at the bottom of the editor

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

show_region_ui
    

Type:
    

boolean, default False

show_seconds
    

Show timing as a timecode instead of frames

Type:
    

boolean, default False

show_sliders
    

Show sliders beside F-Curve channels

Type:
    

boolean, default False

use_auto_lock_translation_axis
    

Automatically locks the movement of keyframes to the dominant axis

Type:
    

boolean, default False

use_auto_merge_keyframes
    

Automatically merge nearby keyframes

Type:
    

boolean, default False

use_auto_normalization
    

Automatically recalculate curve normalization on every curve edit

Type:
    

boolean, default False

use_normalization
    

Display curves in normalized range from -1 to 1, for easier editing of multiple curves with different ranges

Type:
    

boolean, default False

use_only_selected_keyframe_handles
    

Only show and edit handles of selected keyframes

Type:
    

boolean, default False

use_realtime_update
    

When transforming keyframes, changes to the animation data are flushed to other views

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
  *[/]: Positional-only parameter separator (PEP 570)
