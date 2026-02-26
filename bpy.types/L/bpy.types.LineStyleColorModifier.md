# LineStyleColorModifier(LineStyleModifier)

base classes — [`bpy_struct`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct "bpy.types.bpy_struct"), [`LineStyleModifier`](bpy.types.LineStyleModifier.md#bpy.types.LineStyleModifier "bpy.types.LineStyleModifier")

subclasses — [`LineStyleColorModifier_AlongStroke`](bpy.types.LineStyleColorModifier_AlongStroke.md#bpy.types.LineStyleColorModifier_AlongStroke "bpy.types.LineStyleColorModifier_AlongStroke"), [`LineStyleColorModifier_CreaseAngle`](bpy.types.LineStyleColorModifier_CreaseAngle.md#bpy.types.LineStyleColorModifier_CreaseAngle "bpy.types.LineStyleColorModifier_CreaseAngle"), [`LineStyleColorModifier_Curvature_3D`](bpy.types.LineStyleColorModifier_Curvature_3D.md#bpy.types.LineStyleColorModifier_Curvature_3D "bpy.types.LineStyleColorModifier_Curvature_3D"), [`LineStyleColorModifier_DistanceFromCamera`](bpy.types.LineStyleColorModifier_DistanceFromCamera.md#bpy.types.LineStyleColorModifier_DistanceFromCamera "bpy.types.LineStyleColorModifier_DistanceFromCamera"), [`LineStyleColorModifier_DistanceFromObject`](bpy.types.LineStyleColorModifier_DistanceFromObject.md#bpy.types.LineStyleColorModifier_DistanceFromObject "bpy.types.LineStyleColorModifier_DistanceFromObject"), [`LineStyleColorModifier_Material`](bpy.types.LineStyleColorModifier_Material.md#bpy.types.LineStyleColorModifier_Material "bpy.types.LineStyleColorModifier_Material"), [`LineStyleColorModifier_Noise`](bpy.types.LineStyleColorModifier_Noise.md#bpy.types.LineStyleColorModifier_Noise "bpy.types.LineStyleColorModifier_Noise"), [`LineStyleColorModifier_Tangent`](bpy.types.LineStyleColorModifier_Tangent.md#bpy.types.LineStyleColorModifier_Tangent "bpy.types.LineStyleColorModifier_Tangent")

_class _bpy.types.LineStyleColorModifier(_LineStyleModifier_)
    

Base type to define line color modifiers

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

  * [`FreestyleLineStyle.color_modifiers`](../F/bpy.types.FreestyleLineStyle.md#bpy.types.FreestyleLineStyle.color_modifiers "bpy.types.FreestyleLineStyle.color_modifiers")
  * [`LineStyleColorModifiers.new`](bpy.types.LineStyleColorModifiers.md#bpy.types.LineStyleColorModifiers.new "bpy.types.LineStyleColorModifiers.new")

| 

  * [`LineStyleColorModifiers.remove`](bpy.types.LineStyleColorModifiers.md#bpy.types.LineStyleColorModifiers.remove "bpy.types.LineStyleColorModifiers.remove")

  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
