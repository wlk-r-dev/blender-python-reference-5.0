# RaytraceEEVEE(bpy_struct)

base class — [[bpy_struct]]

_class _bpy.types.RaytraceEEVEE(_bpy_struct_)
    

Quality options for the raytracing pipeline

denoise_bilateral
    

Blur the resolved radiance using a bilateral filter

Type:
    

boolean, default True

denoise_spatial
    

Reuse neighbor pixels’ rays

Type:
    

boolean, default True

denoise_temporal
    

Accumulate samples by reprojecting last tracing results

Type:
    

boolean, default True

resolution_scale
    

Determines the number of rays per pixel. Higher resolution uses more memory.

  * `1` 1:1 – Full resolution.

  * `2` 1:2 – Render this effect at 50% render resolution.

  * `4` 1:4 – Render this effect at 25% render resolution.

  * `8` 1:8 – Render this effect at 12.5% render resolution.

  * `16` 1:16 – Render this effect at 6.25% render resolution.


Type:
    

enum in [`'1'`, `'2'`, `'4'`, `'8'`, `'16'`], default `'2'`

screen_trace_quality
    

Precision of the screen space ray-tracing

Type:
    

float in [0, 1], default 0.25

screen_trace_thickness
    

Surface thickness used to detect intersection when using screen-tracing

Type:
    

float in [1e-06, inf], default 0.2

trace_max_roughness
    

Maximum roughness to use the tracing pipeline for. Higher roughness surfaces will use fast GI approximation. A value of 1 will disable fast GI approximation.

Type:
    

float in [0, 1], default 0.5

use_denoise
    

Enable noise reduction techniques for raytraced effects

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

  * [[SceneEEVEE.ray_tracing_options]]

| 


  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
