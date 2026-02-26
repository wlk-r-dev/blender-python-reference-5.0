# KeyMap(bpy_struct)

base class — [`bpy_struct`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct "bpy.types.bpy_struct")

_class _bpy.types.KeyMap(_bpy_struct_)
    

Input configuration, including keymaps

bl_owner_id
    

Internal owner

Type:
    

string, default “”, (never None)

is_modal
    

Indicates that a keymap is used for translate modal events for an operator

Type:
    

boolean, default False, (readonly)

is_user_modified
    

Keymap is defined by the user

Type:
    

boolean, default False

keymap_items
    

Items in the keymap, linking an operator to an input event

Type:
    

[`KeyMapItems`](bpy.types.KeyMapItems.md#bpy.types.KeyMapItems "bpy.types.KeyMapItems") [`bpy_prop_collection`](../_other/bpy.types.bpy_prop_collection.md#bpy.types.bpy_prop_collection "bpy.types.bpy_prop_collection") of [`KeyMapItem`](bpy.types.KeyMapItem.md#bpy.types.KeyMapItem "bpy.types.KeyMapItem"), (readonly)

modal_event_values
    

Give access to the possible event values of this modal keymap’s items (#KeyMapItem.propvalue), for API introspection

Type:
    

[`bpy_prop_collection`](../_other/bpy.types.bpy_prop_collection.md#bpy.types.bpy_prop_collection "bpy.types.bpy_prop_collection") of [`EnumPropertyItem`](../E/bpy.types.EnumPropertyItem.md#bpy.types.EnumPropertyItem "bpy.types.EnumPropertyItem"), (readonly)

name
    

Name of the key map

Type:
    

string, default “”, (readonly, never None)

region_type
    

Optional region type keymap is associated with

Type:
    

enum in [Region Type Items](../../bpy_types_enum_items/region_type_items.md#rna-enum-region-type-items), default `'WINDOW'`, (readonly)

show_expanded_children
    

Children expanded in the user interface

Type:
    

boolean, default False

show_expanded_items
    

Expanded in the user interface

Type:
    

boolean, default False

space_type
    

Optional space type keymap is associated with

Type:
    

enum in [Space Type Items](../../bpy_types_enum_items/space_type_items.md#rna-enum-space-type-items), default `'EMPTY'`, (readonly)

active()
    

active

Returns:
    

Key Map, Active key map

Return type:
    

`KeyMap`

restore_to_default()
    

restore_to_default

restore_item_to_default(_item_)
    

restore_item_to_default

Parameters:
    

**item** ([`KeyMapItem`](bpy.types.KeyMapItem.md#bpy.types.KeyMapItem "bpy.types.KeyMapItem"), (never None)) – Item

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

  * [`GizmoGroup.setup_keymap`](../G/bpy.types.GizmoGroup.md#bpy.types.GizmoGroup.setup_keymap "bpy.types.GizmoGroup.setup_keymap")
  * [`KeyConfig.keymaps`](bpy.types.KeyConfig.md#bpy.types.KeyConfig.keymaps "bpy.types.KeyConfig.keymaps")
  * [`KeyConfigurations.find_item_from_operator`](bpy.types.KeyConfigurations.md#bpy.types.KeyConfigurations.find_item_from_operator "bpy.types.KeyConfigurations.find_item_from_operator")
  * `KeyMap.active`
  * [`KeyMapItems.find_match`](bpy.types.KeyMapItems.md#bpy.types.KeyMapItems.find_match "bpy.types.KeyMapItems.find_match")
  * [`KeyMaps.find`](bpy.types.KeyMaps.md#bpy.types.KeyMaps.find "bpy.types.KeyMaps.find")

| 

  * [`KeyMaps.find_match`](bpy.types.KeyMaps.md#bpy.types.KeyMaps.find_match "bpy.types.KeyMaps.find_match")
  * [`KeyMaps.find_match`](bpy.types.KeyMaps.md#bpy.types.KeyMaps.find_match "bpy.types.KeyMaps.find_match")
  * [`KeyMaps.find_modal`](bpy.types.KeyMaps.md#bpy.types.KeyMaps.find_modal "bpy.types.KeyMaps.find_modal")
  * [`KeyMaps.new`](bpy.types.KeyMaps.md#bpy.types.KeyMaps.new "bpy.types.KeyMaps.new")
  * [`KeyMaps.remove`](bpy.types.KeyMaps.md#bpy.types.KeyMaps.remove "bpy.types.KeyMaps.remove")
  * [`WindowManager.popover_end__internal`](../W/bpy.types.WindowManager.md#bpy.types.WindowManager.popover_end__internal "bpy.types.WindowManager.popover_end__internal")

  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
