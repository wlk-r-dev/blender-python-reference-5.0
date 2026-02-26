# MarbleTexture(Texture)

base classes — [[bpy_struct]], [[ID]], [[Texture]]

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
    

tuple of [[Material]]

Note

Takes `O(len(bpy.data.materials) * len(material.texture_slots))` time.

(readonly)

users_object_modifier
    

Object modifiers that use this texture

Type:
    

tuple of [[Object]]

Note

Takes `O(len(bpy.data.objects) * len(obj.modifiers))` time.

(readonly)

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
  * [[ID.is_linked_packed]]
  * [[ID.is_missing]]
  * [[ID.is_runtime_data]]
  * [[ID.is_editable]]
  * [[ID.tag]]
  * [[ID.is_library_indirect]]
  * [[ID.library]]
  * [[ID.library_weak_reference]]

| 

  * [[ID.asset_data]]
  * [[ID.override_library]]
  * [[ID.preview]]
  * [[Texture.type]]
  * [[Texture.use_clamp]]
  * [[Texture.use_color_ramp]]
  * [[Texture.color_ramp]]
  * [[Texture.intensity]]
  * [[Texture.contrast]]
  * [[Texture.saturation]]
  * [[Texture.factor_red]]
  * [[Texture.factor_green]]
  * [[Texture.factor_blue]]
  * [[Texture.use_preview_alpha]]
  * [[Texture.use_nodes]]
  * [[Texture.node_tree]]
  * [[Texture.animation_data]]
  * [[Texture.users_material]]
  * [[Texture.users_object_modifier]]

  
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
  * [[bpy_struct.type_recast]]

| 

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
  * [[Texture.evaluate]]
  * [[Texture.bl_rna_get_subclass]]
  * [[Texture.bl_rna_get_subclass_py]]

  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
