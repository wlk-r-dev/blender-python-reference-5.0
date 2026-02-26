# MovieTrackingCamera(bpy_struct)

base class — [[bpy_struct]]

_class _bpy.types.MovieTrackingCamera(_bpy_struct_)
    

Match-moving camera data for tracking

brown_k1
    

First coefficient of fourth order Brown-Conrady radial distortion

Type:
    

float in [-inf, inf], default 0.0

brown_k2
    

Second coefficient of fourth order Brown-Conrady radial distortion

Type:
    

float in [-inf, inf], default 0.0

brown_k3
    

Third coefficient of fourth order Brown-Conrady radial distortion

Type:
    

float in [-inf, inf], default 0.0

brown_k4
    

Fourth coefficient of fourth order Brown-Conrady radial distortion

Type:
    

float in [-inf, inf], default 0.0

brown_p1
    

First coefficient of second order Brown-Conrady tangential distortion

Type:
    

float in [-inf, inf], default 0.0

brown_p2
    

Second coefficient of second order Brown-Conrady tangential distortion

Type:
    

float in [-inf, inf], default 0.0

distortion_model
    

Distortion model used for camera lenses

  * `POLYNOMIAL` Polynomial – Radial distortion model which fits common cameras.

  * `DIVISION` Divisions – Division distortion model which better represents wide-angle cameras.

  * `NUKE` Nuke – Nuke distortion model.

  * `BROWN` Brown – Brown-Conrady distortion model.


Type:
    

enum in [`'POLYNOMIAL'`, `'DIVISION'`, `'NUKE'`, `'BROWN'`], default `'POLYNOMIAL'`

division_k1
    

First coefficient of second order division distortion

Type:
    

float in [-inf, inf], default 0.0

division_k2
    

Second coefficient of second order division distortion

Type:
    

float in [-inf, inf], default 0.0

focal_length
    

Camera’s focal length

Type:
    

float in [0.0001, inf], default 0.0

focal_length_pixels
    

Camera’s focal length

Type:
    

float in [0, inf], default 0.0

k1
    

First coefficient of third order polynomial radial distortion

Type:
    

float in [-inf, inf], default 0.0

k2
    

Second coefficient of third order polynomial radial distortion

Type:
    

float in [-inf, inf], default 0.0

k3
    

Third coefficient of third order polynomial radial distortion

Type:
    

float in [-inf, inf], default 0.0

nuke_k1
    

First coefficient of second order Nuke distortion

Type:
    

float in [-inf, inf], default 0.0

nuke_k2
    

Second coefficient of second order Nuke distortion

Type:
    

float in [-inf, inf], default 0.0

pixel_aspect
    

Pixel aspect ratio

Type:
    

float in [0.1, inf], default 1.0

principal_point
    

Optical center of lens

Type:
    

float array of 2 items in [-1, 1], default (0.0, 0.0)

principal_point_pixels
    

Optical center of lens in pixels

Type:
    

float array of 2 items in [-inf, inf], default (0.0, 0.0)

sensor_width
    

Width of CCD sensor in millimeters

Type:
    

float in [0, 500], default 0.0

units
    

Units used for camera focal length

  * `PIXELS` px – Use pixels for units of focal length.

  * `MILLIMETERS` mm – Use millimeters for units of focal length.


Type:
    

enum in [`'PIXELS'`, `'MILLIMETERS'`], default `'PIXELS'`

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

  * [[MovieTracking.camera]]

| 


  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
