# ScrewModifier(Modifier)

base classes — [[bpy_struct]], [[Modifier]]

_class _bpy.types.ScrewModifier(_Modifier_)
    

Revolve edges

angle
    

Angle of revolution

Type:
    

float in [-inf, inf], default 6.28319

axis
    

Screw axis

Type:
    

enum in [Axis Xyz Items](../../bpy_types_enum_items/axis_xyz_items.md#rna-enum-axis-xyz-items), default `'Z'`

iterations
    

Number of times to apply the screw operation

Type:
    

int in [1, 10000], default 1

merge_threshold
    

Limit below which to merge vertices

Type:
    

float in [0, inf], default 0.01

object
    

Object to define the screw axis

Type:
    

[[Object]]

render_steps
    

Number of steps in the revolution

Type:
    

int in [1, 10000], default 16

screw_offset
    

Offset the revolution along its axis

Type:
    

float in [-inf, inf], default 0.0

steps
    

Number of steps in the revolution

Type:
    

int in [1, 10000], default 16

use_merge_vertices
    

Merge adjacent vertices (screw offset must be zero)

Type:
    

boolean, default False

use_normal_calculate
    

Calculate the order of edges (needed for meshes, but not curves)

Type:
    

boolean, default False

use_normal_flip
    

Flip normals of lathed faces

Type:
    

boolean, default False

use_object_screw_offset
    

Use the distance between the objects to make a screw

Type:
    

boolean, default False

use_smooth_shade
    

Output faces with smooth shading rather than flat shaded

Type:
    

boolean, default True

use_stretch_u
    

Stretch the U coordinates between 0 and 1 when UVs are present

Type:
    

boolean, default False

use_stretch_v
    

Stretch the V coordinates between 0 and 1 when UVs are present

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
