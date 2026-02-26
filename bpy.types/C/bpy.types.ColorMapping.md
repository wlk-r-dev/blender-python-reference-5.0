# ColorMapping(bpy_struct)

base class — [[bpy_struct]]

_class _bpy.types.ColorMapping(_bpy_struct_)
    

Color mapping settings

blend_color
    

Blend color to mix with texture output color

Type:
    

[[mathutils.Color]] of 3 items in [0, inf], default (0.0, 0.0, 0.0)

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
    

[[ColorRamp]], (readonly)

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

| 


  
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

| 

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
  * [[bpy_struct.values]]

  
---|---  
  
## References

  * [[ShaderNodeTexBrick.color_mapping]]
  * [[ShaderNodeTexChecker.color_mapping]]
  * [[ShaderNodeTexEnvironment.color_mapping]]
  * [[ShaderNodeTexGabor.color_mapping]]
  * [[ShaderNodeTexGradient.color_mapping]]
  * [[ShaderNodeTexImage.color_mapping]]

| 

  * [[ShaderNodeTexMagic.color_mapping]]
  * [[ShaderNodeTexNoise.color_mapping]]
  * [[ShaderNodeTexSky.color_mapping]]
  * [[ShaderNodeTexVoronoi.color_mapping]]
  * [[ShaderNodeTexWave.color_mapping]]

  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
