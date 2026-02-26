# ShaderFx(bpy_struct)

base class — [[bpy_struct]]

subclasses — [[ShaderFxBlur]], [[ShaderFxColorize]], [[ShaderFxFlip]], [[ShaderFxGlow]], [[ShaderFxPixel]], [[ShaderFxRim]], [[ShaderFxShadow]], [[ShaderFxSwirl]], [[ShaderFxWave]]

_class _bpy.types.ShaderFx(_bpy_struct_)
    

Effect affecting the Grease Pencil object

name
    

Effect name

Type:
    

string, default “”, (never None)

show_expanded
    

Set effect expansion in the user interface

Type:
    

boolean, default False

show_in_editmode
    

Display effect in Edit mode

Type:
    

boolean, default False

show_render
    

Use effect during render

Type:
    

boolean, default False

show_viewport
    

Display effect in viewport

Type:
    

boolean, default False

type
    

Type:
    

enum in [Object Shaderfx Type Items](../../bpy_types_enum_items/object_shaderfx_type_items.md#rna-enum-object-shaderfx-type-items), default `'FX_BLUR'`, (readonly)

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

  * [[Object.shader_effects]]
  * [[ObjectShaderFx.new]]

| 

  * [[ObjectShaderFx.remove]]

  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
