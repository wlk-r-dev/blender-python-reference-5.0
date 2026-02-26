# RenderViews(bpy_struct)

base class — [[bpy_struct]]

_class _bpy.types.RenderViews(_bpy_struct_)
    

Collection of render views

active
    

Active Render View

Type:
    

[[SceneRenderView]], (never None)

active_index
    

Active index in render view array

Type:
    

int in [0, 32767], default 0

new(_name_)
    

Add a render view to scene

Parameters:
    

**name** (_string_ _,__(__never None_ _)_) – New name for the marker (not unique)

Returns:
    

Newly created render view

Return type:
    

[[SceneRenderView]]

remove(_view_)
    

Remove a render view

Parameters:
    

**view** ([[SceneRenderView]], (never None)) – Render view to remove

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

  * [[RenderSettings.views]]

| 


  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
