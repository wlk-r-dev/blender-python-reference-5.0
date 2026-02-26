# ShaderFxShadow(ShaderFx)

base classes — [[bpy_struct]], [[ShaderFx]]

_class _bpy.types.ShaderFxShadow(_ShaderFx_)
    

Shadow effect

amplitude
    

Amplitude of Wave

Type:
    

float in [0, inf], default 0.0

blur
    

Number of pixels for blurring shadow (set to 0 to disable)

Type:
    

int array of 2 items in [0, 32767], default (0, 0)

object
    

Object to determine center of rotation

Type:
    

[[Object]]

offset
    

Offset of the shadow

Type:
    

int array of 2 items in [-32768, 32767], default (0, 0)

orientation
    

Direction of the wave

Type:
    

enum in [`'HORIZONTAL'`, `'VERTICAL'`], default `'HORIZONTAL'`

period
    

Period of Wave

Type:
    

float in [0, inf], default 0.0

phase
    

Phase Shift of Wave

Type:
    

float in [-inf, inf], default 0.0

rotation
    

Rotation around center or object

Type:
    

float in [-6.28319, 6.28319], default 0.0

samples
    

Number of Blur Samples (zero, disable blur)

Type:
    

int in [0, 32], default 4

scale
    

Scale of the shadow

Type:
    

[[mathutils.Vector]] of 2 items in [-inf, inf], default (0.0, 0.0)

shadow_color
    

Color used for Shadow

Type:
    

float array of 4 items in [0, 1], default (0.0, 0.0, 0.0, 0.0)

use_object
    

Use object as center of rotation

Type:
    

boolean, default False

use_wave
    

Use wave effect

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
  * [[ShaderFx.name]]
  * [[ShaderFx.type]]
  * [[ShaderFx.show_viewport]]

| 

  * [[ShaderFx.show_render]]
  * [[ShaderFx.show_in_editmode]]
  * [[ShaderFx.show_expanded]]

  
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
  * [[ShaderFx.bl_rna_get_subclass]]
  * [[ShaderFx.bl_rna_get_subclass_py]]

  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
