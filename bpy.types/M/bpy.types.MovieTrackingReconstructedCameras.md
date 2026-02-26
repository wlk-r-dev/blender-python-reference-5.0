# MovieTrackingReconstructedCameras(bpy_struct)

base class — [[bpy_struct]]

_class _bpy.types.MovieTrackingReconstructedCameras(_bpy_struct_)
    

Collection of solved cameras

find_frame(_*_ , _frame =1_)
    

Find a reconstructed camera for a give frame number

Parameters:
    

**frame** (_int in_ _[__0_ _,__1048574_ _]__,__(__optional_ _)_) – Frame, Frame number to find camera for

Returns:
    

Camera for a given frame

Return type:
    

[[MovieReconstructedCamera]]

matrix_from_frame(_*_ , _frame =1_)
    

Return interpolated camera matrix for a given frame

Parameters:
    

**frame** (_int in_ _[__0_ _,__1048574_ _]__,__(__optional_ _)_) – Frame, Frame number to find camera for

Returns:
    

Matrix, Interpolated camera matrix for a given frame

Return type:
    

[[mathutils.Matrix]] of 4 * 4 items in [-inf, inf]

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

  * [[MovieTrackingReconstruction.cameras]]

| 


  
---|---
  *[*]: Keyword-only parameters separator (PEP 3102)
  *[/]: Positional-only parameter separator (PEP 570)
