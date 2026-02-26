# VoronoiTexture(Texture)

base classes — [[bpy_struct]], [[ID]], [[Texture]]

_class _bpy.types.VoronoiTexture(_Texture_)
    

Procedural voronoi texture

color_mode
    

  * `INTENSITY` Intensity – Only calculate intensity.

  * `POSITION` Position – Color cells by position.

  * `POSITION_OUTLINE` Position and Outline – Use position plus an outline based on F2-F1.

  * `POSITION_OUTLINE_INTENSITY` Position, Outline, and Intensity – Multiply position and outline by intensity.


Type:
    

enum in [`'INTENSITY'`, `'POSITION'`, `'POSITION_OUTLINE'`, `'POSITION_OUTLINE_INTENSITY'`], default `'INTENSITY'`

distance_metric
    

Algorithm used to calculate distance of sample points to feature points

  * `DISTANCE` Actual Distance – sqrt(x*x+y*y+z*z).

  * `DISTANCE_SQUARED` Distance Squared – (x*x+y*y+z*z).

  * `MANHATTAN` Manhattan – The length of the distance in axial directions.

  * `CHEBYCHEV` Chebychev – The length of the longest Axial journey.

  * `MINKOVSKY_HALF` Minkowski 1/2 – Set Minkowski variable to 0.5.

  * `MINKOVSKY_FOUR` Minkowski 4 – Set Minkowski variable to 4.

  * `MINKOVSKY` Minkowski – Use the Minkowski function to calculate distance (exponent value determines the shape of the boundaries).


Type:
    

enum in [`'DISTANCE'`, `'DISTANCE_SQUARED'`, `'MANHATTAN'`, `'CHEBYCHEV'`, `'MINKOVSKY_HALF'`, `'MINKOVSKY_FOUR'`, `'MINKOVSKY'`], default `'DISTANCE'`

minkovsky_exponent
    

Minkowski exponent

Type:
    

float in [0.01, 10], default 2.5

nabla
    

Size of derivative offset used for calculating normal

Type:
    

float in [0.001, 0.1], default 0.025

noise_intensity
    

Scales the intensity of the noise

Type:
    

float in [0.01, 10], default 1.0

noise_scale
    

Scaling for noise input

Type:
    

float in [0.0001, inf], default 0.25

weight_1
    

Voronoi feature weight 1

Type:
    

float in [-2, 2], default 1.0

weight_2
    

Voronoi feature weight 2

Type:
    

float in [-2, 2], default 0.0

weight_3
    

Voronoi feature weight 3

Type:
    

float in [-2, 2], default 0.0

weight_4
    

Voronoi feature weight 4

Type:
    

float in [-2, 2], default 0.0

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
