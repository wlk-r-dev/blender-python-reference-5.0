# BrushTextureSlot(TextureSlot)

base classes — [[bpy_struct]], [[TextureSlot]]

_class _bpy.types.BrushTextureSlot(_TextureSlot_)
    

Texture slot for textures in a Brush data-block

angle
    

Brush texture rotation

Type:
    

float in [0, 6.28319], default 0.0

has_random_texture_angle
    

Type:
    

boolean, default False, (readonly)

has_texture_angle
    

Type:
    

boolean, default False, (readonly)

has_texture_angle_source
    

Type:
    

boolean, default False, (readonly)

map_mode
    

Type:
    

enum in [`'VIEW_PLANE'`, `'AREA_PLANE'`, `'TILED'`, `'3D'`, `'RANDOM'`, `'STENCIL'`], default `'VIEW_PLANE'`

mask_map_mode
    

Type:
    

enum in [`'VIEW_PLANE'`, `'TILED'`, `'RANDOM'`, `'STENCIL'`], default `'VIEW_PLANE'`

random_angle
    

Brush texture random angle

Type:
    

float in [0, 6.28319], default 6.28319

use_rake
    

Type:
    

boolean, default False

use_random
    

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
  * [[TextureSlot.texture]]
  * [[TextureSlot.name]]
  * [[TextureSlot.offset]]
  * [[TextureSlot.scale]]

| 

  * [[TextureSlot.color]]
  * [[TextureSlot.blend_type]]
  * [[TextureSlot.default_value]]
  * [[TextureSlot.output_node]]

  
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
  * [[TextureSlot.bl_rna_get_subclass]]
  * [[TextureSlot.bl_rna_get_subclass_py]]

  
---|---  
  
## References

  * [[Brush.mask_texture_slot]]

| 

  * [[Brush.texture_slot]]

  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
