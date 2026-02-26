# AnnotationFrames(bpy_struct)

base class — [[bpy_struct]]

_class _bpy.types.AnnotationFrames(_bpy_struct_)
    

Collection of annotation frames

new(_frame_number_ , _*_ , _active =False_)
    

Add a new annotation frame

Parameters:
    

  * **frame_number** (_int in_ _[__-1048574_ _,__1048574_ _]_) – Frame Number, The frame on which this sketch appears

  * **active** (_boolean_ _,__(__optional_ _)_) – Active


Returns:
    

The newly created frame

Return type:
    

[[AnnotationFrame]]

remove(_frame_)
    

Remove an annotation frame

Parameters:
    

**frame** ([[AnnotationFrame]], (never None)) – Frame, The frame to remove

copy(_source_)
    

Copy an annotation frame

Parameters:
    

**source** ([[AnnotationFrame]], (never None)) – Source, The source frame

Returns:
    

The newly copied frame

Return type:
    

[[AnnotationFrame]]

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

  * [[AnnotationLayer.frames]]

| 


  
---|---
  *[*]: Keyword-only parameters separator (PEP 3102)
  *[/]: Positional-only parameter separator (PEP 570)
