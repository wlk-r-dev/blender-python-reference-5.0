# Texture(ID)

base classes — [[bpy_struct]], [[ID]]

subclasses — [[BlendTexture]], [[CloudsTexture]], [[DistortedNoiseTexture]], [[ImageTexture]], [[MagicTexture]], [[MarbleTexture]], [[MusgraveTexture]], [[NoiseTexture]], [[StucciTexture]], [[VoronoiTexture]], [[WoodTexture]]

_class _bpy.types.Texture(_ID_)
    

Texture data-block used by materials, lights, worlds and brushes

animation_data
    

Animation data for this data-block

Type:
    

[[AnimData]], (readonly)

color_ramp
    

Type:
    

[[ColorRamp]], (readonly)

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
    

[[NodeTree]], (readonly)

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
    

tuple of [[Material]]

Note

Takes `O(len(bpy.data.materials) * len(material.texture_slots))` time.

(readonly)

users_object_modifier
    

Object modifiers that use this texture

Type:
    

tuple of [[Object]]

Note

Takes `O(len(bpy.data.objects) * len(obj.modifiers))` time.

(readonly)

evaluate(_value_)
    

Evaluate the texture at the given coordinate and returns the result

Parameters:
    

**value** ([[mathutils.Vector]] of 3 items in [-inf, inf]) – The coordinates (x,y,z) of the texture, in case of a 3D texture, the z value is the slice of the texture that is evaluated. For 2D textures such as images, the z value is ignored.

Returns:
    

The result of the texture where (x,y,z,w) are (red, green, blue, intensity). For grayscale textures, often intensity only will be used.

Return type:
    

[[mathutils.Vector]] of 4 items in [-inf, inf]

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
  * [[ID.name]]
  * [[ID.name_full]]
  * [[ID.id_type]]
  * [[ID.session_uid]]
  * [[ID.is_evaluated]]
  * [[ID.original]]
  * [[ID.users]]
  * [[ID.use_fake_user]]
  * [[ID.use_extra_user]]
  * [[ID.is_embedded_data]]

| 

  * [[ID.is_linked_packed]]
  * [[ID.is_missing]]
  * [[ID.is_runtime_data]]
  * [[ID.is_editable]]
  * [[ID.tag]]
  * [[ID.is_library_indirect]]
  * [[ID.library]]
  * [[ID.library_weak_reference]]
  * [[ID.asset_data]]
  * [[ID.override_library]]
  * [[ID.preview]]

  
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
  * [[bpy_struct.keyframe_insert]]
  * [[bpy_struct.keys]]
  * [[bpy_struct.path_from_id]]
  * [[bpy_struct.path_from_module]]
  * [[bpy_struct.path_resolve]]
  * [[bpy_struct.pop]]
  * [[bpy_struct.property_overridable_library_set]]
  * [[bpy_struct.property_unset]]
  * [[bpy_struct.rna_ancestors]]

| 

  * [[bpy_struct.type_recast]]
  * [[bpy_struct.values]]
  * [[ID.bl_system_properties_get]]
  * [[ID.rename]]
  * [[ID.evaluated_get]]
  * [[ID.copy]]
  * [[ID.asset_mark]]
  * [[ID.asset_clear]]
  * [[ID.asset_generate_preview]]
  * [[ID.override_create]]
  * [[ID.override_hierarchy_create]]
  * [[ID.user_clear]]
  * [[ID.user_remap]]
  * [[ID.make_local]]
  * [[ID.user_of_id]]
  * [[ID.animation_data_create]]
  * [[ID.animation_data_clear]]
  * [[ID.update_tag]]
  * [[ID.preview_ensure]]
  * [[ID.bl_rna_get_subclass]]
  * [[ID.bl_rna_get_subclass_py]]

  
---|---  
  
## References

  * [[bpy.context.texture]]
  * [[BlendData.textures]]
  * [[BlendDataTextures.new]]
  * [[BlendDataTextures.remove]]
  * [[Brush.mask_texture]]
  * [[Brush.texture]]
  * [[DisplaceModifier.texture]]
  * [[DynamicPaintSurface.init_texture]]
  * [[FieldSettings.texture]]
  * [[FluidFlowSettings.noise_texture]]
  * [[FreestyleLineStyle.active_texture]]

| 

  * [[NodeSocketTexture.default_value]]
  * [[NodeTreeInterfaceSocketTexture.default_value]]
  * [[ParticleSettings.active_texture]]
  * [[TextureNodeTexture.texture]]
  * [[TextureSlot.texture]]
  * [[VertexWeightEditModifier.mask_texture]]
  * [[VertexWeightMixModifier.mask_texture]]
  * [[VertexWeightProximityModifier.mask_texture]]
  * [[VolumeDisplaceModifier.texture]]
  * [[WarpModifier.texture]]
  * [[WaveModifier.texture]]

  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
