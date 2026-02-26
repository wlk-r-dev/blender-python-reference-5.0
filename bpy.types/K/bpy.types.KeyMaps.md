# KeyMaps(bpy_struct)

base class — [[bpy_struct]]

_class _bpy.types.KeyMaps(_bpy_struct_)
    

Collection of keymaps

new(_name_ , _*_ , _space_type ='EMPTY'_, _region_type ='WINDOW'_, _modal =False_, _tool =False_)
    

Ensure the keymap exists. This will return the one with the given name/space type/region type, or create a new one if it does not exist yet.

Parameters:
    

  * **name** (_string_ _,__(__never None_ _)_) – Name

  * **space_type** (enum in [Space Type Items](../../bpy_types_enum_items/space_type_items.md#rna-enum-space-type-items), (optional)) – Space Type

  * **region_type** (enum in [Region Type Items](../../bpy_types_enum_items/region_type_items.md#rna-enum-region-type-items), (optional)) – Region Type

  * **modal** (_boolean_ _,__(__optional_ _)_) – Modal, Keymap for modal operators

  * **tool** (_boolean_ _,__(__optional_ _)_) – Tool, Keymap for active tools


Returns:
    

Key Map, Added key map

Return type:
    

[[KeyMap]]

remove(_keymap_)
    

remove

Parameters:
    

**keymap** ([[KeyMap]], (never None)) – Key Map, Removed key map

clear()
    

Remove all keymaps.

find(_name_ , _*_ , _space_type ='EMPTY'_, _region_type ='WINDOW'_)
    

find

Parameters:
    

  * **name** (_string_ _,__(__never None_ _)_) – Name

  * **space_type** (enum in [Space Type Items](../../bpy_types_enum_items/space_type_items.md#rna-enum-space-type-items), (optional)) – Space Type

  * **region_type** (enum in [Region Type Items](../../bpy_types_enum_items/region_type_items.md#rna-enum-region-type-items), (optional)) – Region Type


Returns:
    

Key Map, Corresponding key map

Return type:
    

[[KeyMap]]

find_match(_keymap_)
    

find_match

Parameters:
    

**keymap** ([[KeyMap]]) – Key Map, The key map for comparison

Returns:
    

Key Map, Corresponding key map

Return type:
    

[[KeyMap]]

find_modal(_name_)
    

find_modal

Parameters:
    

**name** (_string_ _,__(__never None_ _)_) – Operator Name

Returns:
    

Key Map, Corresponding key map

Return type:
    

[[KeyMap]]

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

  * [[KeyConfig.keymaps]]

| 


  
---|---
  *[*]: Keyword-only parameters separator (PEP 3102)
  *[/]: Positional-only parameter separator (PEP 570)
