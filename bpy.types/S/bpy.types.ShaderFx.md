# ShaderFx(bpy_struct)

base class — [`bpy_struct`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct "bpy.types.bpy_struct")

subclasses — [`ShaderFxBlur`](bpy.types.ShaderFxBlur.md#bpy.types.ShaderFxBlur "bpy.types.ShaderFxBlur"), [`ShaderFxColorize`](bpy.types.ShaderFxColorize.md#bpy.types.ShaderFxColorize "bpy.types.ShaderFxColorize"), [`ShaderFxFlip`](bpy.types.ShaderFxFlip.md#bpy.types.ShaderFxFlip "bpy.types.ShaderFxFlip"), [`ShaderFxGlow`](bpy.types.ShaderFxGlow.md#bpy.types.ShaderFxGlow "bpy.types.ShaderFxGlow"), [`ShaderFxPixel`](bpy.types.ShaderFxPixel.md#bpy.types.ShaderFxPixel "bpy.types.ShaderFxPixel"), [`ShaderFxRim`](bpy.types.ShaderFxRim.md#bpy.types.ShaderFxRim "bpy.types.ShaderFxRim"), [`ShaderFxShadow`](bpy.types.ShaderFxShadow.md#bpy.types.ShaderFxShadow "bpy.types.ShaderFxShadow"), [`ShaderFxSwirl`](bpy.types.ShaderFxSwirl.md#bpy.types.ShaderFxSwirl "bpy.types.ShaderFxSwirl"), [`ShaderFxWave`](bpy.types.ShaderFxWave.md#bpy.types.ShaderFxWave "bpy.types.ShaderFxWave")

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
    

[`bpy.types.Struct`](bpy.types.Struct.md#bpy.types.Struct "bpy.types.Struct") subclass

_classmethod _bl_rna_get_subclass_py(_id_ , _default =None_, _/_)
    

Parameters:
    

**id** (_str_) – The RNA type identifier.

Returns:
    

The class or default when not found.

Return type:
    

type

## Inherited Properties

  * [`bpy_struct.id_data`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.id_data "bpy.types.bpy_struct.id_data")

| 


  
---|---  
  
## Inherited Functions

  * [`bpy_struct.as_pointer`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.as_pointer "bpy.types.bpy_struct.as_pointer")
  * [`bpy_struct.driver_add`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.driver_add "bpy.types.bpy_struct.driver_add")
  * [`bpy_struct.driver_remove`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.driver_remove "bpy.types.bpy_struct.driver_remove")
  * [`bpy_struct.get`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.get "bpy.types.bpy_struct.get")
  * [`bpy_struct.id_properties_clear`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.id_properties_clear "bpy.types.bpy_struct.id_properties_clear")
  * [`bpy_struct.id_properties_ensure`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.id_properties_ensure "bpy.types.bpy_struct.id_properties_ensure")
  * [`bpy_struct.id_properties_ui`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.id_properties_ui "bpy.types.bpy_struct.id_properties_ui")
  * [`bpy_struct.is_property_hidden`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.is_property_hidden "bpy.types.bpy_struct.is_property_hidden")
  * [`bpy_struct.is_property_overridable_library`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.is_property_overridable_library "bpy.types.bpy_struct.is_property_overridable_library")
  * [`bpy_struct.is_property_readonly`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.is_property_readonly "bpy.types.bpy_struct.is_property_readonly")
  * [`bpy_struct.is_property_set`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.is_property_set "bpy.types.bpy_struct.is_property_set")
  * [`bpy_struct.items`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.items "bpy.types.bpy_struct.items")

| 

  * [`bpy_struct.keyframe_delete`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.keyframe_delete "bpy.types.bpy_struct.keyframe_delete")
  * [`bpy_struct.keyframe_insert`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.keyframe_insert "bpy.types.bpy_struct.keyframe_insert")
  * [`bpy_struct.keys`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.keys "bpy.types.bpy_struct.keys")
  * [`bpy_struct.path_from_id`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.path_from_id "bpy.types.bpy_struct.path_from_id")
  * [`bpy_struct.path_from_module`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.path_from_module "bpy.types.bpy_struct.path_from_module")
  * [`bpy_struct.path_resolve`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.path_resolve "bpy.types.bpy_struct.path_resolve")
  * [`bpy_struct.pop`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.pop "bpy.types.bpy_struct.pop")
  * [`bpy_struct.property_overridable_library_set`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.property_overridable_library_set "bpy.types.bpy_struct.property_overridable_library_set")
  * [`bpy_struct.property_unset`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.property_unset "bpy.types.bpy_struct.property_unset")
  * [`bpy_struct.rna_ancestors`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.rna_ancestors "bpy.types.bpy_struct.rna_ancestors")
  * [`bpy_struct.type_recast`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.type_recast "bpy.types.bpy_struct.type_recast")
  * [`bpy_struct.values`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.values "bpy.types.bpy_struct.values")

  
---|---  
  
## References

  * [`Object.shader_effects`](../O/bpy.types.Object.md#bpy.types.Object.shader_effects "bpy.types.Object.shader_effects")
  * [`ObjectShaderFx.new`](../O/bpy.types.ObjectShaderFx.md#bpy.types.ObjectShaderFx.new "bpy.types.ObjectShaderFx.new")

| 

  * [`ObjectShaderFx.remove`](../O/bpy.types.ObjectShaderFx.md#bpy.types.ObjectShaderFx.remove "bpy.types.ObjectShaderFx.remove")

  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
