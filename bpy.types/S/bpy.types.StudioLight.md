# StudioLight(bpy_struct)

base class — [[bpy_struct]]

_class _bpy.types.StudioLight(_bpy_struct_)
    

Studio light

has_specular_highlight_pass
    

Studio light image file has separate “diffuse” and “specular” passes

Type:
    

boolean, default False, (readonly)

index
    

Type:
    

int in [-inf, inf], default 0, (readonly)

is_user_defined
    

Type:
    

boolean, default False, (readonly)

light_ambient
    

Color of the ambient light that uniformly lit the scene

Type:
    

[[mathutils.Color]] of 3 items in [0, inf], default (0.0, 0.0, 0.0), (readonly)

name
    

Type:
    

string, default “”, (readonly, never None)

path
    

Type:
    

string, default “”, (readonly, never None)

solid_lights
    

Lights used to display objects in solid draw mode

Type:
    

[[bpy_prop_collection]] of [[UserSolidLight]], (readonly)

type
    

Type:
    

enum in [`'STUDIO'`, `'WORLD'`, `'MATCAP'`], default `'STUDIO'`, (readonly)

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

  * [[Preferences.studio_lights]]
  * [[StudioLights.load]]
  * [[StudioLights.new]]

| 

  * [[StudioLights.remove]]
  * [[View3DShading.selected_studio_light]]

  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
