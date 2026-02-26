# UnitSettings(bpy_struct)

base class — [[bpy_struct]]

_class _bpy.types.UnitSettings(_bpy_struct_)
    

length_unit
    

Unit that will be used to display length values

Type:
    

enum in [`'DEFAULT'`], default `'DEFAULT'`

mass_unit
    

Unit that will be used to display mass values

Type:
    

enum in [`'DEFAULT'`], default `'DEFAULT'`

scale_length
    

Scale to use when converting between Blender units and dimensions. When working at microscopic or astronomical scale, a small or large unit scale respectively can be used to avoid numerical precision problems

Type:
    

float in [1e-09, inf], default 0.0

system
    

The unit system to use for user interface controls

Type:
    

enum in [`'NONE'`, `'METRIC'`, `'IMPERIAL'`], default `'NONE'`

system_rotation
    

Unit to use for displaying/editing rotation values

  * `DEGREES` Degrees – Use degrees for measuring angles and rotations.

  * `RADIANS` Radians.


Type:
    

enum in [`'DEGREES'`, `'RADIANS'`], default `'DEGREES'`

temperature_unit
    

Unit that will be used to display temperature values

Type:
    

enum in [`'DEFAULT'`], default `'DEFAULT'`

time_unit
    

Unit that will be used to display time values

Type:
    

enum in [`'DEFAULT'`], default `'DEFAULT'`

use_separate
    

Display units in pairs (e.g. 1m 0cm)

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

  * [[Scene.unit_settings]]

| 


  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
