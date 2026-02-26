# KeyMapItem(bpy_struct)

base class — [[bpy_struct]]

_class _bpy.types.KeyMapItem(_bpy_struct_)
    

Item in a Key Map

active
    

Activate or deactivate item

Type:
    

boolean, default False

alt
    

Alt key pressed, -1 for any state

Type:
    

int in [-1, 1], default 0

alt_ui
    

Alt key pressed

Type:
    

boolean, default False

any
    

Any modifier keys pressed

Type:
    

boolean, default False

ctrl
    

Control key pressed, -1 for any state

Type:
    

int in [-1, 1], default 0

ctrl_ui
    

Control key pressed

Type:
    

boolean, default False

direction
    

The direction (only applies to drag events)

Type:
    

enum in [Event Direction Items](../../bpy_types_enum_items/event_direction_items.md#rna-enum-event-direction-items), default `'ANY'`

hyper
    

Hyper key pressed, -1 for any state

Type:
    

int in [-1, 1], default 0

hyper_ui
    

Hyper key pressed. An additional modifier which can be configured on Linux, typically replacing CapsLock

Type:
    

boolean, default False

id
    

ID of the item

Type:
    

int in [-32768, 32767], default 0, (readonly)

idname
    

Identifier of operator to call on input event

Type:
    

string, default “”, (never None)

is_user_defined
    

Is this keymap item user defined (does not just replace a builtin item)

Type:
    

boolean, default False, (readonly)

is_user_modified
    

Is this keymap item modified by the user

Type:
    

boolean, default False, (readonly)

key_modifier
    

Regular key pressed as a modifier

Type:
    

enum in [Event Type Items](../../bpy_types_enum_items/event_type_items.md#rna-enum-event-type-items), default `'NONE'`

map_type
    

Type of event mapping

Type:
    

enum in [`'KEYBOARD'`, `'MOUSE'`, `'NDOF'`, `'TEXTINPUT'`, `'TIMER'`], default `'KEYBOARD'`

name
    

Name of operator (translated) to call on input event

Type:
    

string, default “”, (readonly, never None)

oskey
    

Operating system key pressed, -1 for any state

Type:
    

int in [-1, 1], default 0

oskey_ui
    

Operating system key pressed

Type:
    

boolean, default False

properties
    

Properties to set when the operator is called

Type:
    

[[OperatorProperties]], (readonly)

propvalue
    

The value this event translates to in a modal keymap

Type:
    

enum in [Keymap Propvalue Items](../../bpy_types_enum_items/keymap_propvalue_items.md#rna-enum-keymap-propvalue-items), default `'NONE'`

repeat
    

Active on key-repeat events (when a key is held)

Type:
    

boolean, default False

shift
    

Shift key pressed, -1 for any state

Type:
    

int in [-1, 1], default 0

shift_ui
    

Shift key pressed

Type:
    

boolean, default False

show_expanded
    

Show key map event and property details in the user interface

Type:
    

boolean, default False

type
    

Type of event

Type:
    

enum in [Event Type Items](../../bpy_types_enum_items/event_type_items.md#rna-enum-event-type-items), default `'NONE'`

value
    

Type:
    

enum in [Event Value Items](../../bpy_types_enum_items/event_value_items.md#rna-enum-event-value-items), default `'NOTHING'`

compare(_item_)
    

compare

Parameters:
    

**item** (`KeyMapItem`) – Item

Returns:
    

Comparison result

Return type:
    

boolean

to_string(_*_ , _compact =False_)
    

to_string

Parameters:
    

**compact** (_boolean_ _,__(__optional_ _)_) – Compact

Returns:
    

result

Return type:
    

string, (never None)

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

  * [[KeyConfigurations.find_item_from_operator]]
  * [[KeyMap.keymap_items]]
  * [[KeyMap.restore_item_to_default]]
  * `KeyMapItem.compare`
  * [[KeyMapItems.find_from_operator]]
  * [[KeyMapItems.find_match]]
  * [[KeyMapItems.find_match]]
  * [[KeyMapItems.from_id]]

| 

  * [[KeyMapItems.match_event]]
  * [[KeyMapItems.new]]
  * [[KeyMapItems.new_from_item]]
  * [[KeyMapItems.new_from_item]]
  * [[KeyMapItems.new_modal]]
  * [[KeyMapItems.remove]]
  * [[UILayout.template_event_from_keymap_item]]
  * [[UILayout.template_keymap_item_properties]]

  
---|---
  *[*]: Keyword-only parameters separator (PEP 3102)
  *[/]: Positional-only parameter separator (PEP 570)
