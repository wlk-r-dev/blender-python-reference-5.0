# Scopes(bpy_struct)

base class — [[bpy_struct]]

_class _bpy.types.Scopes(_bpy_struct_)
    

Scopes for statistical view of an image

accuracy
    

Proportion of original image source pixel lines to sample

Type:
    

float in [0, 100], default 0.0

histogram
    

Histogram for viewing image statistics

Type:
    

[[Histogram]], (readonly)

use_full_resolution
    

Sample every pixel of the image

Type:
    

boolean, default False

vectorscope_alpha
    

Opacity of the points

Type:
    

float in [0, 1], default 0.0

vectorscope_mode
    

Type:
    

enum in [`'LUMA'`, `'RGB'`], default `'RGB'`

waveform_alpha
    

Opacity of the points

Type:
    

float in [0, 1], default 0.0

waveform_mode
    

Type:
    

enum in [`'LUMA'`, `'PARADE'`, `'YCBCR601'`, `'YCBCR709'`, `'YCBCRJPG'`, `'RGB'`], default `'LUMA'`

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

  * [[SpaceImageEditor.scopes]]

| 


  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
