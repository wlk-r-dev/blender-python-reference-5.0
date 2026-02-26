# ActionKeyframeStrip(ActionStrip)

base classes — [[bpy_struct]], [[ActionStrip]]

_class _bpy.types.ActionKeyframeStrip(_ActionStrip_)
    

Strip with a set of F-Curves for each action slot

channelbags
    

Type:
    

[[ActionChannelbags]] [[bpy_prop_collection]] of [[ActionChannelbag]], (readonly)

channelbag(_slot_ , _*_ , _ensure =False_)
    

Find the ActionChannelbag for a specific Slot

Parameters:
    

  * **slot** ([[ActionSlot]]) – Slot, The slot for which to find the channelbag

  * **ensure** (_boolean_ _,__(__optional_ _)_) – Create if necessary, Ensure the channelbag exists for this slot, creating it if necessary


Returns:
    

Channels

Return type:
    

[[ActionChannelbag]]

key_insert(_slot_ , _data_path_ , _array_index_ , _value_ , _time_)
    

key_insert

Parameters:
    

  * **slot** ([[ActionSlot]]) – Slot, The slot that identifies which ‘thing’ should be keyed

  * **data_path** (_string_ _,__(__never None_ _)_) – Data Path, F-Curve data path

  * **array_index** (_int in_ _[__-inf_ _,__inf_ _]_) – Array Index, Index of the animated array element, or -1 if the property is not an array

  * **value** (_float in_ _[__-inf_ _,__inf_ _]_) – Value to key, Value of the animated property

  * **time** (_float in_ _[__-inf_ _,__inf_ _]_) – Time of the key, Time, in frames, of the key


Returns:
    

Success, Whether the key was successfully inserted

Return type:
    

boolean

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

  * [[ActionStrip.type]]

  
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

| 

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
  * [[ActionStrip.bl_rna_get_subclass]]
  * [[ActionStrip.bl_rna_get_subclass_py]]

  
---|---
  *[*]: Keyword-only parameters separator (PEP 3102)
  *[/]: Positional-only parameter separator (PEP 570)
