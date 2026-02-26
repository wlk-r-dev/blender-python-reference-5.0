# IDOverrideLibrary(bpy_struct)

base class — [[bpy_struct]]

_class _bpy.types.IDOverrideLibrary(_bpy_struct_)
    

Struct gathering all data needed by overridden linked IDs

hierarchy_root
    

Library override ID used as root of the override hierarchy this ID is a member of

Type:
    

[[ID]], (readonly)

is_in_hierarchy
    

Whether this library override is defined as part of a library hierarchy, or as a single, isolated and autonomous override

Type:
    

boolean, default True

is_system_override
    

Whether this library override exists only for the override hierarchy, or if it is actually editable by the user

Type:
    

boolean, default False

properties
    

List of overridden properties

Type:
    

[[IDOverrideLibraryProperties]] [[bpy_prop_collection]] of [[IDOverrideLibraryProperty]], (readonly)

reference
    

Linked ID used as reference by this override

Type:
    

[[ID]], (readonly)

operations_update()
    

Update the library override operations based on the differences between this override ID and its reference

reset(_*_ , _do_hierarchy =True_, _set_system_override =False_)
    

Reset this override to match again its linked reference ID

Parameters:
    

  * **do_hierarchy** (_boolean_ _,__(__optional_ _)_) – Also reset all the dependencies of this override to match their reference linked IDs

  * **set_system_override** (_boolean_ _,__(__optional_ _)_) – Reset all user-editable overrides as (non-editable) system overrides


destroy(_*_ , _do_hierarchy =True_)
    

Delete this override ID and remap its usages to its linked reference ID instead

Parameters:
    

**do_hierarchy** (_boolean_ _,__(__optional_ _)_) – Also delete all the dependencies of this override and remap their usages to their reference linked IDs

resync(_scene_ , _*_ , _view_layer =None_, _residual_storage =None_, _do_hierarchy_enforce =False_, _do_whole_hierarchy =False_)
    

Resync the data-block and its sub-hierarchy, or the whole hierarchy if requested

Parameters:
    

  * **scene** ([[Scene]], (never None)) – The scene to operate in (for contextual things like keeping active object active, ensuring all overridden objects remain instantiated, etc.)

  * **view_layer** ([[ViewLayer]], (optional)) – The view layer to operate in (same usage as the `scene` data, in case it is not provided the scene’s collection will be used instead)

  * **residual_storage** ([[Collection]], (optional)) – Collection where to store objects that are instantiated in any other collection anymore (garbage collection, will be created if needed and none is provided)

  * **do_hierarchy_enforce** (_boolean_ _,__(__optional_ _)_) – Enforce restoring the dependency hierarchy between data-blocks to match the one from the reference linked hierarchy (WARNING: if some ID pointers have been purposely overridden, these will be reset to their default value)

  * **do_whole_hierarchy** (_boolean_ _,__(__optional_ _)_) – Resync the whole hierarchy this data-block belongs to, not only its own sub-hierarchy


Returns:
    

Success, Whether the resync process was successful or not

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

  * [[ID.override_library]]

| 


  
---|---
  *[*]: Keyword-only parameters separator (PEP 3102)
  *[/]: Positional-only parameter separator (PEP 570)
