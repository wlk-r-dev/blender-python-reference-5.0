# LineStyleTextureSlot(TextureSlot)

base classes — [`bpy_struct`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct "bpy.types.bpy_struct"), [`TextureSlot`](../T/bpy.types.TextureSlot.md#bpy.types.TextureSlot "bpy.types.TextureSlot")

_class _bpy.types.LineStyleTextureSlot(_TextureSlot_)
    

Texture slot for textures in a LineStyle data-block

alpha_factor
    

Amount texture affects alpha

Type:
    

float in [-inf, inf], default 1.0

diffuse_color_factor
    

Amount texture affects diffuse color

Type:
    

float in [-inf, inf], default 1.0

mapping
    

  * `FLAT` Flat – Map X and Y coordinates directly.

  * `CUBE` Cube – Map using the normal vector.

  * `TUBE` Tube – Map with Z as central axis.

  * `SPHERE` Sphere – Map with Z as central axis.


Type:
    

enum in [`'FLAT'`, `'CUBE'`, `'TUBE'`, `'SPHERE'`], default `'FLAT'`

mapping_x
    

Type:
    

enum in [`'NONE'`, `'X'`, `'Y'`, `'Z'`], default `'X'`

mapping_y
    

Type:
    

enum in [`'NONE'`, `'X'`, `'Y'`, `'Z'`], default `'Y'`

mapping_z
    

Type:
    

enum in [`'NONE'`, `'X'`, `'Y'`, `'Z'`], default `'Z'`

texture_coords
    

Texture coordinates used to map the texture onto the background

  * `WINDOW` Window – Use screen coordinates as texture coordinates.

  * `GLOBAL` Global – Use global coordinates for the texture coordinates.

  * `ALONG_STROKE` Along stroke – Use stroke length for texture coordinates.

  * `ORCO` Generated – Use the original undeformed coordinates of the object.


Type:
    

enum in [`'WINDOW'`, `'GLOBAL'`, `'ALONG_STROKE'`, `'ORCO'`], default `'ALONG_STROKE'`

use_map_alpha
    

The texture affects the alpha value

Type:
    

boolean, default False

use_map_color_diffuse
    

The texture affects basic color of the stroke

Type:
    

boolean, default True

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
  * [`TextureSlot.texture`](../T/bpy.types.TextureSlot.md#bpy.types.TextureSlot.texture "bpy.types.TextureSlot.texture")
  * [`TextureSlot.name`](../T/bpy.types.TextureSlot.md#bpy.types.TextureSlot.name "bpy.types.TextureSlot.name")
  * [`TextureSlot.offset`](../T/bpy.types.TextureSlot.md#bpy.types.TextureSlot.offset "bpy.types.TextureSlot.offset")
  * [`TextureSlot.scale`](../T/bpy.types.TextureSlot.md#bpy.types.TextureSlot.scale "bpy.types.TextureSlot.scale")

| 

  * [`TextureSlot.color`](../T/bpy.types.TextureSlot.md#bpy.types.TextureSlot.color "bpy.types.TextureSlot.color")
  * [`TextureSlot.blend_type`](../T/bpy.types.TextureSlot.md#bpy.types.TextureSlot.blend_type "bpy.types.TextureSlot.blend_type")
  * [`TextureSlot.default_value`](../T/bpy.types.TextureSlot.md#bpy.types.TextureSlot.default_value "bpy.types.TextureSlot.default_value")
  * [`TextureSlot.output_node`](../T/bpy.types.TextureSlot.md#bpy.types.TextureSlot.output_node "bpy.types.TextureSlot.output_node")

  
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
  * [`TextureSlot.bl_rna_get_subclass`](../T/bpy.types.TextureSlot.md#bpy.types.TextureSlot.bl_rna_get_subclass "bpy.types.TextureSlot.bl_rna_get_subclass")
  * [`TextureSlot.bl_rna_get_subclass_py`](../T/bpy.types.TextureSlot.md#bpy.types.TextureSlot.bl_rna_get_subclass_py "bpy.types.TextureSlot.bl_rna_get_subclass_py")

  
---|---  
  
## References

  * [`FreestyleLineStyle.texture_slots`](../F/bpy.types.FreestyleLineStyle.md#bpy.types.FreestyleLineStyle.texture_slots "bpy.types.FreestyleLineStyle.texture_slots")
  * [`LineStyleTextureSlots.add`](bpy.types.LineStyleTextureSlots.md#bpy.types.LineStyleTextureSlots.add "bpy.types.LineStyleTextureSlots.add")

| 

  * [`LineStyleTextureSlots.create`](bpy.types.LineStyleTextureSlots.md#bpy.types.LineStyleTextureSlots.create "bpy.types.LineStyleTextureSlots.create")

  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
