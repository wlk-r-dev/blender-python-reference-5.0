# SpaceDopeSheetEditor(Space)

base classes — [[bpy_struct]], [[Space]]

_class _bpy.types.SpaceDopeSheetEditor(_Space_)
    

Dope Sheet space data

cache_cloth
    

Show the active object’s cloth point cache

Type:
    

boolean, default False

cache_dynamicpaint
    

Show the active object’s Dynamic Paint cache

Type:
    

boolean, default False

cache_particles
    

Show the active object’s particle point cache

Type:
    

boolean, default False

cache_rigidbody
    

Show the active object’s Rigid Body cache

Type:
    

boolean, default False

cache_simulation_nodes
    

Show the active object’s simulation nodes cache and bake data

Type:
    

boolean, default False

cache_smoke
    

Show the active object’s smoke cache

Type:
    

boolean, default False

cache_softbody
    

Show the active object’s softbody point cache

Type:
    

boolean, default False

dopesheet
    

Settings for filtering animation data

Type:
    

[[DopeSheet]], (readonly)

mode
    

Editing context being displayed

  * `DOPESHEET` Dope Sheet – Edit all keyframes in scene.

  * `ACTION` Action Editor – Edit keyframes in active object’s Object-level action.

  * `SHAPEKEY` Shape Key Editor – Edit keyframes in active object’s Shape Keys action.

  * `GPENCIL` Grease Pencil – Edit timings for all Grease Pencil sketches in file.

  * `MASK` Mask – Edit timings for Mask Editor splines.

  * `CACHEFILE` Cache File – Edit timings for Cache File data-blocks.

  * `TIMELINE` Timeline – Simple timeline view with playback controls in the header, without channel list, side-panel, or footer.


Type:
    

enum in [`'DOPESHEET'`, `'ACTION'`, `'SHAPEKEY'`, `'GPENCIL'`, `'MASK'`, `'CACHEFILE'`, `'TIMELINE'`], default `'ACTION'`

overlays
    

Settings for display of overlays

Type:
    

[[SpaceDopeSheetOverlay]], (readonly, never None)

show_cache
    

Show the status of cached frames in the timeline

Type:
    

boolean, default False

show_extremes
    

Mark keyframes where the key value flow changes direction, based on comparison with adjacent keys

Type:
    

boolean, default False

show_interpolation
    

Display keyframe handle types and non-Bézier interpolation modes

Type:
    

boolean, default False

show_markers
    

If any exists, show markers in a separate row at the bottom of the editor

Type:
    

boolean, default False

show_pose_markers
    

Show markers belonging to the active action instead of Scene markers (Action and Shape Key Editors only)

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

ui_mode
    

Editing context being displayed

  * `DOPESHEET` Dope Sheet – Edit all keyframes in scene.

  * `ACTION` Action Editor – Edit keyframes in active object’s Object-level action.

  * `SHAPEKEY` Shape Key Editor – Edit keyframes in active object’s Shape Keys action.

  * `GPENCIL` Grease Pencil – Edit timings for all Grease Pencil sketches in file.

  * `MASK` Mask – Edit timings for Mask Editor splines.

  * `CACHEFILE` Cache File – Edit timings for Cache File data-blocks.


Type:
    

enum in [`'DOPESHEET'`, `'ACTION'`, `'SHAPEKEY'`, `'GPENCIL'`, `'MASK'`, `'CACHEFILE'`], default `'ACTION'`

use_auto_merge_keyframes
    

Automatically merge nearby keyframes

Type:
    

boolean, default False

use_marker_sync
    

Sync Markers with keyframe edits

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
