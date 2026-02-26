# Function(bpy_struct)

base class — [[bpy_struct]]

_class _bpy.types.Function(_bpy_struct_)
    

RNA function definition

description
    

Description of the Function’s purpose

Type:
    

string, default “”, (readonly, never None)

identifier
    

Unique name used in the code and scripting

Type:
    

string, default “”, (readonly, never None)

is_registered
    

Function is registered as callback as part of type registration

Type:
    

boolean, default False, (readonly)

is_registered_optional
    

Function is optionally registered as callback part of type registration

Type:
    

boolean, default False, (readonly)

parameters
    

Parameters for the function

Type:
    

[[bpy_prop_collection]] of [[Property]], (readonly)

use_self
    

Function does not pass itself as an argument (becomes a static method in Python)

Type:
    

boolean, default False, (readonly)

use_self_type
    

Function passes itself type as an argument (becomes a class method in Python if use_self is false)

Type:
    

boolean, default False, (readonly)

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

  * [[Struct.functions]]

| 


  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
