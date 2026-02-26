# MovieTrackingPlaneTrack(bpy_struct)

base class — [[bpy_struct]]

_class _bpy.types.MovieTrackingPlaneTrack(_bpy_struct_)
    

Match-moving plane track data for tracking

image
    

Image displayed in the track during editing in clip editor

Type:
    

[[Image]]

image_opacity
    

Opacity of the image

Type:
    

float in [0, 1], default 0.0

markers
    

Collection of markers in track

Type:
    

[[MovieTrackingPlaneMarkers]] [[bpy_prop_collection]] of [[MovieTrackingPlaneMarker]], (readonly)

name
    

Unique name of track

Type:
    

string, default “”, (never None)

select
    

Plane track is selected

Type:
    

boolean, default False

use_auto_keying
    

Automatic keyframe insertion when moving plane corners

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

  * [[MovieTracking.plane_tracks]]
  * [[MovieTrackingObject.plane_tracks]]

| 

  * [[MovieTrackingPlaneTracks.active]]

  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
