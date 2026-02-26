# GPencilSculptGuide(bpy_struct)

base class — [[bpy_struct]]

_class _bpy.types.GPencilSculptGuide(_bpy_struct_)
    

Guides for drawing

angle
    

Direction of lines

Type:
    

float in [-6.28319, 6.28319], default 0.0

angle_snap
    

Angle snapping

Type:
    

float in [-6.28319, 6.28319], default 0.0

location
    

Custom reference point for guides

Type:
    

float array of 3 items in [-inf, inf], default (0.0, 0.0, 0.0)

reference_object
    

Object used for reference point

Type:
    

[[Object]]

reference_point
    

Type of speed guide

  * `CURSOR` Cursor – Use cursor as reference point.

  * `CUSTOM` Custom – Use custom reference point.

  * `OBJECT` Object – Use object as reference point.


Type:
    

enum in [`'CURSOR'`, `'CUSTOM'`, `'OBJECT'`], default `'CURSOR'`

spacing
    

Guide spacing

Type:
    

float in [0, inf], default 20.0

type
    

Type of speed guide

  * `CIRCULAR` Circular – Use single point to create rings.

  * `RADIAL` Radial – Use single point as direction.

  * `PARALLEL` Parallel – Parallel lines.

  * `GRID` Grid – Grid allows horizontal and vertical lines.

  * `ISO` Isometric – Grid allows isometric and vertical lines.


Type:
    

enum in [`'CIRCULAR'`, `'RADIAL'`, `'PARALLEL'`, `'GRID'`, `'ISO'`], default `'CIRCULAR'`

use_guide
    

Enable speed guides

Type:
    

boolean, default False

use_snapping
    

Enable snapping to guides angle or spacing options

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

  * [[GPencilSculptSettings.guide]]

| 


  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
