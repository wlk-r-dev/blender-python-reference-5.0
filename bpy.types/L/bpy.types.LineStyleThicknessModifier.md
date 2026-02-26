# LineStyleThicknessModifier(LineStyleModifier)

base classes — [[bpy_struct]], [[LineStyleModifier]]

subclasses — [[LineStyleThicknessModifier_AlongStroke]], [[LineStyleThicknessModifier_Calligraphy]], [[LineStyleThicknessModifier_CreaseAngle]], [[LineStyleThicknessModifier_Curvature_3D]], [[LineStyleThicknessModifier_DistanceFromCamera]], [[LineStyleThicknessModifier_DistanceFromObject]], [[LineStyleThicknessModifier_Material]], [[LineStyleThicknessModifier_Noise]], [[LineStyleThicknessModifier_Tangent]]

_class _bpy.types.LineStyleThicknessModifier(_LineStyleModifier_)
    

Base type to define line thickness modifiers

name
    

Name of the modifier

Type:
    

string, default “”, (never None)

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
  * [[LineStyleModifier.bl_rna_get_subclass]]
  * [[LineStyleModifier.bl_rna_get_subclass_py]]

  
---|---  
  
## References

  * [[FreestyleLineStyle.thickness_modifiers]]
  * [[LineStyleThicknessModifiers.new]]

| 

  * [[LineStyleThicknessModifiers.remove]]

  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
