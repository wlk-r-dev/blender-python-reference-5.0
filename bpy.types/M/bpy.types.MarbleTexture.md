# MarbleTexture(Texture)

base classes — [`bpy_struct`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct "bpy.types.bpy_struct"), [`ID`](../I/bpy.types.ID.md#bpy.types.ID "bpy.types.ID"), [`Texture`](../T/bpy.types.Texture.md#bpy.types.Texture "bpy.types.Texture")

_class _bpy.types.MarbleTexture(_Texture_)
    

Procedural noise texture

marble_type
    

  * `SOFT` Soft – Use soft marble.

  * `SHARP` Sharp – Use more clearly defined marble.

  * `SHARPER` Sharper – Use very clearly defined marble.


Type:
    

enum in [`'SOFT'`, `'SHARP'`, `'SHARPER'`], default `'SOFT'`

nabla
    

Size of derivative offset used for calculating normal

Type:
    

float in [0.001, 0.1], default 0.025

noise_basis
    

Noise basis used for turbulence

  * `BLENDER_ORIGINAL` Blender Original – Noise algorithm - Blender original: Smooth interpolated noise.

  * `ORIGINAL_PERLIN` Original Perlin – Noise algorithm - Original Perlin: Smooth interpolated noise.

  * `IMPROVED_PERLIN` Improved Perlin – Noise algorithm - Improved Perlin: Smooth interpolated noise.

  * `VORONOI_F1` Voronoi F1 – Noise algorithm - Voronoi F1: Returns distance to the closest feature point.

  * `VORONOI_F2` Voronoi F2 – Noise algorithm - Voronoi F2: Returns distance to the 2nd closest feature point.

  * `VORONOI_F3` Voronoi F3 – Noise algorithm - Voronoi F3: Returns distance to the 3rd closest feature point.

  * `VORONOI_F4` Voronoi F4 – Noise algorithm - Voronoi F4: Returns distance to the 4th closest feature point.

  * `VORONOI_F2_F1` Voronoi F2-F1 – Noise algorithm - Voronoi F1-F2.

  * `VORONOI_CRACKLE` Voronoi Crackle – Noise algorithm - Voronoi Crackle: Voronoi tessellation with sharp edges.

  * `CELL_NOISE` Cell Noise – Noise algorithm - Cell Noise: Square cell tessellation.


Type:
    

enum in [`'BLENDER_ORIGINAL'`, `'ORIGINAL_PERLIN'`, `'IMPROVED_PERLIN'`, `'VORONOI_F1'`, `'VORONOI_F2'`, `'VORONOI_F3'`, `'VORONOI_F4'`, `'VORONOI_F2_F1'`, `'VORONOI_CRACKLE'`, `'CELL_NOISE'`], default `'BLENDER_ORIGINAL'`

noise_basis_2
    

  * `SIN` Sin – Use a sine wave to produce bands.

  * `SAW` Saw – Use a saw wave to produce bands.

  * `TRI` Tri – Use a triangle wave to produce bands.


Type:
    

enum in [`'SIN'`, `'SAW'`, `'TRI'`], default `'SIN'`

noise_depth
    

Depth of the cloud calculation

Type:
    

int in [0, 30], default 2

noise_scale
    

Scaling for noise input

Type:
    

float in [0.0001, inf], default 0.25

noise_type
    

  * `SOFT_NOISE` Soft – Generate soft noise (smooth transitions).

  * `HARD_NOISE` Hard – Generate hard noise (sharp transitions).


Type:
    

enum in [`'SOFT_NOISE'`, `'HARD_NOISE'`], default `'SOFT_NOISE'`

turbulence
    

Turbulence of the bandnoise and ringnoise types

Type:
    

float in [0.0001, inf], default 5.0

users_material
    

Materials that use this texture

Type:
    

tuple of [`Material`](bpy.types.Material.md#bpy.types.Material "bpy.types.Material")

Note

Takes `O(len(bpy.data.materials) * len(material.texture_slots))` time.

(readonly)

users_object_modifier
    

Object modifiers that use this texture

Type:
    

tuple of [`Object`](../O/bpy.types.Object.md#bpy.types.Object "bpy.types.Object")

Note

Takes `O(len(bpy.data.objects) * len(obj.modifiers))` time.

(readonly)

_classmethod _bl_rna_get_subclass(_id_ , _default =None_, _/_)
    

Parameters:
    

**id** (_str_) – The RNA type identifier.

Returns:
    

The RNA type or default when not found.

Return type:
    

[`bpy.types.Struct`](../S/bpy.types.Struct.md#bpy.types.Struct "bpy.types.Struct") subclass

_classmethod _bl_rna_get_subclass_py(_id_ , _default =None_, _/_)
    

Parameters:
    

**id** (_str_) – The RNA type identifier.

Returns:
    

The class or default when not found.

Return type:
    

type

## Inherited Properties

  * [`bpy_struct.id_data`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.id_data "bpy.types.bpy_struct.id_data")
  * [`ID.name`](../I/bpy.types.ID.md#bpy.types.ID.name "bpy.types.ID.name")
  * [`ID.name_full`](../I/bpy.types.ID.md#bpy.types.ID.name_full "bpy.types.ID.name_full")
  * [`ID.id_type`](../I/bpy.types.ID.md#bpy.types.ID.id_type "bpy.types.ID.id_type")
  * [`ID.session_uid`](../I/bpy.types.ID.md#bpy.types.ID.session_uid "bpy.types.ID.session_uid")
  * [`ID.is_evaluated`](../I/bpy.types.ID.md#bpy.types.ID.is_evaluated "bpy.types.ID.is_evaluated")
  * [`ID.original`](../I/bpy.types.ID.md#bpy.types.ID.original "bpy.types.ID.original")
  * [`ID.users`](../I/bpy.types.ID.md#bpy.types.ID.users "bpy.types.ID.users")
  * [`ID.use_fake_user`](../I/bpy.types.ID.md#bpy.types.ID.use_fake_user "bpy.types.ID.use_fake_user")
  * [`ID.use_extra_user`](../I/bpy.types.ID.md#bpy.types.ID.use_extra_user "bpy.types.ID.use_extra_user")
  * [`ID.is_embedded_data`](../I/bpy.types.ID.md#bpy.types.ID.is_embedded_data "bpy.types.ID.is_embedded_data")
  * [`ID.is_linked_packed`](../I/bpy.types.ID.md#bpy.types.ID.is_linked_packed "bpy.types.ID.is_linked_packed")
  * [`ID.is_missing`](../I/bpy.types.ID.md#bpy.types.ID.is_missing "bpy.types.ID.is_missing")
  * [`ID.is_runtime_data`](../I/bpy.types.ID.md#bpy.types.ID.is_runtime_data "bpy.types.ID.is_runtime_data")
  * [`ID.is_editable`](../I/bpy.types.ID.md#bpy.types.ID.is_editable "bpy.types.ID.is_editable")
  * [`ID.tag`](../I/bpy.types.ID.md#bpy.types.ID.tag "bpy.types.ID.tag")
  * [`ID.is_library_indirect`](../I/bpy.types.ID.md#bpy.types.ID.is_library_indirect "bpy.types.ID.is_library_indirect")
  * [`ID.library`](../I/bpy.types.ID.md#bpy.types.ID.library "bpy.types.ID.library")
  * [`ID.library_weak_reference`](../I/bpy.types.ID.md#bpy.types.ID.library_weak_reference "bpy.types.ID.library_weak_reference")

| 

  * [`ID.asset_data`](../I/bpy.types.ID.md#bpy.types.ID.asset_data "bpy.types.ID.asset_data")
  * [`ID.override_library`](../I/bpy.types.ID.md#bpy.types.ID.override_library "bpy.types.ID.override_library")
  * [`ID.preview`](../I/bpy.types.ID.md#bpy.types.ID.preview "bpy.types.ID.preview")
  * [`Texture.type`](../T/bpy.types.Texture.md#bpy.types.Texture.type "bpy.types.Texture.type")
  * [`Texture.use_clamp`](../T/bpy.types.Texture.md#bpy.types.Texture.use_clamp "bpy.types.Texture.use_clamp")
  * [`Texture.use_color_ramp`](../T/bpy.types.Texture.md#bpy.types.Texture.use_color_ramp "bpy.types.Texture.use_color_ramp")
  * [`Texture.color_ramp`](../T/bpy.types.Texture.md#bpy.types.Texture.color_ramp "bpy.types.Texture.color_ramp")
  * [`Texture.intensity`](../T/bpy.types.Texture.md#bpy.types.Texture.intensity "bpy.types.Texture.intensity")
  * [`Texture.contrast`](../T/bpy.types.Texture.md#bpy.types.Texture.contrast "bpy.types.Texture.contrast")
  * [`Texture.saturation`](../T/bpy.types.Texture.md#bpy.types.Texture.saturation "bpy.types.Texture.saturation")
  * [`Texture.factor_red`](../T/bpy.types.Texture.md#bpy.types.Texture.factor_red "bpy.types.Texture.factor_red")
  * [`Texture.factor_green`](../T/bpy.types.Texture.md#bpy.types.Texture.factor_green "bpy.types.Texture.factor_green")
  * [`Texture.factor_blue`](../T/bpy.types.Texture.md#bpy.types.Texture.factor_blue "bpy.types.Texture.factor_blue")
  * [`Texture.use_preview_alpha`](../T/bpy.types.Texture.md#bpy.types.Texture.use_preview_alpha "bpy.types.Texture.use_preview_alpha")
  * [`Texture.use_nodes`](../T/bpy.types.Texture.md#bpy.types.Texture.use_nodes "bpy.types.Texture.use_nodes")
  * [`Texture.node_tree`](../T/bpy.types.Texture.md#bpy.types.Texture.node_tree "bpy.types.Texture.node_tree")
  * [`Texture.animation_data`](../T/bpy.types.Texture.md#bpy.types.Texture.animation_data "bpy.types.Texture.animation_data")
  * [`Texture.users_material`](../T/bpy.types.Texture.md#bpy.types.Texture.users_material "bpy.types.Texture.users_material")
  * [`Texture.users_object_modifier`](../T/bpy.types.Texture.md#bpy.types.Texture.users_object_modifier "bpy.types.Texture.users_object_modifier")

  
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

| 

  * [`bpy_struct.values`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.values "bpy.types.bpy_struct.values")
  * [`ID.bl_system_properties_get`](../I/bpy.types.ID.md#bpy.types.ID.bl_system_properties_get "bpy.types.ID.bl_system_properties_get")
  * [`ID.rename`](../I/bpy.types.ID.md#bpy.types.ID.rename "bpy.types.ID.rename")
  * [`ID.evaluated_get`](../I/bpy.types.ID.md#bpy.types.ID.evaluated_get "bpy.types.ID.evaluated_get")
  * [`ID.copy`](../I/bpy.types.ID.md#bpy.types.ID.copy "bpy.types.ID.copy")
  * [`ID.asset_mark`](../I/bpy.types.ID.md#bpy.types.ID.asset_mark "bpy.types.ID.asset_mark")
  * [`ID.asset_clear`](../I/bpy.types.ID.md#bpy.types.ID.asset_clear "bpy.types.ID.asset_clear")
  * [`ID.asset_generate_preview`](../I/bpy.types.ID.md#bpy.types.ID.asset_generate_preview "bpy.types.ID.asset_generate_preview")
  * [`ID.override_create`](../I/bpy.types.ID.md#bpy.types.ID.override_create "bpy.types.ID.override_create")
  * [`ID.override_hierarchy_create`](../I/bpy.types.ID.md#bpy.types.ID.override_hierarchy_create "bpy.types.ID.override_hierarchy_create")
  * [`ID.user_clear`](../I/bpy.types.ID.md#bpy.types.ID.user_clear "bpy.types.ID.user_clear")
  * [`ID.user_remap`](../I/bpy.types.ID.md#bpy.types.ID.user_remap "bpy.types.ID.user_remap")
  * [`ID.make_local`](../I/bpy.types.ID.md#bpy.types.ID.make_local "bpy.types.ID.make_local")
  * [`ID.user_of_id`](../I/bpy.types.ID.md#bpy.types.ID.user_of_id "bpy.types.ID.user_of_id")
  * [`ID.animation_data_create`](../I/bpy.types.ID.md#bpy.types.ID.animation_data_create "bpy.types.ID.animation_data_create")
  * [`ID.animation_data_clear`](../I/bpy.types.ID.md#bpy.types.ID.animation_data_clear "bpy.types.ID.animation_data_clear")
  * [`ID.update_tag`](../I/bpy.types.ID.md#bpy.types.ID.update_tag "bpy.types.ID.update_tag")
  * [`ID.preview_ensure`](../I/bpy.types.ID.md#bpy.types.ID.preview_ensure "bpy.types.ID.preview_ensure")
  * [`ID.bl_rna_get_subclass`](../I/bpy.types.ID.md#bpy.types.ID.bl_rna_get_subclass "bpy.types.ID.bl_rna_get_subclass")
  * [`ID.bl_rna_get_subclass_py`](../I/bpy.types.ID.md#bpy.types.ID.bl_rna_get_subclass_py "bpy.types.ID.bl_rna_get_subclass_py")
  * [`Texture.evaluate`](../T/bpy.types.Texture.md#bpy.types.Texture.evaluate "bpy.types.Texture.evaluate")
  * [`Texture.bl_rna_get_subclass`](../T/bpy.types.Texture.md#bpy.types.Texture.bl_rna_get_subclass "bpy.types.Texture.bl_rna_get_subclass")
  * [`Texture.bl_rna_get_subclass_py`](../T/bpy.types.Texture.md#bpy.types.Texture.bl_rna_get_subclass_py "bpy.types.Texture.bl_rna_get_subclass_py")

  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
