# WorldMistSettings(bpy_struct)

base class — [[bpy_struct]]

_class _bpy.types.WorldMistSettings(_bpy_struct_)
    

Mist settings for a World data-block

depth
    

Distance over which the mist effect fades in

Type:
    

float in [0, inf], default 25.0

falloff
    

Type of transition used to fade mist

  * `QUADRATIC` Quadratic – Use quadratic progression.

  * `LINEAR` Linear – Use linear progression.

  * `INVERSE_QUADRATIC` Inverse Quadratic – Use inverse quadratic progression.


Type:
    

enum in [`'QUADRATIC'`, `'LINEAR'`, `'INVERSE_QUADRATIC'`], default `'QUADRATIC'`

height
    

Control how much mist density decreases with height

Type:
    

float in [0, 100], default 0.0

intensity
    

Overall minimum intensity of the mist effect

Type:
    

float in [0, 1], default 0.0

start
    

Starting distance of the mist, measured from the camera

Type:
    

float in [0, inf], default 5.0

use_mist
    

Occlude objects with the environment color as they are further away

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

  * [[World.mist_settings]]

| 


  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
