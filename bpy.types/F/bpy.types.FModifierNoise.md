# FModifierNoise(FModifier)

base classes — [[bpy_struct]], [[FModifier]]

_class _bpy.types.FModifierNoise(_FModifier_)
    

Give randomness to the modified F-Curve

blend_type
    

Method of modifying the existing F-Curve

Type:
    

enum in [`'REPLACE'`, `'ADD'`, `'SUBTRACT'`, `'MULTIPLY'`], default `'REPLACE'`

depth
    

Amount of fine level detail present in the noise

Type:
    

int in [0, 32767], default 0

lacunarity
    

Gap between successive frequencies. Depth needs to be greater than 0 for this to have an effect

Type:
    

float in [-inf, inf], default 2.0

offset
    

Time offset for the noise effect

Type:
    

float in [-inf, inf], default 0.0

phase
    

A random seed for the noise effect

Type:
    

float in [-inf, inf], default 1.0

roughness
    

Amount of high frequency detail. Depth needs to be greater than 0 for this to have an effect

Type:
    

float in [-inf, inf], default 0.5

scale
    

Scaling (in time) of the noise

Type:
    

float in [-inf, inf], default 1.0

strength
    

Amplitude of the noise - the amount that it modifies the underlying curve

Type:
    

float in [-inf, inf], default 1.0

use_legacy_noise
    

Use the legacy way of generating noise. Has the issue that it can produce values outside of -1/1

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
  * [[FModifier.name]]
  * [[FModifier.type]]
  * [[FModifier.show_expanded]]
  * [[FModifier.mute]]
  * [[FModifier.is_valid]]
  * [[FModifier.active]]

| 

  * [[FModifier.use_restricted_range]]
  * [[FModifier.frame_start]]
  * [[FModifier.frame_end]]
  * [[FModifier.blend_in]]
  * [[FModifier.blend_out]]
  * [[FModifier.use_influence]]
  * [[FModifier.influence]]

  
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

| 

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
  * [[FModifier.bl_rna_get_subclass]]
  * [[FModifier.bl_rna_get_subclass_py]]

  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
