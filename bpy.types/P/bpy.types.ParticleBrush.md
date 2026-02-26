# ParticleBrush(bpy_struct)

base class — [[bpy_struct]]

_class _bpy.types.ParticleBrush(_bpy_struct_)
    

Particle editing brush

count
    

Particle count

Type:
    

int in [1, 1000], default 10

curve
    

Type:
    

[[CurveMapping]], (readonly)

length_mode
    

  * `GROW` Grow – Make hairs longer.

  * `SHRINK` Shrink – Make hairs shorter.


Type:
    

enum in [`'GROW'`, `'SHRINK'`], default `'GROW'`

puff_mode
    

  * `ADD` Add – Make hairs more puffy.

  * `SUB` Sub – Make hairs less puffy.


Type:
    

enum in [`'ADD'`, `'SUB'`], default `'ADD'`

size
    

Radius of the brush in pixels

Type:
    

int in [1, 32767], default 50

steps
    

Brush steps

Type:
    

int in [1, 32767], default 10

strength
    

Brush strength

Type:
    

float in [0.001, 1], default 0.5

use_puff_volume
    

Apply puff to unselected end-points (helps maintain hair volume when puffing root)

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

  * [[ParticleEdit.brush]]

| 


  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
