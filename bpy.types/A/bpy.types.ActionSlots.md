# ActionSlots(bpy_struct)

base class — [[bpy_struct]]

_class _bpy.types.ActionSlots(_bpy_struct_)
    

Collection of action slots

active
    

Active slot for this action

Type:
    

[[ActionSlot]]

new(_id_type_ , _name_)
    

Add a slot to the Action

Parameters:
    

  * **id_type** (enum in [Id Type Items](../../bpy_types_enum_items/id_type_items.md#rna-enum-id-type-items)) – Data-block Type, The data-block type that the slot is intended for. This is combined with the slot name to create the slot’s unique identifier, and is also used to limit (on a best-effort basis) which data-blocks the slot can be assigned to.

  * **name** (_string_ _,__(__never None_ _)_) – Name, Name of the slot. This will be made unique within the Action among slots of the same type


Returns:
    

Newly created action slot

Return type:
    

[[ActionSlot]]

remove(_action_slot_)
    

Remove the slot from the Action, including all animation that is associated with that slot

Parameters:
    

**action_slot** ([[ActionSlot]]) – Action Slot, The slot to remove

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

  * [[Action.slots]]

| 


  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
