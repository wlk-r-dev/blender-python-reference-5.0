# View3DCursor(bpy_struct)

base class — [[bpy_struct]]

_class _bpy.types.View3DCursor(_bpy_struct_)
    

location
    

Type:
    

[[mathutils.Vector]] of 3 items in [-inf, inf], default (0.0, 0.0, 0.0)

matrix
    

Matrix combining location and rotation of the cursor

Type:
    

[[mathutils.Matrix]] of 4 * 4 items in [-inf, inf], default ((0.0, 0.0, 0.0, 0.0), (0.0, 0.0, 0.0, 0.0), (0.0, 0.0, 0.0, 0.0), (0.0, 0.0, 0.0, 0.0))

rotation_axis_angle
    

Angle of Rotation for Axis-Angle rotation representation

Type:
    

float array of 4 items in [-inf, inf], default (0.0, 0.0, 1.0, 0.0)

rotation_euler
    

3D rotation

Type:
    

[[mathutils.Euler]] rotation of 3 items in [-inf, inf], default (0.0, 0.0, 0.0)

rotation_mode
    

The kind of rotation to apply, values from other rotation modes are not used

Type:
    

enum in [Object Rotation Mode Items](../../bpy_types_enum_items/object_rotation_mode_items.md#rna-enum-object-rotation-mode-items), default `'XYZ'`

rotation_quaternion
    

Rotation in quaternions (keep normalized)

Type:
    

[[mathutils.Quaternion]] rotation of 4 items in [-inf, inf], default (1.0, 0.0, 0.0, 0.0)

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

  * [[Scene.cursor]]

| 


  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
