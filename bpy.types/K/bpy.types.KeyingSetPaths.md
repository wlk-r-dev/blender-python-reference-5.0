# KeyingSetPaths(bpy_struct)

base class — [[bpy_struct]]

_class _bpy.types.KeyingSetPaths(_bpy_struct_)
    

Collection of keying set paths

active
    

Active Keying Set used to insert/delete keyframes

Type:
    

[[KeyingSetPath]]

active_index
    

Current Keying Set index

Type:
    

int in [-inf, inf], default 0

add(_target_id_ , _data_path_ , _*_ , _index =-1_, _group_method ='KEYINGSET'_, _group_name =''_)
    

Add a new path for the Keying Set

Parameters:
    

  * **target_id** ([[ID]]) – Target ID, ID data-block for the destination

  * **data_path** (_string_ _,__(__never None_ _)_) – Data-Path, RNA-Path to destination property

  * **index** (_int in_ _[__-1_ _,__inf_ _]__,__(__optional_ _)_) – Index, The index of the destination property (i.e. axis of Location/Rotation/etc.), or -1 for the entire array

  * **group_method** (enum in [Keyingset Path Grouping Items](../../bpy_types_enum_items/keyingset_path_grouping_items.md#rna-enum-keyingset-path-grouping-items), (optional)) – Grouping Method, Method used to define which Group-name to use

  * **group_name** (_string_ _,__(__optional_ _,__never None_ _)_) – Group Name, Name of Action Group to assign destination to (only if grouping mode is to use this name)


Returns:
    

New Path, Path created and added to the Keying Set

Return type:
    

[[KeyingSetPath]]

remove(_path_)
    

Remove the given path from the Keying Set

Parameters:
    

**path** ([[KeyingSetPath]], (never None)) – Path

clear()
    

Remove all the paths from the Keying Set

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

  * [[KeyingSet.paths]]

| 


  
---|---
  *[*]: Keyword-only parameters separator (PEP 3102)
  *[/]: Positional-only parameter separator (PEP 570)
