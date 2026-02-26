# CurveMapping(bpy_struct)

base class — [`bpy_struct`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct "bpy.types.bpy_struct")

_class _bpy.types.CurveMapping(_bpy_struct_)
    

Curve mapping to map color, vector and scalar values to other values using a user defined curve

black_level
    

For RGB curves, the color that black is mapped to

Type:
    

[`mathutils.Color`](mathutils.md#mathutils.Color "mathutils.Color") of 3 items in [-inf, inf], default (0.0, 0.0, 0.0)

clip_max_x
    

Type:
    

float in [-100, 100], default 0.0

clip_max_y
    

Type:
    

float in [-100, 100], default 0.0

clip_min_x
    

Type:
    

float in [-100, 100], default 0.0

clip_min_y
    

Type:
    

float in [-100, 100], default 0.0

curves
    

Type:
    

[`bpy_prop_collection`](../_other/bpy.types.bpy_prop_collection.md#bpy.types.bpy_prop_collection "bpy.types.bpy_prop_collection") of [`CurveMap`](bpy.types.CurveMap.md#bpy.types.CurveMap "bpy.types.CurveMap"), (readonly)

extend
    

Extrapolate the curve or extend it horizontally

Type:
    

enum in [`'HORIZONTAL'`, `'EXTRAPOLATED'`], default `'HORIZONTAL'`

tone
    

Tone of the curve

  * `STANDARD` Standard – Combined curve is applied to each channel individually, which may result in a change of hue.

  * `FILMLIKE` Filmlike – Keeps the hue constant.


Type:
    

enum in [`'STANDARD'`, `'FILMLIKE'`], default `'STANDARD'`

use_clip
    

Force the curve view to fit a defined boundary

Type:
    

boolean, default False

white_level
    

For RGB curves, the color that white is mapped to

Type:
    

[`mathutils.Color`](mathutils.md#mathutils.Color "mathutils.Color") of 3 items in [-inf, inf], default (0.0, 0.0, 0.0)

update()
    

Update curve mapping after making changes

reset_view()
    

Reset the curve mapping grid to its clipping size

initialize()
    

Initialize curve

evaluate(_curve_ , _position_)
    

Evaluate curve at given location

Parameters:
    

  * **curve** ([`CurveMap`](bpy.types.CurveMap.md#bpy.types.CurveMap "bpy.types.CurveMap"), (never None)) – curve, Curve to evaluate

  * **position** (_float in_ _[__-inf_ _,__inf_ _]_) – Position, Position to evaluate curve at


Returns:
    

Value, Value of curve at given location

Return type:
    

float in [-inf, inf]

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

  * [`Brush.automasking_cavity_curve`](../B/bpy.types.Brush.md#bpy.types.Brush.automasking_cavity_curve "bpy.types.Brush.automasking_cavity_curve")
  * [`Brush.curve_distance_falloff`](../B/bpy.types.Brush.md#bpy.types.Brush.curve_distance_falloff "bpy.types.Brush.curve_distance_falloff")
  * [`Brush.curve_jitter`](../B/bpy.types.Brush.md#bpy.types.Brush.curve_jitter "bpy.types.Brush.curve_jitter")
  * [`Brush.curve_random_hue`](../B/bpy.types.Brush.md#bpy.types.Brush.curve_random_hue "bpy.types.Brush.curve_random_hue")
  * [`Brush.curve_random_saturation`](../B/bpy.types.Brush.md#bpy.types.Brush.curve_random_saturation "bpy.types.Brush.curve_random_saturation")
  * [`Brush.curve_random_value`](../B/bpy.types.Brush.md#bpy.types.Brush.curve_random_value "bpy.types.Brush.curve_random_value")
  * [`Brush.curve_size`](../B/bpy.types.Brush.md#bpy.types.Brush.curve_size "bpy.types.Brush.curve_size")
  * [`Brush.curve_strength`](../B/bpy.types.Brush.md#bpy.types.Brush.curve_strength "bpy.types.Brush.curve_strength")
  * [`BrushCurvesSculptSettings.curve_parameter_falloff`](../B/bpy.types.BrushCurvesSculptSettings.md#bpy.types.BrushCurvesSculptSettings.curve_parameter_falloff "bpy.types.BrushCurvesSculptSettings.curve_parameter_falloff")
  * [`BrushGpencilSettings.curve_jitter`](../B/bpy.types.BrushGpencilSettings.md#bpy.types.BrushGpencilSettings.curve_jitter "bpy.types.BrushGpencilSettings.curve_jitter")
  * [`BrushGpencilSettings.curve_random_hue`](../B/bpy.types.BrushGpencilSettings.md#bpy.types.BrushGpencilSettings.curve_random_hue "bpy.types.BrushGpencilSettings.curve_random_hue")
  * [`BrushGpencilSettings.curve_random_pressure`](../B/bpy.types.BrushGpencilSettings.md#bpy.types.BrushGpencilSettings.curve_random_pressure "bpy.types.BrushGpencilSettings.curve_random_pressure")
  * [`BrushGpencilSettings.curve_random_saturation`](../B/bpy.types.BrushGpencilSettings.md#bpy.types.BrushGpencilSettings.curve_random_saturation "bpy.types.BrushGpencilSettings.curve_random_saturation")
  * [`BrushGpencilSettings.curve_random_strength`](../B/bpy.types.BrushGpencilSettings.md#bpy.types.BrushGpencilSettings.curve_random_strength "bpy.types.BrushGpencilSettings.curve_random_strength")
  * [`BrushGpencilSettings.curve_random_uv`](../B/bpy.types.BrushGpencilSettings.md#bpy.types.BrushGpencilSettings.curve_random_uv "bpy.types.BrushGpencilSettings.curve_random_uv")
  * [`BrushGpencilSettings.curve_random_value`](../B/bpy.types.BrushGpencilSettings.md#bpy.types.BrushGpencilSettings.curve_random_value "bpy.types.BrushGpencilSettings.curve_random_value")
  * [`BrushGpencilSettings.curve_sensitivity`](../B/bpy.types.BrushGpencilSettings.md#bpy.types.BrushGpencilSettings.curve_sensitivity "bpy.types.BrushGpencilSettings.curve_sensitivity")
  * [`BrushGpencilSettings.curve_strength`](../B/bpy.types.BrushGpencilSettings.md#bpy.types.BrushGpencilSettings.curve_strength "bpy.types.BrushGpencilSettings.curve_strength")
  * [`ColorManagedViewSettings.curve_mapping`](bpy.types.ColorManagedViewSettings.md#bpy.types.ColorManagedViewSettings.curve_mapping "bpy.types.ColorManagedViewSettings.curve_mapping")
  * [`CompositorNodeCurveRGB.mapping`](bpy.types.CompositorNodeCurveRGB.md#bpy.types.CompositorNodeCurveRGB.mapping "bpy.types.CompositorNodeCurveRGB.mapping")
  * [`CompositorNodeHueCorrect.mapping`](bpy.types.CompositorNodeHueCorrect.md#bpy.types.CompositorNodeHueCorrect.mapping "bpy.types.CompositorNodeHueCorrect.mapping")
  * [`CompositorNodeTime.curve`](bpy.types.CompositorNodeTime.md#bpy.types.CompositorNodeTime.curve "bpy.types.CompositorNodeTime.curve")
  * [`CurvesModifier.curve_mapping`](bpy.types.CurvesModifier.md#bpy.types.CurvesModifier.curve_mapping "bpy.types.CurvesModifier.curve_mapping")
  * [`EQCurveMappingData.curve_mapping`](../E/bpy.types.EQCurveMappingData.md#bpy.types.EQCurveMappingData.curve_mapping "bpy.types.EQCurveMappingData.curve_mapping")
  * [`GPencilInterpolateSettings.interpolation_curve`](../G/bpy.types.GPencilInterpolateSettings.md#bpy.types.GPencilInterpolateSettings.interpolation_curve "bpy.types.GPencilInterpolateSettings.interpolation_curve")
  * [`GPencilSculptSettings.multiframe_falloff_curve`](../G/bpy.types.GPencilSculptSettings.md#bpy.types.GPencilSculptSettings.multiframe_falloff_curve "bpy.types.GPencilSculptSettings.multiframe_falloff_curve")
  * [`GPencilSculptSettings.thickness_primitive_curve`](../G/bpy.types.GPencilSculptSettings.md#bpy.types.GPencilSculptSettings.thickness_primitive_curve "bpy.types.GPencilSculptSettings.thickness_primitive_curve")
  * [`GreasePencilColorModifier.custom_curve`](../G/bpy.types.GreasePencilColorModifier.md#bpy.types.GreasePencilColorModifier.custom_curve "bpy.types.GreasePencilColorModifier.custom_curve")
  * [`GreasePencilHookModifier.custom_curve`](../G/bpy.types.GreasePencilHookModifier.md#bpy.types.GreasePencilHookModifier.custom_curve "bpy.types.GreasePencilHookModifier.custom_curve")
  * [`GreasePencilNoiseModifier.custom_curve`](../G/bpy.types.GreasePencilNoiseModifier.md#bpy.types.GreasePencilNoiseModifier.custom_curve "bpy.types.GreasePencilNoiseModifier.custom_curve")
  * [`GreasePencilOpacityModifier.custom_curve`](../G/bpy.types.GreasePencilOpacityModifier.md#bpy.types.GreasePencilOpacityModifier.custom_curve "bpy.types.GreasePencilOpacityModifier.custom_curve")
  * [`GreasePencilSmoothModifier.custom_curve`](../G/bpy.types.GreasePencilSmoothModifier.md#bpy.types.GreasePencilSmoothModifier.custom_curve "bpy.types.GreasePencilSmoothModifier.custom_curve")
  * [`GreasePencilThickModifierData.custom_curve`](../G/bpy.types.GreasePencilThickModifierData.md#bpy.types.GreasePencilThickModifierData.custom_curve "bpy.types.GreasePencilThickModifierData.custom_curve")
  * [`GreasePencilTintModifier.custom_curve`](../G/bpy.types.GreasePencilTintModifier.md#bpy.types.GreasePencilTintModifier.custom_curve "bpy.types.GreasePencilTintModifier.custom_curve")

| 

  * [`HookModifier.falloff_curve`](../H/bpy.types.HookModifier.md#bpy.types.HookModifier.falloff_curve "bpy.types.HookModifier.falloff_curve")
  * [`HueCorrectModifier.curve_mapping`](../H/bpy.types.HueCorrectModifier.md#bpy.types.HueCorrectModifier.curve_mapping "bpy.types.HueCorrectModifier.curve_mapping")
  * [`LineStyleAlphaModifier_AlongStroke.curve`](../L/bpy.types.LineStyleAlphaModifier_AlongStroke.md#bpy.types.LineStyleAlphaModifier_AlongStroke.curve "bpy.types.LineStyleAlphaModifier_AlongStroke.curve")
  * [`LineStyleAlphaModifier_CreaseAngle.curve`](../L/bpy.types.LineStyleAlphaModifier_CreaseAngle.md#bpy.types.LineStyleAlphaModifier_CreaseAngle.curve "bpy.types.LineStyleAlphaModifier_CreaseAngle.curve")
  * [`LineStyleAlphaModifier_Curvature_3D.curve`](../L/bpy.types.LineStyleAlphaModifier_Curvature_3D.md#bpy.types.LineStyleAlphaModifier_Curvature_3D.curve "bpy.types.LineStyleAlphaModifier_Curvature_3D.curve")
  * [`LineStyleAlphaModifier_DistanceFromCamera.curve`](../L/bpy.types.LineStyleAlphaModifier_DistanceFromCamera.md#bpy.types.LineStyleAlphaModifier_DistanceFromCamera.curve "bpy.types.LineStyleAlphaModifier_DistanceFromCamera.curve")
  * [`LineStyleAlphaModifier_DistanceFromObject.curve`](../L/bpy.types.LineStyleAlphaModifier_DistanceFromObject.md#bpy.types.LineStyleAlphaModifier_DistanceFromObject.curve "bpy.types.LineStyleAlphaModifier_DistanceFromObject.curve")
  * [`LineStyleAlphaModifier_Material.curve`](../L/bpy.types.LineStyleAlphaModifier_Material.md#bpy.types.LineStyleAlphaModifier_Material.curve "bpy.types.LineStyleAlphaModifier_Material.curve")
  * [`LineStyleAlphaModifier_Noise.curve`](../L/bpy.types.LineStyleAlphaModifier_Noise.md#bpy.types.LineStyleAlphaModifier_Noise.curve "bpy.types.LineStyleAlphaModifier_Noise.curve")
  * [`LineStyleAlphaModifier_Tangent.curve`](../L/bpy.types.LineStyleAlphaModifier_Tangent.md#bpy.types.LineStyleAlphaModifier_Tangent.curve "bpy.types.LineStyleAlphaModifier_Tangent.curve")
  * [`LineStyleThicknessModifier_AlongStroke.curve`](../L/bpy.types.LineStyleThicknessModifier_AlongStroke.md#bpy.types.LineStyleThicknessModifier_AlongStroke.curve "bpy.types.LineStyleThicknessModifier_AlongStroke.curve")
  * [`LineStyleThicknessModifier_CreaseAngle.curve`](../L/bpy.types.LineStyleThicknessModifier_CreaseAngle.md#bpy.types.LineStyleThicknessModifier_CreaseAngle.curve "bpy.types.LineStyleThicknessModifier_CreaseAngle.curve")
  * [`LineStyleThicknessModifier_Curvature_3D.curve`](../L/bpy.types.LineStyleThicknessModifier_Curvature_3D.md#bpy.types.LineStyleThicknessModifier_Curvature_3D.curve "bpy.types.LineStyleThicknessModifier_Curvature_3D.curve")
  * [`LineStyleThicknessModifier_DistanceFromCamera.curve`](../L/bpy.types.LineStyleThicknessModifier_DistanceFromCamera.md#bpy.types.LineStyleThicknessModifier_DistanceFromCamera.curve "bpy.types.LineStyleThicknessModifier_DistanceFromCamera.curve")
  * [`LineStyleThicknessModifier_DistanceFromObject.curve`](../L/bpy.types.LineStyleThicknessModifier_DistanceFromObject.md#bpy.types.LineStyleThicknessModifier_DistanceFromObject.curve "bpy.types.LineStyleThicknessModifier_DistanceFromObject.curve")
  * [`LineStyleThicknessModifier_Material.curve`](../L/bpy.types.LineStyleThicknessModifier_Material.md#bpy.types.LineStyleThicknessModifier_Material.curve "bpy.types.LineStyleThicknessModifier_Material.curve")
  * [`LineStyleThicknessModifier_Tangent.curve`](../L/bpy.types.LineStyleThicknessModifier_Tangent.md#bpy.types.LineStyleThicknessModifier_Tangent.curve "bpy.types.LineStyleThicknessModifier_Tangent.curve")
  * [`Paint.cavity_curve`](../P/bpy.types.Paint.md#bpy.types.Paint.cavity_curve "bpy.types.Paint.cavity_curve")
  * [`ParticleBrush.curve`](../P/bpy.types.ParticleBrush.md#bpy.types.ParticleBrush.curve "bpy.types.ParticleBrush.curve")
  * [`ParticleSettings.clump_curve`](../P/bpy.types.ParticleSettings.md#bpy.types.ParticleSettings.clump_curve "bpy.types.ParticleSettings.clump_curve")
  * [`ParticleSettings.roughness_curve`](../P/bpy.types.ParticleSettings.md#bpy.types.ParticleSettings.roughness_curve "bpy.types.ParticleSettings.roughness_curve")
  * [`ParticleSettings.twist_curve`](../P/bpy.types.ParticleSettings.md#bpy.types.ParticleSettings.twist_curve "bpy.types.ParticleSettings.twist_curve")
  * [`RenderSettings.motion_blur_shutter_curve`](../R/bpy.types.RenderSettings.md#bpy.types.RenderSettings.motion_blur_shutter_curve "bpy.types.RenderSettings.motion_blur_shutter_curve")
  * [`Sculpt.automasking_cavity_curve`](../S/bpy.types.Sculpt.md#bpy.types.Sculpt.automasking_cavity_curve "bpy.types.Sculpt.automasking_cavity_curve")
  * [`Sculpt.automasking_cavity_curve_op`](../S/bpy.types.Sculpt.md#bpy.types.Sculpt.automasking_cavity_curve_op "bpy.types.Sculpt.automasking_cavity_curve_op")
  * [`ShaderNodeFloatCurve.mapping`](../S/bpy.types.ShaderNodeFloatCurve.md#bpy.types.ShaderNodeFloatCurve.mapping "bpy.types.ShaderNodeFloatCurve.mapping")
  * [`ShaderNodeRGBCurve.mapping`](../S/bpy.types.ShaderNodeRGBCurve.md#bpy.types.ShaderNodeRGBCurve.mapping "bpy.types.ShaderNodeRGBCurve.mapping")
  * [`ShaderNodeVectorCurve.mapping`](../S/bpy.types.ShaderNodeVectorCurve.md#bpy.types.ShaderNodeVectorCurve.mapping "bpy.types.ShaderNodeVectorCurve.mapping")
  * [`TextureNodeCurveRGB.mapping`](../T/bpy.types.TextureNodeCurveRGB.md#bpy.types.TextureNodeCurveRGB.mapping "bpy.types.TextureNodeCurveRGB.mapping")
  * [`TextureNodeCurveTime.curve`](../T/bpy.types.TextureNodeCurveTime.md#bpy.types.TextureNodeCurveTime.curve "bpy.types.TextureNodeCurveTime.curve")
  * [`UvSculpt.curve_distance_falloff`](../U/bpy.types.UvSculpt.md#bpy.types.UvSculpt.curve_distance_falloff "bpy.types.UvSculpt.curve_distance_falloff")
  * [`VertexWeightEditModifier.map_curve`](../V/bpy.types.VertexWeightEditModifier.md#bpy.types.VertexWeightEditModifier.map_curve "bpy.types.VertexWeightEditModifier.map_curve")
  * [`VertexWeightProximityModifier.map_curve`](../V/bpy.types.VertexWeightProximityModifier.md#bpy.types.VertexWeightProximityModifier.map_curve "bpy.types.VertexWeightProximityModifier.map_curve")
  * [`WarpModifier.falloff_curve`](../W/bpy.types.WarpModifier.md#bpy.types.WarpModifier.falloff_curve "bpy.types.WarpModifier.falloff_curve")

  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
