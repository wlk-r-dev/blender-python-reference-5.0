# ColorRamp(bpy_struct)

base class — [[bpy_struct]]

_class _bpy.types.ColorRamp(_bpy_struct_)
    

Color ramp mapping a scalar value to a color

color_mode
    

Set color mode to use for interpolation

Type:
    

enum in [`'RGB'`, `'HSV'`, `'HSL'`], default `'RGB'`

elements
    

Type:
    

[[ColorRampElements]] [[bpy_prop_collection]] of [[ColorRampElement]], (readonly)

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

  * [[Brush.gradient]]
  * [[ColorMapping.color_ramp]]
  * [[DynamicPaintBrushSettings.paint_ramp]]
  * [[DynamicPaintBrushSettings.velocity_ramp]]
  * [[FluidDomainSettings.color_ramp]]
  * [[GreasePencilTintModifier.color_ramp]]
  * [[LineStyleColorModifier_AlongStroke.color_ramp]]
  * [[LineStyleColorModifier_CreaseAngle.color_ramp]]
  * [[LineStyleColorModifier_Curvature_3D.color_ramp]]

| 

  * [[LineStyleColorModifier_DistanceFromCamera.color_ramp]]
  * [[LineStyleColorModifier_DistanceFromObject.color_ramp]]
  * [[LineStyleColorModifier_Material.color_ramp]]
  * [[LineStyleColorModifier_Noise.color_ramp]]
  * [[LineStyleColorModifier_Tangent.color_ramp]]
  * [[PreferencesView.weight_color_range]]
  * [[ShaderNodeValToRGB.color_ramp]]
  * [[Texture.color_ramp]]
  * [[TextureNodeValToRGB.color_ramp]]

  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
