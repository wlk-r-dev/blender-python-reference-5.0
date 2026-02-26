# PreferencesFilePaths(bpy_struct)

base class — [[bpy_struct]]

_class _bpy.types.PreferencesFilePaths(_bpy_struct_)
    

Default paths for external files

active_asset_library
    

Index of the asset library being edited in the Preferences UI

Type:
    

int in [-32768, 32767], default 0

animation_player
    

Path to a custom animation/frame sequence player

Type:
    

string, default “”, (never None)

animation_player_preset
    

Preset configs for external animation players

  * `INTERNAL` Internal – Built-in animation player.

  * `DJV` DJV – Open source frame player.

  * `FRAMECYCLER` FrameCycler – Frame player from IRIDAS.

  * `RV` RV – Frame player from Tweak Software.

  * `MPLAYER` MPlayer – Media player for video and PNG/JPEG/SGI image sequences.

  * `CUSTOM` Custom – Custom animation player executable path.


Type:
    

enum in [`'INTERNAL'`, `'DJV'`, `'FRAMECYCLER'`, `'RV'`, `'MPLAYER'`, `'CUSTOM'`], default `'INTERNAL'`

asset_libraries
    

Type:
    

[[AssetLibraryCollection]] [[bpy_prop_collection]] of [[UserAssetLibrary]], (readonly)

auto_save_time
    

The time (in minutes) to wait between automatic temporary saves

Type:
    

int in [1, 60], default 2

file_preview_type
    

What type of blend preview to create

  * `NONE` None – Do not create blend previews.

  * `AUTO` Auto – Automatically select best preview type.

  * `SCREENSHOT` Screenshot – Capture the entire window.

  * `CAMERA` Camera View – Workbench render of scene.


Type:
    

enum in [`'NONE'`, `'AUTO'`, `'SCREENSHOT'`, `'CAMERA'`], default `'AUTO'`

font_directory
    

The default directory to search for loading fonts

Type:
    

string, default “”, (never None, blend relative `//` prefix supported)

i18n_branches_directory
    

The path to the ‘/branches’ directory of your local svn-translation copy, to allow translating from the UI

Type:
    

string, default “”, (never None)

image_editor
    

Path to an image editor

Type:
    

string, default “”, (never None)

recent_files
    

Maximum number of recently opened files to remember

Type:
    

int in [0, 1000], default 200

render_cache_directory
    

Where to cache raw render results

Type:
    

string, default “”, (never None, blend relative `//` prefix supported)

render_output_directory
    

The default directory for rendering output, for new scenes

Type:
    

string, default “”, (never None, blend relative `//` prefix supported)

save_version
    

The number of old versions to maintain in the current directory, when manually saving

Type:
    

int in [0, 32], default 1

script_directories
    

Type:
    

[[ScriptDirectoryCollection]] [[bpy_prop_collection]] of [[ScriptDirectory]], (readonly)

show_hidden_files_datablocks
    

Show files and data-blocks that are normally hidden

Type:
    

boolean, default True

show_recent_locations
    

Show Recent locations list in the File Browser

Type:
    

boolean, default True

show_system_bookmarks
    

Show System locations list in the File Browser

Type:
    

boolean, default True

sound_directory
    

The default directory to search for sounds

Type:
    

string, default “”, (never None, blend relative `//` prefix supported)

temporary_directory
    

The directory for storing temporary save files. The path must reference an existing directory or it will be ignored

Type:
    

string, default “”, (never None)

text_editor
    

Command to launch the text editor, either a full path or a command in $PATH. Use the internal editor when left blank

Type:
    

string, default “”, (never None)

text_editor_args
    

Defines the specific format of the arguments with which the text editor opens files. The supported expansions are as follows:

$filepath The absolute path of the file. $line The line to open at (Optional). $column The column to open from the beginning of the line (Optional). $line0 & column0 start at zero. Example: -f $filepath -l $line -c $column

Type:
    

string, default “”, (never None)

texture_directory
    

The default directory to search for textures

Type:
    

string, default “”, (never None, blend relative `//` prefix supported)

use_auto_save_temporary_files
    

Automatic saving of temporary files in temp directory, uses process ID. Warning: Sculpt and edit mode data won’t be saved

Type:
    

boolean, default True

use_extension_online_access_handled
    

The user has been shown the “Online Access” prompt and made a choice

Type:
    

boolean, default False

use_file_compression
    

Enable file compression when saving .blend files

Type:
    

boolean, default True

use_filter_files
    

Enable filtering of files in the File Browser

Type:
    

boolean, default True

use_load_ui
    

Load user interface setup when loading .blend files

Type:
    

boolean, default True

use_relative_paths
    

Default relative path option for the file selector, when no path is defined yet

Type:
    

boolean, default True

use_scripts_auto_execute
    

Allow any .blend file to run scripts automatically (unsafe with blend files from an untrusted source)

Type:
    

boolean, default False

use_tabs_as_spaces
    

Automatically convert all new tabs into spaces for new and loaded text files

Type:
    

boolean, default True

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

  * [[Preferences.filepaths]]

| 


  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
