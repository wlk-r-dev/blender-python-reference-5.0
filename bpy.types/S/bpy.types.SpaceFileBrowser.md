# SpaceFileBrowser(Space)

base classes — [[bpy_struct]], [[Space]]

_class _bpy.types.SpaceFileBrowser(_Space_)
    

File browser space data

active_operator
    

Type:
    

[[Operator]], (readonly)

bookmarks
    

User’s bookmarks

Type:
    

[[bpy_prop_collection]] of [[FileBrowserFSMenuEntry]]

bookmarks_active
    

Index of active bookmark (-1 if none)

Type:
    

int in [-32768, 32767], default -1

browse_mode
    

Type of the File Editor view (regular file browsing or asset browsing)

Type:
    

enum in [Space File Browse Mode Items](../../bpy_types_enum_items/space_file_browse_mode_items.md#rna-enum-space-file-browse-mode-items), default `'FILES'`

operator
    

Type:
    

[[Operator]], (readonly)

params
    

Parameters and Settings for the Filebrowser

Type:
    

[[FileSelectParams]], (readonly)

recent_folders
    

Type:
    

[[bpy_prop_collection]] of [[FileBrowserFSMenuEntry]]

recent_folders_active
    

Index of active recent folder (-1 if none)

Type:
    

int in [-32768, 32767], default -1

show_region_tool_props
    

Type:
    

boolean, default False

show_region_toolbar
    

Type:
    

boolean, default False

show_region_ui
    

Type:
    

boolean, default False

system_bookmarks
    

System’s bookmarks

Type:
    

[[bpy_prop_collection]] of [[FileBrowserFSMenuEntry]], (readonly)

system_bookmarks_active
    

Index of active system bookmark (-1 if none)

Type:
    

int in [-32768, 32767], default -1

system_folders
    

System’s folders (usually root, available hard drives, etc)

Type:
    

[[bpy_prop_collection]] of [[FileBrowserFSMenuEntry]], (readonly)

system_folders_active
    

Index of active system folder (-1 if none)

Type:
    

int in [-32768, 32767], default -1

activate_asset_by_id(_id_to_activate_ , _*_ , _deferred =False_)
    

Activate and select the asset entry that represents the given ID

Parameters:
    

  * **id_to_activate** ([[ID]]) – id_to_activate

  * **deferred** (_boolean_ _,__(__optional_ _)_) – Whether to activate the ID immediately (false) or after the file browser refreshes (true)


activate_file_by_relative_path(_*_ , _relative_path =''_)
    

Set active file and add to selection based on relative path to current File Browser directory

Parameters:
    

**relative_path** (_string_ _,__(__optional_ _,__never None_ _)_) – relative_path

deselect_all()
    

Deselect all files

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

_classmethod _draw_handler_add(_callback_ , _args_ , _region_type_ , _draw_type_)
    

Add a new draw handler to this space type. It will be called every time the specified region in the space type will be drawn. Note: All arguments are positional only for now.

Parameters:
    

  * **callback** (_Callable_ _[__...__,__Any_ _]_) – A function that will be called when the region is drawn. It gets the specified arguments as input, it’s return value is ignored.

  * **args** (_tuple_ _[__Any_ _,__...__]_) – Arguments that will be passed to the callback.

  * **region_type** (_str_) – The region type the callback draws in; usually `WINDOW`. ([[bpy.types.Region.type]])

  * **draw_type** (_str_) – Usually `POST_PIXEL` for 2D drawing and `POST_VIEW` for 3D drawing. In some cases `PRE_VIEW` can be used. `BACKDROP` can be used for backdrops in the node editor.


Returns:
    

Handler that can be removed later on.

Return type:
    

object

_classmethod _draw_handler_remove(_handler_ , _region_type_)
    

Remove a draw handler that was added previously.

Parameters:
    

  * **handler** (_object_) – The draw handler that should be removed.

  * **region_type** (_str_) – Region type the callback was added to.


## Inherited Properties

  * [[bpy_struct.id_data]]
  * [[Space.type]]

| 

  * [[Space.show_locked_time]]
  * [[Space.show_region_header]]

  
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
  * [[bpy_struct.keyframe_delete]]
  * [[bpy_struct.keyframe_insert]]

| 

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
  * [[Space.bl_rna_get_subclass]]
  * [[Space.bl_rna_get_subclass_py]]
  * [[Space.draw_handler_add]]
  * [[Space.draw_handler_remove]]

  
---|---
  *[*]: Keyword-only parameters separator (PEP 3102)
  *[/]: Positional-only parameter separator (PEP 570)
