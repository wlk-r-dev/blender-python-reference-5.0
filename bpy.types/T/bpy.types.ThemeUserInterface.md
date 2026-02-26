# ThemeUserInterface(bpy_struct)

base class — [[bpy_struct]]

_class _bpy.types.ThemeUserInterface(_bpy_struct_)
    

Theme settings for user interface elements

axis_w
    

W-axis for quaternion and axis-angle rotations

Type:
    

[[mathutils.Color]] of 3 items in [0, 1], default (0.0, 0.0, 0.0)

axis_x
    

Type:
    

[[mathutils.Color]] of 3 items in [0, 1], default (0.0, 0.0, 0.0)

axis_y
    

Type:
    

[[mathutils.Color]] of 3 items in [0, 1], default (0.0, 0.0, 0.0)

axis_z
    

Type:
    

[[mathutils.Color]] of 3 items in [0, 1], default (0.0, 0.0, 0.0)

editor_border
    

Color of the border between editors

Type:
    

[[mathutils.Color]] of 3 items in [0, 1], default (0.0, 0.0, 0.0)

editor_outline
    

Color of the outline of each editor, except the active one

Type:
    

float array of 4 items in [0, 1], default (0.0, 0.0, 0.0, 0.0)

editor_outline_active
    

Color of the outline of the active editor

Type:
    

float array of 4 items in [0, 1], default (0.0, 0.0, 0.0, 0.0)

gizmo_a
    

Type:
    

[[mathutils.Color]] of 3 items in [0, 1], default (0.0, 0.0, 0.0)

gizmo_b
    

Type:
    

[[mathutils.Color]] of 3 items in [0, 1], default (0.0, 0.0, 0.0)

gizmo_hi
    

Type:
    

[[mathutils.Color]] of 3 items in [0, 1], default (0.0, 0.0, 0.0)

gizmo_primary
    

Type:
    

[[mathutils.Color]] of 3 items in [0, 1], default (0.0, 0.0, 0.0)

gizmo_secondary
    

Type:
    

[[mathutils.Color]] of 3 items in [0, 1], default (0.0, 0.0, 0.0)

gizmo_view_align
    

Type:
    

[[mathutils.Color]] of 3 items in [0, 1], default (0.0, 0.0, 0.0)

icon_alpha
    

Transparency of icons in the interface, to reduce contrast

Type:
    

float in [0, 1], default 0.0

icon_autokey
    

Color of Auto Keying indicator when enabled

Type:
    

float array of 4 items in [0, 1], default (0.0, 0.0, 0.0, 0.0)

icon_border_intensity
    

Control the intensity of the border around themes icons

Type:
    

float in [0, 1], default 0.0

icon_collection
    

Type:
    

float array of 4 items in [0, 1], default (0.0, 0.0, 0.0, 0.0)

icon_folder
    

Color of folders in the file browser

Type:
    

float array of 4 items in [0, 1], default (0.0, 0.0, 0.0, 0.0)

icon_modifier
    

Type:
    

float array of 4 items in [0, 1], default (0.0, 0.0, 0.0, 0.0)

icon_object
    

Type:
    

float array of 4 items in [0, 1], default (0.0, 0.0, 0.0, 0.0)

icon_object_data
    

Type:
    

float array of 4 items in [0, 1], default (0.0, 0.0, 0.0, 0.0)

icon_saturation
    

Saturation of icons in the interface

Type:
    

float in [0, 1], default 0.0

icon_scene
    

Type:
    

float array of 4 items in [0, 1], default (0.0, 0.0, 0.0, 0.0)

icon_shading
    

Type:
    

float array of 4 items in [0, 1], default (0.0, 0.0, 0.0, 0.0)

menu_shadow_fac
    

Blending factor for panel and menu shadows

Type:
    

float in [0.01, 1], default 0.0

menu_shadow_width
    

Width of panel and menu shadows, set to zero to disable

Type:
    

int in [0, 24], default 0

panel_active
    

Color of the outline of top-level panels that are active

Type:
    

