# ImageUser(bpy_struct)

base class — [`bpy_struct`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct "bpy.types.bpy_struct")

_class _bpy.types.ImageUser(_bpy_struct_)
    

Parameters defining how an Image data-block is used by another data-block

frame_current
    

Current frame number in image sequence or movie

Type:
    

int in [-1048574, 1048574], default 0

frame_duration
    

Number of images of a movie to use

Type:
    

int in [0, 1048574], default 0

frame_offset
    

Offset the number of the frame to use in the animation

Type:
    

int in [-inf, inf], default 0

frame_start
    

Global starting frame of the movie/sequence, assuming first picture has a #1

Type:
    

int in [-1048574, 1048574], default 0

multilayer_layer
    

Layer in multilayer image

Type:
    

int in [0, 32767], default 0, (readonly)

multilayer_pass
    

Pass in multilayer image

Type:
    

int in [0, 32767], default 0, (readonly)

multilayer_view
    

View in multilayer image

Type:
    

int in [0, 32767], default 0, (readonly)

tile
    

Tile in tiled image

Type:
    

int in [0, inf], default 0

use_auto_refresh
    

Always refresh image on frame changes

Type:
    

boolean, default False

use_cyclic
    

Cycle the images in the movie

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

  * [`CameraBackgroundImage.image_user`](../C/bpy.types.CameraBackgroundImage.md#bpy.types.CameraBackgroundImage.image_user "bpy.types.CameraBackgroundImage.image_user")
  * [`Image.filepath_from_user`](bpy.types.Image.md#bpy.types.Image.filepath_from_user "bpy.types.Image.filepath_from_user")
  * [`ImageTexture.image_user`](bpy.types.ImageTexture.md#bpy.types.ImageTexture.image_user "bpy.types.ImageTexture.image_user")
  * [`Object.image_user`](../O/bpy.types.Object.md#bpy.types.Object.image_user "bpy.types.Object.image_user")
  * [`RenderSlot.clear`](../R/bpy.types.RenderSlot.md#bpy.types.RenderSlot.clear "bpy.types.RenderSlot.clear")
  * [`ShaderNodeTexEnvironment.image_user`](../S/bpy.types.ShaderNodeTexEnvironment.md#bpy.types.ShaderNodeTexEnvironment.image_user "bpy.types.ShaderNodeTexEnvironment.image_user")

| 

  * [`ShaderNodeTexImage.image_user`](../S/bpy.types.ShaderNodeTexImage.md#bpy.types.ShaderNodeTexImage.image_user "bpy.types.ShaderNodeTexImage.image_user")
  * [`SpaceImageEditor.image_user`](../S/bpy.types.SpaceImageEditor.md#bpy.types.SpaceImageEditor.image_user "bpy.types.SpaceImageEditor.image_user")
  * [`TextureNodeImage.image_user`](../T/bpy.types.TextureNodeImage.md#bpy.types.TextureNodeImage.image_user "bpy.types.TextureNodeImage.image_user")
  * [`UILayout.template_image`](../U/bpy.types.UILayout.md#bpy.types.UILayout.template_image "bpy.types.UILayout.template_image")
  * [`UILayout.template_image_layers`](../U/bpy.types.UILayout.md#bpy.types.UILayout.template_image_layers "bpy.types.UILayout.template_image_layers")

  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
