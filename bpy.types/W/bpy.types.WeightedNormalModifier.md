# WeightedNormalModifier(Modifier)

base classes — [[bpy_struct]], [[Modifier]]

_class _bpy.types.WeightedNormalModifier(_Modifier_)
    

invert_vertex_group
    

Invert vertex group influence

Type:
    

boolean, default False

keep_sharp
    

Keep sharp edges as computed for default custom normals, instead of setting a single weighted normal for each vertex

Type:
    

boolean, default False

mode
    

Weighted vertex normal mode to use

  * `FACE_AREA` Face Area – Generate face area weighted normals.

  * `CORNER_ANGLE` Corner Angle – Generate corner angle weighted normals.

  * `FACE_AREA_WITH_ANGLE` Face Area & Angle – Generated normals weighted by both face area and angle.


Type:
    

enum in [`'FACE_AREA'`, `'CORNER_ANGLE'`, `'FACE_AREA_WITH_ANGLE'`], default `'FACE_AREA'`

thresh
    

Threshold value for different weights to be considered equal

Type:
    

float in [0, 10], default 0.01

use_face_influence
    

Use influence of face for weighting

Type:
    

boolean, default False

vertex_group
    

Vertex group name for modifying the selected areas

Type:
    

string, default “”, (never None)

weight
    

Corrective factor applied to faces’ weights, 50 is neutral, lower values increase weight of weak faces, higher values increase weight of strong faces

Type:
    

int in [1, 100], default 50

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
