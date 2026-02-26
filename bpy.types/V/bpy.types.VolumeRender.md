# VolumeRender(bpy_struct)

base class — [[bpy_struct]]

_class _bpy.types.VolumeRender(_bpy_struct_)
    

Volume object render settings

clipping
    

Value under which voxels are considered empty space to optimize rendering

Type:
    

float in [0, 1], default 0.0

precision
    

Specify volume data precision. Lower values reduce memory consumption at the cost of detail.

  * `FULL` Full – Use 32-bit floating-point numbers for all data.

  * `HALF` Half – Use 16-bit floating-point numbers for all data.

  * `VARIABLE` Variable – Use variable bit quantization.


Type:
    

enum in [`'FULL'`, `'HALF'`, `'VARIABLE'`], default `'HALF'`

space
    

Specify volume density and step size in object or world space

  * `OBJECT` Object – Keep volume opacity and detail the same regardless of object scale.

  * `WORLD` World – Specify volume step size and density in world space.


Type:
    

enum in [`'OBJECT'`, `'WORLD'`], default `'OBJECT'`

step_size
    

Distance between volume samples. Lower values render more detail at the cost of performance. If set to zero, the step size is automatically determined based on voxel size.

Type:
    

float in [0, inf], default 0.0

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

  * [[Volume.render]]

| 


  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
