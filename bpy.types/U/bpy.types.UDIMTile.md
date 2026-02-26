# UDIMTile(bpy_struct)

base class — [[bpy_struct]]

_class _bpy.types.UDIMTile(_bpy_struct_)
    

Properties of the UDIM tile

channels
    

Number of channels in the tile pixels buffer

Type:
    

int in [0, inf], default 0, (readonly)

generated_color
    

Fill color for the generated image

Type:
    

float array of 4 items in [0, inf], default (0.0, 0.0, 0.0, 0.0)

generated_height
    

Generated image height

Type:
    

int in [1, 65536], default 0

generated_type
    

Generated image type

Type:
    

enum in [Image Generated Type Items](../../bpy_types_enum_items/image_generated_type_items.md#rna-enum-image-generated-type-items), default `'BLANK'`

generated_width
    

Generated image width

Type:
    

int in [1, 65536], default 0

is_generated_tile
    

Is this image tile generated

Type:
    

boolean, default False, (readonly)

label
    

Tile label

Type:
    

string, default “”, (never None)

number
    

Number of the position that this tile covers

Type:
    

int in [-inf, inf], default 0

size
    

Width and height of the tile buffer in pixels, zero when image data cannot be loaded

Type:
    

int array of 2 items in [-inf, inf], default (0, 0), (readonly)

use_generated_float
    

Generate floating-point buffer

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

  * [[Image.tiles]]
  * [[UDIMTiles.active]]
  * [[UDIMTiles.get]]

| 

  * [[UDIMTiles.new]]
  * [[UDIMTiles.remove]]

  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
