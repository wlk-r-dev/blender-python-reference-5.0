# KeyMap(bpy_struct)

base class — [[bpy_struct]]

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
    

[[KeyMapItems]] [[bpy_prop_collection]] of [[KeyMapItem]], (readonly)

modal_event_values
    

Give access to the possible event values of this modal keymap’s items (#KeyMapItem.propvalue), for API introspection

Type:
    

[[bpy_prop_collection]] of [[EnumPropertyItem]], (readonly)

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
    

**item** ([[KeyMapItem]], (never None)) – Item

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

  * [[GizmoGroup.setup_keymap]]
  * [[KeyConfig.keymaps]]
  * [[KeyConfigurations.find_item_from_operator]]
  * `KeyMap.active`
  * [[KeyMapItems.find_match]]
  * [[KeyMaps.find]]

| 

  * [[KeyMaps.find_match]]
  * [[KeyMaps.find_match]]
  * [[KeyMaps.find_modal]]
  * [[KeyMaps.new]]
  * [[KeyMaps.remove]]
  * [[WindowManager.popover_end__internal]]

  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
