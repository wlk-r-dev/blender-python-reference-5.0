# KeyingSetInfo(bpy_struct)

base class — [[bpy_struct]]

_class _bpy.types.KeyingSetInfo(_bpy_struct_)
    

Callback function defines for builtin Keying Sets

bl_description
    

A short description of the keying set

Type:
    

string, default “”, (never None)

bl_idname
    

If this is set, the Keying Set gets a custom ID, otherwise it takes the name of the class used to define the Keying Set (for example, if the class name is “BUILTIN_KSI_location”, and bl_idname is not set by the script, then bl_idname = “BUILTIN_KSI_location”)

Type:
    

string, default “”, (never None)

bl_label
    

Type:
    

string, default “”, (never None)

bl_options
    

Keying Set options to use when inserting keyframes

Type:
    

enum set in [Keying Flag Items](../../bpy_types_enum_items/keying_flag_items.md#rna-enum-keying-flag-items), default set()

poll(_context_)
    

Test if Keying Set can be used or not

Return type:
    

boolean

iterator(_context_ , _ks_)
    

Call generate() on the structs which have properties to be keyframed

generate(_context_ , _ks_ , _data_)
    

Add Paths to the Keying Set to keyframe the properties of the given data

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

  * [[KeyingSet.type_info]]

| 


  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
