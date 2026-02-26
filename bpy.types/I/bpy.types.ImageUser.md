# ImageUser(bpy_struct)

base class — [[bpy_struct]]

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

  * [[CameraBackgroundImage.image_user]]
  * [[Image.filepath_from_user]]
  * [[ImageTexture.image_user]]
  * [[Object.image_user]]
  * [[RenderSlot.clear]]
  * [[ShaderNodeTexEnvironment.image_user]]

| 

  * [[ShaderNodeTexImage.image_user]]
  * [[SpaceImageEditor.image_user]]
  * [[TextureNodeImage.image_user]]
  * [[UILayout.template_image]]
  * [[UILayout.template_image_layers]]

  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
