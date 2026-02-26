# SceneDisplay(bpy_struct)

base class — [`bpy_struct`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct "bpy.types.bpy_struct")

_class _bpy.types.SceneDisplay(_bpy_struct_)
    

Scene display settings for 3D viewport

light_direction
    

Direction of the light for shadows and highlights

Type:
    

[`mathutils.Vector`](mathutils.md#mathutils.Vector "mathutils.Vector") of 3 items in [-inf, inf], default (0.57735, 0.57735, 0.57735)

matcap_ssao_attenuation
    

Attenuation constant

Type:
    

float in [0, 100000], default 1.0

matcap_ssao_distance
    

Distance of object that contribute to the cavity/edge effect

Type:
    

float in [0, 100000], default 0.2

matcap_ssao_samples
    

Number of samples

Type:
    

int in [1, 500], default 16

render_aa
    

Method of anti-aliasing when rendering final image

  * `OFF` No Anti-Aliasing – Scene will be rendering without any anti-aliasing.

  * `FXAA` Single Pass Anti-Aliasing – Scene will be rendered using a single pass anti-aliasing method (FXAA).

  * `5` 5 Samples – Scene will be rendered using 5 anti-aliasing samples.

  * `8` 8 Samples – Scene will be rendered using 8 anti-aliasing samples.

  * `11` 11 Samples – Scene will be rendered using 11 anti-aliasing samples.

  * `16` 16 Samples – Scene will be rendered using 16 anti-aliasing samples.

  * `32` 32 Samples – Scene will be rendered using 32 anti-aliasing samples.


Type:
    

enum in [`'OFF'`, `'FXAA'`, `'5'`, `'8'`, `'11'`, `'16'`, `'32'`], default `'8'`

shading
    

Shading settings for OpenGL render engine

Type:
    

[`View3DShading`](../V/bpy.types.View3DShading.md#bpy.types.View3DShading "bpy.types.View3DShading"), (readonly)

shadow_focus
    

Shadow factor hardness

Type:
    

float in [0, 1], default 0.0

shadow_shift
    

Shadow termination angle

Type:
    

float in [0, 1], default 0.1

viewport_aa
    

Method of anti-aliasing when rendering 3d viewport

  * `OFF` No Anti-Aliasing – Scene will be rendering without any anti-aliasing.

  * `FXAA` Single Pass Anti-Aliasing – Scene will be rendered using a single pass anti-aliasing method (FXAA).

  * `5` 5 Samples – Scene will be rendered using 5 anti-aliasing samples.

  * `8` 8 Samples – Scene will be rendered using 8 anti-aliasing samples.

  * `11` 11 Samples – Scene will be rendered using 11 anti-aliasing samples.

  * `16` 16 Samples – Scene will be rendered using 16 anti-aliasing samples.

  * `32` 32 Samples – Scene will be rendered using 32 anti-aliasing samples.


Type:
    

enum in [`'OFF'`, `'FXAA'`, `'5'`, `'8'`, `'11'`, `'16'`, `'32'`], default `'FXAA'`

_classmethod _bl_rna_get_subclass(_id_ , _default =None_, _/_)
    

Parameters:
    

**id** (_str_) – The RNA type identifier.

Returns:
    

The RNA type or default when not found.

Return type:
    

[`bpy.types.Struct`](bpy.types.Struct.md#bpy.types.Struct "bpy.types.Struct") subclass

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

  * [`Scene.display`](bpy.types.Scene.md#bpy.types.Scene.display "bpy.types.Scene.display")

| 


  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
