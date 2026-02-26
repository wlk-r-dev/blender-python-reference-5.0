# UserSolidLight(bpy_struct)

base class — [[bpy_struct]]

_class _bpy.types.UserSolidLight(_bpy_struct_)
    

Light used for Studio lighting in solid shading mode

diffuse_color
    

Color of the light’s diffuse highlight

Type:
    

[[mathutils.Color]] of 3 items in [0, inf], default (0.8, 0.8, 0.8)

direction
    

Direction that the light is shining

Type:
    

[[mathutils.Vector]] of 3 items in [-inf, inf], default (0.0, 0.0, 1.0)

smooth
    

Smooth the lighting from this light

Type:
    

float in [0, 1], default 0.5

specular_color
    

Color of the light’s specular highlight

Type:
    

[[mathutils.Color]] of 3 items in [0, inf], default (0.8, 0.8, 0.8)

use
    

Enable this light in solid shading mode

Type:
    

boolean, default True

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

  * [[PreferencesSystem.solid_lights]]

| 

  * [[StudioLight.solid_lights]]

  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
