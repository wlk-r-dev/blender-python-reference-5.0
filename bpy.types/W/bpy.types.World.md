# World(ID)

base classes — [[bpy_struct]], [[ID]]

_class _bpy.types.World(_ID_)
    

World data-block describing the environment and ambient lighting of a scene

animation_data
    

Animation data for this data-block

Type:
    

[[AnimData]], (readonly)

color
    

Color of the background

Type:
    

[[mathutils.Color]] of 3 items in [0, inf], default (0.05, 0.05, 0.05)

cycles
    

Cycles world settings

Type:
    

`CyclesWorldSettings`, (readonly)

cycles_visibility
    

Cycles visibility settings

Type:
    

`CyclesVisibilitySettings`, (readonly)

light_settings
    

World lighting settings

Type:
    

[[WorldLighting]], (readonly, never None)

lightgroup
    

Lightgroup that the world belongs to

Type:
    

string, default “”, (never None)

mist_settings
    

World mist settings

Type:
    

[[WorldMistSettings]], (readonly, never None)

node_tree
    

Node tree for node based worlds

Type:
    

[[NodeTree]], (readonly)

probe_resolution
    

Resolution when baked to a texture

Type:
    

enum in [`'128'`, `'256'`, `'512'`, `'1024'`, `'2048'`, `'4096'`], default `'1024'`

sun_angle
    

Angular diameter of the Sun as seen from the Earth

Type:
    

float in [0, 3.14159], default 0.00918043

sun_shadow_filter_radius
    

Blur shadow aliasing using Percentage Closer Filtering

Type:
    

float in [0, inf], default 1.0

sun_shadow_jitter_overblur
    

Apply shadow tracing to each jittered sample to reduce under-sampling artifacts

Type:
    

float in [0, 100], default 10.0

sun_shadow_maximum_resolution
    

Maximum size of a shadow map pixel. Higher values use less memory at the cost of shadow quality.

Type:
    

float in [0, inf], default 0.001

sun_threshold
    

If non-zero, the maximum value for world contribution that will be recorded inside the world light probe. The excess contribution is converted to a sun light. This reduces the light bleeding caused by very bright light sources.

Type:
    

float in [0, inf], default 10.0

use_eevee_finite_volume
    

The world’s volume used to be rendered by EEVEE Legacy. Conversion is needed for it to render properly.

Type:
    

boolean, default False

use_nodes
    

Use shader nodes to render the world

Deprecated since version 5.0: removal planned in version 6.0

Unused but kept for compatibility reasons. Setting the property has no effect, and getting it always returns True.

Type:
    

boolean, default False

use_sun_shadow
    

Enable sun shadow casting

Type:
    

boolean, default True

use_sun_shadow_jitter
    

Enable jittered soft shadows to increase shadow precision (disabled in viewport unless enabled in the render settings). Has a high performance impact.

Type:
    

boolean, default False

inline_shader_nodes()
    

Get the inlined shader nodes of this world. This preprocesses the node tree to remove nested groups, repeat zones and more.

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

  * [[bpy.context.world]]
  * [[BlendData.worlds]]
  * [[BlendDataWorlds.new]]

| 

  * [[BlendDataWorlds.remove]]
  * [[Scene.world]]
  * [[ViewLayer.world_override]]

  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
