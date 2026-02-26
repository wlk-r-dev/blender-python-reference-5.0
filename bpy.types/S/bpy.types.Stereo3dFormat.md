# Stereo3dFormat(bpy_struct)

base class — [[bpy_struct]]

_class _bpy.types.Stereo3dFormat(_bpy_struct_)
    

Settings for stereo output

anaglyph_type
    

Type:
    

enum in [Stereo3D Anaglyph Type Items](../../bpy_types_enum_items/stereo3d_anaglyph_type_items.md#rna-enum-stereo3d-anaglyph-type-items), default `'RED_CYAN'`

display_mode
    

  * `ANAGLYPH` Anaglyph – Render views for left and right eyes as two differently filtered colors in a single image (anaglyph glasses are required).

  * `INTERLACE` Interlace – Render views for left and right eyes interlaced in a single image (3D-ready monitor is required).

  * `SIDEBYSIDE` Side-by-Side – Render views for left and right eyes side-by-side.

  * `TOPBOTTOM` Top-Bottom – Render views for left and right eyes one above another.


Type:
    

enum in [`'ANAGLYPH'`, `'INTERLACE'`, `'SIDEBYSIDE'`, `'TOPBOTTOM'`], default `'ANAGLYPH'`

interlace_type
    

Type:
    

enum in [Stereo3D Interlace Type Items](../../bpy_types_enum_items/stereo3d_interlace_type_items.md#rna-enum-stereo3d-interlace-type-items), default `'ROW_INTERLEAVED'`

use_interlace_swap
    

Swap left and right stereo channels

Type:
    

boolean, default False

use_sidebyside_crosseyed
    

Right eye should see left image and vice versa

Type:
    

boolean, default False

use_squeezed_frame
    

Combine both views in a squeezed image

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

  * [[Image.stereo_3d_format]]
  * [[ImageStrip.stereo_3d_format]]
  * [[MovieStrip.stereo_3d_format]]

| 

  * [[ImageFormatSettings.stereo_3d_format]]
  * [[UILayout.template_image_stereo_3d]]

  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
