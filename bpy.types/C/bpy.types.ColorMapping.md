# ColorMapping(bpy_struct)

base class — [`bpy_struct`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct "bpy.types.bpy_struct")

_class _bpy.types.ColorMapping(_bpy_struct_)
    

Color mapping settings

blend_color
    

Blend color to mix with texture output color

Type:
    

[`mathutils.Color`](mathutils.md#mathutils.Color "mathutils.Color") of 3 items in [0, inf], default (0.0, 0.0, 0.0)

blend_factor
    

Type:
    

float in [-inf, inf], default 0.0

blend_type
    

Mode used to mix with texture output color

Type:
    

enum in [`'MIX'`, `'DARKEN'`, `'MULTIPLY'`, `'LIGHTEN'`, `'SCREEN'`, `'ADD'`, `'OVERLAY'`, `'SOFT_LIGHT'`, `'LINEAR_LIGHT'`, `'DIFFERENCE'`, `'SUBTRACT'`, `'DIVIDE'`, `'HUE'`, `'SATURATION'`, `'COLOR'`, `'VALUE'`], default `'MIX'`

brightness
    

Adjust the brightness of the texture

Type:
    

float in [0, 2], default 0.0

color_ramp
    

Type:
    

[`ColorRamp`](bpy.types.ColorRamp.md#bpy.types.ColorRamp "bpy.types.ColorRamp"), (readonly)

contrast
    

Adjust the contrast of the texture

Type:
    

float in [0, 5], default 0.0

saturation
    

Adjust the saturation of colors in the texture

Type:
    

float in [0, 2], default 0.0

use_color_ramp
    

Toggle color ramp operations

Type:
    

boolean, default False

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

  * [`ShaderNodeTexBrick.color_mapping`](../S/bpy.types.ShaderNodeTexBrick.md#bpy.types.ShaderNodeTexBrick.color_mapping "bpy.types.ShaderNodeTexBrick.color_mapping")
  * [`ShaderNodeTexChecker.color_mapping`](../S/bpy.types.ShaderNodeTexChecker.md#bpy.types.ShaderNodeTexChecker.color_mapping "bpy.types.ShaderNodeTexChecker.color_mapping")
  * [`ShaderNodeTexEnvironment.color_mapping`](../S/bpy.types.ShaderNodeTexEnvironment.md#bpy.types.ShaderNodeTexEnvironment.color_mapping "bpy.types.ShaderNodeTexEnvironment.color_mapping")
  * [`ShaderNodeTexGabor.color_mapping`](../S/bpy.types.ShaderNodeTexGabor.md#bpy.types.ShaderNodeTexGabor.color_mapping "bpy.types.ShaderNodeTexGabor.color_mapping")
  * [`ShaderNodeTexGradient.color_mapping`](../S/bpy.types.ShaderNodeTexGradient.md#bpy.types.ShaderNodeTexGradient.color_mapping "bpy.types.ShaderNodeTexGradient.color_mapping")
  * [`ShaderNodeTexImage.color_mapping`](../S/bpy.types.ShaderNodeTexImage.md#bpy.types.ShaderNodeTexImage.color_mapping "bpy.types.ShaderNodeTexImage.color_mapping")

| 

  * [`ShaderNodeTexMagic.color_mapping`](../S/bpy.types.ShaderNodeTexMagic.md#bpy.types.ShaderNodeTexMagic.color_mapping "bpy.types.ShaderNodeTexMagic.color_mapping")
  * [`ShaderNodeTexNoise.color_mapping`](../S/bpy.types.ShaderNodeTexNoise.md#bpy.types.ShaderNodeTexNoise.color_mapping "bpy.types.ShaderNodeTexNoise.color_mapping")
  * [`ShaderNodeTexSky.color_mapping`](../S/bpy.types.ShaderNodeTexSky.md#bpy.types.ShaderNodeTexSky.color_mapping "bpy.types.ShaderNodeTexSky.color_mapping")
  * [`ShaderNodeTexVoronoi.color_mapping`](../S/bpy.types.ShaderNodeTexVoronoi.md#bpy.types.ShaderNodeTexVoronoi.color_mapping "bpy.types.ShaderNodeTexVoronoi.color_mapping")
  * [`ShaderNodeTexWave.color_mapping`](../S/bpy.types.ShaderNodeTexWave.md#bpy.types.ShaderNodeTexWave.color_mapping "bpy.types.ShaderNodeTexWave.color_mapping")

  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
