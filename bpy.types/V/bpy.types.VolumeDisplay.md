# VolumeDisplay(bpy_struct)

base class — [[bpy_struct]]

_class _bpy.types.VolumeDisplay(_bpy_struct_)
    

Volume object display settings for 3D viewport

density
    

Thickness of volume display in the viewport

Type:
    

float in [1e-05, inf], default 0.0

interpolation_method
    

Interpolation method to use for volumes in solid mode

  * `LINEAR` Linear – Good smoothness and speed.

  * `CUBIC` Cubic – Smoothed high quality interpolation, but slower.

  * `CLOSEST` Closest – No interpolation.


Type:
    

enum in [`'LINEAR'`, `'CUBIC'`, `'CLOSEST'`], default `'LINEAR'`

slice_axis
    

  * `AUTO` Auto – Adjust slice direction according to the view direction.

  * `X` X – Slice along the X axis.

  * `Y` Y – Slice along the Y axis.

  * `Z` Z – Slice along the Z axis.


Type:
    

enum in [`'AUTO'`, `'X'`, `'Y'`, `'Z'`], default `'AUTO'`

slice_depth
    

Position of the slice

Type:
    

float in [0, 1], default 0.0

use_slice
    

Perform a single slice of the domain object

Type:
    

boolean, default False

wireframe_detail
    

Amount of detail for wireframe display

  * `COARSE` Coarse – Display one box or point for each intermediate tree node.

  * `FINE` Fine – Display box for each leaf node containing 8×8 voxels.


Type:
    

enum in [`'COARSE'`, `'FINE'`], default `'COARSE'`

wireframe_type
    

Type of wireframe display

  * `NONE` None – Don’t display volume in wireframe mode.

  * `BOUNDS` Bounds – Display single bounding box for the entire grid.

  * `BOXES` Boxes – Display bounding boxes for nodes in the volume tree.

  * `POINTS` Points – Display points for nodes in the volume tree.


Type:
    

enum in [`'NONE'`, `'BOUNDS'`, `'BOXES'`, `'POINTS'`], default `'NONE'`

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

  * [[Volume.display]]

| 


  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
