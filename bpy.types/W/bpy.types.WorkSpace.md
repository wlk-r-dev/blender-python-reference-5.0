# WorkSpace(ID)

base classes — [[bpy_struct]], [[ID]]

_class _bpy.types.WorkSpace(_ID_)
    

Workspace data-block, defining the working environment for the user

active_addon
    

Active Add-on in the Workspace Add-ons filter

Type:
    

int in [-inf, inf], default 0

asset_library_reference
    

Active asset library to show in the UI, not used by the Asset Browser (which has its own active asset library)

  * `ALL` All Libraries – Show assets from all of the listed asset libraries.

  * `LOCAL` Current File – Show the assets currently available in this Blender session.

  * `ESSENTIALS` Essentials – Show the basic building blocks and utilities coming with Blender.

  * `CUSTOM` Custom – Show assets from the asset libraries configured in the Preferences.


Type:
    

enum in [`'ALL'`, `'LOCAL'`, `'ESSENTIALS'`, `'CUSTOM'`], default `'ALL'`

object_mode
    

Switch to this object mode when activating the workspace

Type:
    

enum in [Workspace Object Mode Items](../../bpy_types_enum_items/workspace_object_mode_items.md#rna-enum-workspace-object-mode-items), default `'OBJECT'`

owner_ids
    

Type:
    

[[wmOwnerIDs]] [[bpy_prop_collection]] of [[wmOwnerID]], (readonly)

screens
    

Screen layouts of a workspace

Type:
    

[[bpy_prop_collection]] of [[Screen]], (readonly)

sequencer_scene
    

Type:
    

[[Scene]]

tools
    

Type:
    

[[wmTools]] [[bpy_prop_collection]] of [[WorkSpaceTool]], (readonly)

use_filter_by_owner
    

Filter the UI by tags

Type:
    

boolean, default False

use_pin_scene
    

Remember the last used scene for the workspace and switch to it whenever this workspace is activated again

Type:
    

boolean, default False

use_scene_time_sync
    

Set the active scene and time based on the current scene strip

Type:
    

boolean, default False

_classmethod _status_text_set_internal(_text_)
    

Set the status bar text, typically key shortcuts for modal operators

Parameters:
    

**text** (_string_) – Text, New string for the status bar, None clears the text

status_text_set(_text_)
    

Set the status text or None to clear, When text is a function, this will be called with the (header, context) arguments.

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
  * [[ID.name]]
  * [[ID.name_full]]
  * [[ID.id_type]]
  * [[ID.session_uid]]
  * [[ID.is_evaluated]]
  * [[ID.original]]
  * [[ID.users]]
  * [[ID.use_fake_user]]
  * [[ID.use_extra_user]]
  * [[ID.is_embedded_data]]

| 

  * [[ID.is_linked_packed]]
  * [[ID.is_missing]]
  * [[ID.is_runtime_data]]
  * [[ID.is_editable]]
  * [[ID.tag]]
  * [[ID.is_library_indirect]]
  * [[ID.library]]
  * [[ID.library_weak_reference]]
  * [[ID.asset_data]]
  * [[ID.override_library]]
  * [[ID.preview]]

  
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
  * [[bpy_struct.keys]]
  * [[bpy_struct.path_from_id]]
  * [[bpy_struct.path_from_module]]
  * [[bpy_struct.path_resolve]]
  * [[bpy_struct.pop]]
  * [[bpy_struct.property_overridable_library_set]]
  * [[bpy_struct.property_unset]]
  * [[bpy_struct.rna_ancestors]]

| 

  * [[bpy_struct.type_recast]]
  * [[bpy_struct.values]]
  * [[ID.bl_system_properties_get]]
  * [[ID.rename]]
  * [[ID.evaluated_get]]
  * [[ID.copy]]
  * [[ID.asset_mark]]
  * [[ID.asset_clear]]
  * [[ID.asset_generate_preview]]
  * [[ID.override_create]]
  * [[ID.override_hierarchy_create]]
  * [[ID.user_clear]]
  * [[ID.user_remap]]
  * [[ID.make_local]]
  * [[ID.user_of_id]]
  * [[ID.animation_data_create]]
  * [[ID.animation_data_clear]]
  * [[ID.update_tag]]
  * [[ID.preview_ensure]]
  * [[ID.bl_rna_get_subclass]]
  * [[ID.bl_rna_get_subclass_py]]

  
---|---  
  
## References

  * [[BlendData.workspaces]]
  * [[Context.workspace]]

| 

  * [[Window.workspace]]

  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
