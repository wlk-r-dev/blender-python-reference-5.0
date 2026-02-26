# View3DOverlay(bpy_struct)

base class — [`bpy_struct`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct "bpy.types.bpy_struct")

_class _bpy.types.View3DOverlay(_bpy_struct_)
    

Settings for display of overlays in the 3D viewport

bone_wire_alpha
    

Maximum opacity of bones in wireframe display mode

Type:
    

float in [0, inf], default 1.0

display_handle
    

Limit the display of curve handles in edit mode

Type:
    

enum in [`'NONE'`, `'SELECTED'`, `'ALL'`], default `'SELECTED'`

fade_inactive_alpha
    

Strength of the fade effect

Type:
    

float in [0, 1], default 0.4

gpencil_fade_layer
    

Fade layer opacity for Grease Pencil layers except the active one

Type:
    

float in [0, 1], default 0.5

gpencil_fade_objects
    

Fade factor

Type:
    

float in [0, 1], default 0.5

gpencil_grid_color
    

Canvas grid color

Type:
    

[`mathutils.Color`](mathutils.md#mathutils.Color "mathutils.Color") of 3 items in [0, 1], default (0.5, 0.5, 0.5)

gpencil_grid_offset
    

Canvas grid offset

Type:
    

float array of 2 items in [-inf, inf], default (0.0, 0.0)

gpencil_grid_opacity
    

Canvas grid opacity

Type:
    

float in [0.1, 1], default 0.9

gpencil_grid_scale
    

Canvas grid scale

Type:
    

[`mathutils.Vector`](mathutils.md#mathutils.Vector "mathutils.Vector") of 2 items in [0, inf], default (1.0, 1.0)

gpencil_grid_subdivisions
    

Canvas grid subdivisions

Type:
    

int in [1, 100], default 4

gpencil_vertex_paint_opacity
    

Vertex Paint mix factor

Type:
    

float in [0, 1], default 1.0

grid_lines
    

Number of grid lines to display in perspective view

Type:
    

int in [0, 1024], default 16

grid_scale
    

Multiplier for the distance between 3D View grid lines

Type:
    

float in [0, inf], default 1.0

grid_scale_unit
    

Grid cell size scaled by scene unit system settings

Type:
    

float in [-inf, inf], default 0.0, (readonly)

grid_subdivisions
    

Number of subdivisions between grid lines

Type:
    

int in [1, 1024], default 10

normals_constant_screen_size
    

Screen size for normals in the 3D view

Type:
    

float in [0, 100000], default 7.0

normals_length
    

Display size for normals in the 3D view

Type:
    

float in [1e-05, 100000], default 0.1

retopology_offset
    

Offset used to draw edit mesh in front of other geometry

Type:
    

float in [0, inf], default 0.01

sculpt_curves_cage_opacity
    

Opacity of the cage overlay in curves sculpt mode

Type:
    

float in [0, 1], default 0.0

sculpt_mode_face_sets_opacity
    

Type:
    

float in [0, 1], default 1.0

sculpt_mode_mask_opacity
    

Type:
    

float in [0, 1], default 0.75

show_annotation
    

Show annotations for this view

Type:
    

boolean, default True

show_axis_x
    

Show the X axis line

Type:
    

boolean, default True

show_axis_y
    

Show the Y axis line

Type:
    

boolean, default True

show_axis_z
    

Show the Z axis line

Type:
    

boolean, default False

show_bones
    

Display bones (disable to show motion paths only)

Type:
    

boolean, default True

show_camera_guides
    

Show camera composition guides

Type:
    

boolean, default True

show_camera_passepartout
    

Show camera passepartout

Type:
    

boolean, default True

show_cursor
    

Display 3D Cursor Overlay

Type:
    

boolean, default True

show_curve_normals
    

Display 3D curve normals in editmode

Type:
    

boolean, default False

show_edge_bevel_weight
    

Display weights created for the Bevel modifier

Type:
    

boolean, default True

show_edge_crease
    

Display creases created for Subdivision Surface modifier

Type:
    

boolean, default True

show_edge_seams
    

Display UV unwrapping seams

Type:
    

boolean, default True

show_edge_sharp
    

Display sharp edges, used with the Edge Split modifier

Type:
    

boolean, default True

show_extra_edge_angle
    

Display selected edge angle, using global values when set in the transform panel

Type:
    

boolean, default False

show_extra_edge_length
    

Display selected edge lengths, using global values when set in the transform panel

Type:
    

boolean, default False

show_extra_face_angle
    

Display the angles in the selected edges, using global values when set in the transform panel

Type:
    

boolean, default False

show_extra_face_area
    

Display the area of selected faces, using global values when set in the transform panel

Type:
    

boolean, default False

show_extra_indices
    

Display the index numbers of selected vertices, edges, and faces

Type:
    

boolean, default False

show_extras
    

Object details, including empty wire, cameras and other visual guides

Type:
    

boolean, default True

show_face_center
    

Display face center when face selection is enabled in solid shading modes

Type:
    

boolean, default False

show_face_normals
    

Display face normals as lines

Type:
    

boolean, default False

show_face_orientation
    

Show the Face Orientation Overlay

Type:
    

boolean, default False

show_faces
    

Display a face selection overlay

Type:
    

boolean, default True

show_fade_inactive
    

Fade inactive geometry using the viewport background color

Type:
    

boolean, default False

show_floor
    

Show the ground plane grid

Type:
    

boolean, default True

show_freestyle_edge_marks
    

Display Freestyle edge marks, used with the Freestyle renderer

Type:
    

boolean, default True

show_freestyle_face_marks
    

Display Freestyle face marks, used with the Freestyle renderer

Type:
    

boolean, default True

show_light_colors
    

Show light colors

Type:
    

boolean, default False

show_look_dev
    

Show reference spheres with neutral shading that react to lighting to assist in look development

Type:
    

boolean, default False

show_motion_paths
    

Show the Motion Paths Overlay

Type:
    

boolean, default True

show_object_origins
    

Show object center dots

Type:
    

boolean, default True

show_object_origins_all
    

Show the object origin center dot for all (selected and unselected) objects

Type:
    

boolean, default False

show_onion_skins
    

Show the Onion Skinning Overlay

Type:
    

boolean, default False

show_ortho_grid
    

Show grid in orthographic side view

Type:
    

boolean, default True

show_outline_selected
    

Show an outline highlight around selected objects

Type:
    

boolean, default True

show_overlays
    

Display overlays like gizmos and outlines

Type:
    

boolean, default True

show_paint_wire
    

Use wireframe display in painting modes

Type:
    

boolean, default False

show_relationship_lines
    

Show dashed lines indicating parent or constraint relationships

Type:
    

boolean, default True

show_retopology
    

Hide the solid mesh and offset the overlay towards the view. Selection is occluded by inactive geometry, unless X-Ray is enabled

Type:
    

boolean, default False

show_sculpt_curves_cage
    

Show original curves that are currently being edited

Type:
    

boolean, default False

show_sculpt_face_sets
    

Type:
    

boolean, default True

show_sculpt_mask
    

Type:
    

boolean, default True

show_split_normals
    

Display vertex-per-face normals as lines

Type:
    

boolean, default False

show_stats
    

Display scene statistics overlay text

Type:
    

boolean, default False

show_statvis
    

Display statistical information about the mesh

Type:
    

boolean, default False

show_text
    

Display overlay text

Type:
    

boolean, default True

show_vertex_normals
    

Display vertex normals as lines

Type:
    

boolean, default False

show_viewer_attribute
    

Show attribute overlay for active viewer node

Type:
    

boolean, default True

show_viewer_text
    

Show attribute values as text in viewport

Type:
    

boolean, default False

show_weight
    

Display weights in editmode

Type:
    

boolean, default False

show_wireframes
    

Show face edges wires

Type:
    

boolean, default False

show_wpaint_contours
    

Show contour lines formed by points with the same interpolated weight

Type:
    

boolean, default False

show_xray_bone
    

Show the bone selection overlay

Type:
    

boolean, default False

texture_paint_mode_opacity
    

Opacity of the texture paint mode stencil mask overlay

Type:
    

float in [0, 1], default 1.0

use_debug_freeze_view_culling
    

Freeze view culling bounds

Type:
    

boolean, default False

use_gpencil_canvas_xray
    

Show Canvas grid in front

Type:
    

boolean, default False

use_gpencil_edit_lines
    

Show Edit Lines when editing strokes

Type:
    

boolean, default True

use_gpencil_fade_gp_objects
    

Fade Grease Pencil Objects, except the active one

Type:
    

boolean, default False

use_gpencil_fade_layers
    

Toggle fading of Grease Pencil layers except the active one

Type:
    

boolean, default False

use_gpencil_fade_objects
    

Fade all viewport objects with a full color layer to improve visibility

Type:
    

boolean, default False

use_gpencil_grid
    

Display a grid over Grease Pencil paper

Type:
    

boolean, default False

use_gpencil_multiedit_line_only
    

Show Edit Lines only in multiframe

Type:
    

boolean, default False

use_gpencil_onion_skin
    

Show ghosts of the keyframes before and after the current frame

Type:
    

boolean, default False

use_gpencil_onion_skin_active_object
    

Show only the onion skins of the active object

Type:
    

boolean, default False

use_gpencil_show_directions
    

Show stroke drawing direction with a bigger green dot (start) and smaller red dot (end) points

Type:
    

boolean, default False

use_gpencil_show_material_name
    

Show material name assigned to each stroke

Type:
    

boolean, default False

use_normals_constant_screen_size
    

Keep size of normals constant in relation to 3D view

Type:
    

boolean, default False

vertex_opacity
    

Opacity for edit vertices

Type:
    

float in [0, 1], default 1.0

vertex_paint_mode_opacity
    

Opacity of the texture paint mode stencil mask overlay

Type:
    

float in [0, 1], default 1.0

viewer_attribute_opacity
    

Opacity of the attribute that is currently visualized

Type:
    

float in [0, 1], default 1.0

weight_paint_mode_opacity
    

Opacity of the weight paint mode overlay

Type:
    

float in [0, 1], default 1.0

wireframe_opacity
    

Opacity of the displayed edges (1.0 for opaque)

Type:
    

float in [0, 1], default 1.0

wireframe_threshold
    

Adjust the angle threshold for displaying edges (1.0 for all)

Type:
    

float in [0, 1], default 1.0

xray_alpha_bone
    

Opacity to use for bone selection

Type:
    

float in [0, 1], default 0.5

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

  * [`SpaceView3D.overlay`](../S/bpy.types.SpaceView3D.md#bpy.types.SpaceView3D.overlay "bpy.types.SpaceView3D.overlay")

| 


  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
