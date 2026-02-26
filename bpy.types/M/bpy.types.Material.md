# Material(ID)

base classes — [`bpy_struct`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct "bpy.types.bpy_struct"), [`ID`](../I/bpy.types.ID.md#bpy.types.ID "bpy.types.ID")

_class _bpy.types.Material(_ID_)
    

Material data-block to define the appearance of geometric objects for rendering

alpha_threshold
    

A pixel is rendered only if its alpha value is above this threshold

Type:
    

float in [0, 1], default 0.5

animation_data
    

Animation data for this data-block

Type:
    

[`AnimData`](../A/bpy.types.AnimData.md#bpy.types.AnimData "bpy.types.AnimData"), (readonly)

blend_method
    

Blend Mode for Transparent Faces (Deprecated: use ‘surface_render_method’)

  * `OPAQUE` Opaque – Render surface without transparency.

  * `CLIP` Alpha Clip – Use the alpha threshold to clip the visibility (binary visibility).

  * `HASHED` Alpha Hashed – Use noise to dither the binary visibility (works well with multi-samples).

  * `BLEND` Alpha Blend – Render polygon transparent, depending on alpha channel of the texture.


Type:
    

enum in [`'OPAQUE'`, `'CLIP'`, `'HASHED'`, `'BLEND'`], default `'OPAQUE'`

cycles
    

Cycles material settings

Type:
    

`CyclesMaterialSettings`, (readonly)

diffuse_color
    

Diffuse color of the material

Type:
    

float array of 4 items in [0, inf], default (0.8, 0.8, 0.8, 1.0)

displacement_method
    

Method to use for the displacement

  * `BUMP` Bump Only – Bump mapping to simulate the appearance of displacement.

  * `DISPLACEMENT` Displacement Only – Use true displacement of surface only, requires fine subdivision.

  * `BOTH` Displacement and Bump – Combination of true displacement and bump mapping for finer detail.


Type:
    

enum in [`'BUMP'`, `'DISPLACEMENT'`, `'BOTH'`], default `'BUMP'`

grease_pencil
    

Grease Pencil color settings for material

Type:
    

[`MaterialGPencilStyle`](bpy.types.MaterialGPencilStyle.md#bpy.types.MaterialGPencilStyle "bpy.types.MaterialGPencilStyle"), (readonly)

is_grease_pencil
    

True if this material has Grease Pencil data

Type:
    

boolean, default False, (readonly)

line_color
    

Line color used for Freestyle line rendering

Type:
    

float array of 4 items in [0, inf], default (0.0, 0.0, 0.0, 0.0)

line_priority
    

The line color of a higher priority is used at material boundaries

Type:
    

int in [0, 32767], default 0

lineart
    

Line Art settings for material

Type:
    

[`MaterialLineArt`](bpy.types.MaterialLineArt.md#bpy.types.MaterialLineArt "bpy.types.MaterialLineArt"), (readonly)

max_vertex_displacement
    

The max distance a vertex can be displaced. Displacements over this threshold may cause visibility issues.

Type:
    

float in [0, inf], default 0.0

metallic
    

Amount of mirror reflection for raytrace

Type:
    

float in [0, 1], default 0.0

node_tree
    

Node tree for node based materials

Type:
    

[`NodeTree`](../N/bpy.types.NodeTree.md#bpy.types.NodeTree "bpy.types.NodeTree"), (readonly)

paint_active_slot
    

Index of active texture paint slot

Type:
    

int in [0, 32767], default 0

paint_clone_slot
    

Index of clone texture paint slot

Type:
    

int in [0, 32767], default 0

pass_index
    

Index number for the “Material Index” render pass

Type:
    

int in [0, 32767], default 0

preview_render_type
    

Type of preview render

  * `FLAT` Flat – Flat XY plane.

  * `SPHERE` Sphere – Sphere.

  * `CUBE` Cube – Cube.

  * `HAIR` Hair – Hair strands.

  * `SHADERBALL` Shader Ball – Shader ball.

  * `CLOTH` Cloth – Cloth.

  * `FLUID` Fluid – Fluid.


Type:
    

enum in [`'FLAT'`, `'SPHERE'`, `'CUBE'`, `'HAIR'`, `'SHADERBALL'`, `'CLOTH'`, `'FLUID'`], default `'SPHERE'`

refraction_depth
    

Approximate the thickness of the object to compute two refraction events (0 is disabled) (Deprecated)

Type:
    

float in [0, inf], default 0.0

roughness
    

Roughness of the material

Type:
    

float in [0, 1], default 0.4

show_transparent_back
    

Render multiple transparent layers (may introduce transparency sorting problems) (Deprecated: use ‘use_tranparency_overlap’)

Type:
    

boolean, default True

specular_color
    

Specular color of the material

Type:
    

[`mathutils.Color`](mathutils.md#mathutils.Color "mathutils.Color") of 3 items in [0, inf], default (1.0, 1.0, 1.0)

specular_intensity
    

How intense (bright) the specular reflection is

Type:
    

float in [0, 1], default 0.5

surface_render_method
    

Controls the blending and the compatibility with certain features

  * `DITHERED` Dithered – Allows for grayscale hashed transparency, and compatible with render passes and raytracing. Also known as deferred rendering..

  * `BLENDED` Blended – Allows for colored transparency, but incompatible with render passes and raytracing. Also known as forward rendering..


Type:
    

enum in [`'DITHERED'`, `'BLENDED'`], default `'DITHERED'`

texture_paint_images
    

Texture images used for texture painting

Type:
    

[`bpy_prop_collection`](../_other/bpy.types.bpy_prop_collection.md#bpy.types.bpy_prop_collection "bpy.types.bpy_prop_collection") of [`Image`](../I/bpy.types.Image.md#bpy.types.Image "bpy.types.Image"), (readonly)

texture_paint_slots
    

Texture slots defining the mapping and influence of textures

Type:
    

[`bpy_prop_collection`](../_other/bpy.types.bpy_prop_collection.md#bpy.types.bpy_prop_collection "bpy.types.bpy_prop_collection") of [`TexPaintSlot`](../T/bpy.types.TexPaintSlot.md#bpy.types.TexPaintSlot "bpy.types.TexPaintSlot"), (readonly)

thickness_mode
    

Approximation used to model the light interactions inside the object

  * `SPHERE` Sphere – Approximate the object as a sphere whose diameter is equal to the thickness defined by the node tree.

  * `SLAB` Slab – Approximate the object as an infinite slab of thickness defined by the node tree.


Type:
    

enum in [`'SPHERE'`, `'SLAB'`], default `'SPHERE'`

use_backface_culling
    

Use back face culling to hide the back side of faces

Type:
    

boolean, default False

use_backface_culling_lightprobe_volume
    

Consider material single sided for light probe volume capture. Additionally helps rejecting probes inside the object to avoid light leaks.

Type:
    

boolean, default True

use_backface_culling_shadow
    

Use back face culling when casting shadows

Type:
    

boolean, default False

use_nodes
    

Use shader nodes to render the material

Deprecated since version 5.0: removal planned in version 6.0

Unused but kept for compatibility reasons. Setting the property has no effect, and getting it always returns True.

Type:
    

boolean, default False

use_preview_world
    

Use the current world background to light the preview render

Type:
    

boolean, default False

use_raytrace_refraction
    

Use raytracing to determine transmitted color instead of using only light probes. This prevents the surface from contributing to the lighting of surfaces not using this setting.

Type:
    

boolean, default False

use_screen_refraction
    

Use raytracing to determine transmitted color instead of using only light probes. This prevents the surface from contributing to the lighting of surfaces not using this setting. Deprecated: use ‘use_raytrace_refraction’.

Type:
    

boolean, default False

use_sss_translucency
    

Add translucency effect to subsurface (Deprecated)

Type:
    

boolean, default False

use_thickness_from_shadow
    

Use the shadow maps from shadow casting lights to refine the thickness defined by the material node tree

Type:
    

boolean, default False

use_transparency_overlap
    

Render multiple transparent layers (may introduce transparency sorting problems)

Type:
    

boolean, default True

use_transparent_shadow
    

Use transparent shadows for this material if it contains a Transparent BSDF, disabling will render faster but not give accurate shadows

Type:
    

boolean, default True

volume_intersection_method
    

Determines which inner part of the mesh will produce volumetric effect

  * `FAST` Fast – Each face is considered as a medium interface. Gives correct results for manifold geometry that contains no inner parts..

  * `ACCURATE` Accurate – Faces are considered as medium interface only when they have different consecutive facing. Gives correct results as long as the max ray depth is not exceeded. Have significant memory overhead compared to the fast method..


Type:
    

enum in [`'FAST'`, `'ACCURATE'`], default `'FAST'`

inline_shader_nodes()
    

Get the inlined shader nodes of this material. This preprocesses the node tree to remove nested groups, repeat zones and more.

Returns:
    

The inlined shader nodes.

Return type:
    

[`bpy.types.InlineShaderNodes`](../I/bpy.types.InlineShaderNodes.md#bpy.types.InlineShaderNodes "bpy.types.InlineShaderNodes")

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

  * [`bpy.context.material`](../../bpy.context.md#bpy.context.material "bpy.context.material")
  * [`BlendData.materials`](../B/bpy.types.BlendData.md#bpy.types.BlendData.materials "bpy.types.BlendData.materials")
  * [`BlendDataMaterials.create_gpencil_data`](../B/bpy.types.BlendDataMaterials.md#bpy.types.BlendDataMaterials.create_gpencil_data "bpy.types.BlendDataMaterials.create_gpencil_data")
  * [`BlendDataMaterials.new`](../B/bpy.types.BlendDataMaterials.md#bpy.types.BlendDataMaterials.new "bpy.types.BlendDataMaterials.new")
  * [`BlendDataMaterials.remove`](../B/bpy.types.BlendDataMaterials.md#bpy.types.BlendDataMaterials.remove "bpy.types.BlendDataMaterials.remove")
  * [`BlendDataMaterials.remove_gpencil_data`](../B/bpy.types.BlendDataMaterials.md#bpy.types.BlendDataMaterials.remove_gpencil_data "bpy.types.BlendDataMaterials.remove_gpencil_data")
  * [`BrushGpencilSettings.material`](../B/bpy.types.BrushGpencilSettings.md#bpy.types.BrushGpencilSettings.material "bpy.types.BrushGpencilSettings.material")
  * [`BrushGpencilSettings.material_alt`](../B/bpy.types.BrushGpencilSettings.md#bpy.types.BrushGpencilSettings.material_alt "bpy.types.BrushGpencilSettings.material_alt")
  * [`Curve.materials`](../C/bpy.types.Curve.md#bpy.types.Curve.materials "bpy.types.Curve.materials")
  * [`Curves.materials`](../C/bpy.types.Curves.md#bpy.types.Curves.materials "bpy.types.Curves.materials")
  * [`GeometryNodeInputMaterial.material`](../G/bpy.types.GeometryNodeInputMaterial.md#bpy.types.GeometryNodeInputMaterial.material "bpy.types.GeometryNodeInputMaterial.material")
  * [`GreasePencil.materials`](../G/bpy.types.GreasePencil.md#bpy.types.GreasePencil.materials "bpy.types.GreasePencil.materials")
  * [`GreasePencilArrayModifier.material_filter`](../G/bpy.types.GreasePencilArrayModifier.md#bpy.types.GreasePencilArrayModifier.material_filter "bpy.types.GreasePencilArrayModifier.material_filter")
  * [`GreasePencilBuildModifier.material_filter`](../G/bpy.types.GreasePencilBuildModifier.md#bpy.types.GreasePencilBuildModifier.material_filter "bpy.types.GreasePencilBuildModifier.material_filter")
  * [`GreasePencilColorModifier.material_filter`](../G/bpy.types.GreasePencilColorModifier.md#bpy.types.GreasePencilColorModifier.material_filter "bpy.types.GreasePencilColorModifier.material_filter")
  * [`GreasePencilDashModifierData.material_filter`](../G/bpy.types.GreasePencilDashModifierData.md#bpy.types.GreasePencilDashModifierData.material_filter "bpy.types.GreasePencilDashModifierData.material_filter")
  * [`GreasePencilEnvelopeModifier.material_filter`](../G/bpy.types.GreasePencilEnvelopeModifier.md#bpy.types.GreasePencilEnvelopeModifier.material_filter "bpy.types.GreasePencilEnvelopeModifier.material_filter")
  * [`GreasePencilHookModifier.material_filter`](../G/bpy.types.GreasePencilHookModifier.md#bpy.types.GreasePencilHookModifier.material_filter "bpy.types.GreasePencilHookModifier.material_filter")
  * [`GreasePencilLatticeModifier.material_filter`](../G/bpy.types.GreasePencilLatticeModifier.md#bpy.types.GreasePencilLatticeModifier.material_filter "bpy.types.GreasePencilLatticeModifier.material_filter")
  * [`GreasePencilLengthModifier.material_filter`](../G/bpy.types.GreasePencilLengthModifier.md#bpy.types.GreasePencilLengthModifier.material_filter "bpy.types.GreasePencilLengthModifier.material_filter")
  * [`GreasePencilLineartModifier.target_material`](../G/bpy.types.GreasePencilLineartModifier.md#bpy.types.GreasePencilLineartModifier.target_material "bpy.types.GreasePencilLineartModifier.target_material")
  * [`GreasePencilMirrorModifier.material_filter`](../G/bpy.types.GreasePencilMirrorModifier.md#bpy.types.GreasePencilMirrorModifier.material_filter "bpy.types.GreasePencilMirrorModifier.material_filter")
  * [`GreasePencilMultiplyModifier.material_filter`](../G/bpy.types.GreasePencilMultiplyModifier.md#bpy.types.GreasePencilMultiplyModifier.material_filter "bpy.types.GreasePencilMultiplyModifier.material_filter")
  * [`GreasePencilNoiseModifier.material_filter`](../G/bpy.types.GreasePencilNoiseModifier.md#bpy.types.GreasePencilNoiseModifier.material_filter "bpy.types.GreasePencilNoiseModifier.material_filter")

| 

  * [`GreasePencilOffsetModifier.material_filter`](../G/bpy.types.GreasePencilOffsetModifier.md#bpy.types.GreasePencilOffsetModifier.material_filter "bpy.types.GreasePencilOffsetModifier.material_filter")
  * [`GreasePencilOpacityModifier.material_filter`](../G/bpy.types.GreasePencilOpacityModifier.md#bpy.types.GreasePencilOpacityModifier.material_filter "bpy.types.GreasePencilOpacityModifier.material_filter")
  * [`GreasePencilOutlineModifier.material_filter`](../G/bpy.types.GreasePencilOutlineModifier.md#bpy.types.GreasePencilOutlineModifier.material_filter "bpy.types.GreasePencilOutlineModifier.material_filter")
  * [`GreasePencilOutlineModifier.outline_material`](../G/bpy.types.GreasePencilOutlineModifier.md#bpy.types.GreasePencilOutlineModifier.outline_material "bpy.types.GreasePencilOutlineModifier.outline_material")
  * [`GreasePencilShrinkwrapModifier.material_filter`](../G/bpy.types.GreasePencilShrinkwrapModifier.md#bpy.types.GreasePencilShrinkwrapModifier.material_filter "bpy.types.GreasePencilShrinkwrapModifier.material_filter")
  * [`GreasePencilSimplifyModifier.material_filter`](../G/bpy.types.GreasePencilSimplifyModifier.md#bpy.types.GreasePencilSimplifyModifier.material_filter "bpy.types.GreasePencilSimplifyModifier.material_filter")
  * [`GreasePencilSmoothModifier.material_filter`](../G/bpy.types.GreasePencilSmoothModifier.md#bpy.types.GreasePencilSmoothModifier.material_filter "bpy.types.GreasePencilSmoothModifier.material_filter")
  * [`GreasePencilSubdivModifier.material_filter`](../G/bpy.types.GreasePencilSubdivModifier.md#bpy.types.GreasePencilSubdivModifier.material_filter "bpy.types.GreasePencilSubdivModifier.material_filter")
  * [`GreasePencilTextureModifier.material_filter`](../G/bpy.types.GreasePencilTextureModifier.md#bpy.types.GreasePencilTextureModifier.material_filter "bpy.types.GreasePencilTextureModifier.material_filter")
  * [`GreasePencilThickModifierData.material_filter`](../G/bpy.types.GreasePencilThickModifierData.md#bpy.types.GreasePencilThickModifierData.material_filter "bpy.types.GreasePencilThickModifierData.material_filter")
  * [`GreasePencilTintModifier.material_filter`](../G/bpy.types.GreasePencilTintModifier.md#bpy.types.GreasePencilTintModifier.material_filter "bpy.types.GreasePencilTintModifier.material_filter")
  * [`GreasePencilWeightAngleModifier.material_filter`](../G/bpy.types.GreasePencilWeightAngleModifier.md#bpy.types.GreasePencilWeightAngleModifier.material_filter "bpy.types.GreasePencilWeightAngleModifier.material_filter")
  * [`GreasePencilWeightProximityModifier.material_filter`](../G/bpy.types.GreasePencilWeightProximityModifier.md#bpy.types.GreasePencilWeightProximityModifier.material_filter "bpy.types.GreasePencilWeightProximityModifier.material_filter")
  * [`IDMaterials.append`](../I/bpy.types.IDMaterials.md#bpy.types.IDMaterials.append "bpy.types.IDMaterials.append")
  * [`IDMaterials.pop`](../I/bpy.types.IDMaterials.md#bpy.types.IDMaterials.pop "bpy.types.IDMaterials.pop")
  * [`MaterialSlot.material`](bpy.types.MaterialSlot.md#bpy.types.MaterialSlot.material "bpy.types.MaterialSlot.material")
  * [`Mesh.materials`](bpy.types.Mesh.md#bpy.types.Mesh.materials "bpy.types.Mesh.materials")
  * [`MetaBall.materials`](bpy.types.MetaBall.md#bpy.types.MetaBall.materials "bpy.types.MetaBall.materials")
  * [`NodeSocketMaterial.default_value`](../N/bpy.types.NodeSocketMaterial.md#bpy.types.NodeSocketMaterial.default_value "bpy.types.NodeSocketMaterial.default_value")
  * [`NodeTreeInterfaceSocketMaterial.default_value`](../N/bpy.types.NodeTreeInterfaceSocketMaterial.md#bpy.types.NodeTreeInterfaceSocketMaterial.default_value "bpy.types.NodeTreeInterfaceSocketMaterial.default_value")
  * [`Object.active_material`](../O/bpy.types.Object.md#bpy.types.Object.active_material "bpy.types.Object.active_material")
  * [`PointCloud.materials`](../P/bpy.types.PointCloud.md#bpy.types.PointCloud.materials "bpy.types.PointCloud.materials")
  * [`ViewLayer.material_override`](../V/bpy.types.ViewLayer.md#bpy.types.ViewLayer.material_override "bpy.types.ViewLayer.material_override")
  * [`Volume.materials`](../V/bpy.types.Volume.md#bpy.types.Volume.materials "bpy.types.Volume.materials")

  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
