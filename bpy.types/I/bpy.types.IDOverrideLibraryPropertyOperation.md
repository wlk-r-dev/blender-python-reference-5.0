# IDOverrideLibraryPropertyOperation(bpy_struct)

base class — [[bpy_struct]]

_class _bpy.types.IDOverrideLibraryPropertyOperation(_bpy_struct_)
    

Description of an override operation over an overridden property

flag
    

Status flags

  * `MANDATORY` Mandatory – For templates, prevents the user from removing predefined operation (NOT USED).

  * `LOCKED` Locked – Prevents the user from modifying that override operation (NOT USED).

  * `IDPOINTER_MATCH_REFERENCE` Match Reference – The ID pointer overridden by this operation is expected to match the reference hierarchy.

  * `IDPOINTER_ITEM_USE_ID` ID Item Use ID Pointer – RNA collections of IDs only, the reference to the item also uses the ID pointer itself, not only its name.


Type:
    

enum set in {`'MANDATORY'`, `'LOCKED'`, `'IDPOINTER_MATCH_REFERENCE'`, `'IDPOINTER_ITEM_USE_ID'`}, default set(), (readonly)

operation
    

What override operation is performed

  * `NOOP` No-Op – Does nothing, prevents adding actual overrides (NOT USED).

  * `REPLACE` Replace – Replace value of reference by overriding one.

  * `DIFF_ADD` Differential – Stores and apply difference between reference and local value (NOT USED).

  * `DIFF_SUB` Differential – Stores and apply difference between reference and local value (NOT USED).

  * `FACT_MULTIPLY` Factor – Stores and apply multiplication factor between reference and local value (NOT USED).

  * `INSERT_AFTER` Insert After – Insert a new item into collection after the one referenced in subitem_reference_name/_id or _index.

  * `INSERT_BEFORE` Insert Before – Insert a new item into collection before the one referenced in subitem_reference_name/_id or _index (NOT USED).


Type:
    

enum in [`'NOOP'`, `'REPLACE'`, `'DIFF_ADD'`, `'DIFF_SUB'`, `'FACT_MULTIPLY'`, `'INSERT_AFTER'`, `'INSERT_BEFORE'`], default `'REPLACE'`, (readonly)

subitem_local_id
    

Collection of IDs only, used to disambiguate between potential IDs with same name from different libraries

Type:
    

[[ID]], (readonly)

subitem_local_index
    

Used to handle changes into collection

Type:
    

int in [-1, inf], default -1, (readonly)

subitem_local_name
    

Used to handle changes into collection

Type:
    

string, default “”, (readonly, never None)

subitem_reference_id
    

Collection of IDs only, used to disambiguate between potential IDs with same name from different libraries

Type:
    

[[ID]], (readonly)

subitem_reference_index
    

Used to handle changes into collection

Type:
    

int in [-1, inf], default -1, (readonly)

subitem_reference_name
    

Used to handle changes into collection

Type:
    

string, default “”, (readonly, never None)

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

  * [[IDOverrideLibraryProperty.operations]]
  * [[IDOverrideLibraryPropertyOperations.add]]

| 

  * [[IDOverrideLibraryPropertyOperations.remove]]

  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
