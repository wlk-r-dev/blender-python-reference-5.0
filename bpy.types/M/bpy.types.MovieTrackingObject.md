# MovieTrackingObject(bpy_struct)

base class — [[bpy_struct]]

_class _bpy.types.MovieTrackingObject(_bpy_struct_)
    

Match-moving object tracking and reconstruction data

is_camera
    

Object is used for camera tracking

Type:
    

boolean, default False, (readonly)

keyframe_a
    

First keyframe used for reconstruction initialization

Type:
    

int in [-inf, inf], default 0

keyframe_b
    

Second keyframe used for reconstruction initialization

Type:
    

int in [-inf, inf], default 0

name
    

Unique name of object

Type:
    

string, default “”, (never None)

plane_tracks
    

Collection of plane tracks in this tracking data object

Type:
    

[[MovieTrackingObjectPlaneTracks]] [[bpy_prop_collection]] of [[MovieTrackingPlaneTrack]], (readonly)

reconstruction
    

Type:
    

[[MovieTrackingReconstruction]], (readonly)

scale
    

Scale of object solution in camera space

Type:
    

float in [0.0001, 10000], default 1.0

tracks
    

Collection of tracks in this tracking data object

Type:
    

[[MovieTrackingObjectTracks]] [[bpy_prop_collection]] of [[MovieTrackingTrack]], (readonly)

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

  * [[MovieTracking.objects]]
  * [[MovieTrackingObjects.active]]

| 

  * [[MovieTrackingObjects.new]]
  * [[MovieTrackingObjects.remove]]

  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
