# LightProbe(ID)

base classes — [[bpy_struct]], [[ID]]

subclasses — [[LightProbePlane]], [[LightProbeSphere]], [[LightProbeVolume]]

_class _bpy.types.LightProbe(_ID_)
    

Light Probe data-block for lighting capture objects

animation_data
    

Animation data for this data-block

Type:
    

[[AnimData]], (readonly)

clip_start
    

Probe clip start, below which objects will not appear in reflections

Type:
    

float in [1e-06, inf], default 0.8

data_display_size
    

Viewport display size of the sampled data

Type:
    

float in [0, inf], default 0.1

influence_distance
    

Influence distance of the probe

Type:
    

float in [0, inf], default 2.5

invert_visibility_collection
    

Invert visibility collection (Deprecated)

Type:
    

boolean, default False

show_clip
    

Show the clipping distances in the 3D view

Type:
    

boolean, default False

show_data
    

Deprecated, use use_data_display instead

Type:
    

boolean, default False

show_influence
    

Show the influence volume in the 3D view

Type:
    

boolean, default True

type
    

Type of light probe

  * `SPHERE` Sphere – Light probe that captures precise lighting from all directions at a single point in space.

  * `PLANE` Plane – Light probe that captures incoming light from a single direction on a plane.

  * `VOLUME` Volume – Light probe that captures low frequency lighting inside a volume.


Type:
    

enum in [`'SPHERE'`, `'PLANE'`, `'VOLUME'`], default `'SPHERE'`, (readonly)

use_data_display
    

Display sampled data in the viewport to debug captured light

Type:
    

boolean, default False

visibility_bleed_bias
    

Bias for reducing light-bleed on variance shadow maps (Deprecated)

Type:
    

float in [0, 1], default 0.0

visibility_blur
    

Filter size of the visibility blur (Deprecated)

Type:
    

float in [0, 1], default 0.2

visibility_buffer_bias
    

Bias for reducing self shadowing (Deprecated)

Type:
    

float in [0.001, 9999], default 1.0

visibility_collection
    

Restrict objects visible for this probe (Deprecated)

Type:
    

[[Collection]]

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

  * [[bpy.context.lightprobe]]
  * [[BlendData.lightprobes]]

| 

  * [[BlendDataProbes.new]]
  * [[BlendDataProbes.remove]]

  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
