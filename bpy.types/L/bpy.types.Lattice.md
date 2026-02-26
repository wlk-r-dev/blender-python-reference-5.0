# Lattice(ID)

base classes — [[bpy_struct]], [[ID]]

_class _bpy.types.Lattice(_ID_)
    

Lattice data-block defining a grid for deforming other objects

animation_data
    

Animation data for this data-block

Type:
    

[[AnimData]], (readonly)

interpolation_type_u
    

Type:
    

enum in [`'KEY_LINEAR'`, `'KEY_CARDINAL'`, `'KEY_CATMULL_ROM'`, `'KEY_BSPLINE'`], default `'KEY_BSPLINE'`

interpolation_type_v
    

Type:
    

enum in [`'KEY_LINEAR'`, `'KEY_CARDINAL'`, `'KEY_CATMULL_ROM'`, `'KEY_BSPLINE'`], default `'KEY_BSPLINE'`

interpolation_type_w
    

Type:
    

enum in [`'KEY_LINEAR'`, `'KEY_CARDINAL'`, `'KEY_CATMULL_ROM'`, `'KEY_BSPLINE'`], default `'KEY_BSPLINE'`

is_editmode
    

True when used in editmode

Type:
    

boolean, default False, (readonly)

points
    

Points of the lattice

Type:
    

[[bpy_prop_collection]] of [[LatticePoint]], (readonly)

points_u
    

Points in U direction (cannot be changed when there are shape keys)

Type:
    

int in [1, 64], default 0

points_v
    

Points in V direction (cannot be changed when there are shape keys)

Type:
    

int in [1, 64], default 0

points_w
    

Points in W direction (cannot be changed when there are shape keys)

Type:
    

int in [1, 64], default 0

shape_keys
    

Type:
    

[[Key]], (readonly)

use_outside
    

Only display and take into account the outer vertices

Type:
    

boolean, default False

vertex_group
    

Vertex group to apply the influence of the lattice

Type:
    

string, default “”, (never None)

transform(_matrix_ , _*_ , _shape_keys =False_)
    

Transform lattice by a matrix

Parameters:
    

  * **matrix** ([[mathutils.Matrix]] of 4 * 4 items in [-inf, inf]) – Matrix

  * **shape_keys** (_boolean_ _,__(__optional_ _)_) – Transform Shape Keys


update_gpu_tag()
    

update_gpu_tag

unit_test_compare(_*_ , _lattice =None_, _threshold =7.1526e-06_)
    

unit_test_compare

Parameters:
    

  * **lattice** (`Lattice`, (optional)) – Lattice to compare to

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

  * [[bpy.context.lattice]]
  * [[BlendData.lattices]]
  * [[BlendDataLattices.new]]

| 

  * [[BlendDataLattices.remove]]
  * `Lattice.unit_test_compare`

  
---|---
  *[*]: Keyword-only parameters separator (PEP 3102)
  *[/]: Positional-only parameter separator (PEP 570)
