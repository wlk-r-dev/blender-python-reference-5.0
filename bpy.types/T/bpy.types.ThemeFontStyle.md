# ThemeFontStyle(bpy_struct)

base class — [[bpy_struct]]

_class _bpy.types.ThemeFontStyle(_bpy_struct_)
    

Theme settings for Font

character_weight
    

Weight of the characters. 100-900, 400 is normal.

Type:
    

int in [100, 900], default 400

points
    

Font size in points

Type:
    

float in [6, 32], default 0.0

shadow
    

Shadow type (0 none, 3, 5 blur, 6 outline)

Type:
    

int in [0, 6], default 0

shadow_alpha
    

Type:
    

float in [0, 1], default 0.0

shadow_offset_x
    

Shadow offset in pixels

Type:
    

int in [-10, 10], default 0

shadow_offset_y
    

Shadow offset in pixels

Type:
    

int in [-10, 10], default 0

shadow_value
    

Shadow color in gray value

Type:
    

float in [0, 1], default 0.0

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

  * [[ThemeStyle.panel_title]]
  * [[ThemeStyle.tooltip]]

| 

  * [[ThemeStyle.widget]]

  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
