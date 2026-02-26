# SceneGpencil(bpy_struct)

base class — [[bpy_struct]]

_class _bpy.types.SceneGpencil(_bpy_struct_)
    

Render settings

aa_samples
    

Number of supersampling anti-aliasing samples per pixel for final render

Type:
    

int in [1, inf], default 8

antialias_threshold
    

Threshold for edge detection algorithm (higher values might over-blur some part of the image)

Type:
    

float in [0, inf], default 1.0

antialias_threshold_render
    

Threshold for edge detection algorithm (higher values might over-blur some part of the image). Only applies to final render

Type:
    

float in [0, inf], default 0.25

motion_blur_steps
    

Controls accuracy of motion blur, more steps result in longer render time. Only used when Motion Blur is enabled. Set to 0 to disable motion blur for Grease Pencil

Type:
    

int in [0, inf], default 8

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

  * [[Scene.grease_pencil_settings]]

| 


  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
