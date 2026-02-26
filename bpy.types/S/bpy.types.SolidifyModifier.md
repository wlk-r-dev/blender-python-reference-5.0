# SolidifyModifier(Modifier)

base classes — [[bpy_struct]], [[Modifier]]

_class _bpy.types.SolidifyModifier(_Modifier_)
    

Create a solid skin, compensating for sharp angles

bevel_convex
    

Edge bevel weight to be added to outside edges

Type:
    

float in [-1, 1], default 0.0

edge_crease_inner
    

Assign a crease to inner edges

Type:
    

float in [0, 1], default 0.0

edge_crease_outer
    

Assign a crease to outer edges

Type:
    

float in [0, 1], default 0.0

edge_crease_rim
    

Assign a crease to the edges making up the rim

Type:
    

float in [0, 1], default 0.0

invert_vertex_group
    

Invert the vertex group influence

Type:
    

boolean, default False

material_offset
    

Offset material index of generated faces

Type:
    

int in [-32768, 32767], default 0

material_offset_rim
    

Offset material index of generated rim faces

Type:
    

int in [-32768, 32767], default 0

nonmanifold_boundary_mode
    

Selects the boundary adjustment algorithm

  * `NONE` None – No shape correction.

  * `ROUND` Round – Round open perimeter shape.

  * `FLAT` Flat – Flat open perimeter shape.


Type:
    

enum in [`'NONE'`, `'ROUND'`, `'FLAT'`], default `'NONE'`

nonmanifold_merge_threshold
    

Distance within which degenerated geometry is merged

Type:
    

float in [0, 1], default 0.0001

nonmanifold_thickness_mode
    

Selects the used thickness algorithm

  * `FIXED` Fixed – Most basic thickness calculation.

  * `EVEN` Even – Even thickness calculation which takes the angle between faces into account.

  * `CONSTRAINTS` Constraints – Thickness calculation using constraints, most advanced.


Type:
    

enum in [`'FIXED'`, `'EVEN'`, `'CONSTRAINTS'`], default `'CONSTRAINTS'`

offset
    

Offset the thickness from the center

Type:
    

float in [-inf, inf], default -1.0

rim_vertex_group
    

Vertex group that the generated rim geometry will be weighted to

Type:
    

string, default “”, (never None)

shell_vertex_group
    

Vertex group that the generated shell geometry will be weighted to

Type:
    

string, default “”, (never None)

solidify_mode
    

Selects the used algorithm

  * `EXTRUDE` Simple – Output a solidified version of a mesh by simple extrusion.

  * `NON_MANIFOLD` Complex – Output a manifold mesh even if the base mesh is non-manifold, where edges have 3 or more connecting faces. This method is slower..


Type:
    

enum in [`'EXTRUDE'`, `'NON_MANIFOLD'`], default `'EXTRUDE'`

thickness
    

Thickness of the shell

Type:
    

float in [-inf, inf], default 0.01

thickness_clamp
    

Offset clamp based on geometry scale

Type:
    

float in [0, 100], default 0.0

thickness_vertex_group
    

Thickness factor to use for zero vertex group influence

Type:
    

float in [0, 1], default 0.0

use_even_offset
    

Maintain thickness by adjusting for sharp corners (slow, disable when not needed)

Type:
    

boolean, default False

use_flat_faces
    

Make faces use the minimal vertex weight assigned to their vertices (ensures new faces remain parallel to their original ones, slow, disable when not needed)

Type:
    

boolean, default False

use_flip_normals
    

Invert the face direction

Type:
    

boolean, default False

use_quality_normals
    

Calculate normals which result in more even thickness (slow, disable when not needed)

Type:
    

boolean, default False

use_rim
    

Create edge loops between the inner and outer surfaces on face edges (slow, disable when not needed)

Type:
    

boolean, default True

use_rim_only
    

Only add the rim to the original data

Type:
    

boolean, default False

use_thickness_angle_clamp
    

Clamp thickness based on angles

Type:
    

boolean, default False

vertex_group
    

Vertex group name

Type:
    

string, default “”, (never None)

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
  * [[Modifier.name]]
  * [[Modifier.type]]
  * [[Modifier.show_viewport]]
  * [[Modifier.show_render]]
  * [[Modifier.show_in_editmode]]
  * [[Modifier.show_on_cage]]

| 

  * [[Modifier.show_expanded]]
  * [[Modifier.is_active]]
  * [[Modifier.use_pin_to_last]]
  * [[Modifier.is_override_data]]
  * [[Modifier.use_apply_on_spline]]
  * [[Modifier.execution_time]]
  * [[Modifier.persistent_uid]]

  
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

| 

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
  * [[Modifier.bl_rna_get_subclass]]
  * [[Modifier.bl_rna_get_subclass_py]]

  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
