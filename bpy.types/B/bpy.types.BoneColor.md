# BoneColor(bpy_struct)

base class — [[bpy_struct]]

_class _bpy.types.BoneColor(_bpy_struct_)
    

Theme color or custom color of a bone

custom
    

The custom bone colors, used when palette is ‘CUSTOM’

Type:
    

[[ThemeBoneColorSet]], (readonly, never None)

is_custom
    

A color palette is user-defined, instead of using a theme-defined one

Type:
    

boolean, default False, (readonly)

palette
    

Color palette to use

Type:
    

enum in [`'DEFAULT'`, `'THEME01'`, `'THEME02'`, `'THEME03'`, `'THEME04'`, `'THEME05'`, `'THEME06'`, `'THEME07'`, `'THEME08'`, `'THEME09'`, `'THEME10'`, `'THEME11'`, `'THEME12'`, `'THEME13'`, `'THEME14'`, `'THEME15'`, `'THEME16'`, `'THEME17'`, `'THEME18'`, `'THEME19'`, `'THEME20'`, `'CUSTOM'`], default `'DEFAULT'`

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

  * [[Bone.color]]
  * [[EditBone.color]]

| 

  * [[PoseBone.color]]

  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
