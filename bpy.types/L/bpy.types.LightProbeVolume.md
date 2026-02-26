# LightProbeVolume(LightProbe)

base classes — [`bpy_struct`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct "bpy.types.bpy_struct"), [`ID`](../I/bpy.types.ID.md#bpy.types.ID "bpy.types.ID"), [`LightProbe`](bpy.types.LightProbe.md#bpy.types.LightProbe "bpy.types.LightProbe")

_class _bpy.types.LightProbeVolume(_LightProbe_)
    

Light probe that captures low frequency lighting inside a volume

bake_samples
    

Number of ray directions to evaluate when baking

Type:
    

int in [1, inf], default 2048

capture_distance
    

Distance around the probe volume that will be considered during the bake

Type:
    

float in [1e-06, inf], default 20.0

capture_emission
    

Bake emissive surfaces for more accurate lighting

Type:
    

boolean, default True

capture_indirect
    

Bake light bounces from light sources for more accurate lighting

Type:
    

boolean, default True

capture_world
    

Bake incoming light from the world instead of just the visibility for more accurate lighting, but lose correct blending to surrounding irradiance volumes

Type:
    

boolean, default False

clamp_direct
    

Clamp the direct lighting intensity to reduce noise (0 to disable)

Type:
    

float in [0, inf], default 0.0

clamp_indirect
    

Clamp the indirect lighting intensity to reduce noise (0 to disable)

Type:
    

float in [0, inf], default 10.0

dilation_radius
    

Radius in grid sample to search valid grid samples to copy into invalid grid samples

Type:
    

float in [1, 5], default 1.0

dilation_threshold
    

Ratio of front-facing surface hits under which a grid sample will reuse neighbors grid sample lighting

Type:
    

float in [0, 1], default 0.5

escape_bias
    

Distance to search for valid capture positions to prevent lighting artifacts

Type:
    

float in [0, 1], default 0.1

facing_bias
    

Smoother irradiance interpolation but introduce light bleeding

Type:
    

float in [0, inf], default 0.5

intensity
    

Modify the intensity of the lighting captured by this probe

Type:
    

float in [0, inf], default 1.0

normal_bias
    

Offset sampling of the irradiance grid in the surface normal direction to reduce light bleeding

Type:
    

float in [0, inf], default 0.3

resolution_x
    

Number of samples along the x axis of the volume

Type:
    

int in [1, 256], default 4

resolution_y
    

Number of samples along the y axis of the volume

Type:
    

int in [1, 256], default 4

resolution_z
    

Number of samples along the z axis of the volume

Type:
    

int in [1, 256], default 4

surface_bias
    

Moves capture points away from surfaces to prevent artifacts

Type:
    

float in [0, 1], default 0.05

surfel_density
    

Number of surfels to spawn in one local unit distance (higher values improve quality)

Type:
    

int in [1, inf], default 20

validity_threshold
    

Ratio of front-facing surface hits under which a grid sample will not be considered for lighting

Type:
    

float in [0, 1], default 0.4

view_bias
    

Offset sampling of the irradiance grid in the viewing direction to reduce light bleeding

Type:
    

float in [0, inf], default 0.0

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

| 

  * [`ID.library_weak_reference`](../I/bpy.types.ID.md#bpy.types.ID.library_weak_reference "bpy.types.ID.library_weak_reference")
  * [`ID.asset_data`](../I/bpy.types.ID.md#bpy.types.ID.asset_data "bpy.types.ID.asset_data")
  * [`ID.override_library`](../I/bpy.types.ID.md#bpy.types.ID.override_library "bpy.types.ID.override_library")
  * [`ID.preview`](../I/bpy.types.ID.md#bpy.types.ID.preview "bpy.types.ID.preview")
  * [`LightProbe.type`](bpy.types.LightProbe.md#bpy.types.LightProbe.type "bpy.types.LightProbe.type")
  * [`LightProbe.clip_start`](bpy.types.LightProbe.md#bpy.types.LightProbe.clip_start "bpy.types.LightProbe.clip_start")
  * [`LightProbe.show_clip`](bpy.types.LightProbe.md#bpy.types.LightProbe.show_clip "bpy.types.LightProbe.show_clip")
  * [`LightProbe.show_influence`](bpy.types.LightProbe.md#bpy.types.LightProbe.show_influence "bpy.types.LightProbe.show_influence")
  * [`LightProbe.influence_distance`](bpy.types.LightProbe.md#bpy.types.LightProbe.influence_distance "bpy.types.LightProbe.influence_distance")
  * [`LightProbe.visibility_buffer_bias`](bpy.types.LightProbe.md#bpy.types.LightProbe.visibility_buffer_bias "bpy.types.LightProbe.visibility_buffer_bias")
  * [`LightProbe.visibility_bleed_bias`](bpy.types.LightProbe.md#bpy.types.LightProbe.visibility_bleed_bias "bpy.types.LightProbe.visibility_bleed_bias")
  * [`LightProbe.visibility_blur`](bpy.types.LightProbe.md#bpy.types.LightProbe.visibility_blur "bpy.types.LightProbe.visibility_blur")
  * [`LightProbe.visibility_collection`](bpy.types.LightProbe.md#bpy.types.LightProbe.visibility_collection "bpy.types.LightProbe.visibility_collection")
  * [`LightProbe.invert_visibility_collection`](bpy.types.LightProbe.md#bpy.types.LightProbe.invert_visibility_collection "bpy.types.LightProbe.invert_visibility_collection")
  * [`LightProbe.show_data`](bpy.types.LightProbe.md#bpy.types.LightProbe.show_data "bpy.types.LightProbe.show_data")
  * [`LightProbe.use_data_display`](bpy.types.LightProbe.md#bpy.types.LightProbe.use_data_display "bpy.types.LightProbe.use_data_display")
  * [`LightProbe.data_display_size`](bpy.types.LightProbe.md#bpy.types.LightProbe.data_display_size "bpy.types.LightProbe.data_display_size")
  * [`LightProbe.animation_data`](bpy.types.LightProbe.md#bpy.types.LightProbe.animation_data "bpy.types.LightProbe.animation_data")

  
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
  * [`LightProbe.bl_rna_get_subclass`](bpy.types.LightProbe.md#bpy.types.LightProbe.bl_rna_get_subclass "bpy.types.LightProbe.bl_rna_get_subclass")
  * [`LightProbe.bl_rna_get_subclass_py`](bpy.types.LightProbe.md#bpy.types.LightProbe.bl_rna_get_subclass_py "bpy.types.LightProbe.bl_rna_get_subclass_py")

  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
