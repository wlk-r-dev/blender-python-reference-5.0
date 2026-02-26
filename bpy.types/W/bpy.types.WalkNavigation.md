# WalkNavigation(bpy_struct)

base class — [[bpy_struct]]

_class _bpy.types.WalkNavigation(_bpy_struct_)
    

Walk navigation settings

jump_height
    

Maximum height of a jump

Type:
    

float in [0.1, 100], default 0.4

mouse_speed
    

Speed factor for when looking around, high values mean faster mouse movement

Type:
    

float in [0.01, 10], default 1.0

teleport_time
    

Interval of time warp when teleporting in navigation mode

Type:
    

float in [0, 10], default 0.2

use_gravity
    

Walk with gravity, or free navigate

Type:
    

boolean, default False

use_mouse_reverse
    

Reverse the vertical movement of the mouse

Type:
    

boolean, default False

view_height
    

View distance from the floor when walking

Type:
    

float in [0, 1000], default 1.6

walk_speed
    

Base speed for walking and flying

Type:
    

float in [0.01, 100], default 2.5

walk_speed_factor
    

Multiplication factor when using the fast or slow modifiers

Type:
    

float in [0.01, 10], default 5.0

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

  * [[PreferencesInput.walk_navigation]]

| 


  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
