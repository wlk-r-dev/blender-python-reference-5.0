# Scene(ID)

base classes — [`bpy_struct`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct "bpy.types.bpy_struct"), [`ID`](../I/bpy.types.ID.md#bpy.types.ID "bpy.types.ID")

_class _bpy.types.Scene(_ID_)
    

Scene data-block, consisting in objects and defining time and render related settings

active_clip
    

Active Movie Clip that can be used by motion tracking constraints or as a camera’s background image

Type:
    

[`MovieClip`](../M/bpy.types.MovieClip.md#bpy.types.MovieClip "bpy.types.MovieClip")

animation_data
    

Animation data for this data-block

Type:
    

[`AnimData`](../A/bpy.types.AnimData.md#bpy.types.AnimData "bpy.types.AnimData"), (readonly)

annotation
    

Data-block used for annotations in the 3D view

Type:
    

[`Annotation`](../A/bpy.types.Annotation.md#bpy.types.Annotation "bpy.types.Annotation")

audio_distance_model
    

Distance model for distance attenuation calculation

  * `NONE` None – No distance attenuation.

  * `INVERSE` Inverse – Inverse distance model.

  * `INVERSE_CLAMPED` Inverse Clamped – Inverse distance model with clamping.

  * `LINEAR` Linear – Linear distance model.

  * `LINEAR_CLAMPED` Linear Clamped – Linear distance model with clamping.

  * `EXPONENT` Exponential – Exponential distance model.

  * `EXPONENT_CLAMPED` Exponential Clamped – Exponential distance model with clamping.


Type:
    

enum in [`'NONE'`, `'INVERSE'`, `'INVERSE_CLAMPED'`, `'LINEAR'`, `'LINEAR_CLAMPED'`, `'EXPONENT'`, `'EXPONENT_CLAMPED'`], default `'INVERSE_CLAMPED'`

audio_doppler_factor
    

Pitch factor for Doppler effect calculation

Type:
    

float in [0, inf], default 1.0

audio_doppler_speed
    

Speed of sound for Doppler effect calculation

Type:
    

float in [0.01, inf], default 343.3

audio_volume
    

Audio volume

Type:
    

float in [0, 100], default 1.0

background_set
    

Background set scene

Type:
    

`Scene`

camera
    

Active camera, used for rendering the scene

Type:
    

[`Object`](../O/bpy.types.Object.md#bpy.types.Object "bpy.types.Object")

collection
    

Scene root collection that owns all the objects and other collections instantiated in the scene

Type:
    

[`Collection`](../C/bpy.types.Collection.md#bpy.types.Collection "bpy.types.Collection"), (readonly, never None)

compositing_node_group
    

Compositor Nodes

Type:
    

[`NodeTree`](../N/bpy.types.NodeTree.md#bpy.types.NodeTree "bpy.types.NodeTree")

cursor
    

Type:
    

[`View3DCursor`](../V/bpy.types.View3DCursor.md#bpy.types.View3DCursor "bpy.types.View3DCursor"), (readonly, never None)

cycles
    

Cycles render settings

Type:
    

`CyclesRenderSettings`, (readonly)

cycles_curves
    

Cycles curves rendering settings

Type:
    

`CyclesCurveRenderSettings`, (readonly)

display
    

Scene display settings for 3D viewport

Type:
    

[`SceneDisplay`](bpy.types.SceneDisplay.md#bpy.types.SceneDisplay "bpy.types.SceneDisplay"), (readonly)

display_settings
    

Settings of device saved image would be displayed on

Type:
    

[`ColorManagedDisplaySettings`](../C/bpy.types.ColorManagedDisplaySettings.md#bpy.types.ColorManagedDisplaySettings "bpy.types.ColorManagedDisplaySettings"), (readonly)

eevee
    

EEVEE settings for the scene

Type:
    

[`SceneEEVEE`](bpy.types.SceneEEVEE.md#bpy.types.SceneEEVEE "bpy.types.SceneEEVEE"), (readonly)

frame_current
    

Current frame, to update animation data from Python frame_set() instead

Type:
    

int in [-1048574, 1048574], default 1

frame_current_final
    

Current frame with subframe and time remapping applied

Type:
    

float in [-1.04857e+06, 1.04857e+06], default 0.0, (readonly)

frame_end
    

Final frame of the playback/rendering range

Type:
    

int in [0, 1048574], default 250

frame_float
    

Type:
    

float in [-1.04857e+06, 1.04857e+06], default 0.0

frame_preview_end
    

Alternative end frame for UI playback

Type:
    

int in [-inf, inf], default 0

frame_preview_start
    

Alternative start frame for UI playback

Type:
    

int in [-inf, inf], default 0

frame_start
    

First frame of the playback/rendering range

Type:
    

int in [0, 1048574], default 1

frame_step
    

Number of frames to skip forward while rendering/playing back each frame

Type:
    

int in [0, 1048574], default 1

frame_subframe
    

Type:
    

float in [0, 1], default 0.0

gravity
    

Constant acceleration in a given direction

Type:
    

[`mathutils.Vector`](mathutils.md#mathutils.Vector "mathutils.Vector") of 3 items in [-inf, inf], default (0.0, 0.0, -9.81)

grease_pencil_settings
    

Grease Pencil settings for the scene

Type:
    

[`SceneGpencil`](bpy.types.SceneGpencil.md#bpy.types.SceneGpencil "bpy.types.SceneGpencil"), (readonly)

hydra
    

Hydra settings for the scene

Type:
    

[`SceneHydra`](bpy.types.SceneHydra.md#bpy.types.SceneHydra "bpy.types.SceneHydra"), (readonly)

is_nla_tweakmode
    

Whether there is any action referenced by NLA being edited (strictly read-only)

Type:
    

boolean, default False, (readonly)

keying_sets
    

Absolute Keying Sets for this Scene

Type:
    

[`KeyingSets`](../K/bpy.types.KeyingSets.md#bpy.types.KeyingSets "bpy.types.KeyingSets") [`bpy_prop_collection`](../_other/bpy.types.bpy_prop_collection.md#bpy.types.bpy_prop_collection "bpy.types.bpy_prop_collection") of [`KeyingSet`](../K/bpy.types.KeyingSet.md#bpy.types.KeyingSet "bpy.types.KeyingSet"), (readonly)

keying_sets_all
    

All Keying Sets available for use (Builtins and Absolute Keying Sets for this Scene)

Type:
    

[`KeyingSetsAll`](../K/bpy.types.KeyingSetsAll.md#bpy.types.KeyingSetsAll "bpy.types.KeyingSetsAll") [`bpy_prop_collection`](../_other/bpy.types.bpy_prop_collection.md#bpy.types.bpy_prop_collection "bpy.types.bpy_prop_collection") of [`KeyingSet`](../K/bpy.types.KeyingSet.md#bpy.types.KeyingSet "bpy.types.KeyingSet"), (readonly)

lock_frame_selection_to_range
    

Don’t allow frame to be selected with mouse outside of frame range

Type:
    

boolean, default False

objects
    

Type:
    

[`SceneObjects`](bpy.types.SceneObjects.md#bpy.types.SceneObjects "bpy.types.SceneObjects") [`bpy_prop_collection`](../_other/bpy.types.bpy_prop_collection.md#bpy.types.bpy_prop_collection "bpy.types.bpy_prop_collection") of [`Object`](../O/bpy.types.Object.md#bpy.types.Object "bpy.types.Object"), (readonly)

render
    

Type:
    

[`RenderSettings`](../R/bpy.types.RenderSettings.md#bpy.types.RenderSettings "bpy.types.RenderSettings"), (readonly, never None)

rigidbody_world
    

Type:
    

[`RigidBodyWorld`](../R/bpy.types.RigidBodyWorld.md#bpy.types.RigidBodyWorld "bpy.types.RigidBodyWorld"), (readonly)

safe_areas
    

Type:
    

[`DisplaySafeAreas`](../D/bpy.types.DisplaySafeAreas.md#bpy.types.DisplaySafeAreas "bpy.types.DisplaySafeAreas"), (readonly, never None)

sequence_editor
    

Type:
    

[`SequenceEditor`](bpy.types.SequenceEditor.md#bpy.types.SequenceEditor "bpy.types.SequenceEditor"), (readonly)

sequencer_colorspace_settings
    

Settings of color space sequencer is working in

Type:
    

[`ColorManagedSequencerColorspaceSettings`](../C/bpy.types.ColorManagedSequencerColorspaceSettings.md#bpy.types.ColorManagedSequencerColorspaceSettings "bpy.types.ColorManagedSequencerColorspaceSettings"), (readonly)

show_keys_from_selected_only
    

Only include channels relating to selected objects and data

Type:
    

boolean, default True

show_subframe
    

Display and allow setting fractional frame values for the current frame

Type:
    

boolean, default False

simulation_frame_end
    

Frame at which simulations end

Type:
    

int in [-inf, inf], default 250

simulation_frame_start
    

Frame at which simulations start

Type:
    

int in [-inf, inf], default 1

sync_mode
    

How to sync playback

  * `NONE` Play Every Frame – Do not sync, play every frame.

  * `FRAME_DROP` Frame Dropping – Drop frames if playback is too slow.

  * `AUDIO_SYNC` Sync to Audio – Sync to audio playback, dropping frames.


Type:
    

enum in [`'NONE'`, `'FRAME_DROP'`, `'AUDIO_SYNC'`], default `'AUDIO_SYNC'`

time_jump_delta
    

Number of frames or seconds to jump forward or backward

Type:
    

float in [0.1, inf], default 1.0

time_jump_unit
    

Which unit to use for time jumps in the timeline

  * `FRAME` Frame – Jump by frames.

  * `SECOND` Second – Jump by seconds.


Type:
    

enum in [`'FRAME'`, `'SECOND'`], default `'SECOND'`

timeline_markers
    

Markers used in all timelines for the current scene

Type:
    

[`TimelineMarkers`](../T/bpy.types.TimelineMarkers.md#bpy.types.TimelineMarkers "bpy.types.TimelineMarkers") [`bpy_prop_collection`](../_other/bpy.types.bpy_prop_collection.md#bpy.types.bpy_prop_collection "bpy.types.bpy_prop_collection") of [`TimelineMarker`](../T/bpy.types.TimelineMarker.md#bpy.types.TimelineMarker "bpy.types.TimelineMarker"), (readonly)

tool_settings
    

Type:
    

[`ToolSettings`](../T/bpy.types.ToolSettings.md#bpy.types.ToolSettings "bpy.types.ToolSettings"), (readonly, never None)

transform_orientation_slots
    

Type:
    

[`bpy_prop_collection`](../_other/bpy.types.bpy_prop_collection.md#bpy.types.bpy_prop_collection "bpy.types.bpy_prop_collection") of [`TransformOrientationSlot`](../T/bpy.types.TransformOrientationSlot.md#bpy.types.TransformOrientationSlot "bpy.types.TransformOrientationSlot"), (readonly)

unit_settings
    

Unit editing settings

Type:
    

[`UnitSettings`](../U/bpy.types.UnitSettings.md#bpy.types.UnitSettings "bpy.types.UnitSettings"), (readonly, never None)

use_audio
    

Play back of audio from Sequence Editor, otherwise mute audio

Type:
    

boolean, default False

use_audio_scrub
    

Play audio from Sequence Editor while scrubbing

Type:
    

boolean, default False

use_custom_simulation_range
    

Use a simulation range that is different from the scene range for simulation nodes that don’t override the frame range themselves

Type:
    

boolean, default False

use_gravity
    

Use global gravity for all dynamics

Type:
    

boolean, default True

use_nodes
    

Enable the compositing node group.

Deprecated since version 5.0: removal planned in version 6.0

Unused but kept for compatibility reasons. Setting the property has no effect, and getting it always returns True. Use #scene.render.use_compositing to turn compositing to enable or disable compositing.

Type:
    

boolean, default False

use_preview_range
    

Use an alternative start/end frame range for animation playback and view renders

Type:
    

boolean, default False

use_stamp_note
    

User defined note for the render stamping

Type:
    

string, default “”, (never None)

view_layers
    

Type:
    

[`ViewLayers`](../V/bpy.types.ViewLayers.md#bpy.types.ViewLayers "bpy.types.ViewLayers") [`bpy_prop_collection`](../_other/bpy.types.bpy_prop_collection.md#bpy.types.bpy_prop_collection "bpy.types.bpy_prop_collection") of [`ViewLayer`](../V/bpy.types.ViewLayer.md#bpy.types.ViewLayer "bpy.types.ViewLayer"), (readonly)

view_settings
    

Color management settings applied on image before saving

Type:
    

[`ColorManagedViewSettings`](../C/bpy.types.ColorManagedViewSettings.md#bpy.types.ColorManagedViewSettings "bpy.types.ColorManagedViewSettings"), (readonly)

world
    

World used for rendering the scene

Type:
    

[`World`](../W/bpy.types.World.md#bpy.types.World "bpy.types.World")

_classmethod _update_render_engine()
    

Trigger a render engine update

statistics(_view_layer_)
    

statistics

Parameters:
    

**view_layer** ([`ViewLayer`](../V/bpy.types.ViewLayer.md#bpy.types.ViewLayer "bpy.types.ViewLayer"), (never None)) – View Layer

Returns:
    

Statistics

Return type:
    

string, (never None)

frame_set(_frame_ , _*_ , _subframe =0.0_)
    

Set scene frame updating all objects and view layers immediately

Parameters:
    

  * **frame** (_int in_ _[__-1048574_ _,__1048574_ _]_) – Frame number to set

  * **subframe** (_float in_ _[__0_ _,__1_ _]__,__(__optional_ _)_) – Subframe time, between 0.0 and 1.0


uvedit_aspect(_object_)
    

Get uv aspect for current object

Parameters:
    

**object** ([`Object`](../O/bpy.types.Object.md#bpy.types.Object "bpy.types.Object"), (never None)) – Object

Returns:
    

aspect

Return type:
    

[`mathutils.Vector`](mathutils.md#mathutils.Vector "mathutils.Vector") of 2 items in [0, inf]

ray_cast(_depsgraph_ , _origin_ , _direction_ , _*_ , _distance =1.70141e+38_)
    

Cast a ray onto evaluated geometry in world-space

Parameters:
    

  * **depsgraph** ([`Depsgraph`](../D/bpy.types.Depsgraph.md#bpy.types.Depsgraph "bpy.types.Depsgraph"), (never None)) – The current dependency graph

  * **distance** (_float in_ _[__0_ _,__inf_ _]__,__(__optional_ _)_) – Maximum distance


Returns:
    

`result`, boolean

`location`, The hit location of this ray cast, [`mathutils.Vector`](mathutils.md#mathutils.Vector "mathutils.Vector") of 3 items in [-inf, inf]

`normal`, The face normal at the ray cast hit location, [`mathutils.Vector`](mathutils.md#mathutils.Vector "mathutils.Vector") of 3 items in [-inf, inf]

`index`, The face index, -1 when original data isn’t available, int in [-inf, inf]

`object`, Ray cast object, [`Object`](../O/bpy.types.Object.md#bpy.types.Object "bpy.types.Object")

`matrix`, Matrix, [`mathutils.Matrix`](mathutils.md#mathutils.Matrix "mathutils.Matrix") of 4 * 4 items in [-inf, inf]

Return type:
    

(boolean, [`mathutils.Vector`](mathutils.md#mathutils.Vector "mathutils.Vector") of 3 items in [-inf, inf], [`mathutils.Vector`](mathutils.md#mathutils.Vector "mathutils.Vector") of 3 items in [-inf, inf], int in [-inf, inf], [`Object`](../O/bpy.types.Object.md#bpy.types.Object "bpy.types.Object"), [`mathutils.Matrix`](mathutils.md#mathutils.Matrix "mathutils.Matrix") of 4 * 4 items in [-inf, inf])

sequence_editor_create()
    

Ensure sequence editor is valid in this scene

Returns:
    

New sequence editor data or nullptr

Return type:
    

[`SequenceEditor`](bpy.types.SequenceEditor.md#bpy.types.SequenceEditor "bpy.types.SequenceEditor")

sequence_editor_clear()
    

Clear sequence editor in this scene

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

## Inherited Properties

  * [`bpy_struct.id_data`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.id_data "bpy.types.bpy_struct.id_data")
  * [`ID.name`](../I/bpy.types.ID.md#bpy.types.ID.name "bpy.types.ID.name")
  * [`ID.name_full`](../I/bpy.types.ID.md#bpy.types.ID.name_full "bpy.types.ID.name_full")
  * [`ID.id_type`](../I/bpy.types.ID.md#bpy.types.ID.id_type "bpy.types.ID.id_type")
  * [`ID.session_uid`](../I/bpy.types.ID.md#bpy.types.ID.session_uid "bpy.types.ID.session_uid")
  * [`ID.is_evaluated`](../I/bpy.types.ID.md#bpy.types.ID.is_evaluated "bpy.types.ID.is_evaluated")
  * [`ID.original`](../I/bpy.types.ID.md#bpy.types.ID.original "bpy.types.ID.original")
  * [`ID.users`](../I/bpy.types.ID.md#bpy.types.ID.users "bpy.types.ID.users")
  * [`ID.use_fake_user`](../I/bpy.types.ID.md#bpy.types.ID.use_fake_user "bpy.types.ID.use_fake_user")
  * [`ID.use_extra_user`](../I/bpy.types.ID.md#bpy.types.ID.use_extra_user "bpy.types.ID.use_extra_user")
  * [`ID.is_embedded_data`](../I/bpy.types.ID.md#bpy.types.ID.is_embedded_data "bpy.types.ID.is_embedded_data")

| 

  * [`ID.is_linked_packed`](../I/bpy.types.ID.md#bpy.types.ID.is_linked_packed "bpy.types.ID.is_linked_packed")
  * [`ID.is_missing`](../I/bpy.types.ID.md#bpy.types.ID.is_missing "bpy.types.ID.is_missing")
  * [`ID.is_runtime_data`](../I/bpy.types.ID.md#bpy.types.ID.is_runtime_data "bpy.types.ID.is_runtime_data")
  * [`ID.is_editable`](../I/bpy.types.ID.md#bpy.types.ID.is_editable "bpy.types.ID.is_editable")
  * [`ID.tag`](../I/bpy.types.ID.md#bpy.types.ID.tag "bpy.types.ID.tag")
  * [`ID.is_library_indirect`](../I/bpy.types.ID.md#bpy.types.ID.is_library_indirect "bpy.types.ID.is_library_indirect")
  * [`ID.library`](../I/bpy.types.ID.md#bpy.types.ID.library "bpy.types.ID.library")
  * [`ID.library_weak_reference`](../I/bpy.types.ID.md#bpy.types.ID.library_weak_reference "bpy.types.ID.library_weak_reference")
  * [`ID.asset_data`](../I/bpy.types.ID.md#bpy.types.ID.asset_data "bpy.types.ID.asset_data")
  * [`ID.override_library`](../I/bpy.types.ID.md#bpy.types.ID.override_library "bpy.types.ID.override_library")
  * [`ID.preview`](../I/bpy.types.ID.md#bpy.types.ID.preview "bpy.types.ID.preview")

  
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
  * [`bpy_struct.keys`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.keys "bpy.types.bpy_struct.keys")
  * [`bpy_struct.path_from_id`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.path_from_id "bpy.types.bpy_struct.path_from_id")
  * [`bpy_struct.path_from_module`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.path_from_module "bpy.types.bpy_struct.path_from_module")
  * [`bpy_struct.path_resolve`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.path_resolve "bpy.types.bpy_struct.path_resolve")
  * [`bpy_struct.pop`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.pop "bpy.types.bpy_struct.pop")
  * [`bpy_struct.property_overridable_library_set`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.property_overridable_library_set "bpy.types.bpy_struct.property_overridable_library_set")
  * [`bpy_struct.property_unset`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.property_unset "bpy.types.bpy_struct.property_unset")
  * [`bpy_struct.rna_ancestors`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.rna_ancestors "bpy.types.bpy_struct.rna_ancestors")

| 

  * [`bpy_struct.type_recast`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.type_recast "bpy.types.bpy_struct.type_recast")
  * [`bpy_struct.values`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.values "bpy.types.bpy_struct.values")
  * [`ID.bl_system_properties_get`](../I/bpy.types.ID.md#bpy.types.ID.bl_system_properties_get "bpy.types.ID.bl_system_properties_get")
  * [`ID.rename`](../I/bpy.types.ID.md#bpy.types.ID.rename "bpy.types.ID.rename")
  * [`ID.evaluated_get`](../I/bpy.types.ID.md#bpy.types.ID.evaluated_get "bpy.types.ID.evaluated_get")
  * [`ID.copy`](../I/bpy.types.ID.md#bpy.types.ID.copy "bpy.types.ID.copy")
  * [`ID.asset_mark`](../I/bpy.types.ID.md#bpy.types.ID.asset_mark "bpy.types.ID.asset_mark")
  * [`ID.asset_clear`](../I/bpy.types.ID.md#bpy.types.ID.asset_clear "bpy.types.ID.asset_clear")
  * [`ID.asset_generate_preview`](../I/bpy.types.ID.md#bpy.types.ID.asset_generate_preview "bpy.types.ID.asset_generate_preview")
  * [`ID.override_create`](../I/bpy.types.ID.md#bpy.types.ID.override_create "bpy.types.ID.override_create")
  * [`ID.override_hierarchy_create`](../I/bpy.types.ID.md#bpy.types.ID.override_hierarchy_create "bpy.types.ID.override_hierarchy_create")
  * [`ID.user_clear`](../I/bpy.types.ID.md#bpy.types.ID.user_clear "bpy.types.ID.user_clear")
  * [`ID.user_remap`](../I/bpy.types.ID.md#bpy.types.ID.user_remap "bpy.types.ID.user_remap")
  * [`ID.make_local`](../I/bpy.types.ID.md#bpy.types.ID.make_local "bpy.types.ID.make_local")
  * [`ID.user_of_id`](../I/bpy.types.ID.md#bpy.types.ID.user_of_id "bpy.types.ID.user_of_id")
  * [`ID.animation_data_create`](../I/bpy.types.ID.md#bpy.types.ID.animation_data_create "bpy.types.ID.animation_data_create")
  * [`ID.animation_data_clear`](../I/bpy.types.ID.md#bpy.types.ID.animation_data_clear "bpy.types.ID.animation_data_clear")
  * [`ID.update_tag`](../I/bpy.types.ID.md#bpy.types.ID.update_tag "bpy.types.ID.update_tag")
  * [`ID.preview_ensure`](../I/bpy.types.ID.md#bpy.types.ID.preview_ensure "bpy.types.ID.preview_ensure")
  * [`ID.bl_rna_get_subclass`](../I/bpy.types.ID.md#bpy.types.ID.bl_rna_get_subclass "bpy.types.ID.bl_rna_get_subclass")
  * [`ID.bl_rna_get_subclass_py`](../I/bpy.types.ID.md#bpy.types.ID.bl_rna_get_subclass_py "bpy.types.ID.bl_rna_get_subclass_py")

  
---|---  
  
## References

  * [`bpy.context.scene`](../../bpy.context.md#bpy.context.scene "bpy.context.scene")
  * [`bpy.context.sequencer_scene`](../../bpy.context.md#bpy.context.sequencer_scene "bpy.context.sequencer_scene")
  * [`BlendData.scenes`](../B/bpy.types.BlendData.md#bpy.types.BlendData.scenes "bpy.types.BlendData.scenes")
  * [`BlendDataScenes.new`](../B/bpy.types.BlendDataScenes.md#bpy.types.BlendDataScenes.new "bpy.types.BlendDataScenes.new")
  * [`BlendDataScenes.remove`](../B/bpy.types.BlendDataScenes.md#bpy.types.BlendDataScenes.remove "bpy.types.BlendDataScenes.remove")
  * [`Camera.view_frame`](../C/bpy.types.Camera.md#bpy.types.Camera.view_frame "bpy.types.Camera.view_frame")
  * [`CompositorNodeCryptomatteV2.scene`](../C/bpy.types.CompositorNodeCryptomatteV2.md#bpy.types.CompositorNodeCryptomatteV2.scene "bpy.types.CompositorNodeCryptomatteV2.scene")
  * [`CompositorNodeDefocus.scene`](../C/bpy.types.CompositorNodeDefocus.md#bpy.types.CompositorNodeDefocus.scene "bpy.types.CompositorNodeDefocus.scene")
  * [`CompositorNodeRLayers.scene`](../C/bpy.types.CompositorNodeRLayers.md#bpy.types.CompositorNodeRLayers.scene "bpy.types.CompositorNodeRLayers.scene")
  * [`Context.scene`](../C/bpy.types.Context.md#bpy.types.Context.scene "bpy.types.Context.scene")
  * [`Depsgraph.scene`](../D/bpy.types.Depsgraph.md#bpy.types.Depsgraph.scene "bpy.types.Depsgraph.scene")
  * [`Depsgraph.scene_eval`](../D/bpy.types.Depsgraph.md#bpy.types.Depsgraph.scene_eval "bpy.types.Depsgraph.scene_eval")
  * [`ID.override_hierarchy_create`](../I/bpy.types.ID.md#bpy.types.ID.override_hierarchy_create "bpy.types.ID.override_hierarchy_create")
  * [`IDOverrideLibrary.resync`](../I/bpy.types.IDOverrideLibrary.md#bpy.types.IDOverrideLibrary.resync "bpy.types.IDOverrideLibrary.resync")
  * [`Image.save_render`](../I/bpy.types.Image.md#bpy.types.Image.save_render "bpy.types.Image.save_render")

| 

  * [`Object.crazyspace_eval`](../O/bpy.types.Object.md#bpy.types.Object.crazyspace_eval "bpy.types.Object.crazyspace_eval")
  * [`Object.is_deform_modified`](../O/bpy.types.Object.md#bpy.types.Object.is_deform_modified "bpy.types.Object.is_deform_modified")
  * [`Object.is_modified`](../O/bpy.types.Object.md#bpy.types.Object.is_modified "bpy.types.Object.is_modified")
  * [`RenderEngine.bind_display_space_shader`](../R/bpy.types.RenderEngine.md#bpy.types.RenderEngine.bind_display_space_shader "bpy.types.RenderEngine.bind_display_space_shader")
  * [`RenderEngine.get_preview_pixel_size`](../R/bpy.types.RenderEngine.md#bpy.types.RenderEngine.get_preview_pixel_size "bpy.types.RenderEngine.get_preview_pixel_size")
  * [`RenderEngine.register_pass`](../R/bpy.types.RenderEngine.md#bpy.types.RenderEngine.register_pass "bpy.types.RenderEngine.register_pass")
  * [`RenderEngine.support_display_space_shader`](../R/bpy.types.RenderEngine.md#bpy.types.RenderEngine.support_display_space_shader "bpy.types.RenderEngine.support_display_space_shader")
  * [`RenderEngine.update_render_passes`](../R/bpy.types.RenderEngine.md#bpy.types.RenderEngine.update_render_passes "bpy.types.RenderEngine.update_render_passes")
  * `Scene.background_set`
  * [`SceneStrip.scene`](bpy.types.SceneStrip.md#bpy.types.SceneStrip.scene "bpy.types.SceneStrip.scene")
  * [`StripsMeta.new_scene`](bpy.types.StripsMeta.md#bpy.types.StripsMeta.new_scene "bpy.types.StripsMeta.new_scene")
  * [`StripsTopLevel.new_scene`](bpy.types.StripsTopLevel.md#bpy.types.StripsTopLevel.new_scene "bpy.types.StripsTopLevel.new_scene")
  * [`Window.scene`](../W/bpy.types.Window.md#bpy.types.Window.scene "bpy.types.Window.scene")
  * [`WorkSpace.sequencer_scene`](../W/bpy.types.WorkSpace.md#bpy.types.WorkSpace.sequencer_scene "bpy.types.WorkSpace.sequencer_scene")

  
---|---
  *[*]: Keyword-only parameters separator (PEP 3102)
  *[/]: Positional-only parameter separator (PEP 570)
