# Light(ID)

base classes — [[bpy_struct]], [[ID]]

subclasses — [[AreaLight]], [[PointLight]], [[SpotLight]], [[SunLight]]

_class _bpy.types.Light(_ID_)
    

Light data-block for lighting a scene

animation_data
    

Animation data for this data-block

Type:
    

[[AnimData]], (readonly)

color
    

Light color

Type:
    

[[mathutils.Color]] of 3 items in [0, inf], default (1.0, 1.0, 1.0)

cutoff_distance
    

Distance at which the light influence will be set to 0

Type:
    

float in [0, inf], default 40.0

cycles
    

Cycles light settings

Type:
    

`CyclesLightSettings`, (readonly)

diffuse_factor
    

Diffuse reflection multiplier

Type:
    

float in [0, inf], default 1.0

exposure
    

Scales the power of the light exponentially, multiplying the intensity by 2^exposure

Type:
    

float in [-32, 32], default 0.0

node_tree
    

Node tree for node based lights

Type:
    

[[NodeTree]], (readonly)

normalize
    

Normalize intensity by light area, for consistent total light output regardless of size and shape

Type:
    

boolean, default True

specular_factor
    

Specular reflection multiplier

Type:
    

float in [0, inf], default 1.0

temperature
    

Light color temperature in Kelvin

Type:
    

float in [800, 20000], default 6500.0

temperature_color
    

Color from Temperature

Type:
    

[[mathutils.Color]] of 3 items in [0, inf], default (0.0, 0.0, 0.0), (readonly)

transmission_factor
    

Transmission light multiplier

Type:
    

float in [0, inf], default 1.0

type
    

Type of light

Type:
    

enum in [Light Type Items](../../bpy_types_enum_items/light_type_items.md#rna-enum-light-type-items), default `'POINT'`

use_custom_distance
    

Use custom attenuation distance instead of global light threshold

Type:
    

boolean, default False

use_nodes
    

Use shader nodes to render the light

Type:
    

boolean, default False

use_shadow
    

Type:
    

boolean, default True

use_temperature
    

Use blackbody temperature to define a natural light color

Type:
    

boolean, default False

volume_factor
    

Volume light multiplier

Type:
    

float in [0, inf], default 1.0

area(_*_ , _matrix_world =((0.0, 0.0, 0.0, 0.0), (0.0, 0.0, 0.0, 0.0), (0.0, 0.0, 0.0, 0.0), (0.0, 0.0, 0.0, 0.0))_)
    

Compute light area based on type and shape. The normalize option divides light intensity by this area

Parameters:
    

**matrix_world** ([[mathutils.Matrix]] of 4 * 4 items in [-inf, inf], (optional)) – Object to world space transformation matrix

Returns:
    

area

Return type:
    

float in [-inf, inf]

inline_shader_nodes()
    

Get the inlined shader nodes of this light. This preprocesses the node tree to remove nested groups, repeat zones and more.

Returns:
    

The inlined shader nodes.

Return type:
    

[[bpy.types.InlineShaderNodes]]

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

  * [[bpy.context.light]]
  * [[BlendData.lights]]

| 

  * [[BlendDataLights.new]]
  * [[BlendDataLights.remove]]

  
---|---
  *[*]: Keyword-only parameters separator (PEP 3102)
  *[/]: Positional-only parameter separator (PEP 570)
