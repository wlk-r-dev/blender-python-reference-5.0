# NormalEditModifier(Modifier)

base classes — [[bpy_struct]], [[Modifier]]

_class _bpy.types.NormalEditModifier(_Modifier_)
    

Modifier affecting/generating custom normals

invert_vertex_group
    

Invert vertex group influence

Type:
    

boolean, default False

mix_factor
    

How much of generated normals to mix with existing ones

Type:
    

float in [0, 1], default 1.0

mix_limit
    

Maximum angle between old and new normals

Type:
    

float in [0, 3.14159], default 3.14159

mix_mode
    

How to mix generated normals with existing ones

  * `COPY` Copy – Copy new normals (overwrite existing).

  * `ADD` Add – Copy sum of new and old normals.

  * `SUB` Subtract – Copy new normals minus old normals.

  * `MUL` Multiply – Copy product of old and new normals (not cross product).


Type:
    

enum in [`'COPY'`, `'ADD'`, `'SUB'`, `'MUL'`], default `'COPY'`

mode
    

How to affect (generate) normals

  * `RADIAL` Radial – From an ellipsoid (shape defined by the boundbox’s dimensions, target is optional).

  * `DIRECTIONAL` Directional – Normals ‘track’ (point to) the target object.


Type:
    

enum in [`'RADIAL'`, `'DIRECTIONAL'`], default `'RADIAL'`

no_polynors_fix
    

Do not flip polygons when their normals are not consistent with their newly computed custom vertex normals

Type:
    

boolean, default False

offset
    

Offset from object’s center

Type:
    

[[mathutils.Vector]] of 3 items in [-inf, inf], default (0.0, 0.0, 0.0)

target
    

Target object used to affect normals

Type:
    

[[Object]]

use_direction_parallel
    

Use same direction for all normals, from origin to target’s center (Directional mode only)

Type:
    

boolean, default True

vertex_group
    

Vertex group name for selecting/weighting the affected areas

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
