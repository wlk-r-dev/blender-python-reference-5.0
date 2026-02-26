# DecimateModifier(Modifier)

base classes — [[bpy_struct]], [[Modifier]]

_class _bpy.types.DecimateModifier(_Modifier_)
    

Decimation modifier

angle_limit
    

Only dissolve angles below this (planar only)

Type:
    

float in [0, 3.14159], default 0.0872665

decimate_type
    

  * `COLLAPSE` Collapse – Use edge collapsing.

  * `UNSUBDIV` Un-Subdivide – Use un-subdivide face reduction.

  * `DISSOLVE` Planar – Dissolve geometry to form planar polygons.


Type:
    

enum in [`'COLLAPSE'`, `'UNSUBDIV'`, `'DISSOLVE'`], default `'COLLAPSE'`

delimit
    

Limit merging geometry

Type:
    

enum set in [Mesh Delimit Mode Items](../../bpy_types_enum_items/mesh_delimit_mode_items.md#rna-enum-mesh-delimit-mode-items), default set()

face_count
    

The current number of faces in the decimated mesh

Type:
    

int in [-inf, inf], default 0, (readonly)

invert_vertex_group
    

Invert vertex group influence (collapse only)

Type:
    

boolean, default False

iterations
    

Number of times reduce the geometry (unsubdivide only)

Type:
    

int in [0, 32767], default 0

ratio
    

Ratio of triangles to reduce to (collapse only)

Type:
    

float in [0, 1], default 1.0

symmetry_axis
    

Axis of symmetry

Type:
    

enum in [Axis Xyz Items](../../bpy_types_enum_items/axis_xyz_items.md#rna-enum-axis-xyz-items), default `'X'`

use_collapse_triangulate
    

Keep triangulated faces resulting from decimation (collapse only)

Type:
    

boolean, default False

use_dissolve_boundaries
    

Dissolve all vertices in between face boundaries (planar only)

Type:
    

boolean, default False

use_symmetry
    

Maintain symmetry on an axis

Type:
    

boolean, default False

vertex_group
    

Vertex group name (collapse only)

Type:
    

string, default “”, (never None)

vertex_group_factor
    

Vertex group strength

Type:
    

float in [0, 1000], default 1.0

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
