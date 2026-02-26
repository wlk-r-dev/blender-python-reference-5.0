# BlendDataFonts(bpy_struct)

base class — [[bpy_struct]]

_class _bpy.types.BlendDataFonts(_bpy_struct_)
    

Collection of fonts

load(_filepath_ , _*_ , _check_existing =False_)
    

Load a new font into the main database

Parameters:
    

  * **filepath** (string, (never None, blend relative `//` prefix supported)) – path of the font to load

  * **check_existing** (_boolean_ _,__(__optional_ _)_) – Using existing data-block if this file is already loaded


Returns:
    

New font data-block

Return type:
    

[[VectorFont]]

remove(_vfont_ , _*_ , _do_unlink =True_, _do_id_user =True_, _do_ui_user =True_)
    

Remove a font from the current blendfile

Parameters:
    

  * **vfont** ([[VectorFont]], (never None)) – Font to remove

  * **do_unlink** (_boolean_ _,__(__optional_ _)_) – Unlink all usages of this font before deleting it

  * **do_id_user** (_boolean_ _,__(__optional_ _)_) – Decrement user counter of all data-blocks used by this font

  * **do_ui_user** (_boolean_ _,__(__optional_ _)_) – Make sure interface does not reference this font


tag(_value_)
    

tag

Parameters:
    

**value** (_boolean_) – Value

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

  * [[BlendData.fonts]]

| 


  
---|---
  *[*]: Keyword-only parameters separator (PEP 3102)
  *[/]: Positional-only parameter separator (PEP 570)
