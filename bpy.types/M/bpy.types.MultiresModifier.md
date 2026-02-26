# MultiresModifier(Modifier)

base classes — [[bpy_struct]], [[Modifier]]

_class _bpy.types.MultiresModifier(_Modifier_)
    

Multiresolution mesh modifier

boundary_smooth
    

Controls how open boundaries are smoothed

Type:
    

enum in [Subdivision Boundary Smooth Items](../../bpy_types_enum_items/subdivision_boundary_smooth_items.md#rna-enum-subdivision-boundary-smooth-items), default `'ALL'`

filepath
    

Path to external displacements file

Type:
    

string, default “”, (never None, blend relative `//` prefix supported)

is_external
    

Store multires displacements outside the .blend file, to save memory

Type:
    

boolean, default False, (readonly)

levels
    

Number of subdivisions to use in the viewport

Type:
    

int in [0, 255], default 0

quality
    

Accuracy of vertex positions, lower value is faster but less precise

Type:
    

int in [1, 10], default 4

render_levels
    

The subdivision level visible at render time

Type:
    

int in [0, 255], default 0

sculpt_levels
    

Number of subdivisions to use in sculpt mode

Type:
    

int in [0, 255], default 0

show_only_control_edges
    

Skip drawing/rendering of interior subdivided edges

Type:
    

boolean, default True

total_levels
    

Number of subdivisions for which displacements are stored

Type:
    

int in [0, 255], default 0, (readonly)

use_creases
    

Use mesh crease information to sharpen edges or corners

Type:
    

boolean, default True

use_custom_normals
    

Interpolates existing custom normals to resulting mesh

Type:
    

boolean, default False

use_sculpt_base_mesh
    

Make Sculpt Mode tools deform the base mesh while previewing the displacement of higher subdivision levels

Type:
    

boolean, default False

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
