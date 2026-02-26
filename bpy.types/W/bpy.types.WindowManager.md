# WindowManager(ID)

base classes — [`bpy_struct`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct "bpy.types.bpy_struct"), [`ID`](../I/bpy.types.ID.md#bpy.types.ID "bpy.types.ID")

_class _bpy.types.WindowManager(_ID_)
    

Window manager data-block defining open windows and other user interface data

addon_filter
    

Filter add-ons by category

Type:
    

enum in []

addon_search
    

Filter by add-on name, author & category

Type:
    

string, default “”, (never None)

addon_support
    

Display support level

  * `OFFICIAL` Official – Officially supported.

  * `COMMUNITY` Community – Maintained by community developers.


Type:
    

enum set in {`'OFFICIAL'`, `'COMMUNITY'`}, default {`'COMMUNITY'`, `'OFFICIAL'`}

addon_tags
    

Type:
    

[`bpy_prop_collection`](../_other/bpy.types.bpy_prop_collection.md#bpy.types.bpy_prop_collection "bpy.types.bpy_prop_collection") of `BlExtDummyGroup`, (readonly)

asset_path_dummy
    

Full path to the Blender file containing the active asset

Type:
    

string, default “”, (readonly, never None)

extension_search
    

Filter by extension name, author & category

Type:
    

string, default “”, (never None)

extension_show_panel_available
    

Only show installed extensions

Type:
    

boolean, default True

extension_show_panel_installed
    

Only show installed extensions

Type:
    

boolean, default True

extension_tags
    

Type:
    

[`bpy_prop_collection`](../_other/bpy.types.bpy_prop_collection.md#bpy.types.bpy_prop_collection "bpy.types.bpy_prop_collection") of `BlExtDummyGroup`, (readonly)

extension_type
    

Show extensions by type

  * `ALL` All – Show all extension types.

  * `ADDON` Add-ons – Only show add-ons.

  * `THEME` Themes – Only show themes.


Type:
    

enum in [`'ALL'`, `'ADDON'`, `'THEME'`], default `'ADDON'`

extensions_blocked
    

Number of installed extensions which are blocked

Type:
    

int in [-inf, inf], default 0

extensions_updates
    

Number of extensions with available update

Type:
    

int in [-inf, inf], default 0

is_interface_locked
    

If true, the interface is currently locked by a running job and data should not be modified from application timers. Otherwise, the running job might conflict with the handler causing unexpected results or even crashes.

Type:
    

boolean, default False, (readonly)

keyconfigs
    

Registered key configurations

Type:
    

[`KeyConfigurations`](../K/bpy.types.KeyConfigurations.md#bpy.types.KeyConfigurations "bpy.types.KeyConfigurations") [`bpy_prop_collection`](../_other/bpy.types.bpy_prop_collection.md#bpy.types.bpy_prop_collection "bpy.types.bpy_prop_collection") of [`KeyConfig`](../K/bpy.types.KeyConfig.md#bpy.types.KeyConfig "bpy.types.KeyConfig"), (readonly)

operators
    

Operator registry

Type:
    

[`bpy_prop_collection`](../_other/bpy.types.bpy_prop_collection.md#bpy.types.bpy_prop_collection "bpy.types.bpy_prop_collection") of [`Operator`](../O/bpy.types.Operator.md#bpy.types.Operator "bpy.types.Operator"), (readonly)

poselib_previous_action
    

Type:
    

[`Action`](../A/bpy.types.Action.md#bpy.types.Action "bpy.types.Action")

preset_name
    

Name for new preset

Type:
    

string, default “New Preset”, (never None)

windows
    

Open windows

Type:
    

[`bpy_prop_collection`](../_other/bpy.types.bpy_prop_collection.md#bpy.types.bpy_prop_collection "bpy.types.bpy_prop_collection") of [`Window`](bpy.types.Window.md#bpy.types.Window "bpy.types.Window"), (readonly)

xr_session_settings
    

Type:
    

[`XrSessionSettings`](../X/bpy.types.XrSessionSettings.md#bpy.types.XrSessionSettings "bpy.types.XrSessionSettings"), (readonly, never None)

xr_session_state
    

Runtime state information about the VR session

Type:
    

[`XrSessionState`](../X/bpy.types.XrSessionState.md#bpy.types.XrSessionState "bpy.types.XrSessionState"), (readonly)

clipboard
    

Clipboard text storage.

Type:
    

str

_classmethod _fileselect_add(_operator_)
    

Opens a file selector with an operator.

Parameters:
    

**operator** ([`Operator`](../O/bpy.types.Operator.md#bpy.types.Operator "bpy.types.Operator")) – Operator to call

This method is used from the operators `invoke` callback which must then return `{'RUNNING_MODAL'}`.

Accepting the file selector will run the operators `execute` callback.

The following properties are supported:

`filepath`: `bpy.props.StringProperty(subtype='FILE_PATH')`
    

Represents the absolute path to the file.

`dirpath`: `bpy.props.StringProperty(subtype='DIR_PATH')`
    

Represents the absolute path to the directory.

`filename`: `bpy.props.StringProperty(subtype='FILE_NAME')`
    

Represents the filename without the leading directory.

`files`: `bpy.props.CollectionProperty(type=bpy.types.OperatorFileListElement)`
    

When present in the operator this collection includes all selected files.

`filter_glob`: `bpy.props.StringProperty(default="*.ext")`
    

When present in the operator and it’s not empty, it will be used as a file filter (example value: `*.zip;*.py;*.exe`).

`check_existing`: `bpy.props.BoolProperty()`
    

If this property is present and set to `True`, the operator will warn if the provided file-path already exists by highlighting the filename input field in red.

Warning

After opening the file-browser the user may continue to use Blender, this means it is possible for the user to change the context in ways that would cause the operators `poll` function to fail.

Unless the operator reads all necessary data from the context before the file-selector is opened, it is recommended for operators to check the `poll` function from `execute` to ensure the context is still valid.

Example from the body of an operators `execute` function:
    
    
    if self.options.is_invoke:
        # The context may have changed since invoking the file selector.
        if not self.poll(context):
            self.report({'ERROR'}, "Invalid context")
            return {'CANCELLED'}
    

_classmethod _modal_handler_add(_operator_)
    

Add a modal handler to the window manager, for the given modal operator (called by invoke() with self, just before returning {‘RUNNING_MODAL’})

Parameters:
    

**operator** ([`Operator`](../O/bpy.types.Operator.md#bpy.types.Operator "bpy.types.Operator")) – Operator to call

Returns:
    

Whether adding the handler was successful

Return type:
    

boolean

event_timer_add(_time_step_ , _*_ , _window =None_)
    

Add a timer to the given window, to generate periodic ‘TIMER’ events

Parameters:
    

  * **time_step** (_float in_ _[__0_ _,__inf_ _]_) – Time Step, Interval in seconds between timer events

  * **window** ([`Window`](bpy.types.Window.md#bpy.types.Window "bpy.types.Window"), (optional)) – Window to attach the timer to, or None


Return type:
    

[`Timer`](../T/bpy.types.Timer.md#bpy.types.Timer "bpy.types.Timer")

event_timer_remove(_timer_)
    

event_timer_remove

_classmethod _gizmo_group_type_ensure(_identifier_)
    

Activate an existing widget group (when the persistent option isn’t set)

Parameters:
    

**identifier** (_string_ _,__(__never None_ _)_) – Gizmo group type name

_classmethod _gizmo_group_type_unlink_delayed(_identifier_)
    

Unlink a widget group (when the persistent option is set)

Parameters:
    

**identifier** (_string_ _,__(__never None_ _)_) – Gizmo group type name

progress_begin(_min_ , _max_)
    

Start progress report

Parameters:
    

  * **min** (_float in_ _[__-inf_ _,__inf_ _]_) – min, any value in range [0,9999]

  * **max** (_float in_ _[__-inf_ _,__inf_ _]_) – max, any value in range [min+1,9998]


progress_update(_value_)
    

Update the progress feedback

Parameters:
    

**value** (_float in_ _[__-inf_ _,__inf_ _]_) – value, Any value between min and max as set in progress_begin()

progress_end()
    

Terminate progress report

_classmethod _invoke_props_popup(_operator_ , _event_)
    

Operator popup invoke (show operator properties and execute it automatically on changes)

Parameters:
    

  * **operator** ([`Operator`](../O/bpy.types.Operator.md#bpy.types.Operator "bpy.types.Operator")) – Operator to call

  * **event** ([`Event`](../E/bpy.types.Event.md#bpy.types.Event "bpy.types.Event")) – Event


Returns:
    

result

Return type:
    

enum set in [Operator Return Items](../../bpy_types_enum_items/operator_return_items.md#rna-enum-operator-return-items)

_classmethod _invoke_props_dialog(_operator_ , _*_ , _width =300_, _title =''_, _confirm_text =''_, _cancel_default =False_, _text_ctxt =''_, _translate =True_)
    

Operator dialog (non-autoexec popup) invoke (show operator properties and only execute it on click on OK button)

Parameters:
    

  * **operator** ([`Operator`](../O/bpy.types.Operator.md#bpy.types.Operator "bpy.types.Operator")) – Operator to call

  * **width** (_int in_ _[__0_ _,__inf_ _]__,__(__optional_ _)_) – Width of the popup

  * **title** (_string_ _,__(__optional_ _,__never None_ _)_) – Title, Optional text to show as title of the popup

  * **confirm_text** (_string_ _,__(__optional_ _,__never None_ _)_) – Confirm Text, Optional text to show instead to the default “OK” confirmation button text

  * **cancel_default** (_boolean_ _,__(__optional_ _)_) – cancel_default

  * **text_ctxt** (_string_ _,__(__optional_ _)_) – Override automatic translation context of the given text

  * **translate** (_boolean_ _,__(__optional_ _)_) – Translate the given text, when UI translation is enabled


Returns:
    

result

Return type:
    

enum set in [Operator Return Items](../../bpy_types_enum_items/operator_return_items.md#rna-enum-operator-return-items)

_classmethod _invoke_search_popup(_operator_)
    

Operator search popup invoke which searches values of the operator’s [`bpy.types.Operator.bl_property`](../O/bpy.types.Operator.md#bpy.types.Operator.bl_property "bpy.types.Operator.bl_property") (which must be an EnumProperty), executing it on confirmation

Parameters:
    

**operator** ([`Operator`](../O/bpy.types.Operator.md#bpy.types.Operator "bpy.types.Operator")) – Operator to call

_classmethod _invoke_popup(_operator_ , _*_ , _width =300_)
    

Operator popup invoke (only shows operator’s properties, without executing it)

Parameters:
    

  * **operator** ([`Operator`](../O/bpy.types.Operator.md#bpy.types.Operator "bpy.types.Operator")) – Operator to call

  * **width** (_int in_ _[__0_ _,__inf_ _]__,__(__optional_ _)_) – Width of the popup


Returns:
    

result

Return type:
    

enum set in [Operator Return Items](../../bpy_types_enum_items/operator_return_items.md#rna-enum-operator-return-items)

_classmethod _invoke_confirm(_operator_ , _event_ , _*_ , _title =''_, _message =''_, _confirm_text =''_, _icon ='NONE'_, _text_ctxt =''_, _translate =True_)
    

Operator confirmation popup (only to let user confirm the execution, no operator properties shown)

Parameters:
    

  * **operator** ([`Operator`](../O/bpy.types.Operator.md#bpy.types.Operator "bpy.types.Operator")) – Operator to call

  * **event** ([`Event`](../E/bpy.types.Event.md#bpy.types.Event "bpy.types.Event")) – Event

  * **title** (_string_ _,__(__optional_ _,__never None_ _)_) – Title, Optional text to show as title of the popup

  * **message** (_string_ _,__(__optional_ _,__never None_ _)_) – Message, Optional first line of content text

  * **confirm_text** (_string_ _,__(__optional_ _,__never None_ _)_) – Confirm Text, Optional text to show instead to the default “OK” confirmation button text

  * **icon** (enum in [`'NONE'`, `'WARNING'`, `'QUESTION'`, `'ERROR'`, `'INFO'`], (optional)) – Icon, Optional icon displayed in the dialog

  * **text_ctxt** (_string_ _,__(__optional_ _)_) – Override automatic translation context of the given text

  * **translate** (_boolean_ _,__(__optional_ _)_) – Translate the given text, when UI translation is enabled


Returns:
    

result

Return type:
    

enum set in [Operator Return Items](../../bpy_types_enum_items/operator_return_items.md#rna-enum-operator-return-items)

_classmethod _popmenu_begin__internal(_title_ , _*_ , _icon ='NONE'_)
    

popmenu_begin__internal

Parameters:
    

**icon** (enum in [Icon Items](../../bpy_types_enum_items/icon_items.md#rna-enum-icon-items), (optional)) – icon

Return type:
    

[`UIPopupMenu`](../U/bpy.types.UIPopupMenu.md#bpy.types.UIPopupMenu "bpy.types.UIPopupMenu"), (never None)

_classmethod _popmenu_end__internal(_menu_)
    

popmenu_end__internal

_classmethod _popover_begin__internal(_*_ , _ui_units_x =0_, _from_active_button =False_)
    

popover_begin__internal

Parameters:
    

  * **ui_units_x** (_int in_ _[__0_ _,__inf_ _]__,__(__optional_ _)_) – ui_units_x

  * **from_active_button** (_boolean_ _,__(__optional_ _)_) – Use Button, Use the active button for positioning


Return type:
    

[`UIPopover`](../U/bpy.types.UIPopover.md#bpy.types.UIPopover "bpy.types.UIPopover"), (never None)

_classmethod _popover_end__internal(_menu_ , _*_ , _keymap =None_)
    

popover_end__internal

Parameters:
    

**keymap** ([`KeyMap`](../K/bpy.types.KeyMap.md#bpy.types.KeyMap "bpy.types.KeyMap"), (optional)) – Key Map, Active key map

_classmethod _piemenu_begin__internal(_title_ , _*_ , _icon ='NONE'_, _event =None_)
    

piemenu_begin__internal

Parameters:
    

**icon** (enum in [Icon Items](../../bpy_types_enum_items/icon_items.md#rna-enum-icon-items), (optional)) – icon

Return type:
    

[`UIPieMenu`](../U/bpy.types.UIPieMenu.md#bpy.types.UIPieMenu "bpy.types.UIPieMenu"), (never None)

_classmethod _piemenu_end__internal(_menu_)
    

piemenu_end__internal

_classmethod _operator_properties_last(_operator_)
    

operator_properties_last

Return type:
    

[`OperatorProperties`](../O/bpy.types.OperatorProperties.md#bpy.types.OperatorProperties "bpy.types.OperatorProperties"), (never None)

print_undo_steps()
    

print_undo_steps

_classmethod _tag_script_reload()
    

Tag for refreshing the interface after scripts have been reloaded

popover(_draw_func_ , _*_ , _ui_units_x =0_, _keymap =None_, _from_active_button =False_)
    

popup_menu(_draw_func_ , _*_ , _title =''_, _icon ='NONE'_)
    

Popup menus can be useful for creating menus without having to register menu classes.

Note that they will not block the scripts execution, so the caller can’t wait for user input.
    
    
    import bpy
    
    
    def draw(self, context):
        self.layout.label(text="Hello World")
    
    
    bpy.context.window_manager.popup_menu(draw, title="Greeting", icon='INFO')
    

popup_menu_pie(_event_ , _draw_func_ , _*_ , _title =''_, _icon ='NONE'_)
    

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

_classmethod _draw_cursor_add(_callback_ , _args_ , _space_type_ , _region_type_)
    

Add a new draw cursor handler to this space type. It will be called every time the cursor for the specified region in the space type will be drawn. Note: All arguments are positional only for now.

Parameters:
    

  * **callback** (_Callable_ _[__...__,__Any_ _]_) – A function that will be called when the cursor is drawn. It gets the specified arguments as input with the mouse position (`tuple[int, int]`) as last argument.

  * **args** (_tuple_ _[__Any_ _,__...__]_) – Arguments that will be passed to the callback.

  * **space_type** (_str_) – The space type the callback draws in; for example `VIEW_3D`. ([`bpy.types.Space.type`](../S/bpy.types.Space.md#bpy.types.Space.type "bpy.types.Space.type"))

  * **region_type** (_str_) – The region type the callback draws in; usually `WINDOW`. ([`bpy.types.Region.type`](../R/bpy.types.Region.md#bpy.types.Region.type "bpy.types.Region.type"))


Returns:
    

Handler that can be removed later on.

Return type:
    

object

_classmethod _draw_cursor_remove(_handler_)
    

Remove a draw cursor handler that was added previously.

Parameters:
    

**handler** (_object_) – The draw cursor handler that should be removed.

## Inherited Properties

  * [`bpy_struct.id_data`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.id_data "bpy.types.bpy_struct.id_data")
  * [`ID.name`](../I/bpy.types.ID.md#bpy.types.ID.name "bpy.types.ID.name")
  * [`ID.name_full`](../I/bpy.types.ID.md#bpy.types.ID.name_full "bpy.types.ID.name_full")
  * [`ID.id_type`](../I/bpy.types.ID.md#bpy.types.ID.id_type "bpy.types.ID.id_type")
  * [`ID.session_uid`](../I/bpy.types.ID.md#bpy.types.ID.session_uid "bpy.types.ID.session_uid")
  * [`ID.is_evaluated`](../I/bpy.types.ID.md#bpy.types.ID.is_evaluated "bpy.types.ID.is_evaluated")
  * [`ID.original`](../I/bpy.types.ID.md#bpy.types.ID.original "bpy.types.ID.original")
  * [`ID.users`](../I/bpy.types.ID.md#bpy.types.ID.users "bpy.types.ID.users")
  * [`ID.use_fake_user`](../I/bpy.types.ID.md#bpy.types.ID.use_fake_user "bpy.types.ID.use_fake_user")
  * [`ID.use_extra_user`](../I/bpy.types.ID.md#bpy.types.ID.use_extra_user "bpy.types.ID.use_extra_user")
  * [`ID.is_embedded_data`](../I/bpy.types.ID.md#bpy.types.ID.is_embedded_data "bpy.types.ID.is_embedded_data")

| 

  * [`ID.is_linked_packed`](../I/bpy.types.ID.md#bpy.types.ID.is_linked_packed "bpy.types.ID.is_linked_packed")
  * [`ID.is_missing`](../I/bpy.types.ID.md#bpy.types.ID.is_missing "bpy.types.ID.is_missing")
  * [`ID.is_runtime_data`](../I/bpy.types.ID.md#bpy.types.ID.is_runtime_data "bpy.types.ID.is_runtime_data")
  * [`ID.is_editable`](../I/bpy.types.ID.md#bpy.types.ID.is_editable "bpy.types.ID.is_editable")
  * [`ID.tag`](../I/bpy.types.ID.md#bpy.types.ID.tag "bpy.types.ID.tag")
  * [`ID.is_library_indirect`](../I/bpy.types.ID.md#bpy.types.ID.is_library_indirect "bpy.types.ID.is_library_indirect")
  * [`ID.library`](../I/bpy.types.ID.md#bpy.types.ID.library "bpy.types.ID.library")
  * [`ID.library_weak_reference`](../I/bpy.types.ID.md#bpy.types.ID.library_weak_reference "bpy.types.ID.library_weak_reference")
  * [`ID.asset_data`](../I/bpy.types.ID.md#bpy.types.ID.asset_data "bpy.types.ID.asset_data")
  * [`ID.override_library`](../I/bpy.types.ID.md#bpy.types.ID.override_library "bpy.types.ID.override_library")
  * [`ID.preview`](../I/bpy.types.ID.md#bpy.types.ID.preview "bpy.types.ID.preview")

  
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
  * [`bpy_struct.keys`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.keys "bpy.types.bpy_struct.keys")
  * [`bpy_struct.path_from_id`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.path_from_id "bpy.types.bpy_struct.path_from_id")
  * [`bpy_struct.path_from_module`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.path_from_module "bpy.types.bpy_struct.path_from_module")
  * [`bpy_struct.path_resolve`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.path_resolve "bpy.types.bpy_struct.path_resolve")
  * [`bpy_struct.pop`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.pop "bpy.types.bpy_struct.pop")
  * [`bpy_struct.property_overridable_library_set`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.property_overridable_library_set "bpy.types.bpy_struct.property_overridable_library_set")
  * [`bpy_struct.property_unset`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.property_unset "bpy.types.bpy_struct.property_unset")
  * [`bpy_struct.rna_ancestors`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.rna_ancestors "bpy.types.bpy_struct.rna_ancestors")

| 

  * [`bpy_struct.type_recast`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.type_recast "bpy.types.bpy_struct.type_recast")
  * [`bpy_struct.values`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.values "bpy.types.bpy_struct.values")
  * [`ID.bl_system_properties_get`](../I/bpy.types.ID.md#bpy.types.ID.bl_system_properties_get "bpy.types.ID.bl_system_properties_get")
  * [`ID.rename`](../I/bpy.types.ID.md#bpy.types.ID.rename "bpy.types.ID.rename")
  * [`ID.evaluated_get`](../I/bpy.types.ID.md#bpy.types.ID.evaluated_get "bpy.types.ID.evaluated_get")
  * [`ID.copy`](../I/bpy.types.ID.md#bpy.types.ID.copy "bpy.types.ID.copy")
  * [`ID.asset_mark`](../I/bpy.types.ID.md#bpy.types.ID.asset_mark "bpy.types.ID.asset_mark")
  * [`ID.asset_clear`](../I/bpy.types.ID.md#bpy.types.ID.asset_clear "bpy.types.ID.asset_clear")
  * [`ID.asset_generate_preview`](../I/bpy.types.ID.md#bpy.types.ID.asset_generate_preview "bpy.types.ID.asset_generate_preview")
  * [`ID.override_create`](../I/bpy.types.ID.md#bpy.types.ID.override_create "bpy.types.ID.override_create")
  * [`ID.override_hierarchy_create`](../I/bpy.types.ID.md#bpy.types.ID.override_hierarchy_create "bpy.types.ID.override_hierarchy_create")
  * [`ID.user_clear`](../I/bpy.types.ID.md#bpy.types.ID.user_clear "bpy.types.ID.user_clear")
  * [`ID.user_remap`](../I/bpy.types.ID.md#bpy.types.ID.user_remap "bpy.types.ID.user_remap")
  * [`ID.make_local`](../I/bpy.types.ID.md#bpy.types.ID.make_local "bpy.types.ID.make_local")
  * [`ID.user_of_id`](../I/bpy.types.ID.md#bpy.types.ID.user_of_id "bpy.types.ID.user_of_id")
  * [`ID.animation_data_create`](../I/bpy.types.ID.md#bpy.types.ID.animation_data_create "bpy.types.ID.animation_data_create")
  * [`ID.animation_data_clear`](../I/bpy.types.ID.md#bpy.types.ID.animation_data_clear "bpy.types.ID.animation_data_clear")
  * [`ID.update_tag`](../I/bpy.types.ID.md#bpy.types.ID.update_tag "bpy.types.ID.update_tag")
  * [`ID.preview_ensure`](../I/bpy.types.ID.md#bpy.types.ID.preview_ensure "bpy.types.ID.preview_ensure")
  * [`ID.bl_rna_get_subclass`](../I/bpy.types.ID.md#bpy.types.ID.bl_rna_get_subclass "bpy.types.ID.bl_rna_get_subclass")
  * [`ID.bl_rna_get_subclass_py`](../I/bpy.types.ID.md#bpy.types.ID.bl_rna_get_subclass_py "bpy.types.ID.bl_rna_get_subclass_py")

  
---|---  
  
## References

  * [`BlendData.window_managers`](../B/bpy.types.BlendData.md#bpy.types.BlendData.window_managers "bpy.types.BlendData.window_managers")

| 

  * [`Context.window_manager`](../C/bpy.types.Context.md#bpy.types.Context.window_manager "bpy.types.Context.window_manager")

  
---|---
  *[*]: Keyword-only parameters separator (PEP 3102)
  *[/]: Positional-only parameter separator (PEP 570)
