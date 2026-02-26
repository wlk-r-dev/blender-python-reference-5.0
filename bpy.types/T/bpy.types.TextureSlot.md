# TextureSlot(bpy_struct)

base class — [[bpy_struct]]

subclasses — [[BrushTextureSlot]], [[LineStyleTextureSlot]], [[ParticleSettingsTextureSlot]]

_class _bpy.types.TextureSlot(_bpy_struct_)
    

Texture slot defining the mapping and influence of a texture

blend_type
    

Mode used to apply the texture

Type:
    

enum in [`'MIX'`, `'DARKEN'`, `'MULTIPLY'`, `'LIGHTEN'`, `'SCREEN'`, `'ADD'`, `'OVERLAY'`, `'SOFT_LIGHT'`, `'LINEAR_LIGHT'`, `'DIFFERENCE'`, `'SUBTRACT'`, `'DIVIDE'`, `'HUE'`, `'SATURATION'`, `'COLOR'`, `'VALUE'`], default `'MIX'`

color
    

Default color for textures that don’t return RGB or when RGB to intensity is enabled

Type:
    

[[mathutils.Color]] of 3 items in [0, inf], default (1.0, 1.0, 1.0)

default_value
    

Value to use for Ref, Spec, Amb, Emit, Alpha, RayMir, TransLu and Hard

Type:
    

float in [-inf, inf], default 1.0

name
    

Texture slot name

Type:
    

string, default “”, (readonly, never None)

offset
    

Fine tune of the texture mapping X, Y and Z locations

Type:
    

[[mathutils.Vector]] of 3 items in [-inf, inf], default (0.0, 0.0, 0.0)

output_node
    

Which output node to use, for node-based textures

Type:
    

enum in [`'DEFAULT'`], default `'DEFAULT'`

scale
    

Set scaling for the texture’s X, Y and Z sizes

Type:
    

[[mathutils.Vector]] of 3 items in [-inf, inf], default (1.0, 1.0, 1.0)

texture
    

Texture data-block used by this texture slot

Type:
    

[[Texture]]

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

  * [[bpy.context.texture_slot]]

| 

  * [[UILayout.template_preview]]

  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
