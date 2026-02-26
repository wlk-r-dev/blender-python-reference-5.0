# SpaceFileBrowser(Space)

base classes — [`bpy_struct`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct "bpy.types.bpy_struct"), [`Space`](bpy.types.Space.md#bpy.types.Space "bpy.types.Space")

_class _bpy.types.SpaceFileBrowser(_Space_)
    

File browser space data

active_operator
    

Type:
    

[`Operator`](../O/bpy.types.Operator.md#bpy.types.Operator "bpy.types.Operator"), (readonly)

bookmarks
    

User’s bookmarks

Type:
    

[`bpy_prop_collection`](../_other/bpy.types.bpy_prop_collection.md#bpy.types.bpy_prop_collection "bpy.types.bpy_prop_collection") of [`FileBrowserFSMenuEntry`](../F/bpy.types.FileBrowserFSMenuEntry.md#bpy.types.FileBrowserFSMenuEntry "bpy.types.FileBrowserFSMenuEntry")

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
    

[`Operator`](../O/bpy.types.Operator.md#bpy.types.Operator "bpy.types.Operator"), (readonly)

params
    

Parameters and Settings for the Filebrowser

Type:
    

[`FileSelectParams`](../F/bpy.types.FileSelectParams.md#bpy.types.FileSelectParams "bpy.types.FileSelectParams"), (readonly)

recent_folders
    

Type:
    

[`bpy_prop_collection`](../_other/bpy.types.bpy_prop_collection.md#bpy.types.bpy_prop_collection "bpy.types.bpy_prop_collection") of [`FileBrowserFSMenuEntry`](../F/bpy.types.FileBrowserFSMenuEntry.md#bpy.types.FileBrowserFSMenuEntry "bpy.types.FileBrowserFSMenuEntry")

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
    

[`bpy_prop_collection`](../_other/bpy.types.bpy_prop_collection.md#bpy.types.bpy_prop_collection "bpy.types.bpy_prop_collection") of [`FileBrowserFSMenuEntry`](../F/bpy.types.FileBrowserFSMenuEntry.md#bpy.types.FileBrowserFSMenuEntry "bpy.types.FileBrowserFSMenuEntry"), (readonly)

system_bookmarks_active
    

Index of active system bookmark (-1 if none)

Type:
    

int in [-32768, 32767], default -1

system_folders
    

System’s folders (usually root, available hard drives, etc)

Type:
    

[`bpy_prop_collection`](../_other/bpy.types.bpy_prop_collection.md#bpy.types.bpy_prop_collection "bpy.types.bpy_prop_collection") of [`FileBrowserFSMenuEntry`](../F/bpy.types.FileBrowserFSMenuEntry.md#bpy.types.FileBrowserFSMenuEntry "bpy.types.FileBrowserFSMenuEntry"), (readonly)

system_folders_active
    

Index of active system folder (-1 if none)

Type:
    

int in [-32768, 32767], default -1

activate_asset_by_id(_id_to_activate_ , _*_ , _deferred =False_)
    

Activate and select the asset entry that represents the given ID

Parameters:
    

  * **id_to_activate** ([`ID`](../I/bpy.types.ID.md#bpy.types.ID "bpy.types.ID")) – id_to_activate

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
    

[`bpy.types.Struct`](bpy.types.Struct.md#bpy.types.Struct "bpy.types.Struct") subclass

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

  * **region_type** (_str_) – The region type the callback draws in; usually `WINDOW`. ([`bpy.types.Region.type`](../R/bpy.types.Region.md#bpy.types.Region.type "bpy.types.Region.type"))

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

  * [`bpy_struct.id_data`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.id_data "bpy.types.bpy_struct.id_data")
  * [`Space.type`](bpy.types.Space.md#bpy.types.Space.type "bpy.types.Space.type")

| 

  * [`Space.show_locked_time`](bpy.types.Space.md#bpy.types.Space.show_locked_time "bpy.types.Space.show_locked_time")
  * [`Space.show_region_header`](bpy.types.Space.md#bpy.types.Space.show_region_header "bpy.types.Space.show_region_header")

  
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
  * [`bpy_struct.keyframe_delete`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.keyframe_delete "bpy.types.bpy_struct.keyframe_delete")
  * [`bpy_struct.keyframe_insert`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.keyframe_insert "bpy.types.bpy_struct.keyframe_insert")

| 

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
  * [`Space.bl_rna_get_subclass`](bpy.types.Space.md#bpy.types.Space.bl_rna_get_subclass "bpy.types.Space.bl_rna_get_subclass")
  * [`Space.bl_rna_get_subclass_py`](bpy.types.Space.md#bpy.types.Space.bl_rna_get_subclass_py "bpy.types.Space.bl_rna_get_subclass_py")
  * [`Space.draw_handler_add`](bpy.types.Space.md#bpy.types.Space.draw_handler_add "bpy.types.Space.draw_handler_add")
  * [`Space.draw_handler_remove`](bpy.types.Space.md#bpy.types.Space.draw_handler_remove "bpy.types.Space.draw_handler_remove")

  
---|---
  *[*]: Keyword-only parameters separator (PEP 3102)
  *[/]: Positional-only parameter separator (PEP 570)
