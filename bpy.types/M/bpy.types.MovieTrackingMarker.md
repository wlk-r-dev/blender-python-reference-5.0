# MovieTrackingMarker(bpy_struct)

base class — [[bpy_struct]]

_class _bpy.types.MovieTrackingMarker(_bpy_struct_)
    

Match-moving marker data for tracking

co
    

Marker position at frame in normalized coordinates

Type:
    

[[mathutils.Vector]] of 2 items in [-inf, inf], default (0.0, 0.0)

frame
    

Frame number marker is keyframed on

Type:
    

int in [-inf, inf], default 0

is_keyed
    

Whether the position of the marker is keyframed or tracked

Type:
    

boolean, default True

mute
    

Is marker muted for current frame

Type:
    

boolean, default False

pattern_bound_box
    

Pattern area bounding box in normalized coordinates

Type:
    

float multi-dimensional array of 2 * 2 items in [-inf, inf], default ((0.0, 0.0), (0.0, 0.0)), (readonly)

pattern_corners
    

Array of coordinates which represents pattern’s corners in normalized coordinates relative to marker position

Type:
    

float multi-dimensional array of 4 * 2 items in [-inf, inf], default ((0.0, 0.0), (0.0, 0.0), (0.0, 0.0), (0.0, 0.0))

search_max
    

Right-bottom corner of search area in normalized coordinates relative to marker position

Type:
    

[[mathutils.Vector]] of 2 items in [-inf, inf], default (0.0, 0.0)

search_min
    

Left-bottom corner of search area in normalized coordinates relative to marker position

Type:
    

[[mathutils.Vector]] of 2 items in [-inf, inf], default (0.0, 0.0)

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

  * [[MovieTrackingMarkers.find_frame]]
  * [[MovieTrackingMarkers.insert_frame]]

| 

  * [[MovieTrackingTrack.markers]]

  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
