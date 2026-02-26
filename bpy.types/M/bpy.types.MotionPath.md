# MotionPath(bpy_struct)

base class — [[bpy_struct]]

_class _bpy.types.MotionPath(_bpy_struct_)
    

Cache of the world-space positions of an element over a frame range

color
    

Custom color for motion path before the current frame

Type:
    

[[mathutils.Color]] of 3 items in [0, inf], default (0.0, 0.0, 0.0)

color_post
    

Custom color for motion path after the current frame

Type:
    

[[mathutils.Color]] of 3 items in [0, inf], default (0.0, 0.0, 0.0)

frame_end
    

End frame of the stored range

Type:
    

int in [-inf, inf], default 0, (readonly)

frame_start
    

Starting frame of the stored range

Type:
    

int in [-inf, inf], default 0, (readonly)

is_modified
    

Path is being edited

Type:
    

boolean, default False

length
    

Number of frames cached

Type:
    

int in [-inf, inf], default 0, (readonly)

line_thickness
    

Line thickness for motion path

Type:
    

int in [1, 6], default 0

lines
    

Use straight lines between keyframe points

Type:
    

boolean, default False

points
    

Cached positions per frame

Type:
    

[[bpy_prop_collection]] of [[MotionPathVert]], (readonly)

use_bone_head
    

For PoseBone paths, use the bone head location when calculating this path

Type:
    

boolean, default False, (readonly)

use_custom_color
    

Use custom color for this motion path

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

  * [[Object.motion_path]]

| 

  * [[PoseBone.motion_path]]

  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
