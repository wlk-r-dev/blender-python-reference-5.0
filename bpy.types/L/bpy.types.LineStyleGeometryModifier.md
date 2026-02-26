# LineStyleGeometryModifier(LineStyleModifier)

base classes — [`bpy_struct`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct "bpy.types.bpy_struct"), [`LineStyleModifier`](bpy.types.LineStyleModifier.md#bpy.types.LineStyleModifier "bpy.types.LineStyleModifier")

subclasses — [`LineStyleGeometryModifier_2DOffset`](bpy.types.LineStyleGeometryModifier_2DOffset.md#bpy.types.LineStyleGeometryModifier_2DOffset "bpy.types.LineStyleGeometryModifier_2DOffset"), [`LineStyleGeometryModifier_2DTransform`](bpy.types.LineStyleGeometryModifier_2DTransform.md#bpy.types.LineStyleGeometryModifier_2DTransform "bpy.types.LineStyleGeometryModifier_2DTransform"), [`LineStyleGeometryModifier_BackboneStretcher`](bpy.types.LineStyleGeometryModifier_BackboneStretcher.md#bpy.types.LineStyleGeometryModifier_BackboneStretcher "bpy.types.LineStyleGeometryModifier_BackboneStretcher"), [`LineStyleGeometryModifier_BezierCurve`](bpy.types.LineStyleGeometryModifier_BezierCurve.md#bpy.types.LineStyleGeometryModifier_BezierCurve "bpy.types.LineStyleGeometryModifier_BezierCurve"), [`LineStyleGeometryModifier_Blueprint`](bpy.types.LineStyleGeometryModifier_Blueprint.md#bpy.types.LineStyleGeometryModifier_Blueprint "bpy.types.LineStyleGeometryModifier_Blueprint"), [`LineStyleGeometryModifier_GuidingLines`](bpy.types.LineStyleGeometryModifier_GuidingLines.md#bpy.types.LineStyleGeometryModifier_GuidingLines "bpy.types.LineStyleGeometryModifier_GuidingLines"), [`LineStyleGeometryModifier_PerlinNoise1D`](bpy.types.LineStyleGeometryModifier_PerlinNoise1D.md#bpy.types.LineStyleGeometryModifier_PerlinNoise1D "bpy.types.LineStyleGeometryModifier_PerlinNoise1D"), [`LineStyleGeometryModifier_PerlinNoise2D`](bpy.types.LineStyleGeometryModifier_PerlinNoise2D.md#bpy.types.LineStyleGeometryModifier_PerlinNoise2D "bpy.types.LineStyleGeometryModifier_PerlinNoise2D"), [`LineStyleGeometryModifier_Polygonalization`](bpy.types.LineStyleGeometryModifier_Polygonalization.md#bpy.types.LineStyleGeometryModifier_Polygonalization "bpy.types.LineStyleGeometryModifier_Polygonalization"), [`LineStyleGeometryModifier_Sampling`](bpy.types.LineStyleGeometryModifier_Sampling.md#bpy.types.LineStyleGeometryModifier_Sampling "bpy.types.LineStyleGeometryModifier_Sampling"), [`LineStyleGeometryModifier_Simplification`](bpy.types.LineStyleGeometryModifier_Simplification.md#bpy.types.LineStyleGeometryModifier_Simplification "bpy.types.LineStyleGeometryModifier_Simplification"), [`LineStyleGeometryModifier_SinusDisplacement`](bpy.types.LineStyleGeometryModifier_SinusDisplacement.md#bpy.types.LineStyleGeometryModifier_SinusDisplacement "bpy.types.LineStyleGeometryModifier_SinusDisplacement"), [`LineStyleGeometryModifier_SpatialNoise`](bpy.types.LineStyleGeometryModifier_SpatialNoise.md#bpy.types.LineStyleGeometryModifier_SpatialNoise "bpy.types.LineStyleGeometryModifier_SpatialNoise"), [`LineStyleGeometryModifier_TipRemover`](bpy.types.LineStyleGeometryModifier_TipRemover.md#bpy.types.LineStyleGeometryModifier_TipRemover "bpy.types.LineStyleGeometryModifier_TipRemover")

_class _bpy.types.LineStyleGeometryModifier(_LineStyleModifier_)
    

Base type to define stroke geometry modifiers

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

  * [`FreestyleLineStyle.geometry_modifiers`](../F/bpy.types.FreestyleLineStyle.md#bpy.types.FreestyleLineStyle.geometry_modifiers "bpy.types.FreestyleLineStyle.geometry_modifiers")
  * [`LineStyleGeometryModifiers.new`](bpy.types.LineStyleGeometryModifiers.md#bpy.types.LineStyleGeometryModifiers.new "bpy.types.LineStyleGeometryModifiers.new")

| 

  * [`LineStyleGeometryModifiers.remove`](bpy.types.LineStyleGeometryModifiers.md#bpy.types.LineStyleGeometryModifiers.remove "bpy.types.LineStyleGeometryModifiers.remove")

  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
