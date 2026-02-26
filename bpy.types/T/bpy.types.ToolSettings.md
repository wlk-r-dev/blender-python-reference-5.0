# ToolSettings(bpy_struct)

base class — [[bpy_struct]]

_class _bpy.types.ToolSettings(_bpy_struct_)
    

anim_fix_to_cam_use_loc
    

Create location keys when fixing to the scene camera

Type:
    

boolean, default True

anim_fix_to_cam_use_rot
    

Create rotation keys when fixing to the scene camera

Type:
    

boolean, default True

anim_fix_to_cam_use_scale
    

Create scale keys when fixing to the scene camera

Type:
    

boolean, default True

anim_mirror_bone
    

Bone to use for the mirroring

Type:
    

string, default “”, (never None)

anim_mirror_object
    

Object to mirror over. Leave empty and name a bone to always mirror over that bone of the active armature

Type:
    

[[Object]]

anim_relative_object
    

Object to which matrices are made relative

Type:
    

[[Object]]

annotation_stroke_placement_view2d
    

  * `IMAGE` Image – Stick stroke to the image.

  * `VIEW` View – Stick stroke to the view.


Type:
    

enum in [`'IMAGE'`, `'VIEW'`], default `'IMAGE'`

annotation_stroke_placement_view3d
    

How annotation strokes are orientated in 3D space

  * `CURSOR` 3D Cursor – Draw stroke at 3D cursor location.

  * `VIEW` View – Stick stroke to the view.

  * `SURFACE` Surface – Stick stroke to surfaces.


Type:
    

enum in [`'CURSOR'`, `'VIEW'`, `'SURFACE'`], default `'CURSOR'`

annotation_thickness
    

Thickness of annotation strokes

Type:
    

int in [1, 10], default 3

auto_keying_mode
    

Mode of automatic keyframe insertion for objects, bones and masks

Type:
    

enum in [`'ADD_REPLACE_KEYS'`, `'REPLACE_KEYS'`], default `'ADD_REPLACE_KEYS'`

curve_paint_settings
    

Type:
    

[[CurvePaintSettings]], (readonly, never None)

curves_sculpt
    

Type:
    

[[CurvesSculpt]], (readonly)

custom_bevel_profile_preset
    

Used for defining a profile’s path

Type:
    

[[CurveProfile]], (readonly)

double_threshold
    

Threshold distance for Auto Merge

Type:
    

float in [0, 1], default 0.001

gpencil_interpolate
    

Settings for Grease Pencil interpolation tools

Type:
    

[[GPencilInterpolateSettings]], (readonly)

gpencil_paint
    

Type:
    

[[GpPaint]], (readonly)

gpencil_sculpt
    

Settings for stroke sculpting tools and brushes

Type:
    

[[GPencilSculptSettings]], (readonly)

gpencil_sculpt_paint
    

Type:
    

[[GpSculptPaint]], (readonly)

gpencil_selectmode_edit
    

Type:
    

