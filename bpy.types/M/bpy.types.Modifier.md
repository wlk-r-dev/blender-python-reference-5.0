# Modifier(bpy_struct)

base class — [`bpy_struct`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct "bpy.types.bpy_struct")

subclasses — [`ArmatureModifier`](../A/bpy.types.ArmatureModifier.md#bpy.types.ArmatureModifier "bpy.types.ArmatureModifier"), [`ArrayModifier`](../A/bpy.types.ArrayModifier.md#bpy.types.ArrayModifier "bpy.types.ArrayModifier"), [`BevelModifier`](../B/bpy.types.BevelModifier.md#bpy.types.BevelModifier "bpy.types.BevelModifier"), [`BooleanModifier`](../B/bpy.types.BooleanModifier.md#bpy.types.BooleanModifier "bpy.types.BooleanModifier"), [`BuildModifier`](../B/bpy.types.BuildModifier.md#bpy.types.BuildModifier "bpy.types.BuildModifier"), [`CastModifier`](../C/bpy.types.CastModifier.md#bpy.types.CastModifier "bpy.types.CastModifier"), [`ClothModifier`](../C/bpy.types.ClothModifier.md#bpy.types.ClothModifier "bpy.types.ClothModifier"), [`CollisionModifier`](../C/bpy.types.CollisionModifier.md#bpy.types.CollisionModifier "bpy.types.CollisionModifier"), [`CorrectiveSmoothModifier`](../C/bpy.types.CorrectiveSmoothModifier.md#bpy.types.CorrectiveSmoothModifier "bpy.types.CorrectiveSmoothModifier"), [`CurveModifier`](../C/bpy.types.CurveModifier.md#bpy.types.CurveModifier "bpy.types.CurveModifier"), [`DataTransferModifier`](../D/bpy.types.DataTransferModifier.md#bpy.types.DataTransferModifier "bpy.types.DataTransferModifier"), [`DecimateModifier`](../D/bpy.types.DecimateModifier.md#bpy.types.DecimateModifier "bpy.types.DecimateModifier"), [`DisplaceModifier`](../D/bpy.types.DisplaceModifier.md#bpy.types.DisplaceModifier "bpy.types.DisplaceModifier"), [`DynamicPaintModifier`](../D/bpy.types.DynamicPaintModifier.md#bpy.types.DynamicPaintModifier "bpy.types.DynamicPaintModifier"), [`EdgeSplitModifier`](../E/bpy.types.EdgeSplitModifier.md#bpy.types.EdgeSplitModifier "bpy.types.EdgeSplitModifier"), [`ExplodeModifier`](../E/bpy.types.ExplodeModifier.md#bpy.types.ExplodeModifier "bpy.types.ExplodeModifier"), [`FluidModifier`](../F/bpy.types.FluidModifier.md#bpy.types.FluidModifier "bpy.types.FluidModifier"), [`GreasePencilArmatureModifier`](../G/bpy.types.GreasePencilArmatureModifier.md#bpy.types.GreasePencilArmatureModifier "bpy.types.GreasePencilArmatureModifier"), [`GreasePencilArrayModifier`](../G/bpy.types.GreasePencilArrayModifier.md#bpy.types.GreasePencilArrayModifier "bpy.types.GreasePencilArrayModifier"), [`GreasePencilBuildModifier`](../G/bpy.types.GreasePencilBuildModifier.md#bpy.types.GreasePencilBuildModifier "bpy.types.GreasePencilBuildModifier"), [`GreasePencilColorModifier`](../G/bpy.types.GreasePencilColorModifier.md#bpy.types.GreasePencilColorModifier "bpy.types.GreasePencilColorModifier"), [`GreasePencilDashModifierData`](../G/bpy.types.GreasePencilDashModifierData.md#bpy.types.GreasePencilDashModifierData "bpy.types.GreasePencilDashModifierData"), [`GreasePencilEnvelopeModifier`](../G/bpy.types.GreasePencilEnvelopeModifier.md#bpy.types.GreasePencilEnvelopeModifier "bpy.types.GreasePencilEnvelopeModifier"), [`GreasePencilHookModifier`](../G/bpy.types.GreasePencilHookModifier.md#bpy.types.GreasePencilHookModifier "bpy.types.GreasePencilHookModifier"), [`GreasePencilLatticeModifier`](../G/bpy.types.GreasePencilLatticeModifier.md#bpy.types.GreasePencilLatticeModifier "bpy.types.GreasePencilLatticeModifier"), [`GreasePencilLengthModifier`](../G/bpy.types.GreasePencilLengthModifier.md#bpy.types.GreasePencilLengthModifier "bpy.types.GreasePencilLengthModifier"), [`GreasePencilLineartModifier`](../G/bpy.types.GreasePencilLineartModifier.md#bpy.types.GreasePencilLineartModifier "bpy.types.GreasePencilLineartModifier"), [`GreasePencilMirrorModifier`](../G/bpy.types.GreasePencilMirrorModifier.md#bpy.types.GreasePencilMirrorModifier "bpy.types.GreasePencilMirrorModifier"), [`GreasePencilMultiplyModifier`](../G/bpy.types.GreasePencilMultiplyModifier.md#bpy.types.GreasePencilMultiplyModifier "bpy.types.GreasePencilMultiplyModifier"), [`GreasePencilNoiseModifier`](../G/bpy.types.GreasePencilNoiseModifier.md#bpy.types.GreasePencilNoiseModifier "bpy.types.GreasePencilNoiseModifier"), [`GreasePencilOffsetModifier`](../G/bpy.types.GreasePencilOffsetModifier.md#bpy.types.GreasePencilOffsetModifier "bpy.types.GreasePencilOffsetModifier"), [`GreasePencilOpacityModifier`](../G/bpy.types.GreasePencilOpacityModifier.md#bpy.types.GreasePencilOpacityModifier "bpy.types.GreasePencilOpacityModifier"), [`GreasePencilOutlineModifier`](../G/bpy.types.GreasePencilOutlineModifier.md#bpy.types.GreasePencilOutlineModifier "bpy.types.GreasePencilOutlineModifier"), [`GreasePencilShrinkwrapModifier`](../G/bpy.types.GreasePencilShrinkwrapModifier.md#bpy.types.GreasePencilShrinkwrapModifier "bpy.types.GreasePencilShrinkwrapModifier"), [`GreasePencilSimplifyModifier`](../G/bpy.types.GreasePencilSimplifyModifier.md#bpy.types.GreasePencilSimplifyModifier "bpy.types.GreasePencilSimplifyModifier"), [`GreasePencilSmoothModifier`](../G/bpy.types.GreasePencilSmoothModifier.md#bpy.types.GreasePencilSmoothModifier "bpy.types.GreasePencilSmoothModifier"), [`GreasePencilSubdivModifier`](../G/bpy.types.GreasePencilSubdivModifier.md#bpy.types.GreasePencilSubdivModifier "bpy.types.GreasePencilSubdivModifier"), [`GreasePencilTextureModifier`](../G/bpy.types.GreasePencilTextureModifier.md#bpy.types.GreasePencilTextureModifier "bpy.types.GreasePencilTextureModifier"), [`GreasePencilThickModifierData`](../G/bpy.types.GreasePencilThickModifierData.md#bpy.types.GreasePencilThickModifierData "bpy.types.GreasePencilThickModifierData"), [`GreasePencilTimeModifier`](../G/bpy.types.GreasePencilTimeModifier.md#bpy.types.GreasePencilTimeModifier "bpy.types.GreasePencilTimeModifier"), [`GreasePencilTintModifier`](../G/bpy.types.GreasePencilTintModifier.md#bpy.types.GreasePencilTintModifier "bpy.types.GreasePencilTintModifier"), [`GreasePencilWeightAngleModifier`](../G/bpy.types.GreasePencilWeightAngleModifier.md#bpy.types.GreasePencilWeightAngleModifier "bpy.types.GreasePencilWeightAngleModifier"), [`GreasePencilWeightProximityModifier`](../G/bpy.types.GreasePencilWeightProximityModifier.md#bpy.types.GreasePencilWeightProximityModifier "bpy.types.GreasePencilWeightProximityModifier"), [`HookModifier`](../H/bpy.types.HookModifier.md#bpy.types.HookModifier "bpy.types.HookModifier"), [`LaplacianDeformModifier`](../L/bpy.types.LaplacianDeformModifier.md#bpy.types.LaplacianDeformModifier "bpy.types.LaplacianDeformModifier"), [`LaplacianSmoothModifier`](../L/bpy.types.LaplacianSmoothModifier.md#bpy.types.LaplacianSmoothModifier "bpy.types.LaplacianSmoothModifier"), [`LatticeModifier`](../L/bpy.types.LatticeModifier.md#bpy.types.LatticeModifier "bpy.types.LatticeModifier"), [`MaskModifier`](bpy.types.MaskModifier.md#bpy.types.MaskModifier "bpy.types.MaskModifier"), [`MeshCacheModifier`](bpy.types.MeshCacheModifier.md#bpy.types.MeshCacheModifier "bpy.types.MeshCacheModifier"), [`MeshDeformModifier`](bpy.types.MeshDeformModifier.md#bpy.types.MeshDeformModifier "bpy.types.MeshDeformModifier"), [`MeshSequenceCacheModifier`](bpy.types.MeshSequenceCacheModifier.md#bpy.types.MeshSequenceCacheModifier "bpy.types.MeshSequenceCacheModifier"), [`MeshToVolumeModifier`](bpy.types.MeshToVolumeModifier.md#bpy.types.MeshToVolumeModifier "bpy.types.MeshToVolumeModifier"), [`MirrorModifier`](bpy.types.MirrorModifier.md#bpy.types.MirrorModifier "bpy.types.MirrorModifier"), [`MultiresModifier`](bpy.types.MultiresModifier.md#bpy.types.MultiresModifier "bpy.types.MultiresModifier"), [`NodesModifier`](../N/bpy.types.NodesModifier.md#bpy.types.NodesModifier "bpy.types.NodesModifier"), [`NormalEditModifier`](../N/bpy.types.NormalEditModifier.md#bpy.types.NormalEditModifier "bpy.types.NormalEditModifier"), [`OceanModifier`](../O/bpy.types.OceanModifier.md#bpy.types.OceanModifier "bpy.types.OceanModifier"), [`ParticleInstanceModifier`](../P/bpy.types.ParticleInstanceModifier.md#bpy.types.ParticleInstanceModifier "bpy.types.ParticleInstanceModifier"), [`ParticleSystemModifier`](../P/bpy.types.ParticleSystemModifier.md#bpy.types.ParticleSystemModifier "bpy.types.ParticleSystemModifier"), [`RemeshModifier`](../R/bpy.types.RemeshModifier.md#bpy.types.RemeshModifier "bpy.types.RemeshModifier"), [`ScrewModifier`](../S/bpy.types.ScrewModifier.md#bpy.types.ScrewModifier "bpy.types.ScrewModifier"), [`ShrinkwrapModifier`](../S/bpy.types.ShrinkwrapModifier.md#bpy.types.ShrinkwrapModifier "bpy.types.ShrinkwrapModifier"), [`SimpleDeformModifier`](../S/bpy.types.SimpleDeformModifier.md#bpy.types.SimpleDeformModifier "bpy.types.SimpleDeformModifier"), [`SkinModifier`](../S/bpy.types.SkinModifier.md#bpy.types.SkinModifier "bpy.types.SkinModifier"), [`SmoothModifier`](../S/bpy.types.SmoothModifier.md#bpy.types.SmoothModifier "bpy.types.SmoothModifier"), [`SoftBodyModifier`](../S/bpy.types.SoftBodyModifier.md#bpy.types.SoftBodyModifier "bpy.types.SoftBodyModifier"), [`SolidifyModifier`](../S/bpy.types.SolidifyModifier.md#bpy.types.SolidifyModifier "bpy.types.SolidifyModifier"), [`SubsurfModifier`](../S/bpy.types.SubsurfModifier.md#bpy.types.SubsurfModifier "bpy.types.SubsurfModifier"), [`SurfaceDeformModifier`](../S/bpy.types.SurfaceDeformModifier.md#bpy.types.SurfaceDeformModifier "bpy.types.SurfaceDeformModifier"), [`SurfaceModifier`](../S/bpy.types.SurfaceModifier.md#bpy.types.SurfaceModifier "bpy.types.SurfaceModifier"), [`TriangulateModifier`](../T/bpy.types.TriangulateModifier.md#bpy.types.TriangulateModifier "bpy.types.TriangulateModifier"), [`UVProjectModifier`](../U/bpy.types.UVProjectModifier.md#bpy.types.UVProjectModifier "bpy.types.UVProjectModifier"), [`UVWarpModifier`](../U/bpy.types.UVWarpModifier.md#bpy.types.UVWarpModifier "bpy.types.UVWarpModifier"), [`VertexWeightEditModifier`](../V/bpy.types.VertexWeightEditModifier.md#bpy.types.VertexWeightEditModifier "bpy.types.VertexWeightEditModifier"), [`VertexWeightMixModifier`](../V/bpy.types.VertexWeightMixModifier.md#bpy.types.VertexWeightMixModifier "bpy.types.VertexWeightMixModifier"), [`VertexWeightProximityModifier`](../V/bpy.types.VertexWeightProximityModifier.md#bpy.types.VertexWeightProximityModifier "bpy.types.VertexWeightProximityModifier"), [`VolumeDisplaceModifier`](../V/bpy.types.VolumeDisplaceModifier.md#bpy.types.VolumeDisplaceModifier "bpy.types.VolumeDisplaceModifier"), [`VolumeToMeshModifier`](../V/bpy.types.VolumeToMeshModifier.md#bpy.types.VolumeToMeshModifier "bpy.types.VolumeToMeshModifier"), [`WarpModifier`](../W/bpy.types.WarpModifier.md#bpy.types.WarpModifier "bpy.types.WarpModifier"), [`WaveModifier`](../W/bpy.types.WaveModifier.md#bpy.types.WaveModifier "bpy.types.WaveModifier"), [`WeightedNormalModifier`](../W/bpy.types.WeightedNormalModifier.md#bpy.types.WeightedNormalModifier "bpy.types.WeightedNormalModifier"), [`WeldModifier`](../W/bpy.types.WeldModifier.md#bpy.types.WeldModifier "bpy.types.WeldModifier"), [`WireframeModifier`](../W/bpy.types.WireframeModifier.md#bpy.types.WireframeModifier "bpy.types.WireframeModifier")

_class _bpy.types.Modifier(_bpy_struct_)
    

Modifier affecting the geometry data of an object

execution_time
    

Time in seconds that the modifier took to evaluate. This is only set on evaluated objects. If multiple modifiers run in parallel, execution time is not a reliable metric.

Type:
    

float in [-inf, inf], default 0.0, (readonly)

is_active
    

The active modifier in the list

Type:
    

boolean, default False

is_override_data
    

In a local override object, whether this modifier comes from the linked reference object, or is local to the override

Type:
    

boolean, default False, (readonly)

name
    

Modifier name

Type:
    

string, default “”, (never None)

persistent_uid
    

Uniquely identifies the modifier within the modifier stack that it is part of

Type:
    

int in [-inf, inf], default 0, (readonly)

show_expanded
    

Set modifier expanded in the user interface

Type:
    

boolean, default False

show_in_editmode
    

Display modifier in Edit mode

Type:
    

boolean, default False

show_on_cage
    

Adjust edit cage to modifier result

Type:
    

boolean, default False

show_render
    

Use modifier during render

Type:
    

boolean, default False

show_viewport
    

Display modifier in viewport

Type:
    

boolean, default False

type
    

Type:
    

enum in [Object Modifier Type Items](../../bpy_types_enum_items/object_modifier_type_items.md#rna-enum-object-modifier-type-items), default `'GREASE_PENCIL_VERTEX_WEIGHT_PROXIMITY'`, (readonly)

use_apply_on_spline
    

Apply this and all preceding deformation modifiers on splines’ points rather than on filled curve/surface

Type:
    

boolean, default False

use_pin_to_last
    

Keep the modifier at the end of the list

Type:
    

boolean, default False

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

  * [`Object.modifiers`](../O/bpy.types.Object.md#bpy.types.Object.modifiers "bpy.types.Object.modifiers")
  * [`ObjectModifiers.active`](../O/bpy.types.ObjectModifiers.md#bpy.types.ObjectModifiers.active "bpy.types.ObjectModifiers.active")

| 

  * [`ObjectModifiers.new`](../O/bpy.types.ObjectModifiers.md#bpy.types.ObjectModifiers.new "bpy.types.ObjectModifiers.new")
  * [`ObjectModifiers.remove`](../O/bpy.types.ObjectModifiers.md#bpy.types.ObjectModifiers.remove "bpy.types.ObjectModifiers.remove")

  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
