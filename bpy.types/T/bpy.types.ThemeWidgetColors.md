# ThemeWidgetColors(bpy_struct)

base class — [[bpy_struct]]

_class _bpy.types.ThemeWidgetColors(_bpy_struct_)
    

Theme settings for widget color sets

inner
    

Type:
    

float array of 4 items in [0, 1], default (0.0, 0.0, 0.0, 0.0)

inner_sel
    

Type:
    

float array of 4 items in [0, 1], default (0.0, 0.0, 0.0, 0.0)

item
    

Type:
    

float array of 4 items in [0, 1], default (0.0, 0.0, 0.0, 0.0)

outline
    

Type:
    

float array of 4 items in [0, 1], default (0.0, 0.0, 0.0, 0.0)

outline_sel
    

Type:
    

float array of 4 items in [0, 1], default (0.0, 0.0, 0.0, 0.0)

roundness
    

Amount of edge rounding

Type:
    

float in [0, 1], default 0.0

shadedown
    

Type:
    

int in [-100, 100], default 0

shadetop
    

Type:
    

int in [-100, 100], default 0

show_shaded
    

Type:
    

boolean, default False

text
    

Type:
    

[[mathutils.Color]] of 3 items in [0, 1], default (0.0, 0.0, 0.0)

text_sel
    

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

  * [[ThemeUserInterface.wcol_box]]
  * [[ThemeUserInterface.wcol_curve]]
  * [[ThemeUserInterface.wcol_list_item]]
  * [[ThemeUserInterface.wcol_menu]]
  * [[ThemeUserInterface.wcol_menu_back]]
  * [[ThemeUserInterface.wcol_menu_item]]
  * [[ThemeUserInterface.wcol_num]]
  * [[ThemeUserInterface.wcol_numslider]]
  * [[ThemeUserInterface.wcol_option]]
  * [[ThemeUserInterface.wcol_pie_menu]]
  * [[ThemeUserInterface.wcol_progress]]

| 

  * [[ThemeUserInterface.wcol_pulldown]]
  * [[ThemeUserInterface.wcol_radio]]
  * [[ThemeUserInterface.wcol_regular]]
  * [[ThemeUserInterface.wcol_scroll]]
  * [[ThemeUserInterface.wcol_tab]]
  * [[ThemeUserInterface.wcol_text]]
  * [[ThemeUserInterface.wcol_toggle]]
  * [[ThemeUserInterface.wcol_tool]]
  * [[ThemeUserInterface.wcol_toolbar_item]]
  * [[ThemeUserInterface.wcol_tooltip]]

  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