float array of 4 items in [0, 1], default (0.0, 0.0, 0.0, 0.0)

panel_back
    

Type:
    

float array of 4 items in [0, 1], default (0.0, 0.0, 0.0, 0.0)

panel_header
    

Type:
    

float array of 4 items in [0, 1], default (0.0, 0.0, 0.0, 0.0)

panel_outline
    

Color of the outline of top-level panels

Type:
    

float array of 4 items in [0, 1], default (0.0, 0.0, 0.0, 0.0)

panel_roundness
    

Roundness of the corners of panels and sub-panels

Type:
    

float in [0, 1], default 0.4

panel_sub_back
    

Type:
    

float array of 4 items in [0, 1], default (0.0, 0.0, 0.0, 0.0)

panel_text
    

Type:
    

[[mathutils.Color]] of 3 items in [0, 1], default (0.0, 0.0, 0.0)

panel_title
    

Type:
    

[[mathutils.Color]] of 3 items in [0, 1], default (0.0, 0.0, 0.0)

transparent_checker_primary
    

Primary color of checkerboard pattern indicating transparent areas

Type:
    

[[mathutils.Color]] of 3 items in [0, 1], default (0.0, 0.0, 0.0)

transparent_checker_secondary
    

Secondary color of checkerboard pattern indicating transparent areas

Type:
    

[[mathutils.Color]] of 3 items in [0, 1], default (0.0, 0.0, 0.0)

transparent_checker_size
    

Size of checkerboard pattern indicating transparent areas

Type:
    

int in [2, 48], default 0

wcol_box
    

Type:
    

[[ThemeWidgetColors]], (readonly, never None)

wcol_curve
    

Type:
    

[[ThemeWidgetColors]], (readonly, never None)

wcol_list_item
    

Type:
    

[[ThemeWidgetColors]], (readonly, never None)

wcol_menu
    

Type:
    

[[ThemeWidgetColors]], (readonly, never None)

wcol_menu_back
    

Type:
    

[[ThemeWidgetColors]], (readonly, never None)

wcol_menu_item
    

Type:
    

[[ThemeWidgetColors]], (readonly, never None)

wcol_num
    

Type:
    

[[ThemeWidgetColors]], (readonly, never None)

wcol_numslider
    

Type:
    

[[ThemeWidgetColors]], (readonly, never None)

wcol_option
    

Type:
    

[[ThemeWidgetColors]], (readonly, never None)

wcol_pie_menu
    

Type:
    

[[ThemeWidgetColors]], (readonly, never None)

wcol_progress
    

Type:
    

[[ThemeWidgetColors]], (readonly, never None)

wcol_pulldown
    

Type:
    

[[ThemeWidgetColors]], (readonly, never None)

wcol_radio
    

Type:
    

[[ThemeWidgetColors]], (readonly, never None)

wcol_regular
    

Type:
    

[[ThemeWidgetColors]], (readonly, never None)

wcol_scroll
    

Type:
    

[[ThemeWidgetColors]], (readonly, never None)

wcol_state
    

Type:
    

[[ThemeWidgetStateColors]], (readonly, never None)

wcol_tab
    

Type:
    

[[ThemeWidgetColors]], (readonly, never None)

wcol_text
    

Type:
    

[[ThemeWidgetColors]], (readonly, never None)

wcol_toggle
    

Type:
    

[[ThemeWidgetColors]], (readonly, never None)

wcol_tool
    

Type:
    

[[ThemeWidgetColors]], (readonly, never None)

wcol_toolbar_item
    

Type:
    

[[ThemeWidgetColors]], (readonly, never None)

wcol_tooltip
    

Type:
    

[[ThemeWidgetColors]], (readonly, never None)

widget_emboss
    

Color of the 1px shadow line underlying widgets

Type:
    

float array of 4 items in [0, 1], default (0.0, 0.0, 0.0, 0.0)

widget_text_cursor
    

Color of the text insertion cursor (caret)

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

  * [[Theme.user_interface]]

| 


  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
