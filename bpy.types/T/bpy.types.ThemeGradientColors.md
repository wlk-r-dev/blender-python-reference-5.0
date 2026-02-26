# ThemeGradientColors(bpy_struct)

base class — [[bpy_struct]]

_class _bpy.types.ThemeGradientColors(_bpy_struct_)
    

Theme settings for background colors and gradient

background_type
    

Type of background in the 3D viewport

  * `SINGLE_COLOR` Single Color – Use a solid color as viewport background.

  * `LINEAR` Linear Gradient – Use a screen space vertical linear gradient as viewport background.

  * `RADIAL` Vignette – Use a radial gradient as viewport background.


Type:
    

enum in [`'SINGLE_COLOR'`, `'LINEAR'`, `'RADIAL'`], default `'SINGLE_COLOR'`

gradient
    

Type:
    

[[mathutils.Color]] of 3 items in [0, 1], default (0.0, 0.0, 0.0)

high_gradient
    

Type:
    

[[mathutils.Color]] of 3 items in [0, 1], default (0.0, 0.0, 0.0)

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

  * [[ThemeSpaceGradient.gradients]]

| 


  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
