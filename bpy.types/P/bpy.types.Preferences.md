# Preferences(bpy_struct)

base class — [[bpy_struct]]

_class _bpy.types.Preferences(_bpy_struct_)
    

Global preferences

active_section
    

Preferences

Type:
    

enum in [Preference Section Items](../../bpy_types_enum_items/preference_section_items.md#rna-enum-preference-section-items), default `'INTERFACE'`

addons
    

Type:
    

[[Addons]] [[bpy_prop_collection]] of [[Addon]], (readonly)

app_template
    

Type:
    

string, default “”, (never None)

apps
    

Preferences that work only for apps

Type:
    

[[PreferencesApps]], (readonly, never None)

autoexec_paths
    

Type:
    

[[PathCompareCollection]] [[bpy_prop_collection]] of [[PathCompare]], (readonly)

edit
    

Settings for interacting with Blender data

Type:
    

[[PreferencesEdit]], (readonly, never None)

experimental
    

Settings for features that are still early in their development stage

Type:
    

[[PreferencesExperimental]], (readonly, never None)

extensions
    

Settings for extensions

Type:
    

[[PreferencesExtensions]], (readonly, never None)

filepaths
    

Default paths for external files

Type:
    

[[PreferencesFilePaths]], (readonly, never None)

inputs
    

Settings for input devices

Type:
    

[[PreferencesInput]], (readonly, never None)

is_dirty
    

Preferences have changed

Type:
    

boolean, default False

keymap
    

Shortcut setup for keyboards and other input devices

Type:
    

[[PreferencesKeymap]], (readonly, never None)

studio_lights
    

Type:
    

[[StudioLights]] [[bpy_prop_collection]] of [[StudioLight]], (readonly)

system
    

Graphics driver and operating system settings

Type:
    

[[PreferencesSystem]], (readonly, never None)

themes
    

Type:
    

[[bpy_prop_collection]] of [[Theme]], (readonly)

ui_styles
    

Type:
    

[[bpy_prop_collection]] of [[ThemeStyle]], (readonly)

use_preferences_save
    

Save preferences on exit when modified (unless factory settings have been loaded)

Type:
    

boolean, default True

use_recent_searches
    

Sort the recently searched items at the top

Type:
    

boolean, default True

version
    

Version of Blender the userpref.blend was saved with

Type:
    

int array of 3 items in [0, inf], default (0, 0, 0), (readonly)

view
    

Preferences related to viewing data

Type:
    

[[PreferencesView]], (readonly, never None)

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

  * [[Context.preferences]]

| 


  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
