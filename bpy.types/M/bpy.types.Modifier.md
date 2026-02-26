# Modifier(bpy_struct)

base class — [[bpy_struct]]

subclasses — [[ArmatureModifier]], [[ArrayModifier]], [[BevelModifier]], [[BooleanModifier]], [[BuildModifier]], [[CastModifier]], [[ClothModifier]], [[CollisionModifier]], [[CorrectiveSmoothModifier]], [[CurveModifier]], [[DataTransferModifier]], [[DecimateModifier]], [[DisplaceModifier]], [[DynamicPaintModifier]], [[EdgeSplitModifier]], [[ExplodeModifier]], [[FluidModifier]], [[GreasePencilArmatureModifier]], [[GreasePencilArrayModifier]], [[GreasePencilBuildModifier]], [[GreasePencilColorModifier]], [[GreasePencilDashModifierData]], [[GreasePencilEnvelopeModifier]], [[GreasePencilHookModifier]], [[GreasePencilLatticeModifier]], [[GreasePencilLengthModifier]], [[GreasePencilLineartModifier]], [[GreasePencilMirrorModifier]], [[GreasePencilMultiplyModifier]], [[GreasePencilNoiseModifier]], [[GreasePencilOffsetModifier]], [[GreasePencilOpacityModifier]], [[GreasePencilOutlineModifier]], [[GreasePencilShrinkwrapModifier]], [[GreasePencilSimplifyModifier]], [[GreasePencilSmoothModifier]], [[GreasePencilSubdivModifier]], [[GreasePencilTextureModifier]], [[GreasePencilThickModifierData]], [[GreasePencilTimeModifier]], [[GreasePencilTintModifier]], [[GreasePencilWeightAngleModifier]], [[GreasePencilWeightProximityModifier]], [[HookModifier]], [[LaplacianDeformModifier]], [[LaplacianSmoothModifier]], [[LatticeModifier]], [[MaskModifier]], [[MeshCacheModifier]], [[MeshDeformModifier]], [[MeshSequenceCacheModifier]], [[MeshToVolumeModifier]], [[MirrorModifier]], [[MultiresModifier]], [[NodesModifier]], [[NormalEditModifier]], [[OceanModifier]], [[ParticleInstanceModifier]], [[ParticleSystemModifier]], [[RemeshModifier]], [[ScrewModifier]], [[ShrinkwrapModifier]], [[SimpleDeformModifier]], [[SkinModifier]], [[SmoothModifier]], [[SoftBodyModifier]], [[SolidifyModifier]], [[SubsurfModifier]], [[SurfaceDeformModifier]], [[SurfaceModifier]], [[TriangulateModifier]], [[UVProjectModifier]], [[UVWarpModifier]], [[VertexWeightEditModifier]], [[VertexWeightMixModifier]], [[VertexWeightProximityModifier]], [[VolumeDisplaceModifier]], [[VolumeToMeshModifier]], [[WarpModifier]], [[WaveModifier]], [[WeightedNormalModifier]], [[WeldModifier]], [[WireframeModifier]]

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

  * [[Object.modifiers]]
  * [[ObjectModifiers.active]]

| 

  * [[ObjectModifiers.new]]
  * [[ObjectModifiers.remove]]

  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
