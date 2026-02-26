# XrActionMapBindings(bpy_struct)

base class — [[bpy_struct]]

_class _bpy.types.XrActionMapBindings(_bpy_struct_)
    

Collection of XR action map bindings

new(_name_ , _replace_existing_)
    

new

Parameters:
    

  * **name** (_string_ _,__(__never None_ _)_) – Name of the action map binding

  * **replace_existing** (_boolean_) – Replace Existing, Replace any existing binding with the same name


Returns:
    

Binding, Added action map binding

Return type:
    

[[XrActionMapBinding]]

new_from_binding(_binding_)
    

new_from_binding

Parameters:
    

**binding** ([[XrActionMapBinding]], (never None)) – Binding, Binding to use as a reference

Returns:
    

Binding, Added action map binding

Return type:
    

[[XrActionMapBinding]]

remove(_binding_)
    

remove

Parameters:
    

**binding** ([[XrActionMapBinding]], (never None)) – Binding

find(_name_)
    

find

Parameters:
    

**name** (_string_ _,__(__never None_ _)_) – Name

Returns:
    

Binding, The action map binding with the given name

Return type:
    

[[XrActionMapBinding]]

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

  * [[XrActionMapItem.bindings]]

| 


  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
