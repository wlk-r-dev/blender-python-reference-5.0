# ThemeNLAEditor(bpy_struct)

base class — [[bpy_struct]]

_class _bpy.types.ThemeNLAEditor(_bpy_struct_)
    

Theme settings for the NLA Editor

active_action
    

Animation data-block has active action

Type:
    

float array of 4 items in [0, 1], default (0.0, 0.0, 0.0, 0.0)

active_action_unset
    

Animation data-block does not have active action

Type:
    

float array of 4 items in [0, 1], default (0.0, 0.0, 0.0, 0.0)

grid
    

Type:
    

[[mathutils.Color]] of 3 items in [0, 1], default (0.0, 0.0, 0.0)

keyframe_border
    

Color of keyframe border

Type:
    

float array of 4 items in [0, 1], default (0.0, 0.0, 0.0, 0.0)

keyframe_border_selected
    

Color of selected keyframe border

Type:
    

float array of 4 items in [0, 1], default (0.0, 0.0, 0.0, 0.0)

meta_strips
    

Unselected Meta Strip (for grouping related strips)

Type:
    

[[mathutils.Color]] of 3 items in [0, 1], default (0.0, 0.0, 0.0)

meta_strips_selected
    

Selected Meta Strip (for grouping related strips)

Type:
    

[[mathutils.Color]] of 3 items in [0, 1], default (0.0, 0.0, 0.0)

sound_strips
    

Unselected Sound Strip (for timing speaker sounds)

Type:
    

[[mathutils.Color]] of 3 items in [0, 1], default (0.0, 0.0, 0.0)

sound_strips_selected
    

Selected Sound Strip (for timing speaker sounds)

Type:
    

[[mathutils.Color]] of 3 items in [0, 1], default (0.0, 0.0, 0.0)

space
    

Settings for space

Type:
    

[[ThemeSpaceGeneric]], (readonly, never None)

strips
    

Unselected Action-Clip Strip

Type:
    

[[mathutils.Color]] of 3 items in [0, 1], default (0.0, 0.0, 0.0)

strips_selected
    

Selected Action-Clip Strip

Type:
    

[[mathutils.Color]] of 3 items in [0, 1], default (0.0, 0.0, 0.0)

transition_strips
    

Unselected Transition Strip

Type:
    

[[mathutils.Color]] of 3 items in [0, 1], default (0.0, 0.0, 0.0)

transition_strips_selected
    

Selected Transition Strip

Type:
    

[[mathutils.Color]] of 3 items in [0, 1], default (0.0, 0.0, 0.0)

tweak
    

Color for strip/action being “tweaked” or edited

Type:
    

[[mathutils.Color]] of 3 items in [0, 1], default (0.0, 0.0, 0.0)

tweak_duplicate
    

Warning/error indicator color for strips referencing the strip being tweaked

Type:
    

[[mathutils.Color]] of 3 items in [0, 1], default (0.0, 0.0, 0.0)

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

  * [[Theme.nla_editor]]

| 


  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
