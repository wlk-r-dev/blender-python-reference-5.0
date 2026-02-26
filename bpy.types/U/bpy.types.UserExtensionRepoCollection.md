# UserExtensionRepoCollection(bpy_struct)

base class — [[bpy_struct]]

_class _bpy.types.UserExtensionRepoCollection(_bpy_struct_)
    

Collection of user extension repositories

_classmethod _new(_*_ , _name =''_, _module =''_, _custom_directory =''_, _remote_url =''_, _source ='USER'_)
    

Add a new repository

Parameters:
    

  * **name** (_string_ _,__(__optional_ _,__never None_ _)_) – Name

  * **module** (_string_ _,__(__optional_ _,__never None_ _)_) – Module

  * **custom_directory** (_string_ _,__(__optional_ _,__never None_ _)_) – Custom Directory

  * **remote_url** (_string_ _,__(__optional_ _,__never None_ _)_) – Remote URL

  * **source** (enum in [`'USER'`, `'SYSTEM'`], (optional)) – 

Source, How the repository is managed

    * `USER` User – Repository managed by the user, stored in user directories.

    * `SYSTEM` System – Read-only repository provided by the system.


Returns:
    

Newly added repository

Return type:
    

[[UserExtensionRepo]]

_classmethod _remove(_repo_)
    

Remove repos

Parameters:
    

**repo** ([[UserExtensionRepo]], (never None)) – Repository to remove

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

  * [[PreferencesExtensions.repos]]

| 


  
---|---
  *[*]: Keyword-only parameters separator (PEP 3102)
  *[/]: Positional-only parameter separator (PEP 570)
