# ShrinkwrapConstraint(Constraint)

base classes — [`bpy_struct`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct "bpy.types.bpy_struct"), [`Constraint`](../C/bpy.types.Constraint.md#bpy.types.Constraint "bpy.types.Constraint")

_class _bpy.types.ShrinkwrapConstraint(_Constraint_)
    

Create constraint-based shrinkwrap relationship

cull_face
    

Stop vertices from projecting to a face on the target when facing towards/away

  * `OFF` Off – No culling.

  * `FRONT` Front – No projection when in front of the face.

  * `BACK` Back – No projection when behind the face.


Type:
    

enum in [`'OFF'`, `'FRONT'`, `'BACK'`], default `'OFF'`

distance
    

Distance to Target

Type:
    

float in [0, inf], default 0.0

project_axis
    

Axis constrain to

Type:
    

enum in [Object Axis Items](../../bpy_types_enum_items/object_axis_items.md#rna-enum-object-axis-items), default `'POS_X'`

project_axis_space
    

Space for the projection axis

  * `WORLD` World Space – The constraint is applied relative to the world coordinate system.

  * `CUSTOM` Custom Space – The constraint is applied in local space of a custom object/bone/vertex group.

  * `POSE` Pose Space – The constraint is applied in Pose Space, the object transformation is ignored.

  * `LOCAL_WITH_PARENT` Local With Parent – The constraint is applied relative to the rest pose local coordinate system of the bone, thus including the parent-induced transformation.

  * `LOCAL` Local Space – The constraint is applied relative to the local coordinate system of the object.


Type:
    

enum in [`'WORLD'`, `'CUSTOM'`, `'POSE'`, `'LOCAL_WITH_PARENT'`, `'LOCAL'`], default `'WORLD'`

project_limit
    

Limit the distance used for projection (zero disables)

Type:
    

float in [0, inf], default 0.0

shrinkwrap_type
    

Select type of shrinkwrap algorithm for target position

  * `NEAREST_SURFACE` Nearest Surface Point – Shrink the location to the nearest target surface.

  * `PROJECT` Project – Shrink the location to the nearest target surface along a given axis.

  * `NEAREST_VERTEX` Nearest Vertex – Shrink the location to the nearest target vertex.

  * `TARGET_PROJECT` Target Normal Project – Shrink the location to the nearest target surface along the interpolated vertex normals of the target.


Type:
    

enum in [`'NEAREST_SURFACE'`, `'PROJECT'`, `'NEAREST_VERTEX'`, `'TARGET_PROJECT'`], default `'NEAREST_SURFACE'`

target
    

Target Mesh object

Type:
    

[`Object`](../O/bpy.types.Object.md#bpy.types.Object "bpy.types.Object")

track_axis
    

Axis that is aligned to the normal

Type:
    

enum in [`'TRACK_X'`, `'TRACK_Y'`, `'TRACK_Z'`, `'TRACK_NEGATIVE_X'`, `'TRACK_NEGATIVE_Y'`, `'TRACK_NEGATIVE_Z'`], default `'TRACK_X'`

use_invert_cull
    

When projecting in the opposite direction invert the face cull mode

Type:
    

boolean, default False

use_project_opposite
    

Project in both specified and opposite directions

Type:
    

boolean, default False

use_track_normal
    

Align the specified axis to the surface normal

Type:
    

boolean, default False

wrap_mode
    

Select how to constrain the object to the target surface

Type:
    

enum in [Modifier Shrinkwrap Mode Items](../../bpy_types_enum_items/modifier_shrinkwrap_mode_items.md#rna-enum-modifier-shrinkwrap-mode-items), default `'ON_SURFACE'`

_classmethod _bl_rna_get_subclass(_id_ , _default =None_, _/_)
    

Parameters:
    

**id** (_str_) – The RNA type identifier.

Returns:
    

The RNA type or default when not found.

Return type:
    

[`bpy.types.Struct`](bpy.types.Struct.md#bpy.types.Struct "bpy.types.Struct") subclass

_classmethod _bl_rna_get_subclass_py(_id_ , _default =None_, _/_)
    

Parameters:
    

**id** (_str_) – The RNA type identifier.

Returns:
    

The class or default when not found.

Return type:
    

type

## Inherited Properties

  * [`bpy_struct.id_data`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.id_data "bpy.types.bpy_struct.id_data")
  * [`Constraint.name`](../C/bpy.types.Constraint.md#bpy.types.Constraint.name "bpy.types.Constraint.name")
  * [`Constraint.type`](../C/bpy.types.Constraint.md#bpy.types.Constraint.type "bpy.types.Constraint.type")
  * [`Constraint.is_override_data`](../C/bpy.types.Constraint.md#bpy.types.Constraint.is_override_data "bpy.types.Constraint.is_override_data")
  * [`Constraint.owner_space`](../C/bpy.types.Constraint.md#bpy.types.Constraint.owner_space "bpy.types.Constraint.owner_space")
  * [`Constraint.target_space`](../C/bpy.types.Constraint.md#bpy.types.Constraint.target_space "bpy.types.Constraint.target_space")
  * [`Constraint.space_object`](../C/bpy.types.Constraint.md#bpy.types.Constraint.space_object "bpy.types.Constraint.space_object")
  * [`Constraint.space_subtarget`](../C/bpy.types.Constraint.md#bpy.types.Constraint.space_subtarget "bpy.types.Constraint.space_subtarget")

| 

  * [`Constraint.mute`](../C/bpy.types.Constraint.md#bpy.types.Constraint.mute "bpy.types.Constraint.mute")
  * [`Constraint.enabled`](../C/bpy.types.Constraint.md#bpy.types.Constraint.enabled "bpy.types.Constraint.enabled")
  * [`Constraint.show_expanded`](../C/bpy.types.Constraint.md#bpy.types.Constraint.show_expanded "bpy.types.Constraint.show_expanded")
  * [`Constraint.is_valid`](../C/bpy.types.Constraint.md#bpy.types.Constraint.is_valid "bpy.types.Constraint.is_valid")
  * [`Constraint.active`](../C/bpy.types.Constraint.md#bpy.types.Constraint.active "bpy.types.Constraint.active")
  * [`Constraint.influence`](../C/bpy.types.Constraint.md#bpy.types.Constraint.influence "bpy.types.Constraint.influence")
  * [`Constraint.error_location`](../C/bpy.types.Constraint.md#bpy.types.Constraint.error_location "bpy.types.Constraint.error_location")
  * [`Constraint.error_rotation`](../C/bpy.types.Constraint.md#bpy.types.Constraint.error_rotation "bpy.types.Constraint.error_rotation")

  
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
  * [`bpy_struct.keyframe_delete`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.keyframe_delete "bpy.types.bpy_struct.keyframe_delete")

| 

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
  * [`Constraint.bl_rna_get_subclass`](../C/bpy.types.Constraint.md#bpy.types.Constraint.bl_rna_get_subclass "bpy.types.Constraint.bl_rna_get_subclass")
  * [`Constraint.bl_rna_get_subclass_py`](../C/bpy.types.Constraint.md#bpy.types.Constraint.bl_rna_get_subclass_py "bpy.types.Constraint.bl_rna_get_subclass_py")

  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
