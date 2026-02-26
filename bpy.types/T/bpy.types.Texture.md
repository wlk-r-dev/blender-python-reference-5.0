# Texture(ID)

base classes — [`bpy_struct`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct "bpy.types.bpy_struct"), [`ID`](../I/bpy.types.ID.md#bpy.types.ID "bpy.types.ID")

subclasses — [`BlendTexture`](../B/bpy.types.BlendTexture.md#bpy.types.BlendTexture "bpy.types.BlendTexture"), [`CloudsTexture`](../C/bpy.types.CloudsTexture.md#bpy.types.CloudsTexture "bpy.types.CloudsTexture"), [`DistortedNoiseTexture`](../D/bpy.types.DistortedNoiseTexture.md#bpy.types.DistortedNoiseTexture "bpy.types.DistortedNoiseTexture"), [`ImageTexture`](../I/bpy.types.ImageTexture.md#bpy.types.ImageTexture "bpy.types.ImageTexture"), [`MagicTexture`](../M/bpy.types.MagicTexture.md#bpy.types.MagicTexture "bpy.types.MagicTexture"), [`MarbleTexture`](../M/bpy.types.MarbleTexture.md#bpy.types.MarbleTexture "bpy.types.MarbleTexture"), [`MusgraveTexture`](../M/bpy.types.MusgraveTexture.md#bpy.types.MusgraveTexture "bpy.types.MusgraveTexture"), [`NoiseTexture`](../N/bpy.types.NoiseTexture.md#bpy.types.NoiseTexture "bpy.types.NoiseTexture"), [`StucciTexture`](../S/bpy.types.StucciTexture.md#bpy.types.StucciTexture "bpy.types.StucciTexture"), [`VoronoiTexture`](../V/bpy.types.VoronoiTexture.md#bpy.types.VoronoiTexture "bpy.types.VoronoiTexture"), [`WoodTexture`](../W/bpy.types.WoodTexture.md#bpy.types.WoodTexture "bpy.types.WoodTexture")

_class _bpy.types.Texture(_ID_)
    

Texture data-block used by materials, lights, worlds and brushes

animation_data
    

Animation data for this data-block

Type:
    

[`AnimData`](../A/bpy.types.AnimData.md#bpy.types.AnimData "bpy.types.AnimData"), (readonly)

color_ramp
    

Type:
    

[`ColorRamp`](../C/bpy.types.ColorRamp.md#bpy.types.ColorRamp "bpy.types.ColorRamp"), (readonly)

contrast
    

Adjust the contrast of the texture

Type:
    

float in [0, 5], default 1.0

factor_blue
    

Type:
    

float in [0, 2], default 1.0

factor_green
    

Type:
    

float in [0, 2], default 1.0

factor_red
    

Type:
    

float in [0, 2], default 1.0

intensity
    

Adjust the brightness of the texture

Type:
    

float in [0, 2], default 1.0

node_tree
    

Node tree for node-based textures

Type:
    

[`NodeTree`](../N/bpy.types.NodeTree.md#bpy.types.NodeTree "bpy.types.NodeTree"), (readonly)

saturation
    

Adjust the saturation of colors in the texture

Type:
    

float in [0, 2], default 1.0

type
    

Type:
    

enum in [Texture Type Items](../../bpy_types_enum_items/texture_type_items.md#rna-enum-texture-type-items), default `'IMAGE'`

use_clamp
    

Set negative texture RGB and intensity values to zero, for some uses like displacement this option can be disabled to get the full range

Type:
    

boolean, default False

use_color_ramp
    

Map the texture intensity to the color ramp. Note that the alpha value is used for image textures, enable “Calculate Alpha” for images without an alpha channel.

Type:
    

boolean, default False

use_nodes
    

Make this a node-based texture

Type:
    

boolean, default False

use_preview_alpha
    

Show Alpha in Preview Render

Type:
    

boolean, default False

users_material
    

Materials that use this texture

Type:
    

tuple of [`Material`](../M/bpy.types.Material.md#bpy.types.Material "bpy.types.Material")

Note

Takes `O(len(bpy.data.materials) * len(material.texture_slots))` time.

(readonly)

users_object_modifier
    

Object modifiers that use this texture

Type:
    

tuple of [`Object`](../O/bpy.types.Object.md#bpy.types.Object "bpy.types.Object")

Note

Takes `O(len(bpy.data.objects) * len(obj.modifiers))` time.

(readonly)

evaluate(_value_)
    

Evaluate the texture at the given coordinate and returns the result

Parameters:
    

**value** ([`mathutils.Vector`](mathutils.md#mathutils.Vector "mathutils.Vector") of 3 items in [-inf, inf]) – The coordinates (x,y,z) of the texture, in case of a 3D texture, the z value is the slice of the texture that is evaluated. For 2D textures such as images, the z value is ignored.

Returns:
    

The result of the texture where (x,y,z,w) are (red, green, blue, intensity). For grayscale textures, often intensity only will be used.

Return type:
    

[`mathutils.Vector`](mathutils.md#mathutils.Vector "mathutils.Vector") of 4 items in [-inf, inf]

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
  * [`ID.name`](../I/bpy.types.ID.md#bpy.types.ID.name "bpy.types.ID.name")
  * [`ID.name_full`](../I/bpy.types.ID.md#bpy.types.ID.name_full "bpy.types.ID.name_full")
  * [`ID.id_type`](../I/bpy.types.ID.md#bpy.types.ID.id_type "bpy.types.ID.id_type")
  * [`ID.session_uid`](../I/bpy.types.ID.md#bpy.types.ID.session_uid "bpy.types.ID.session_uid")
  * [`ID.is_evaluated`](../I/bpy.types.ID.md#bpy.types.ID.is_evaluated "bpy.types.ID.is_evaluated")
  * [`ID.original`](../I/bpy.types.ID.md#bpy.types.ID.original "bpy.types.ID.original")
  * [`ID.users`](../I/bpy.types.ID.md#bpy.types.ID.users "bpy.types.ID.users")
  * [`ID.use_fake_user`](../I/bpy.types.ID.md#bpy.types.ID.use_fake_user "bpy.types.ID.use_fake_user")
  * [`ID.use_extra_user`](../I/bpy.types.ID.md#bpy.types.ID.use_extra_user "bpy.types.ID.use_extra_user")
  * [`ID.is_embedded_data`](../I/bpy.types.ID.md#bpy.types.ID.is_embedded_data "bpy.types.ID.is_embedded_data")

| 

  * [`ID.is_linked_packed`](../I/bpy.types.ID.md#bpy.types.ID.is_linked_packed "bpy.types.ID.is_linked_packed")
  * [`ID.is_missing`](../I/bpy.types.ID.md#bpy.types.ID.is_missing "bpy.types.ID.is_missing")
  * [`ID.is_runtime_data`](../I/bpy.types.ID.md#bpy.types.ID.is_runtime_data "bpy.types.ID.is_runtime_data")
  * [`ID.is_editable`](../I/bpy.types.ID.md#bpy.types.ID.is_editable "bpy.types.ID.is_editable")
  * [`ID.tag`](../I/bpy.types.ID.md#bpy.types.ID.tag "bpy.types.ID.tag")
  * [`ID.is_library_indirect`](../I/bpy.types.ID.md#bpy.types.ID.is_library_indirect "bpy.types.ID.is_library_indirect")
  * [`ID.library`](../I/bpy.types.ID.md#bpy.types.ID.library "bpy.types.ID.library")
  * [`ID.library_weak_reference`](../I/bpy.types.ID.md#bpy.types.ID.library_weak_reference "bpy.types.ID.library_weak_reference")
  * [`ID.asset_data`](../I/bpy.types.ID.md#bpy.types.ID.asset_data "bpy.types.ID.asset_data")
  * [`ID.override_library`](../I/bpy.types.ID.md#bpy.types.ID.override_library "bpy.types.ID.override_library")
  * [`ID.preview`](../I/bpy.types.ID.md#bpy.types.ID.preview "bpy.types.ID.preview")

  
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
  * [`bpy_struct.keyframe_insert`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.keyframe_insert "bpy.types.bpy_struct.keyframe_insert")
  * [`bpy_struct.keys`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.keys "bpy.types.bpy_struct.keys")
  * [`bpy_struct.path_from_id`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.path_from_id "bpy.types.bpy_struct.path_from_id")
  * [`bpy_struct.path_from_module`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.path_from_module "bpy.types.bpy_struct.path_from_module")
  * [`bpy_struct.path_resolve`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.path_resolve "bpy.types.bpy_struct.path_resolve")
  * [`bpy_struct.pop`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.pop "bpy.types.bpy_struct.pop")
  * [`bpy_struct.property_overridable_library_set`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.property_overridable_library_set "bpy.types.bpy_struct.property_overridable_library_set")
  * [`bpy_struct.property_unset`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.property_unset "bpy.types.bpy_struct.property_unset")
  * [`bpy_struct.rna_ancestors`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.rna_ancestors "bpy.types.bpy_struct.rna_ancestors")

| 

  * [`bpy_struct.type_recast`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.type_recast "bpy.types.bpy_struct.type_recast")
  * [`bpy_struct.values`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.values "bpy.types.bpy_struct.values")
  * [`ID.bl_system_properties_get`](../I/bpy.types.ID.md#bpy.types.ID.bl_system_properties_get "bpy.types.ID.bl_system_properties_get")
  * [`ID.rename`](../I/bpy.types.ID.md#bpy.types.ID.rename "bpy.types.ID.rename")
  * [`ID.evaluated_get`](../I/bpy.types.ID.md#bpy.types.ID.evaluated_get "bpy.types.ID.evaluated_get")
  * [`ID.copy`](../I/bpy.types.ID.md#bpy.types.ID.copy "bpy.types.ID.copy")
  * [`ID.asset_mark`](../I/bpy.types.ID.md#bpy.types.ID.asset_mark "bpy.types.ID.asset_mark")
  * [`ID.asset_clear`](../I/bpy.types.ID.md#bpy.types.ID.asset_clear "bpy.types.ID.asset_clear")
  * [`ID.asset_generate_preview`](../I/bpy.types.ID.md#bpy.types.ID.asset_generate_preview "bpy.types.ID.asset_generate_preview")
  * [`ID.override_create`](../I/bpy.types.ID.md#bpy.types.ID.override_create "bpy.types.ID.override_create")
  * [`ID.override_hierarchy_create`](../I/bpy.types.ID.md#bpy.types.ID.override_hierarchy_create "bpy.types.ID.override_hierarchy_create")
  * [`ID.user_clear`](../I/bpy.types.ID.md#bpy.types.ID.user_clear "bpy.types.ID.user_clear")
  * [`ID.user_remap`](../I/bpy.types.ID.md#bpy.types.ID.user_remap "bpy.types.ID.user_remap")
  * [`ID.make_local`](../I/bpy.types.ID.md#bpy.types.ID.make_local "bpy.types.ID.make_local")
  * [`ID.user_of_id`](../I/bpy.types.ID.md#bpy.types.ID.user_of_id "bpy.types.ID.user_of_id")
  * [`ID.animation_data_create`](../I/bpy.types.ID.md#bpy.types.ID.animation_data_create "bpy.types.ID.animation_data_create")
  * [`ID.animation_data_clear`](../I/bpy.types.ID.md#bpy.types.ID.animation_data_clear "bpy.types.ID.animation_data_clear")
  * [`ID.update_tag`](../I/bpy.types.ID.md#bpy.types.ID.update_tag "bpy.types.ID.update_tag")
  * [`ID.preview_ensure`](../I/bpy.types.ID.md#bpy.types.ID.preview_ensure "bpy.types.ID.preview_ensure")
  * [`ID.bl_rna_get_subclass`](../I/bpy.types.ID.md#bpy.types.ID.bl_rna_get_subclass "bpy.types.ID.bl_rna_get_subclass")
  * [`ID.bl_rna_get_subclass_py`](../I/bpy.types.ID.md#bpy.types.ID.bl_rna_get_subclass_py "bpy.types.ID.bl_rna_get_subclass_py")

  
---|---  
  
## References

  * [`bpy.context.texture`](../../bpy.context.md#bpy.context.texture "bpy.context.texture")
  * [`BlendData.textures`](../B/bpy.types.BlendData.md#bpy.types.BlendData.textures "bpy.types.BlendData.textures")
  * [`BlendDataTextures.new`](../B/bpy.types.BlendDataTextures.md#bpy.types.BlendDataTextures.new "bpy.types.BlendDataTextures.new")
  * [`BlendDataTextures.remove`](../B/bpy.types.BlendDataTextures.md#bpy.types.BlendDataTextures.remove "bpy.types.BlendDataTextures.remove")
  * [`Brush.mask_texture`](../B/bpy.types.Brush.md#bpy.types.Brush.mask_texture "bpy.types.Brush.mask_texture")
  * [`Brush.texture`](../B/bpy.types.Brush.md#bpy.types.Brush.texture "bpy.types.Brush.texture")
  * [`DisplaceModifier.texture`](../D/bpy.types.DisplaceModifier.md#bpy.types.DisplaceModifier.texture "bpy.types.DisplaceModifier.texture")
  * [`DynamicPaintSurface.init_texture`](../D/bpy.types.DynamicPaintSurface.md#bpy.types.DynamicPaintSurface.init_texture "bpy.types.DynamicPaintSurface.init_texture")
  * [`FieldSettings.texture`](../F/bpy.types.FieldSettings.md#bpy.types.FieldSettings.texture "bpy.types.FieldSettings.texture")
  * [`FluidFlowSettings.noise_texture`](../F/bpy.types.FluidFlowSettings.md#bpy.types.FluidFlowSettings.noise_texture "bpy.types.FluidFlowSettings.noise_texture")
  * [`FreestyleLineStyle.active_texture`](../F/bpy.types.FreestyleLineStyle.md#bpy.types.FreestyleLineStyle.active_texture "bpy.types.FreestyleLineStyle.active_texture")

| 

  * [`NodeSocketTexture.default_value`](../N/bpy.types.NodeSocketTexture.md#bpy.types.NodeSocketTexture.default_value "bpy.types.NodeSocketTexture.default_value")
  * [`NodeTreeInterfaceSocketTexture.default_value`](../N/bpy.types.NodeTreeInterfaceSocketTexture.md#bpy.types.NodeTreeInterfaceSocketTexture.default_value "bpy.types.NodeTreeInterfaceSocketTexture.default_value")
  * [`ParticleSettings.active_texture`](../P/bpy.types.ParticleSettings.md#bpy.types.ParticleSettings.active_texture "bpy.types.ParticleSettings.active_texture")
  * [`TextureNodeTexture.texture`](bpy.types.TextureNodeTexture.md#bpy.types.TextureNodeTexture.texture "bpy.types.TextureNodeTexture.texture")
  * [`TextureSlot.texture`](bpy.types.TextureSlot.md#bpy.types.TextureSlot.texture "bpy.types.TextureSlot.texture")
  * [`VertexWeightEditModifier.mask_texture`](../V/bpy.types.VertexWeightEditModifier.md#bpy.types.VertexWeightEditModifier.mask_texture "bpy.types.VertexWeightEditModifier.mask_texture")
  * [`VertexWeightMixModifier.mask_texture`](../V/bpy.types.VertexWeightMixModifier.md#bpy.types.VertexWeightMixModifier.mask_texture "bpy.types.VertexWeightMixModifier.mask_texture")
  * [`VertexWeightProximityModifier.mask_texture`](../V/bpy.types.VertexWeightProximityModifier.md#bpy.types.VertexWeightProximityModifier.mask_texture "bpy.types.VertexWeightProximityModifier.mask_texture")
  * [`VolumeDisplaceModifier.texture`](../V/bpy.types.VolumeDisplaceModifier.md#bpy.types.VolumeDisplaceModifier.texture "bpy.types.VolumeDisplaceModifier.texture")
  * [`WarpModifier.texture`](../W/bpy.types.WarpModifier.md#bpy.types.WarpModifier.texture "bpy.types.WarpModifier.texture")
  * [`WaveModifier.texture`](../W/bpy.types.WaveModifier.md#bpy.types.WaveModifier.texture "bpy.types.WaveModifier.texture")

  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
