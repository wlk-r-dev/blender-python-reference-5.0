# LineStyleThicknessModifier(LineStyleModifier)

base classes — [`bpy_struct`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct "bpy.types.bpy_struct"), [`LineStyleModifier`](bpy.types.LineStyleModifier.md#bpy.types.LineStyleModifier "bpy.types.LineStyleModifier")

subclasses — [`LineStyleThicknessModifier_AlongStroke`](bpy.types.LineStyleThicknessModifier_AlongStroke.md#bpy.types.LineStyleThicknessModifier_AlongStroke "bpy.types.LineStyleThicknessModifier_AlongStroke"), [`LineStyleThicknessModifier_Calligraphy`](bpy.types.LineStyleThicknessModifier_Calligraphy.md#bpy.types.LineStyleThicknessModifier_Calligraphy "bpy.types.LineStyleThicknessModifier_Calligraphy"), [`LineStyleThicknessModifier_CreaseAngle`](bpy.types.LineStyleThicknessModifier_CreaseAngle.md#bpy.types.LineStyleThicknessModifier_CreaseAngle "bpy.types.LineStyleThicknessModifier_CreaseAngle"), [`LineStyleThicknessModifier_Curvature_3D`](bpy.types.LineStyleThicknessModifier_Curvature_3D.md#bpy.types.LineStyleThicknessModifier_Curvature_3D "bpy.types.LineStyleThicknessModifier_Curvature_3D"), [`LineStyleThicknessModifier_DistanceFromCamera`](bpy.types.LineStyleThicknessModifier_DistanceFromCamera.md#bpy.types.LineStyleThicknessModifier_DistanceFromCamera "bpy.types.LineStyleThicknessModifier_DistanceFromCamera"), [`LineStyleThicknessModifier_DistanceFromObject`](bpy.types.LineStyleThicknessModifier_DistanceFromObject.md#bpy.types.LineStyleThicknessModifier_DistanceFromObject "bpy.types.LineStyleThicknessModifier_DistanceFromObject"), [`LineStyleThicknessModifier_Material`](bpy.types.LineStyleThicknessModifier_Material.md#bpy.types.LineStyleThicknessModifier_Material "bpy.types.LineStyleThicknessModifier_Material"), [`LineStyleThicknessModifier_Noise`](bpy.types.LineStyleThicknessModifier_Noise.md#bpy.types.LineStyleThicknessModifier_Noise "bpy.types.LineStyleThicknessModifier_Noise"), [`LineStyleThicknessModifier_Tangent`](bpy.types.LineStyleThicknessModifier_Tangent.md#bpy.types.LineStyleThicknessModifier_Tangent "bpy.types.LineStyleThicknessModifier_Tangent")

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
    

[`bpy.types.Struct`](../S/bpy.types.Struct.md#bpy.types.Struct "bpy.types.Struct") subclass

_classmethod _bl_rna_get_subclass_py(_id_ , _default =None_, _/_)
    

Parameters:
    

**id** (_str_) – The RNA type identifier.

Returns:
    

The class or default when not found.

Return type:
    

type

## Inherited Properties

  * [`bpy_struct.id_data`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.id_data "bpy.types.bpy_struct.id_data")

| 


  
---|---  
  
## Inherited Functions

  * [`bpy_struct.as_pointer`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.as_pointer "bpy.types.bpy_struct.as_pointer")
  * [`bpy_struct.driver_add`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.driver_add "bpy.types.bpy_struct.driver_add")
  * [`bpy_struct.driver_remove`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.driver_remove "bpy.types.bpy_struct.driver_remove")
  * [`bpy_struct.get`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.get "bpy.types.bpy_struct.get")
  * [`bpy_struct.id_properties_clear`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.id_properties_clear "bpy.types.bpy_struct.id_properties_clear")
  * [`bpy_struct.id_properties_ensure`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.id_properties_ensure "bpy.types.bpy_struct.id_properties_ensure")
  * [`bpy_struct.id_properties_ui`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.id_properties_ui "bpy.types.bpy_struct.id_properties_ui")
  * [`bpy_struct.is_property_hidden`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.is_property_hidden "bpy.types.bpy_struct.is_property_hidden")
  * [`bpy_struct.is_property_overridable_library`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.is_property_overridable_library "bpy.types.bpy_struct.is_property_overridable_library")
  * [`bpy_struct.is_property_readonly`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.is_property_readonly "bpy.types.bpy_struct.is_property_readonly")
  * [`bpy_struct.is_property_set`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.is_property_set "bpy.types.bpy_struct.is_property_set")
  * [`bpy_struct.items`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.items "bpy.types.bpy_struct.items")
  * [`bpy_struct.keyframe_delete`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.keyframe_delete "bpy.types.bpy_struct.keyframe_delete")

| 

  * [`bpy_struct.keyframe_insert`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.keyframe_insert "bpy.types.bpy_struct.keyframe_insert")
  * [`bpy_struct.keys`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.keys "bpy.types.bpy_struct.keys")
  * [`bpy_struct.path_from_id`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.path_from_id "bpy.types.bpy_struct.path_from_id")
  * [`bpy_struct.path_from_module`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.path_from_module "bpy.types.bpy_struct.path_from_module")
  * [`bpy_struct.path_resolve`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.path_resolve "bpy.types.bpy_struct.path_resolve")
  * [`bpy_struct.pop`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.pop "bpy.types.bpy_struct.pop")
  * [`bpy_struct.property_overridable_library_set`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.property_overridable_library_set "bpy.types.bpy_struct.property_overridable_library_set")
  * [`bpy_struct.property_unset`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.property_unset "bpy.types.bpy_struct.property_unset")
  * [`bpy_struct.rna_ancestors`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.rna_ancestors "bpy.types.bpy_struct.rna_ancestors")
  * [`bpy_struct.type_recast`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.type_recast "bpy.types.bpy_struct.type_recast")
  * [`bpy_struct.values`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.values "bpy.types.bpy_struct.values")
  * [`LineStyleModifier.bl_rna_get_subclass`](bpy.types.LineStyleModifier.md#bpy.types.LineStyleModifier.bl_rna_get_subclass "bpy.types.LineStyleModifier.bl_rna_get_subclass")
  * [`LineStyleModifier.bl_rna_get_subclass_py`](bpy.types.LineStyleModifier.md#bpy.types.LineStyleModifier.bl_rna_get_subclass_py "bpy.types.LineStyleModifier.bl_rna_get_subclass_py")

  
---|---  
  
## References

  * [`FreestyleLineStyle.thickness_modifiers`](../F/bpy.types.FreestyleLineStyle.md#bpy.types.FreestyleLineStyle.thickness_modifiers "bpy.types.FreestyleLineStyle.thickness_modifiers")
  * [`LineStyleThicknessModifiers.new`](bpy.types.LineStyleThicknessModifiers.md#bpy.types.LineStyleThicknessModifiers.new "bpy.types.LineStyleThicknessModifiers.new")

| 

  * [`LineStyleThicknessModifiers.remove`](bpy.types.LineStyleThicknessModifiers.md#bpy.types.LineStyleThicknessModifiers.remove "bpy.types.LineStyleThicknessModifiers.remove")

  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
