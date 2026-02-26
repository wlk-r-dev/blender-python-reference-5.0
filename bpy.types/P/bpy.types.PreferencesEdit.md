# PreferencesEdit(bpy_struct)

base class — [`bpy_struct`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct "bpy.types.bpy_struct")

_class _bpy.types.PreferencesEdit(_bpy_struct_)
    

Settings for interacting with Blender data

auto_keying_mode
    

Mode of automatic keyframe insertion for Objects and Bones (default setting used for new Scenes)

Type:
    

enum in [`'ADD_REPLACE_KEYS'`, `'REPLACE_KEYS'`], default `'ADD_REPLACE_KEYS'`

collection_instance_empty_size
    

Display size of the empty when new collection instances are created

Type:
    

float in [0.001, inf], default 1.0

connect_strips_by_default
    

Connect newly added movie strips by default if they have multiple channels

Type:
    

boolean, default True

fcurve_new_auto_smoothing
    

Auto Handle Smoothing mode used for newly added F-Curves

Type:
    

enum in [Fcurve Auto Smoothing Items](../../bpy_types_enum_items/fcurve_auto_smoothing_items.md#rna-enum-fcurve-auto-smoothing-items), default `'CONT_ACCEL'`

fcurve_unselected_alpha
    

The opacity of unselected F-Curves against the background of the Graph Editor

Type:
    

float in [0.001, 1], default 0.25

grease_pencil_default_color
    

Color of new annotation layers

Type:
    

float array of 4 items in [0, inf], default (0.38, 0.61, 0.78, 0.9)

grease_pencil_eraser_radius
    

Radius of eraser ‘brush’

Type:
    

int in [1, 500], default 25

grease_pencil_euclidean_distance
    

Distance moved by mouse when drawing stroke to include

Type:
    

int in [0, 100], default 2

grease_pencil_manhattan_distance
    

Pixels moved by mouse per axis when drawing stroke

Type:
    

int in [0, 100], default 1

key_insert_channels
    

Which channels to insert keys at when no keying set is active

Type:
    

enum set in {`'LOCATION'`, `'ROTATION'`, `'SCALE'`, `'ROTATE_MODE'`, `'CUSTOM_PROPS'`}, default {`'CUSTOM_PROPS'`, `'LOCATION'`, `'ROTATION'`, `'SCALE'`}

keyframe_new_handle_type
    

Handle type for handles of new keyframes

Type:
    

enum in [Keyframe Handle Type Items](../../bpy_types_enum_items/keyframe_handle_type_items.md#rna-enum-keyframe-handle-type-items), default `'AUTO_CLAMPED'`

keyframe_new_interpolation_type
    

Interpolation mode used for first keyframe on newly added F-Curves (subsequent keyframes take interpolation from preceding keyframe)

Type:
    

enum in [Beztriple Interpolation Mode Items](../../bpy_types_enum_items/beztriple_interpolation_mode_items.md#rna-enum-beztriple-interpolation-mode-items), default `'BEZIER'`

material_link
    

Toggle whether the material is linked to object data or the object block

  * `OBDATA` Object Data – Toggle whether the material is linked to object data or the object block.

  * `OBJECT` Object – Toggle whether the material is linked to object data or the object block.


Type:
    

enum in [`'OBDATA'`, `'OBJECT'`], default `'OBDATA'`

node_margin
    

Minimum distance between nodes for Auto-offsetting nodes

Type:
    

int in [0, 255], default 40

node_preview_resolution
    

Resolution used for Shader node previews (should be changed for performance convenience)

Type:
    

int in [50, 250], default 120

node_use_insert_offset
    

Automatically offset the following or previous nodes in a chain when inserting a new node

Type:
    

boolean, default True

object_align
    

The default alignment for objects added from a 3D viewport menu

  * `WORLD` World – Align newly added objects to the world coordinate system.

  * `VIEW` View – Align newly added objects to the active 3D view orientation.

  * `CURSOR` 3D Cursor – Align newly added objects to the 3D Cursor’s rotation.


Type:
    

enum in [`'WORLD'`, `'VIEW'`, `'CURSOR'`], default `'WORLD'`

sculpt_paint_overlay_color
    

Color of texture overlay

Type:
    

[`mathutils.Color`](mathutils.md#mathutils.Color "mathutils.Color") of 3 items in [0, inf], default (0.0, 0.0, 0.0)

show_only_selected_curve_keyframes
    

Only keyframes of selected F-Curves are visible and editable

Type:
    

boolean, default False

undo_memory_limit
    

Maximum memory usage in megabytes (0 means unlimited)

Type:
    

int in [0, inf], default 0

undo_steps
    

Number of undo steps available (smaller values conserve memory)

Type:
    

int in [0, 256], default 32

use_anim_channel_group_colors
    

Use animation channel group colors; generally this is used to show bone group colors

Type:
    

boolean, default False

use_auto_keyframe_insert_needed
    

Auto-Keying will skip inserting keys that don’t affect the animation

Type:
    

boolean, default True

use_auto_keying
    

Automatic keyframe insertion for Objects and Bones (default setting used for new Scenes)

Type:
    

boolean, default False

use_auto_keying_warning
    

Show warning indicators when transforming objects and bones if auto keying is enabled

Type:
    

boolean, default True

use_cursor_lock_adjust
    

Place the cursor without ‘jumping’ to the new location (when lock-to-cursor is used)

Type:
    

boolean, default True

use_duplicate_action
    

Causes actions to be duplicated with the data-blocks

Type:
    

boolean, default True

use_duplicate_armature
    

Causes armature data to be duplicated with the object

Type:
    

boolean, default True

use_duplicate_camera
    

Causes camera data to be duplicated with the object

Type:
    

boolean, default True

use_duplicate_curve
    

Causes curve data to be duplicated with the object

Type:
    

boolean, default True

use_duplicate_curves
    

Causes curves data to be duplicated with the object

Type:
    

boolean, default True

use_duplicate_grease_pencil
    

Causes Grease Pencil data to be duplicated with the object

Type:
    

boolean, default True

use_duplicate_lattice
    

Causes lattice data to be duplicated with the object

Type:
    

boolean, default True

use_duplicate_light
    

Causes light data to be duplicated with the object

Type:
    

boolean, default True

use_duplicate_lightprobe
    

Causes light probe data to be duplicated with the object

Type:
    

boolean, default True

use_duplicate_material
    

Causes material data to be duplicated with the object

Type:
    

boolean, default False

use_duplicate_mesh
    

Causes mesh data to be duplicated with the object

Type:
    

boolean, default True

use_duplicate_metaball
    

Causes metaball data to be duplicated with the object

Type:
    

boolean, default True

use_duplicate_node_tree
    

Make copies of node groups when duplicating nodes in the node editor

Type:
    

boolean, default False

use_duplicate_particle
    

Causes particle systems to be duplicated with the object

Type:
    

boolean, default False

use_duplicate_pointcloud
    

Causes point cloud data to be duplicated with the object

Type:
    

boolean, default True

use_duplicate_speaker
    

Causes speaker data to be duplicated with the object

Type:
    

boolean, default True

use_duplicate_surface
    

Causes surface data to be duplicated with the object

Type:
    

boolean, default True

use_duplicate_text
    

Causes text data to be duplicated with the object

Type:
    

boolean, default True

use_duplicate_volume
    

Causes volume data to be duplicated with the object

Type:
    

boolean, default False

use_enter_edit_mode
    

Enter edit mode automatically after adding a new object

Type:
    

boolean, default False

use_fcurve_high_quality_drawing
    

Draw F-Curves using Anti-Aliasing (disable for better performance)

Type:
    

boolean, default True

use_global_undo
    

Global undo works by keeping a full copy of the file itself in memory, so takes extra memory

Type:
    

boolean, default True

use_insertkey_xyz_to_rgb
    

Color for newly added transformation F-Curves (Location, Rotation, Scale) and also Color is based on the transform axis

Type:
    

boolean, default True

use_keyframe_insert_available
    

Insert Keyframes only for properties that are already animated

Type:
    

boolean, default False

use_keyframe_insert_needed
    

When keying manually, skip inserting keys that don’t affect the animation

Type:
    

boolean, default False

use_mouse_depth_cursor
    

Use the surface depth for cursor placement

Type:
    

boolean, default True

use_negative_frames
    

Current frame number can be manually set to a negative value

Type:
    

boolean, default False

use_text_edit_auto_close
    

Automatically close relevant character pairs when typing in the text editor

Type:
    

boolean, default False

use_visual_keying
    

Use Visual keying automatically for constrained objects

Type:
    

boolean, default False

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

  * [`Preferences.edit`](bpy.types.Preferences.md#bpy.types.Preferences.edit "bpy.types.Preferences.edit")

| 


  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
