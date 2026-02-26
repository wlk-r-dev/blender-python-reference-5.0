# SubsurfModifier(Modifier)

base classes — [[bpy_struct]], [[Modifier]]

_class _bpy.types.SubsurfModifier(_Modifier_)
    

Subdivision surface modifier

adaptive_object_edge_length
    

Target object space edge length for adaptive subdivision

Type:
    

float in [0.0001, 1000], default 0.01

adaptive_pixel_size
    

Target polygon pixel size for adaptive subdivision

Type:
    

float in [0.1, 1000], default 1.0

adaptive_space
    

How to adaptively subdivide the mesh

  * `PIXEL` Pixel – Subdivide polygons to reach a specified pixel size on screen.

  * `OBJECT` Object – Subdivide to reach a specified edge length in object space. This is required to use adaptive subdivision for instanced meshes.


Type:
    

enum in [`'PIXEL'`, `'OBJECT'`], default `'PIXEL'`

boundary_smooth
    

Controls how open boundaries are smoothed

Type:
    

enum in [Subdivision Boundary Smooth Items](../../bpy_types_enum_items/subdivision_boundary_smooth_items.md#rna-enum-subdivision-boundary-smooth-items), default `'ALL'`

levels
    

Number of subdivisions to perform in the 3D viewport

Type:
    

int in [0, 11], default 1

open_adaptive_subdivision_panel
    

Type:
    

boolean, default False

open_advanced_panel
    

Type:
    

boolean, default False

quality
    

Accuracy of vertex positions, lower value is faster but less precise

Type:
    

int in [1, 10], default 3

render_levels
    

Number of subdivisions to perform when rendering

Type:
    

int in [0, 11], default 2

show_only_control_edges
    

Skip displaying interior subdivided edges

Type:
    

boolean, default True

subdivision_type
    

Select type of subdivision algorithm

  * `CATMULL_CLARK` Catmull-Clark – Create a smooth curved surface using the Catmull-Clark subdivision scheme.

  * `SIMPLE` Simple – Subdivide faces without changing shape.


Type:
    

enum in [`'CATMULL_CLARK'`, `'SIMPLE'`], default `'CATMULL_CLARK'`

use_adaptive_subdivision
    

Adaptively subdivide mesh based on camera distance

Type:
    

boolean, default False

use_creases
    

Use mesh crease information to sharpen edges or corners

Type:
    

boolean, default True

use_custom_normals
    

Interpolates existing custom normals to resulting mesh

Type:
    

boolean, default False

use_limit_surface
    

Place vertices at the surface that would be produced with infinite levels of subdivision (smoothest possible shape)

Type:
    

boolean, default True

uv_smooth
    

Controls how smoothing is applied to UVs

Type:
    

enum in [Subdivision Uv Smooth Items](../../bpy_types_enum_items/subdivision_uv_smooth_items.md#rna-enum-subdivision-uv-smooth-items), default `'PRESERVE_BOUNDARIES'`

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
