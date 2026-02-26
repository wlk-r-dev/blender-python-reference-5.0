# ActionGroup(bpy_struct)

base class — [[bpy_struct]]

_class _bpy.types.ActionGroup(_bpy_struct_)
    

Groups of F-Curves

channels
    

F-Curves in this group

Type:
    

[[bpy_prop_collection]] of [[FCurve]], (readonly)

color_set
    

Custom color set to use

Type:
    

enum in [Color Sets Items](../../bpy_types_enum_items/color_sets_items.md#rna-enum-color-sets-items), default `'DEFAULT'`

colors
    

Copy of the colors associated with the group’s color set

Type:
    

[[ThemeBoneColorSet]], (readonly, never None)

is_custom_color_set
    

Color set is user-defined instead of a fixed theme color set

Type:
    

boolean, default False, (readonly)

lock
    

Action group is locked

Type:
    

boolean, default False

mute
    

Action group is muted

Type:
    

boolean, default False

name
    

Type:
    

string, default “”, (never None)

select
    

Action group is selected

Type:
    

boolean, default False

show_expanded
    

Action group is expanded except in graph editor

Type:
    

boolean, default False

show_expanded_graph
    

Action group is expanded in graph editor

Type:
    

boolean, default False

use_pin
    

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

  * [[ActionChannelbag.groups]]
  * [[ActionChannelbagGroups.new]]

| 

  * [[ActionChannelbagGroups.remove]]
  * [[FCurve.group]]

  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
