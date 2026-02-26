# BlendFileColorspace(bpy_struct)

base class — [[bpy_struct]]

_class _bpy.types.BlendFileColorspace(_bpy_struct_)
    

Information about the color space used for data-blocks in a blend file

is_missing_opencolorio_config
    

A color space, view or display was not found, which likely means the OpenColorIO config used to create this blend file is missing

Type:
    

boolean, default False, (readonly)

working_space
    

Color space used for all scene linear colors in this file, and for compositing, shader and geometry nodes processing

  * `Linear Rec.709` Linear Rec.709 – Linear BT.709 with illuminant D65 white point.

  * `Linear Rec.2020` Linear Rec.2020 – Linear BT.2020 with illuminant D65 white point.

  * `ACEScg` ACEScg – Linear AP1 with ACES white point.


Type:
    

enum in [`'Linear Rec.709'`, `'Linear Rec.2020'`, `'ACEScg'`], (readonly)

working_space_interop_id
    

Unique identifier for common color spaces, as defined by the Color Interop Forum. May be empty if there is no interop ID for the working space. Common values are lin_rec709_scene, lin_rec2020_scene and lin_ap1_scene (for ACEScg)

Type:
    

string, default “”, (readonly, never None)

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

  * [[BlendData.colorspace]]

| 


  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
