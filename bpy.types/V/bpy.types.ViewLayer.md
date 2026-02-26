# ViewLayer(bpy_struct)

base class — [`bpy_struct`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct "bpy.types.bpy_struct")

_class _bpy.types.ViewLayer(_bpy_struct_)
    

View layer

active_aov
    

Active AOV

Type:
    

[`AOV`](../A/bpy.types.AOV.md#bpy.types.AOV "bpy.types.AOV"), (readonly)

active_aov_index
    

Index of active AOV

Type:
    

int in [0, inf], default 0

active_layer_collection
    

Active layer collection in this view layer’s hierarchy

Type:
    

[`LayerCollection`](../L/bpy.types.LayerCollection.md#bpy.types.LayerCollection "bpy.types.LayerCollection"), (never None)

active_lightgroup
    

Active Lightgroup

Type:
    

[`Lightgroup`](../L/bpy.types.Lightgroup.md#bpy.types.Lightgroup "bpy.types.Lightgroup"), (readonly)

active_lightgroup_index
    

Index of active lightgroup

Type:
    

int in [0, inf], default 0

aovs
    

Type:
    

[`AOVs`](../A/bpy.types.AOVs.md#bpy.types.AOVs "bpy.types.AOVs") [`bpy_prop_collection`](../_other/bpy.types.bpy_prop_collection.md#bpy.types.bpy_prop_collection "bpy.types.bpy_prop_collection") of [`AOV`](../A/bpy.types.AOV.md#bpy.types.AOV "bpy.types.AOV"), (readonly)

cycles
    

Cycles ViewLayer Settings

Type:
    

`CyclesRenderLayerSettings`, (readonly)

depsgraph
    

Dependencies in the scene data

Type:
    

[`Depsgraph`](../D/bpy.types.Depsgraph.md#bpy.types.Depsgraph "bpy.types.Depsgraph"), (readonly)

eevee
    

View layer settings for EEVEE

Type:
    

[`ViewLayerEEVEE`](bpy.types.ViewLayerEEVEE.md#bpy.types.ViewLayerEEVEE "bpy.types.ViewLayerEEVEE"), (readonly, never None)

freestyle_settings
    

Type:
    

[`FreestyleSettings`](../F/bpy.types.FreestyleSettings.md#bpy.types.FreestyleSettings "bpy.types.FreestyleSettings"), (readonly, never None)

has_export_collections
    

At least one Collection in this View Layer has an exporter

Type:
    

boolean, default False, (readonly)

layer_collection
    

Root of collections hierarchy of this view layer, its ‘collection’ pointer property is the same as the scene’s master collection

Type:
    

[`LayerCollection`](../L/bpy.types.LayerCollection.md#bpy.types.LayerCollection "bpy.types.LayerCollection"), (readonly, never None)

lightgroups
    

Type:
    

[`Lightgroups`](../L/bpy.types.Lightgroups.md#bpy.types.Lightgroups "bpy.types.Lightgroups") [`bpy_prop_collection`](../_other/bpy.types.bpy_prop_collection.md#bpy.types.bpy_prop_collection "bpy.types.bpy_prop_collection") of [`Lightgroup`](../L/bpy.types.Lightgroup.md#bpy.types.Lightgroup "bpy.types.Lightgroup"), (readonly)

material_override
    

Material to override all other materials in this view layer

Type:
    

[`Material`](../M/bpy.types.Material.md#bpy.types.Material "bpy.types.Material")

name
    

View layer name

Type:
    

string, default “”, (never None)

objects
    

All the objects in this layer

Type:
    

[`LayerObjects`](../L/bpy.types.LayerObjects.md#bpy.types.LayerObjects "bpy.types.LayerObjects") [`bpy_prop_collection`](../_other/bpy.types.bpy_prop_collection.md#bpy.types.bpy_prop_collection "bpy.types.bpy_prop_collection") of [`Object`](../O/bpy.types.Object.md#bpy.types.Object "bpy.types.Object"), (readonly)

pass_alpha_threshold
    

Z, Index, normal, UV and vector passes are only affected by surfaces with alpha transparency equal to or higher than this threshold

Type:
    

float in [0, 1], default 0.5

pass_cryptomatte_depth
    

Sets how many unique objects can be distinguished per pixel

Type:
    

int in [2, 16], default 6

samples
    

Override number of render samples for this view layer, 0 will use the scene setting

Type:
    

int in [0, inf], default 0

use
    

Enable or disable rendering of this View Layer

Type:
    

boolean, default True

use_ao
    

Render Ambient Occlusion in this Layer

Type:
    

boolean, default True

use_freestyle
    

Render stylized strokes in this Layer

Type:
    

boolean, default True

use_grease_pencil
    

Render Grease Pencil on this layer

Type:
    

boolean, default True

use_motion_blur
    

Render motion blur in this Layer, if enabled in the scene

Type:
    

boolean, default True

use_pass_ambient_occlusion
    

Deliver Ambient Occlusion pass

Type:
    

boolean, default False

use_pass_combined
    

Deliver full combined RGBA buffer

Type:
    

boolean, default True

use_pass_cryptomatte_accurate
    

Generate a more accurate cryptomatte pass

Type:
    

boolean, default True

use_pass_cryptomatte_asset
    

Render cryptomatte asset pass, for isolating groups of objects with the same parent

Type:
    

boolean, default False

use_pass_cryptomatte_material
    

Render cryptomatte material pass, for isolating materials in compositing

Type:
    

boolean, default False

use_pass_cryptomatte_object
    

Render cryptomatte object pass, for isolating objects in compositing

Type:
    

boolean, default False

use_pass_diffuse_color
    

Deliver diffuse color pass

Type:
    

boolean, default False

use_pass_diffuse_direct
    

Deliver diffuse direct pass

Type:
    

boolean, default False

use_pass_diffuse_indirect
    

Deliver diffuse indirect pass

Type:
    

boolean, default False

use_pass_emit
    

Deliver emission pass

Type:
    

boolean, default False

use_pass_environment
    

Deliver environment lighting pass

Type:
    

boolean, default False

use_pass_glossy_color
    

Deliver glossy color pass

Type:
    

boolean, default False

use_pass_glossy_direct
    

Deliver glossy direct pass

Type:
    

boolean, default False

use_pass_glossy_indirect
    

Deliver glossy indirect pass

Type:
    

boolean, default False

use_pass_grease_pencil
    

Deliver Grease Pencil render result in a separate pass

Type:
    

boolean, default False

use_pass_material_index
    

Deliver material index pass

Type:
    

boolean, default False

use_pass_mist
    

Deliver mist factor pass (0.0 to 1.0)

Type:
    

boolean, default False

use_pass_normal
    

Deliver normal pass

Type:
    

boolean, default False

use_pass_object_index
    

Deliver object index pass

Type:
    

boolean, default False

use_pass_position
    

Deliver position pass

Type:
    

boolean, default False

use_pass_shadow
    

Deliver shadow pass

Type:
    

boolean, default False

use_pass_subsurface_color
    

Deliver subsurface color pass

Type:
    

boolean, default False

use_pass_subsurface_direct
    

Deliver subsurface direct pass

Type:
    

boolean, default False

use_pass_subsurface_indirect
    

Deliver subsurface indirect pass

Type:
    

boolean, default False

use_pass_transmission_color
    

Deliver transmission color pass

Type:
    

boolean, default False

use_pass_transmission_direct
    

Deliver transmission direct pass

Type:
    

boolean, default False

use_pass_transmission_indirect
    

Deliver transmission indirect pass

Type:
    

boolean, default False

use_pass_uv
    

Deliver texture UV pass

Type:
    

boolean, default False

use_pass_vector
    

Deliver speed vector pass

Type:
    

boolean, default False

use_pass_z
    

Deliver depth values pass

Type:
    

boolean, default False

use_sky
    

Render Sky in this Layer

Type:
    

boolean, default True

use_solid
    

Render Solid faces in this Layer

Type:
    

boolean, default True

use_strand
    

Render Strands in this Layer

Type:
    

boolean, default True

use_volumes
    

Render volumes in this Layer

Type:
    

boolean, default True

world_override
    

Override world in this view layer

Type:
    

[`World`](../W/bpy.types.World.md#bpy.types.World "bpy.types.World")

bl_system_properties_get(_*_ , _do_create =False_)
    

DEBUG ONLY. Internal access to runtime-defined RNA data storage, intended solely for testing and debugging purposes. Do not access it in regular scripting work, and in particular, do not assume that it contains writable data

Parameters:
    

**do_create** (_boolean_ _,__(__optional_ _)_) – Ensure that system properties are created if they do not exist yet

Returns:
    

The system properties root container, or None if there are no system properties stored in this data yet, and its creation was not requested

Return type:
    

[`PropertyGroup`](../P/bpy.types.PropertyGroup.md#bpy.types.PropertyGroup "bpy.types.PropertyGroup")

_classmethod _update_render_passes()
    

Requery the enabled render passes from the render engine

update()
    

Update data tagged to be updated from previous access to data or operators

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

| 


  
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

| 

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
  * [`bpy_struct.values`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.values "bpy.types.bpy_struct.values")

  
---|---  
  
## References

  * [`bpy.context.view_layer`](../../bpy.context.md#bpy.context.view_layer "bpy.context.view_layer")
  * [`Context.view_layer`](../C/bpy.types.Context.md#bpy.types.Context.view_layer "bpy.types.Context.view_layer")
  * [`Depsgraph.view_layer`](../D/bpy.types.Depsgraph.md#bpy.types.Depsgraph.view_layer "bpy.types.Depsgraph.view_layer")
  * [`Depsgraph.view_layer_eval`](../D/bpy.types.Depsgraph.md#bpy.types.Depsgraph.view_layer_eval "bpy.types.Depsgraph.view_layer_eval")
  * [`ID.override_hierarchy_create`](../I/bpy.types.ID.md#bpy.types.ID.override_hierarchy_create "bpy.types.ID.override_hierarchy_create")
  * [`IDOverrideLibrary.resync`](../I/bpy.types.IDOverrideLibrary.md#bpy.types.IDOverrideLibrary.resync "bpy.types.IDOverrideLibrary.resync")
  * [`LayerCollection.has_selected_objects`](../L/bpy.types.LayerCollection.md#bpy.types.LayerCollection.has_selected_objects "bpy.types.LayerCollection.has_selected_objects")
  * [`Object.hide_get`](../O/bpy.types.Object.md#bpy.types.Object.hide_get "bpy.types.Object.hide_get")
  * [`Object.hide_set`](../O/bpy.types.Object.md#bpy.types.Object.hide_set "bpy.types.Object.hide_set")
  * [`Object.holdout_get`](../O/bpy.types.Object.md#bpy.types.Object.holdout_get "bpy.types.Object.holdout_get")
  * [`Object.indirect_only_get`](../O/bpy.types.Object.md#bpy.types.Object.indirect_only_get "bpy.types.Object.indirect_only_get")

| 

  * [`Object.select_get`](../O/bpy.types.Object.md#bpy.types.Object.select_get "bpy.types.Object.select_get")
  * [`Object.select_set`](../O/bpy.types.Object.md#bpy.types.Object.select_set "bpy.types.Object.select_set")
  * [`Object.visible_get`](../O/bpy.types.Object.md#bpy.types.Object.visible_get "bpy.types.Object.visible_get")
  * [`RenderEngine.register_pass`](../R/bpy.types.RenderEngine.md#bpy.types.RenderEngine.register_pass "bpy.types.RenderEngine.register_pass")
  * [`RenderEngine.update_render_passes`](../R/bpy.types.RenderEngine.md#bpy.types.RenderEngine.update_render_passes "bpy.types.RenderEngine.update_render_passes")
  * [`Scene.statistics`](../S/bpy.types.Scene.md#bpy.types.Scene.statistics "bpy.types.Scene.statistics")
  * [`Scene.view_layers`](../S/bpy.types.Scene.md#bpy.types.Scene.view_layers "bpy.types.Scene.view_layers")
  * [`ViewLayers.new`](bpy.types.ViewLayers.md#bpy.types.ViewLayers.new "bpy.types.ViewLayers.new")
  * [`ViewLayers.remove`](bpy.types.ViewLayers.md#bpy.types.ViewLayers.remove "bpy.types.ViewLayers.remove")
  * [`Window.view_layer`](../W/bpy.types.Window.md#bpy.types.Window.view_layer "bpy.types.Window.view_layer")

  
---|---
  *[*]: Keyword-only parameters separator (PEP 3102)
  *[/]: Positional-only parameter separator (PEP 570)
