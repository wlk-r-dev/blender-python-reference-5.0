# Theme(bpy_struct)

base class — [[bpy_struct]]

_class _bpy.types.Theme(_bpy_struct_)
    

User interface styling and color settings

bone_color_sets
    

Type:
    

[[bpy_prop_collection]] of [[ThemeBoneColorSet]], (readonly, never None)

clip_editor
    

Type:
    

[[ThemeClipEditor]], (readonly, never None)

collection_color
    

Type:
    

[[bpy_prop_collection]] of [[ThemeCollectionColor]], (readonly, never None)

common
    

Theme properties shared by different editors

Type:
    

[[ThemeCommon]], (readonly, never None)

console
    

Type:
    

[[ThemeConsole]], (readonly, never None)

dopesheet_editor
    

Type:
    

[[ThemeDopeSheet]], (readonly, never None)

file_browser
    

Type:
    

[[ThemeFileBrowser]], (readonly, never None)

filepath
    

The path to the preset loaded into this theme (if any)

Type:
    

string, default “”, (never None)

graph_editor
    

Type:
    

[[ThemeGraphEditor]], (readonly, never None)

image_editor
    

Type:
    

[[ThemeImageEditor]], (readonly, never None)

info
    

Type:
    

[[ThemeInfo]], (readonly, never None)

name
    

Name of the theme

Type:
    

string, default “”, (never None)

nla_editor
    

Type:
    

[[ThemeNLAEditor]], (readonly, never None)

node_editor
    

Type:
    

[[ThemeNodeEditor]], (readonly, never None)

outliner
    

Type:
    

[[ThemeOutliner]], (readonly, never None)

preferences
    

Type:
    

[[ThemePreferences]], (readonly, never None)

properties
    

Type:
    

[[ThemeProperties]], (readonly, never None)

regions
    

Theme properties for common editor regions

Type:
    

[[ThemeRegions]], (readonly, never None)

sequence_editor
    

Type:
    

[[ThemeSequenceEditor]], (readonly, never None)

spreadsheet
    

Type:
    

[[ThemeSpreadsheet]], (readonly, never None)

statusbar
    

Type:
    

[[ThemeStatusBar]], (readonly, never None)

strip_color
    

Type:
    

[[bpy_prop_collection]] of [[ThemeStripColor]], (readonly, never None)

text_editor
    

Type:
    

[[ThemeTextEditor]], (readonly, never None)

theme_area
    

Type:
    

enum in [`'USER_INTERFACE'`, `'STYLE'`, `'REGIONS'`, `'COMMON'`, `'VIEW_3D'`, `'DOPESHEET_EDITOR'`, `'FILE_BROWSER'`, `'GRAPH_EDITOR'`, `'IMAGE_EDITOR'`, `'INFO'`, `'CLIP_EDITOR'`, `'NODE_EDITOR'`, `'NLA_EDITOR'`, `'OUTLINER'`, `'PREFERENCES'`, `'PROPERTIES'`, `'CONSOLE'`, `'SPREADSHEET'`, `'STATUSBAR'`, `'TEXT_EDITOR'`, `'TOPBAR'`, `'SEQUENCE_EDITOR'`, `'BONE_COLOR_SETS'`], default `'USER_INTERFACE'`

topbar
    

Type:
    

[[ThemeTopBar]], (readonly, never None)

user_interface
    

Type:
    

[[ThemeUserInterface]], (readonly, never None)

view_3d
    

Type:
    

[[ThemeView3D]], (readonly, never None)

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

  * [[Preferences.themes]]

| 


  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