enum in [Grease Pencil Selectmode Items](../../bpy_types_enum_items/grease_pencil_selectmode_items.md#rna-enum-grease-pencil-selectmode-items), default `'POINT'`

gpencil_stroke_placement_view3d
    

  * `ORIGIN` Origin – Draw stroke at Object origin.

  * `CURSOR` 3D Cursor – Draw stroke at 3D cursor location.

  * `SURFACE` Surface – Stick stroke to surfaces.

  * `STROKE` Stroke – Stick stroke to other strokes.


Type:
    

enum in [`'ORIGIN'`, `'CURSOR'`, `'SURFACE'`, `'STROKE'`], default `'ORIGIN'`

gpencil_stroke_snap_mode
    

  * `NONE` All Points – Snap to all points.

  * `ENDS` End Points – Snap to first and last points and interpolate.

  * `FIRST` First Point – Snap to first point.


Type:
    

enum in [`'NONE'`, `'ENDS'`, `'FIRST'`], default `'NONE'`

gpencil_surface_offset
    

Offset along the normal when drawing on surfaces

Type:
    

float in [0, 1], default 0.15

gpencil_vertex_paint
    

Type:
    

[[GpVertexPaint]], (readonly)

gpencil_weight_paint
    

Type:
    

[[GpWeightPaint]], (readonly)

image_paint
    

Type:
    

[[ImagePaint]], (readonly)

keyframe_type
    

Type of keyframes to create when inserting keyframes

Type:
    

enum in [Beztriple Keyframe Type Items](../../bpy_types_enum_items/beztriple_keyframe_type_items.md#rna-enum-beztriple-keyframe-type-items), default `'KEYFRAME'`

lock_markers
    

Prevent marker editing

Type:
    

boolean, default False

lock_object_mode
    

Restrict selection to objects using the same mode as the active object, to prevent accidental mode switch when selecting

Type:
    

boolean, default True

mesh_select_mode
    

Which mesh elements selection works on

Type:
    

boolean array of 3 items, default (False, False, False)

normal_vector
    

Normal vector used to copy, add or multiply

Type:
    

[[mathutils.Vector]] of 3 items in [-inf, inf], default (0.0, 0.0, 0.0)

paint_mode
    

Type:
    

[[PaintModeSettings]], (readonly)

particle_edit
    

Type:
    

[[ParticleEdit]], (readonly)

plane_axis
    

The axis used for placing the base region

Type:
    

enum in [Axis Xyz Items](../../bpy_types_enum_items/axis_xyz_items.md#rna-enum-axis-xyz-items), default `'Z'`

plane_axis_auto
    

Select the closest axis when placing objects (surface overrides)

Type:
    

boolean, default True

plane_depth
    

The initial depth used when placing the cursor

  * `SURFACE` Surface – Start placing on the surface, using the 3D cursor position as a fallback.

  * `CURSOR_PLANE` Cursor Plane – Start placement using a point projected onto the orientation axis at the 3D cursor position.

  * `CURSOR_VIEW` Cursor View – Start placement using a point projected onto the view plane at the 3D cursor position.


Type:
    

enum in [`'SURFACE'`, `'CURSOR_PLANE'`, `'CURSOR_VIEW'`], default `'SURFACE'`

plane_orientation
    

The initial depth used when placing the cursor

  * `SURFACE` Surface – Use the surface normal (using the transform orientation as a fallback).

  * `DEFAULT` Default – Use the current transform orientation.


Type:
    

enum in [`'SURFACE'`, `'DEFAULT'`], default `'SURFACE'`

playhead_snap_distance
    

Maximum distance for snapping in pixels

Type:
    

int in [-inf, inf], default 20

proportional_distance
    

Display size for proportional editing circle

Type:
    

float in [1e-05, 5000], default 1.0

proportional_edit_falloff
    

Falloff type for proportional editing mode

Type:
    

enum in [Proportional Falloff Items](../../bpy_types_enum_items/proportional_falloff_items.md#rna-enum-proportional-falloff-items), default `'SMOOTH'`

proportional_size
    

Display size for proportional editing circle

Type:
    

float in [1e-05, 5000], default 1.0

sculpt
    

Type:
    

[[Sculpt]], (readonly)

sequencer_tool_settings
    

Type:
    

[[SequencerToolSettings]], (readonly, never None)

show_uv_local_view
    

Display only faces with the currently displayed image assigned

Type:
    

boolean, default False

snap_angle_increment_2d
    

Angle used for rotation increments in 2D editors

Type:
    

float in [0, 3.14159], default 0.0872665

snap_angle_increment_2d_precision
    

Precision angle used for rotation increments in 2D editors

Type:
    

float in [0, 3.14159], default 0.0174533

snap_angle_increment_3d
    

Angle used for rotation increments in 3D editors

Type:
    

float in [0, 3.14159], default 0.0872665

snap_angle_increment_3d_precision
    

Precision angle used for rotation increments in 3D editors

Type:
    

float in [0, 3.14159], default 0.0174533

snap_anim_element
    

Type of element to snap to

Type:
    

enum in [Snap Animation Element Items](../../bpy_types_enum_items/snap_animation_element_items.md#rna-enum-snap-animation-element-items), default `'FRAME'`

snap_elements
    

Type of element to snap to

Type:
    

enum set in [Snap Element Items](../../bpy_types_enum_items/snap_element_items.md#rna-enum-snap-element-items), default {`'INCREMENT'`}

snap_elements_base
    

Type of element for the “Snap Base” to snap to

  * `INCREMENT` Increment – Snap to increments.

  * `GRID` Grid – Snap to grid.

  * `VERTEX` Vertex – Snap to vertices.

  * `EDGE` Edge – Snap to edges.

  * `FACE` Face – Snap by projecting onto faces.

  * `VOLUME` Volume – Snap to volume.

  * `EDGE_MIDPOINT` Edge Center – Snap to the middle of edges.

  * `EDGE_PERPENDICULAR` Edge Perpendicular – Snap to the nearest point on an edge.


Type:
    

enum set in {`'INCREMENT'`, `'GRID'`, `'VERTEX'`, `'EDGE'`, `'FACE'`, `'VOLUME'`, `'EDGE_MIDPOINT'`, `'EDGE_PERPENDICULAR'`}, default {`'INCREMENT'`}

snap_elements_individual
    

Type of element for individual transformed elements to snap to

  * `FACE_PROJECT` Face Project – Snap by projecting onto faces.

  * `FACE_NEAREST` Face Nearest – Snap to nearest point on faces.


Type:
    

enum set in {`'FACE_PROJECT'`, `'FACE_NEAREST'`}, default set()

snap_elements_tool
    

The target to use while snapping

  * `GEOMETRY` Geometry – Snap to all geometry.

  * `DEFAULT` Default – Use the current snap settings.


Type:
    

enum in [`'GEOMETRY'`, `'DEFAULT'`], default `'GEOMETRY'`

snap_face_nearest_steps
    

Number of steps to break transformation into for face nearest snapping

Type:
    

int in [1, 100], default 1

snap_playhead_element
    

Type of element to snap to

  * `FRAME` Frames – Snap to frame increments.

  * `SECOND` Seconds – Snap to second increments.

  * `MARKER` Markers – Snap to markers.

  * `KEY` Keyframes – Snap to keyframes.

  * `Strip` Strips – Snap to Strips.


Type:
    

enum set in {`'FRAME'`, `'SECOND'`, `'MARKER'`, `'KEY'`, `'Strip'`}, default {`'KEY'`, `'Strip'`}

snap_playhead_frame_step
    

At which interval to snap to frames

Type:
    

int in [1, 32768], default 2

snap_playhead_second_step
    

At which interval to snap to seconds

Type:
    

int in [1, 32768], default 1

snap_target
    

Which part to snap onto the target

Type:
    

enum in [Snap Source Items](../../bpy_types_enum_items/snap_source_items.md#rna-enum-snap-source-items), default `'CLOSEST'`

snap_uv_element
    

Type of element to snap to

  * `INCREMENT` Increment – Snap to increments of grid.

  * `GRID` Grid – Snap to grid.

  * `VERTEX` Vertex – Snap to vertices.


Type:
    

enum set in {`'INCREMENT'`, `'GRID'`, `'VERTEX'`}, default {`'INCREMENT'`}

statvis
    

Type:
    

[[MeshStatVis]], (readonly, never None)

transform_pivot_point
    

Pivot center for rotation/scaling

  * `BOUNDING_BOX_CENTER` Bounding Box Center – Pivot around bounding box center of selected object(s).

  * `CURSOR` 3D Cursor – Pivot around the 3D cursor.

  * `INDIVIDUAL_ORIGINS` Individual Origins – Pivot around each object’s own origin.

  * `MEDIAN_POINT` Median Point – Pivot around the median point of selected objects.

  * `ACTIVE_ELEMENT` Active Element – Pivot around active object.


Type:
    

enum in [`'BOUNDING_BOX_CENTER'`, `'CURSOR'`, `'INDIVIDUAL_ORIGINS'`, `'MEDIAN_POINT'`, `'ACTIVE_ELEMENT'`], default `'MEDIAN_POINT'`

use_annotation_project_only_selected
    

Project the strokes only onto selected objects

Type:
    

boolean, default False

use_annotation_stroke_endpoints
    

Only use the first and last parts of the stroke for snapping

Type:
    

boolean, default False

use_auto_normalize
    

Ensure all bone-deforming vertex groups add up to 1.0 while weight painting or assigning to vertices

Type:
    

boolean, default False

use_edge_path_live_unwrap
    

Changing edge seams recalculates UV unwrap

Type:
    

boolean, default False

use_gpencil_automerge_strokes
    

Join the last drawn stroke with previous strokes in the active layer by distance

Type:
    

boolean, default False

use_gpencil_draw_additive
    

When creating new frames, the strokes from the previous/active frame are included as the basis for the new one

Type:
    

boolean, default False

use_gpencil_draw_onback
    

New strokes are drawn below of all strokes in the layer

Type:
    

boolean, default False

use_gpencil_project_only_selected
    

Project the strokes only onto selected objects

Type:
    

boolean, default False

use_gpencil_select_mask_point
    

Only sculpt selected stroke points

Type:
    

boolean, default False

use_gpencil_select_mask_segment
    

Only sculpt selected stroke points between other strokes

Type:
    

boolean, default False

use_gpencil_select_mask_stroke
    

Only sculpt selected strokes

Type:
    

boolean, default False

use_gpencil_thumbnail_list
    

Show compact list of colors instead of thumbnails

Type:
    

boolean, default True

use_gpencil_vertex_select_mask_point
    

Only paint selected stroke points

Type:
    

boolean, default False

use_gpencil_vertex_select_mask_segment
    

Only paint selected stroke points between other strokes

Type:
    

boolean, default False

use_gpencil_vertex_select_mask_stroke
    

Only paint selected strokes

Type:
    

boolean, default False

use_gpencil_weight_data_add
    

Weight data for new strokes is added according to the current vertex group and weight. If no vertex group selected, weight is not added.

Type:
    

boolean, default False

use_grease_pencil_multi_frame_editing
    

Enable multi-frame editing

Type:
    

boolean, default False

use_keyframe_cycle_aware
    

For channels with cyclic extrapolation, keyframe insertion is automatically remapped inside the cycle time range, and keeps ends in sync. Curves newly added to actions with a Manual Frame Range and Cyclic Animation are automatically made cyclic.

Type:
    

boolean, default False

use_keyframe_insert_auto
    

Automatic keyframe insertion for objects, bones and masks

Type:
    

boolean, default True

use_keyframe_insert_keyingset
    

Automatic keyframe insertion using active Keying Set only

Type:
    

boolean, default False

use_lock_relative
    

Display bone-deforming groups as if all locked deform groups were deleted, and the remaining ones were re-normalized

Type:
    

boolean, default False

use_mesh_automerge
    

Automatically merge vertices moved to the same location

Type:
    

boolean, default False

use_mesh_automerge_and_split
    

Automatically split edges and faces

Type:
    

boolean, default False

use_multipaint
    

Paint across the weights of all selected bones, maintaining their relative influence

Type:
    

boolean, default False

use_proportional_action
    

Proportional editing in action editor

Type:
    

boolean, default False

use_proportional_connected
    

Proportional Editing using connected geometry only

Type:
    

boolean, default False

use_proportional_edit
    

Proportional edit mode

Type:
    

boolean, default False

use_proportional_edit_mask
    

Proportional editing mask mode

Type:
    

boolean, default False

use_proportional_edit_objects
    

Proportional editing object mode

Type:
    

boolean, default False

use_proportional_fcurve
    

Proportional editing in F-Curve editor

Type:
    

boolean, default False

use_proportional_projected
    

Proportional Editing using screen space locations

Type:
    

boolean, default False

use_record_with_nla
    

Add a new NLA Track + Strip for every loop/pass made over the animation to allow non-destructive tweaking

Type:
    

boolean, default False

use_snap
    

Snap during transform

Type:
    

boolean, default False

use_snap_align_rotation
    

Align rotation with the snapping target

Type:
    

boolean, default False

use_snap_anim
    

Enable snapping when transforming keyframes

Type:
    

boolean, default True

use_snap_backface_culling
    

Exclude back facing geometry from snapping

Type:
    

boolean, default False

use_snap_driver
    

Enable snapping when transforming keys in the Driver Editor

Type:
    

boolean, default False

use_snap_driver_absolute
    

Snap to full values

Type:
    

boolean, default False

use_snap_edit
    

Snap onto non-active objects in edit mode (edit mode only)

Type:
    

boolean, default True

use_snap_grid_absolute
    

Absolute grid alignment while translating (based on the pivot center)

Type:
    

boolean, default False

use_snap_node
    

Snap Node during transform

Type:
    

boolean, default False

use_snap_nonedit
    

Snap onto objects not in edit mode (edit mode only)

Type:
    

boolean, default True

use_snap_peel_object
    

Consider objects as whole when finding volume center

Type:
    

boolean, default False

use_snap_playhead
    

Snap playhead when scrubbing

Type:
    

boolean, default False

use_snap_rotate
    

Rotate is affected by the snapping settings

Type:
    

boolean, default False

use_snap_scale
    

Scale is affected by snapping settings

Type:
    

boolean, default False

use_snap_selectable
    

Snap only onto objects that are selectable

Type:
    

boolean, default False

use_snap_self
    

Snap onto itself only if enabled (edit mode only)

Type:
    

boolean, default True

use_snap_sequencer
    

Snap strips during transform

Type:
    

boolean, default True

use_snap_time_absolute
    

Absolute time alignment when transforming keyframes

Type:
    

boolean, default False

use_snap_to_same_target
    

Snap only to target that source was initially near (“Face Nearest” only)

Type:
    

boolean, default False

use_snap_translate
    

Move is affected by snapping settings

Type:
    

boolean, default True

use_snap_uv
    

Snap UV during transform

Type:
    

boolean, default False

use_transform_correct_face_attributes
    

Correct data such as UVs and color attributes when transforming

Type:
    

boolean, default False

use_transform_correct_keep_connected
    

During the Face Attributes correction, merge attributes connected to the same vertex

Type:
    

boolean, default False

use_transform_data_origin
    

Transform object origins, while leaving the shape in place

Type:
    

boolean, default False

use_transform_pivot_point_align
    

Only transform object locations, without affecting rotation or scaling

Type:
    

boolean, default False

use_transform_skip_children
    

Transform the parents, leaving the children in place

Type:
    

boolean, default False

use_uv_custom_region
    

Custom defined region

Type:
    

boolean, default False

use_uv_select_island
    

Island selection

Type:
    

boolean, default False

use_uv_select_sync
    

Keep UV and edit mode mesh selection in sync

Type:
    

boolean, default True

uv_sculpt
    

Type:
    

[[UvSculpt]], (readonly)

uv_sculpt_all_islands
    

Brush operates on all islands

Type:
    

boolean, default False

uv_sculpt_lock_borders
    

Disable editing of boundary edges

Type:
    

boolean, default False

uv_select_mode
    

UV selection and display mode

Type:
    

enum in [Mesh Select Mode Uv Items](../../bpy_types_enum_items/mesh_select_mode_uv_items.md#rna-enum-mesh-select-mode-uv-items), default `'VERTEX'`

uv_sticky_select_mode
    

Method for extending UV vertex selection

  * `DISABLED` Disabled – Sticky vertex selection disabled.

  * `SHARED_LOCATION` Shared Location – Select UVs that are at the same location and share a mesh vertex.

  * `SHARED_VERTEX` Shared Vertex – Select UVs that share a mesh vertex, whether or not they are at the same location.


Type:
    

enum in [`'DISABLED'`, `'SHARED_LOCATION'`, `'SHARED_VERTEX'`], default `'SHARED_LOCATION'`

vertex_group_subset
    

Filter Vertex groups for Display

  * `ALL` All – All Vertex Groups.

  * `BONE_DEFORM` Deform – Vertex Groups assigned to Deform Bones.

  * `OTHER_DEFORM` Other – Vertex Groups assigned to non Deform Bones.


Type:
    

enum in [`'ALL'`, `'BONE_DEFORM'`, `'OTHER_DEFORM'`], default `'ALL'`

vertex_group_user
    

Display unweighted vertices

  * `NONE` None.

  * `ACTIVE` Active – Show vertices with no weights in the active group.

  * `ALL` All – Show vertices with no weights in any group.


Type:
    

enum in [`'NONE'`, `'ACTIVE'`, `'ALL'`], default `'ACTIVE'`

vertex_group_weight
    

Weight to assign in vertex groups

Type:
    

float in [0, 1], default 1.0

vertex_paint
    

Type:
    

[[VertexPaint]], (readonly)

weight_paint
    

Type:
    

[[VertexPaint]], (readonly)

workspace_tool_type
    

Action when dragging in the viewport

Type:
    

enum in [`'DEFAULT'`, `'FALLBACK'`], default `'FALLBACK'`

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

  * [[bpy.context.tool_settings]]
  * [[Context.tool_settings]]

| 

  * [[Scene.tool_settings]]

  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
