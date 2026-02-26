# RenderResult(bpy_struct)

base class — [[bpy_struct]]

_class _bpy.types.RenderResult(_bpy_struct_)
    

Result of rendering, including all layers and passes

layers
    

Type:
    

[[bpy_prop_collection]] of [[RenderLayer]], (readonly)

resolution_x
    

Type:
    

int in [-inf, inf], default 0, (readonly)

resolution_y
    

Type:
    

int in [-inf, inf], default 0, (readonly)

views
    

Type:
    

[[bpy_prop_collection]] of [[RenderView]], (readonly)

load_from_file(_filepath_)
    

Copies the pixels of this render result from an image file

Parameters:
    

**filepath** (_string_ _,__(__never None_ _)_) – File Name, Filename to load into this render tile, must be no smaller than the render result

stamp_data_add_field(_field_ , _value_)
    

Add engine-specific stamp data to the result

Parameters:
    

  * **field** (_string_ _,__(__never None_ _)_) – Field, Name of the stamp field to add

  * **value** (_string_ _,__(__never None_ _)_) – Value, Value of the stamp data


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

  * [[RenderEngine.begin_result]]
  * [[RenderEngine.end_result]]

| 

  * [[RenderEngine.get_result]]
  * [[RenderEngine.update_result]]

  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
