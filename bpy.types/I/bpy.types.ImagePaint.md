# ImagePaint(Paint)

base classes — [[bpy_struct]], [[Paint]]

_class _bpy.types.ImagePaint(_Paint_)
    

Properties of image and texture painting mode

canvas
    

Image used as canvas

Type:
    

[[Image]]

clone_alpha
    

Opacity of clone image display

Type:
    

float in [0, 1], default 0.5

clone_image
    

Image used as clone source

Type:
    

[[Image]]

clone_offset
    

Type:
    

[[mathutils.Vector]] of 2 items in [-inf, inf], default (0.0, 0.0)

dither
    

Amount of dithering when painting on byte images

Type:
    

float in [0, 2], default 0.0

interpolation
    

Texture filtering type

  * `LINEAR` Linear – Linear interpolation.

  * `CLOSEST` Closest – No interpolation (sample closest texel).


Type:
    

enum in [`'LINEAR'`, `'CLOSEST'`], default `'LINEAR'`

invert_stencil
    

Invert the stencil layer

Type:
    

boolean, default False

missing_materials
    

The mesh is missing materials

Type:
    

boolean, default False, (readonly)

missing_stencil
    

Image Painting does not have a stencil

Type:
    

boolean, default False, (readonly)

missing_texture
    

Image Painting does not have a texture to paint on

Type:
    

boolean, default False, (readonly)

missing_uvs
    

A UV layer is missing on the mesh

Type:
    

boolean, default False, (readonly)

mode
    

Mode of operation for projection painting

  * `MATERIAL` Material – Detect image slots from the material.

  * `IMAGE` Single Image – Set image for texture painting directly.


Type:
    

enum in [`'MATERIAL'`, `'IMAGE'`], default `'MATERIAL'`

normal_angle
    

Paint most on faces pointing towards the view according to this angle

Type:
    

int in [0, 90], default 80

screen_grab_size
    

Size to capture the image for re-projecting

Type:
    

int array of 2 items in [512, 16384], default (0, 0)

seam_bleed
    

Extend paint beyond the faces’ UVs to reduce seams (in pixels, slower)

Type:
    

int in [-32768, 32767], default 2

stencil_color
    

Stencil color in the viewport

Type:
    

[[mathutils.Color]] of 3 items in [0, 1], default (0.0, 0.0, 0.0)

stencil_image
    

Image used as stencil

Type:
    

[[Image]]

use_backface_culling
    

Ignore faces pointing away from the view (faster)

Type:
    

boolean, default True

use_clone_layer
    

Use another UV map as clone source, otherwise use the 3D cursor as the source

Type:
    

boolean, default False

use_normal_falloff
    

Paint most on faces pointing towards the view

Type:
    

boolean, default True

use_occlude
    

Only paint onto the faces directly under the brush (slower)

Type:
    

boolean, default True

use_stencil_layer
    

Set the mask layer from the UV map buttons

Type:
    

boolean, default False

detect_data()
    

Check if required texpaint data exist

Return type:
    

boolean

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
  * [[Paint.brush]]
  * [[Paint.brush_asset_reference]]
  * [[Paint.eraser_brush]]
  * [[Paint.eraser_brush_asset_reference]]
  * [[Paint.palette]]
  * [[Paint.show_brush]]
  * [[Paint.show_brush_on_surface]]
  * [[Paint.show_low_resolution]]
  * [[Paint.use_sculpt_delay_updates]]
  * [[Paint.use_symmetry_x]]
  * [[Paint.use_symmetry_y]]

| 

  * [[Paint.use_symmetry_z]]
  * [[Paint.use_symmetry_feather]]
  * [[Paint.cavity_curve]]
  * [[Paint.use_cavity]]
  * [[Paint.tile_offset]]
  * [[Paint.tile_x]]
  * [[Paint.tile_y]]
  * [[Paint.tile_z]]
  * [[Paint.show_strength_curve]]
  * [[Paint.show_size_curve]]
  * [[Paint.show_jitter_curve]]
  * [[Paint.unified_paint_settings]]

  
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

| 

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
  * [[Paint.bl_rna_get_subclass]]
  * [[Paint.bl_rna_get_subclass_py]]

  
---|---  
  
## References

  * [[ToolSettings.image_paint]]

| 


  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
