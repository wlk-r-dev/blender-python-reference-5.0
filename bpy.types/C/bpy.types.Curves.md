# Curves(ID)

base classes — [[bpy_struct]], [[ID]]

_class _bpy.types.Curves(_ID_)
    

Hair data-block for hair curves

animation_data
    

Animation data for this data-block

Type:
    

[[AnimData]], (readonly)

attributes
    

Geometry attributes

Type:
    

[[AttributeGroupCurves]] [[bpy_prop_collection]] of [[Attribute]], (readonly)

color_attributes
    

Geometry color attributes

Type:
    

[[AttributeGroupCurves]] [[bpy_prop_collection]] of [[Attribute]], (readonly)

curve_offset_data
    

Type:
    

[[bpy_prop_collection]] of [[IntAttributeValue]], (readonly)

curves
    

All curves in the data-block

Type:
    

[[bpy_prop_collection]] of [[CurveSlice]], (readonly)

materials
    

Type:
    

[[IDMaterials]] [[bpy_prop_collection]] of [[Material]], (readonly)

normals
    

The curve normal value at each of the curve’s control points

Type:
    

[[bpy_prop_collection]] of [[FloatVectorValueReadOnly]], (readonly)

points
    

Control points of all curves

Type:
    

[[bpy_prop_collection]] of [[CurvePoint]], (readonly)

position_data
    

Type:
    

[[bpy_prop_collection]] of [[FloatVectorAttributeValue]], (readonly)

selection_domain
    

Type:
    

enum in [Attribute Curves Domain Items](../../bpy_types_enum_items/attribute_curves_domain_items.md#rna-enum-attribute-curves-domain-items), default `'POINT'`

surface
    

Mesh object that the curves can be attached to

Type:
    

[[Object]]

surface_collision_distance
    

Distance to keep the curves away from the surface

Type:
    

float in [1.192e-07, inf], default 0.005

surface_uv_map
    

The name of the attribute on the surface mesh used to define the attachment of each curve

Type:
    

string, default “”, (never None)

use_mirror_x
    

Enable symmetry in the X axis

Type:
    

boolean, default False

use_mirror_y
    

Enable symmetry in the Y axis

Type:
    

boolean, default False

use_mirror_z
    

Enable symmetry in the Z axis

Type:
    

boolean, default False

use_sculpt_collision
    

Enable collision with the surface while sculpting

Type:
    

boolean, default False

add_curves(_sizes_)
    

add_curves

Parameters:
    

**sizes** (_int array_ _of_ _1 items in_ _[__0_ _,__inf_ _]_) – Sizes, The number of points in each curve

remove_curves(_*_ , _indices =(0,)_)
    

Remove all curves. If indices are provided, remove only the curves with the given indices.

Parameters:
    

**indices** (_int array_ _of_ _1 items in_ _[__0_ _,__inf_ _]__,__(__optional_ _)_) – Indices, The indices of the curves to remove

resize_curves(_sizes_ , _*_ , _indices =(0,)_)
    

Resize all existing curves. If indices are provided, resize only the curves with the given indices. If the new size for a curve is smaller, the curve is trimmed. If the new size for a curve is larger, the new end values are default initialized.

Parameters:
    

  * **sizes** (_int array_ _of_ _1 items in_ _[__1_ _,__inf_ _]_) – Sizes, The number of points in each curve

  * **indices** (_int array_ _of_ _1 items in_ _[__0_ _,__inf_ _]__,__(__optional_ _)_) – Indices, The indices of the curves to resize


reorder_curves(_new_indices_)
    

Reorder the curves by the new indices.

Parameters:
    

**new_indices** (_int array_ _of_ _1 items in_ _[__0_ _,__inf_ _]_) – New indices, The new index for each of the curves

set_types(_*_ , _type ='CATMULL_ROM'_, _indices =(0,)_)
    

Set the curve type. If indices are provided, set only the types with the given curve indices.

Parameters:
    

  * **type** (enum in [Curves Type Items](../../bpy_types_enum_items/curves_type_items.md#rna-enum-curves-type-items), (optional)) – Type

  * **indices** (_int array_ _of_ _1 items in_ _[__0_ _,__inf_ _]__,__(__optional_ _)_) – Indices, The indices of the curves to resize


unit_test_compare(_*_ , _curves =None_, _threshold =7.1526e-06_)
    

unit_test_compare

Parameters:
    

  * **curves** (`Curves`, (optional)) – Curves to compare to

  * **threshold** (_float in_ _[__0_ _,__inf_ _]__,__(__optional_ _)_) – Threshold, Comparison tolerance threshold


Returns:
    

Return value, String description of result of comparison

Return type:
    

string, (never None)

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
  * [[ID.name]]
  * [[ID.name_full]]
  * [[ID.id_type]]
  * [[ID.session_uid]]
  * [[ID.is_evaluated]]
  * [[ID.original]]
  * [[ID.users]]
  * [[ID.use_fake_user]]
  * [[ID.use_extra_user]]
  * [[ID.is_embedded_data]]

| 

  * [[ID.is_linked_packed]]
  * [[ID.is_missing]]
  * [[ID.is_runtime_data]]
  * [[ID.is_editable]]
  * [[ID.tag]]
  * [[ID.is_library_indirect]]
  * [[ID.library]]
  * [[ID.library_weak_reference]]
  * [[ID.asset_data]]
  * [[ID.override_library]]
  * [[ID.preview]]

  
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
  * [[bpy_struct.keyframe_insert]]
  * [[bpy_struct.keys]]
  * [[bpy_struct.path_from_id]]
  * [[bpy_struct.path_from_module]]
  * [[bpy_struct.path_resolve]]
  * [[bpy_struct.pop]]
  * [[bpy_struct.property_overridable_library_set]]
  * [[bpy_struct.property_unset]]
  * [[bpy_struct.rna_ancestors]]

| 

  * [[bpy_struct.type_recast]]
  * [[bpy_struct.values]]
  * [[ID.bl_system_properties_get]]
  * [[ID.rename]]
  * [[ID.evaluated_get]]
  * [[ID.copy]]
  * [[ID.asset_mark]]
  * [[ID.asset_clear]]
  * [[ID.asset_generate_preview]]
  * [[ID.override_create]]
  * [[ID.override_hierarchy_create]]
  * [[ID.user_clear]]
  * [[ID.user_remap]]
  * [[ID.make_local]]
  * [[ID.user_of_id]]
  * [[ID.animation_data_create]]
  * [[ID.animation_data_clear]]
  * [[ID.update_tag]]
  * [[ID.preview_ensure]]
  * [[ID.bl_rna_get_subclass]]
  * [[ID.bl_rna_get_subclass_py]]

  
---|---  
  
## References

  * [[BlendData.hair_curves]]
  * [[BlendDataHairCurves.new]]

| 

  * [[BlendDataHairCurves.remove]]
  * `Curves.unit_test_compare`

  
---|---
  *[*]: Keyword-only parameters separator (PEP 3102)
  *[/]: Positional-only parameter separator (PEP 570)
