# Theme(bpy_struct)

base class — [`bpy_struct`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct "bpy.types.bpy_struct")

_class _bpy.types.Theme(_bpy_struct_)
    

User interface styling and color settings

bone_color_sets
    

Type:
    

[`bpy_prop_collection`](../_other/bpy.types.bpy_prop_collection.md#bpy.types.bpy_prop_collection "bpy.types.bpy_prop_collection") of [`ThemeBoneColorSet`](bpy.types.ThemeBoneColorSet.md#bpy.types.ThemeBoneColorSet "bpy.types.ThemeBoneColorSet"), (readonly, never None)

clip_editor
    

Type:
    

[`ThemeClipEditor`](bpy.types.ThemeClipEditor.md#bpy.types.ThemeClipEditor "bpy.types.ThemeClipEditor"), (readonly, never None)

collection_color
    

Type:
    

[`bpy_prop_collection`](../_other/bpy.types.bpy_prop_collection.md#bpy.types.bpy_prop_collection "bpy.types.bpy_prop_collection") of [`ThemeCollectionColor`](bpy.types.ThemeCollectionColor.md#bpy.types.ThemeCollectionColor "bpy.types.ThemeCollectionColor"), (readonly, never None)

common
    

Theme properties shared by different editors

Type:
    

[`ThemeCommon`](bpy.types.ThemeCommon.md#bpy.types.ThemeCommon "bpy.types.ThemeCommon"), (readonly, never None)

console
    

Type:
    

[`ThemeConsole`](bpy.types.ThemeConsole.md#bpy.types.ThemeConsole "bpy.types.ThemeConsole"), (readonly, never None)

dopesheet_editor
    

Type:
    

[`ThemeDopeSheet`](bpy.types.ThemeDopeSheet.md#bpy.types.ThemeDopeSheet "bpy.types.ThemeDopeSheet"), (readonly, never None)

file_browser
    

Type:
    

[`ThemeFileBrowser`](bpy.types.ThemeFileBrowser.md#bpy.types.ThemeFileBrowser "bpy.types.ThemeFileBrowser"), (readonly, never None)

filepath
    

The path to the preset loaded into this theme (if any)

Type:
    

string, default “”, (never None)

graph_editor
    

Type:
    

[`ThemeGraphEditor`](bpy.types.ThemeGraphEditor.md#bpy.types.ThemeGraphEditor "bpy.types.ThemeGraphEditor"), (readonly, never None)

image_editor
    

Type:
    

[`ThemeImageEditor`](bpy.types.ThemeImageEditor.md#bpy.types.ThemeImageEditor "bpy.types.ThemeImageEditor"), (readonly, never None)

info
    

Type:
    

[`ThemeInfo`](bpy.types.ThemeInfo.md#bpy.types.ThemeInfo "bpy.types.ThemeInfo"), (readonly, never None)

name
    

Name of the theme

Type:
    

string, default “”, (never None)

nla_editor
    

Type:
    

[`ThemeNLAEditor`](bpy.types.ThemeNLAEditor.md#bpy.types.ThemeNLAEditor "bpy.types.ThemeNLAEditor"), (readonly, never None)

node_editor
    

Type:
    

[`ThemeNodeEditor`](bpy.types.ThemeNodeEditor.md#bpy.types.ThemeNodeEditor "bpy.types.ThemeNodeEditor"), (readonly, never None)

outliner
    

Type:
    

[`ThemeOutliner`](bpy.types.ThemeOutliner.md#bpy.types.ThemeOutliner "bpy.types.ThemeOutliner"), (readonly, never None)

preferences
    

Type:
    

[`ThemePreferences`](bpy.types.ThemePreferences.md#bpy.types.ThemePreferences "bpy.types.ThemePreferences"), (readonly, never None)

properties
    

Type:
    

[`ThemeProperties`](bpy.types.ThemeProperties.md#bpy.types.ThemeProperties "bpy.types.ThemeProperties"), (readonly, never None)

regions
    

Theme properties for common editor regions

Type:
    

[`ThemeRegions`](bpy.types.ThemeRegions.md#bpy.types.ThemeRegions "bpy.types.ThemeRegions"), (readonly, never None)

sequence_editor
    

Type:
    

[`ThemeSequenceEditor`](bpy.types.ThemeSequenceEditor.md#bpy.types.ThemeSequenceEditor "bpy.types.ThemeSequenceEditor"), (readonly, never None)

spreadsheet
    

Type:
    

[`ThemeSpreadsheet`](bpy.types.ThemeSpreadsheet.md#bpy.types.ThemeSpreadsheet "bpy.types.ThemeSpreadsheet"), (readonly, never None)

statusbar
    

Type:
    

[`ThemeStatusBar`](bpy.types.ThemeStatusBar.md#bpy.types.ThemeStatusBar "bpy.types.ThemeStatusBar"), (readonly, never None)

strip_color
    

Type:
    

[`bpy_prop_collection`](../_other/bpy.types.bpy_prop_collection.md#bpy.types.bpy_prop_collection "bpy.types.bpy_prop_collection") of [`ThemeStripColor`](bpy.types.ThemeStripColor.md#bpy.types.ThemeStripColor "bpy.types.ThemeStripColor"), (readonly, never None)

text_editor
    

Type:
    

[`ThemeTextEditor`](bpy.types.ThemeTextEditor.md#bpy.types.ThemeTextEditor "bpy.types.ThemeTextEditor"), (readonly, never None)

theme_area
    

Type:
    

enum in [`'USER_INTERFACE'`, `'STYLE'`, `'REGIONS'`, `'COMMON'`, `'VIEW_3D'`, `'DOPESHEET_EDITOR'`, `'FILE_BROWSER'`, `'GRAPH_EDITOR'`, `'IMAGE_EDITOR'`, `'INFO'`, `'CLIP_EDITOR'`, `'NODE_EDITOR'`, `'NLA_EDITOR'`, `'OUTLINER'`, `'PREFERENCES'`, `'PROPERTIES'`, `'CONSOLE'`, `'SPREADSHEET'`, `'STATUSBAR'`, `'TEXT_EDITOR'`, `'TOPBAR'`, `'SEQUENCE_EDITOR'`, `'BONE_COLOR_SETS'`], default `'USER_INTERFACE'`

topbar
    

Type:
    

[`ThemeTopBar`](bpy.types.ThemeTopBar.md#bpy.types.ThemeTopBar "bpy.types.ThemeTopBar"), (readonly, never None)

user_interface
    

Type:
    

[`ThemeUserInterface`](bpy.types.ThemeUserInterface.md#bpy.types.ThemeUserInterface "bpy.types.ThemeUserInterface"), (readonly, never None)

view_3d
    

Type:
    

[`ThemeView3D`](bpy.types.ThemeView3D.md#bpy.types.ThemeView3D "bpy.types.ThemeView3D"), (readonly, never None)

_classmethod _bl_rna_get_subclass(_id_ , _default =None_, _/_)
    

Parameters:
    

**id** (_str_) – The RNA type identifier.

Returns:
    

The RNA type or default when not found.

Return type:
    

[`bpy.types.Struct`](../S/bpy.types.Struct.md#bpy.types.Struct "bpy.types.Struct") subclass

_classmethod _bl_rna_get_subclass_py(_id_ , _default =None_, _/_)
    

Parameters:
    

**id** (_str_) – The RNA type identifier.

Returns:
    

The class or default when not found.

Return type:
    

type

## Inherited Properties

  * [`bpy_struct.id_data`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.id_data "bpy.types.bpy_struct.id_data")

| 


  
---|---  
  
## Inherited Functions

  * [`bpy_struct.as_pointer`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.as_pointer "bpy.types.bpy_struct.as_pointer")
  * [`bpy_struct.driver_add`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.driver_add "bpy.types.bpy_struct.driver_add")
  * [`bpy_struct.driver_remove`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.driver_remove "bpy.types.bpy_struct.driver_remove")
  * [`bpy_struct.get`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.get "bpy.types.bpy_struct.get")
  * [`bpy_struct.id_properties_clear`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.id_properties_clear "bpy.types.bpy_struct.id_properties_clear")
  * [`bpy_struct.id_properties_ensure`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.id_properties_ensure "bpy.types.bpy_struct.id_properties_ensure")
  * [`bpy_struct.id_properties_ui`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.id_properties_ui "bpy.types.bpy_struct.id_properties_ui")
  * [`bpy_struct.is_property_hidden`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.is_property_hidden "bpy.types.bpy_struct.is_property_hidden")
  * [`bpy_struct.is_property_overridable_library`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.is_property_overridable_library "bpy.types.bpy_struct.is_property_overridable_library")
  * [`bpy_struct.is_property_readonly`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.is_property_readonly "bpy.types.bpy_struct.is_property_readonly")
  * [`bpy_struct.is_property_set`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.is_property_set "bpy.types.bpy_struct.is_property_set")
  * [`bpy_struct.items`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.items "bpy.types.bpy_struct.items")

| 

  * [`bpy_struct.keyframe_delete`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.keyframe_delete "bpy.types.bpy_struct.keyframe_delete")
  * [`bpy_struct.keyframe_insert`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.keyframe_insert "bpy.types.bpy_struct.keyframe_insert")
  * [`bpy_struct.keys`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.keys "bpy.types.bpy_struct.keys")
  * [`bpy_struct.path_from_id`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.path_from_id "bpy.types.bpy_struct.path_from_id")
  * [`bpy_struct.path_from_module`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.path_from_module "bpy.types.bpy_struct.path_from_module")
  * [`bpy_struct.path_resolve`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.path_resolve "bpy.types.bpy_struct.path_resolve")
  * [`bpy_struct.pop`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.pop "bpy.types.bpy_struct.pop")
  * [`bpy_struct.property_overridable_library_set`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.property_overridable_library_set "bpy.types.bpy_struct.property_overridable_library_set")
  * [`bpy_struct.property_unset`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.property_unset "bpy.types.bpy_struct.property_unset")
  * [`bpy_struct.rna_ancestors`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.rna_ancestors "bpy.types.bpy_struct.rna_ancestors")
  * [`bpy_struct.type_recast`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.type_recast "bpy.types.bpy_struct.type_recast")
  * [`bpy_struct.values`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.values "bpy.types.bpy_struct.values")

  
---|---  
  
## References

  * [`Preferences.themes`](../P/bpy.types.Preferences.md#bpy.types.Preferences.themes "bpy.types.Preferences.themes")

| 


  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
