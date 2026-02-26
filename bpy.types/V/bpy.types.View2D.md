# View2D(bpy_struct)

base class — [[bpy_struct]]

_class _bpy.types.View2D(_bpy_struct_)
    

Scroll and zoom for a 2D region

region_to_view(_x_ , _y_)
    

Transform region coordinates to 2D view

Parameters:
    

  * **x** (_float in_ _[__-inf_ _,__inf_ _]_) – x, Region x coordinate

  * **y** (_float in_ _[__-inf_ _,__inf_ _]_) – y, Region y coordinate


Returns:
    

Result, View coordinates

Return type:
    

float array of 2 items in [-inf, inf]

view_to_region(_x_ , _y_ , _*_ , _clip =True_)
    

Transform 2D view coordinates to region

Parameters:
    

  * **x** (_float in_ _[__-inf_ _,__inf_ _]_) – x, 2D View x coordinate

  * **y** (_float in_ _[__-inf_ _,__inf_ _]_) – y, 2D View y coordinate

  * **clip** (_boolean_ _,__(__optional_ _)_) – Clip, Clip coordinates to the visible region


Returns:
    

Result, Region coordinates

Return type:
    

int array of 2 items in [-inf, inf]

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

  * [[Region.view2d]]

| 


  
---|---
  *[*]: Keyword-only parameters separator (PEP 3102)
  *[/]: Positional-only parameter separator (PEP 570)
