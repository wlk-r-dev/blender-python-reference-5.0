# KeyMapItems(bpy_struct)

base class — [[bpy_struct]]

_class _bpy.types.KeyMapItems(_bpy_struct_)
    

Collection of keymap items

new(_idname_ , _type_ , _value_ , _*_ , _any =False_, _shift =0_, _ctrl =0_, _alt =0_, _oskey =0_, _hyper =0_, _key_modifier ='NONE'_, _direction ='ANY'_, _repeat =False_, _head =False_)
    

new

Parameters:
    

  * **idname** (_string_ _,__(__never None_ _)_) – Operator Identifier

  * **type** (enum in [Event Type Items](../../bpy_types_enum_items/event_type_items.md#rna-enum-event-type-items)) – Type

  * **value** (enum in [Event Value Items](../../bpy_types_enum_items/event_value_items.md#rna-enum-event-value-items)) – Value

  * **any** (_boolean_ _,__(__optional_ _)_) – Any

  * **shift** (_int in_ _[__-1_ _,__1_ _]__,__(__optional_ _)_) – Shift

  * **ctrl** (_int in_ _[__-1_ _,__1_ _]__,__(__optional_ _)_) – Ctrl

  * **alt** (_int in_ _[__-1_ _,__1_ _]__,__(__optional_ _)_) – Alt

  * **oskey** (_int in_ _[__-1_ _,__1_ _]__,__(__optional_ _)_) – OS Key

  * **hyper** (_int in_ _[__-1_ _,__1_ _]__,__(__optional_ _)_) – Hyper

  * **key_modifier** (enum in [Event Type Items](../../bpy_types_enum_items/event_type_items.md#rna-enum-event-type-items), (optional)) – Key Modifier

  * **direction** (enum in [Event Direction Items](../../bpy_types_enum_items/event_direction_items.md#rna-enum-event-direction-items), (optional)) – Direction

  * **repeat** (_boolean_ _,__(__optional_ _)_) – Repeat, When set, accept key-repeat events

  * **head** (_boolean_ _,__(__optional_ _)_) – At Head, Force item to be added at start (not end) of key map so that it doesn’t get blocked by an existing key map item


Returns:
    

Item, Added key map item

Return type:
    

[[KeyMapItem]]

new_modal(_propvalue_ , _type_ , _value_ , _*_ , _any =False_, _shift =0_, _ctrl =0_, _alt =0_, _oskey =0_, _hyper =0_, _key_modifier ='NONE'_, _direction ='ANY'_, _repeat =False_)
    

new_modal

Parameters:
    

  * **propvalue** (_string_ _,__(__never None_ _)_) – Property Value

  * **type** (enum in [Event Type Items](../../bpy_types_enum_items/event_type_items.md#rna-enum-event-type-items)) – Type

  * **value** (enum in [Event Value Items](../../bpy_types_enum_items/event_value_items.md#rna-enum-event-value-items)) – Value

  * **any** (_boolean_ _,__(__optional_ _)_) – Any

  * **shift** (_int in_ _[__-1_ _,__1_ _]__,__(__optional_ _)_) – Shift

  * **ctrl** (_int in_ _[__-1_ _,__1_ _]__,__(__optional_ _)_) – Ctrl

  * **alt** (_int in_ _[__-1_ _,__1_ _]__,__(__optional_ _)_) – Alt

  * **oskey** (_int in_ _[__-1_ _,__1_ _]__,__(__optional_ _)_) – OS Key

  * **hyper** (_int in_ _[__-1_ _,__1_ _]__,__(__optional_ _)_) – Hyper

  * **key_modifier** (enum in [Event Type Items](../../bpy_types_enum_items/event_type_items.md#rna-enum-event-type-items), (optional)) – Key Modifier

  * **direction** (enum in [Event Direction Items](../../bpy_types_enum_items/event_direction_items.md#rna-enum-event-direction-items), (optional)) – Direction

  * **repeat** (_boolean_ _,__(__optional_ _)_) – Repeat, When set, accept key-repeat events


Returns:
    

Item, Added key map item

Return type:
    

[[KeyMapItem]]

new_from_item(_item_ , _*_ , _head =False_)
    

new_from_item

Parameters:
    

  * **item** ([[KeyMapItem]], (never None)) – Item, Item to use as a reference

  * **head** (_boolean_ _,__(__optional_ _)_) – At Head


Returns:
    

Item, Added key map item

Return type:
    

[[KeyMapItem]]

remove(_item_)
    

remove

Parameters:
    

**item** ([[KeyMapItem]], (never None)) – Item

from_id(_id_)
    

from_id

Parameters:
    

**id** (_int in_ _[__-inf_ _,__inf_ _]_) – id, ID of the item

Returns:
    

Item

Return type:
    

[[KeyMapItem]]

find_from_operator(_idname_ , _*_ , _properties =None_, _include ={'ACTIONZONE', 'KEYBOARD', 'MOUSE', 'NDOF'}_, _exclude ={}_)
    

find_from_operator

Parameters:
    

  * **idname** (_string_ _,__(__never None_ _)_) – Operator Identifier

  * **include** (enum set in [Event Type Mask Items](../../bpy_types_enum_items/event_type_mask_items.md#rna-enum-event-type-mask-items), (optional)) – Include

  * **exclude** (enum set in [Event Type Mask Items](../../bpy_types_enum_items/event_type_mask_items.md#rna-enum-event-type-mask-items), (optional)) – Exclude


Return type:
    

[[KeyMapItem]]

find_match(_keymap_ , _item_)
    

find_match

Parameters:
    

  * **keymap** ([[KeyMap]]) – The matching keymap

  * **item** ([[KeyMapItem]]) – The matching keymap item


Returns:
    

The keymap item from this keymap which matches the keymap item from the arguments passed in

Return type:
    

[[KeyMapItem]]

match_event(_event_)
    

match_event

Return type:
    

[[KeyMapItem]]

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

  * [[KeyMap.keymap_items]]

| 


  
---|---
  *[*]: Keyword-only parameters separator (PEP 3102)
  *[/]: Positional-only parameter separator (PEP 570)
