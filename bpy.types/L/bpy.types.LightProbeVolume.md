# LightProbeVolume(LightProbe)

base classes — [[bpy_struct]], [[ID]], [[LightProbe]]

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

| 

  * [[ID.library_weak_reference]]
  * [[ID.asset_data]]
  * [[ID.override_library]]
  * [[ID.preview]]
  * [[LightProbe.type]]
  * [[LightProbe.clip_start]]
  * [[LightProbe.show_clip]]
  * [[LightProbe.show_influence]]
  * [[LightProbe.influence_distance]]
  * [[LightProbe.visibility_buffer_bias]]
  * [[LightProbe.visibility_bleed_bias]]
  * [[LightProbe.visibility_blur]]
  * [[LightProbe.visibility_collection]]
  * [[LightProbe.invert_visibility_collection]]
  * [[LightProbe.show_data]]
  * [[LightProbe.use_data_display]]
  * [[LightProbe.data_display_size]]
  * [[LightProbe.animation_data]]

  
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
  * [[LightProbe.bl_rna_get_subclass]]
  * [[LightProbe.bl_rna_get_subclass_py]]

  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
