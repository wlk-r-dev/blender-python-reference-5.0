# ColorRamp(bpy_struct)

base class — [`bpy_struct`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct "bpy.types.bpy_struct")

_class _bpy.types.ColorRamp(_bpy_struct_)
    

Color ramp mapping a scalar value to a color

color_mode
    

Set color mode to use for interpolation

Type:
    

enum in [`'RGB'`, `'HSV'`, `'HSL'`], default `'RGB'`

elements
    

Type:
    

[`ColorRampElements`](bpy.types.ColorRampElements.md#bpy.types.ColorRampElements "bpy.types.ColorRampElements") [`bpy_prop_collection`](../_other/bpy.types.bpy_prop_collection.md#bpy.types.bpy_prop_collection "bpy.types.bpy_prop_collection") of [`ColorRampElement`](bpy.types.ColorRampElement.md#bpy.types.ColorRampElement "bpy.types.ColorRampElement"), (readonly)

hue_interpolation
    

Set color interpolation

Type:
    

enum in [`'NEAR'`, `'FAR'`, `'CW'`, `'CCW'`], default `'NEAR'`

interpolation
    

Set interpolation between color stops

Type:
    

enum in [`'EASE'`, `'CARDINAL'`, `'LINEAR'`, `'B_SPLINE'`, `'CONSTANT'`], default `'LINEAR'`

evaluate(_position_)
    

Evaluate Color Ramp

Parameters:
    

**position** (_float in_ _[__0_ _,__1_ _]_) – Position, Evaluate Color Ramp at position

Returns:
    

Color, Color at given position

Return type:
    

float array of 4 items in [-inf, inf]

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

| 

  * [`bpy_struct.keyframe_delete`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.keyframe_delete "bpy.types.bpy_struct.keyframe_delete")
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

  
---|---  
  
## References

  * [`Brush.gradient`](../B/bpy.types.Brush.md#bpy.types.Brush.gradient "bpy.types.Brush.gradient")
  * [`ColorMapping.color_ramp`](bpy.types.ColorMapping.md#bpy.types.ColorMapping.color_ramp "bpy.types.ColorMapping.color_ramp")
  * [`DynamicPaintBrushSettings.paint_ramp`](../D/bpy.types.DynamicPaintBrushSettings.md#bpy.types.DynamicPaintBrushSettings.paint_ramp "bpy.types.DynamicPaintBrushSettings.paint_ramp")
  * [`DynamicPaintBrushSettings.velocity_ramp`](../D/bpy.types.DynamicPaintBrushSettings.md#bpy.types.DynamicPaintBrushSettings.velocity_ramp "bpy.types.DynamicPaintBrushSettings.velocity_ramp")
  * [`FluidDomainSettings.color_ramp`](../F/bpy.types.FluidDomainSettings.md#bpy.types.FluidDomainSettings.color_ramp "bpy.types.FluidDomainSettings.color_ramp")
  * [`GreasePencilTintModifier.color_ramp`](../G/bpy.types.GreasePencilTintModifier.md#bpy.types.GreasePencilTintModifier.color_ramp "bpy.types.GreasePencilTintModifier.color_ramp")
  * [`LineStyleColorModifier_AlongStroke.color_ramp`](../L/bpy.types.LineStyleColorModifier_AlongStroke.md#bpy.types.LineStyleColorModifier_AlongStroke.color_ramp "bpy.types.LineStyleColorModifier_AlongStroke.color_ramp")
  * [`LineStyleColorModifier_CreaseAngle.color_ramp`](../L/bpy.types.LineStyleColorModifier_CreaseAngle.md#bpy.types.LineStyleColorModifier_CreaseAngle.color_ramp "bpy.types.LineStyleColorModifier_CreaseAngle.color_ramp")
  * [`LineStyleColorModifier_Curvature_3D.color_ramp`](../L/bpy.types.LineStyleColorModifier_Curvature_3D.md#bpy.types.LineStyleColorModifier_Curvature_3D.color_ramp "bpy.types.LineStyleColorModifier_Curvature_3D.color_ramp")

| 

  * [`LineStyleColorModifier_DistanceFromCamera.color_ramp`](../L/bpy.types.LineStyleColorModifier_DistanceFromCamera.md#bpy.types.LineStyleColorModifier_DistanceFromCamera.color_ramp "bpy.types.LineStyleColorModifier_DistanceFromCamera.color_ramp")
  * [`LineStyleColorModifier_DistanceFromObject.color_ramp`](../L/bpy.types.LineStyleColorModifier_DistanceFromObject.md#bpy.types.LineStyleColorModifier_DistanceFromObject.color_ramp "bpy.types.LineStyleColorModifier_DistanceFromObject.color_ramp")
  * [`LineStyleColorModifier_Material.color_ramp`](../L/bpy.types.LineStyleColorModifier_Material.md#bpy.types.LineStyleColorModifier_Material.color_ramp "bpy.types.LineStyleColorModifier_Material.color_ramp")
  * [`LineStyleColorModifier_Noise.color_ramp`](../L/bpy.types.LineStyleColorModifier_Noise.md#bpy.types.LineStyleColorModifier_Noise.color_ramp "bpy.types.LineStyleColorModifier_Noise.color_ramp")
  * [`LineStyleColorModifier_Tangent.color_ramp`](../L/bpy.types.LineStyleColorModifier_Tangent.md#bpy.types.LineStyleColorModifier_Tangent.color_ramp "bpy.types.LineStyleColorModifier_Tangent.color_ramp")
  * [`PreferencesView.weight_color_range`](../P/bpy.types.PreferencesView.md#bpy.types.PreferencesView.weight_color_range "bpy.types.PreferencesView.weight_color_range")
  * [`ShaderNodeValToRGB.color_ramp`](../S/bpy.types.ShaderNodeValToRGB.md#bpy.types.ShaderNodeValToRGB.color_ramp "bpy.types.ShaderNodeValToRGB.color_ramp")
  * [`Texture.color_ramp`](../T/bpy.types.Texture.md#bpy.types.Texture.color_ramp "bpy.types.Texture.color_ramp")
  * [`TextureNodeValToRGB.color_ramp`](../T/bpy.types.TextureNodeValToRGB.md#bpy.types.TextureNodeValToRGB.color_ramp "bpy.types.TextureNodeValToRGB.color_ramp")

  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
