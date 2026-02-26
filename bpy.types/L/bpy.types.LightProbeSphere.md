# LightProbeSphere(LightProbe)

base classes — [[bpy_struct]], [[ID]], [[LightProbe]]

_class _bpy.types.LightProbeSphere(_LightProbe_)
    

Light probe that captures precise lighting from all directions at a single point in space

clip_end
    

Probe clip end, beyond which objects will not appear in reflections

Type:
    

float in [1e-06, inf], default 20.0

falloff
    

Control how fast the probe influence decreases

Type:
    

float in [0, 1], default 0.2

influence_type
    

Type of influence volume

Type:
    

enum in [`'ELIPSOID'`, `'BOX'`], default `'ELIPSOID'`

parallax_distance
    

Lowest corner of the parallax bounding box

Type:
    

float in [0, inf], default 2.5

parallax_type
    

Type of parallax volume

Type:
    

enum in [`'ELIPSOID'`, `'BOX'`], default `'ELIPSOID'`

show_parallax
    

Show the parallax correction volume in the 3D view

Type:
    

boolean, default False

use_custom_parallax
    

Enable custom settings for the parallax correction volume

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
