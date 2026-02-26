# IDOverrideLibraryPropertyOperations(bpy_struct)

base class — [`bpy_struct`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct "bpy.types.bpy_struct")

_class _bpy.types.IDOverrideLibraryPropertyOperations(_bpy_struct_)
    

Collection of override operations

add(_operation_ , _*_ , _use_id =False_, _subitem_reference_name =''_, _subitem_local_name =''_, _subitem_reference_id =None_, _subitem_local_id =None_, _subitem_reference_index =-1_, _subitem_local_index =-1_)
    

Add a new operation

Parameters:
    

  * **operation** (enum in [`'NOOP'`, `'REPLACE'`, `'DIFF_ADD'`, `'DIFF_SUB'`, `'FACT_MULTIPLY'`, `'INSERT_AFTER'`, `'INSERT_BEFORE'`]) – 

Operation, What override operation is performed

    * `NOOP` No-Op – Does nothing, prevents adding actual overrides (NOT USED).

    * `REPLACE` Replace – Replace value of reference by overriding one.

    * `DIFF_ADD` Differential – Stores and apply difference between reference and local value (NOT USED).

    * `DIFF_SUB` Differential – Stores and apply difference between reference and local value (NOT USED).

    * `FACT_MULTIPLY` Factor – Stores and apply multiplication factor between reference and local value (NOT USED).

    * `INSERT_AFTER` Insert After – Insert a new item into collection after the one referenced in subitem_reference_name/_id or _index.

    * `INSERT_BEFORE` Insert Before – Insert a new item into collection before the one referenced in subitem_reference_name/_id or _index (NOT USED).

  * **use_id** (_boolean_ _,__(__optional_ _)_) – Use ID Pointer Subitem, Whether the found or created liboverride operation should use ID pointers or not

  * **subitem_reference_name** (_string_ _,__(__optional_ _,__never None_ _)_) – Subitem Reference Name, Used to handle insertions or ID replacements into collection

  * **subitem_local_name** (_string_ _,__(__optional_ _,__never None_ _)_) – Subitem Local Name, Used to handle insertions or ID replacements into collection

  * **subitem_reference_id** ([`ID`](bpy.types.ID.md#bpy.types.ID "bpy.types.ID"), (optional)) – Subitem Reference ID, Used to handle ID replacements into collection

  * **subitem_local_id** ([`ID`](bpy.types.ID.md#bpy.types.ID "bpy.types.ID"), (optional)) – Subitem Local ID, Used to handle ID replacements into collection

  * **subitem_reference_index** (_int in_ _[__-1_ _,__inf_ _]__,__(__optional_ _)_) – Subitem Reference Index, Used to handle insertions or ID replacements into collection

  * **subitem_local_index** (_int in_ _[__-1_ _,__inf_ _]__,__(__optional_ _)_) – Subitem Local Index, Used to handle insertions or ID replacements into collection


Returns:
    

New Operation, Created operation

Return type:
    

[`IDOverrideLibraryPropertyOperation`](bpy.types.IDOverrideLibraryPropertyOperation.md#bpy.types.IDOverrideLibraryPropertyOperation "bpy.types.IDOverrideLibraryPropertyOperation")

remove(_operation_)
    

Remove and delete an operation

Parameters:
    

**operation** ([`IDOverrideLibraryPropertyOperation`](bpy.types.IDOverrideLibraryPropertyOperation.md#bpy.types.IDOverrideLibraryPropertyOperation "bpy.types.IDOverrideLibraryPropertyOperation")) – Operation, Override operation to be deleted

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

  * [`IDOverrideLibraryProperty.operations`](bpy.types.IDOverrideLibraryProperty.md#bpy.types.IDOverrideLibraryProperty.operations "bpy.types.IDOverrideLibraryProperty.operations")

| 


  
---|---
  *[*]: Keyword-only parameters separator (PEP 3102)
  *[/]: Positional-only parameter separator (PEP 570)
