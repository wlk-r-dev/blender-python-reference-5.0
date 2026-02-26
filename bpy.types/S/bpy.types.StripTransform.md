# StripTransform(bpy_struct)

base class — [[bpy_struct]]

_class _bpy.types.StripTransform(_bpy_struct_)
    

Transform parameters for a sequence strip

filter
    

Type of filter to use for image transformation

  * `AUTO` Auto – Automatically choose filter based on scaling factor.

  * `NEAREST` Nearest – Use nearest sample.

  * `BILINEAR` Bilinear – Interpolate between 2×2 samples.

  * `CUBIC_MITCHELL` Cubic Mitchell – Cubic Mitchell filter on 4×4 samples.

  * `CUBIC_BSPLINE` Cubic B-Spline – Cubic B-Spline filter (blurry but no ringing) on 4×4 samples.

  * `BOX` Box – Averages source image samples that fall under destination pixel.


Type:
    

enum in [`'AUTO'`, `'NEAREST'`, `'BILINEAR'`, `'CUBIC_MITCHELL'`, `'CUBIC_BSPLINE'`, `'BOX'`], default `'AUTO'`

offset_x
    

Move along X axis

Type:
    

float in [-inf, inf], default 0.0

offset_y
    

Move along Y axis

Type:
    

float in [-inf, inf], default 0.0

origin
    

Origin of image for transformation

Type:
    

float array of 2 items in [-inf, inf], default (0.0, 0.0)

rotation
    

Rotate around image center

Type:
    

float in [-inf, inf], default 0.0

scale_x
    

Scale along X axis

Type:
    

float in [0, inf], default 1.0

scale_y
    

Scale along Y axis

Type:
    

float in [0, inf], default 1.0

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

  * [[EffectStrip.transform]]
  * [[ImageStrip.transform]]
  * [[MaskStrip.transform]]
  * [[MetaStrip.transform]]

| 

  * [[MovieClipStrip.transform]]
  * [[MovieStrip.transform]]
  * [[SceneStrip.transform]]

  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
