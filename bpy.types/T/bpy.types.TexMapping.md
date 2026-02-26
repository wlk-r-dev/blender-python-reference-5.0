# TexMapping(bpy_struct)

base class — [[bpy_struct]]

_class _bpy.types.TexMapping(_bpy_struct_)
    

Texture coordinate mapping settings

mapping
    

  * `FLAT` Flat – Map X and Y coordinates directly.

  * `CUBE` Cube – Map using the normal vector.

  * `TUBE` Tube – Map with Z as central axis.

  * `SPHERE` Sphere – Map with Z as central axis.


Type:
    

enum in [`'FLAT'`, `'CUBE'`, `'TUBE'`, `'SPHERE'`], default `'FLAT'`

mapping_x
    

Type:
    

enum in [`'NONE'`, `'X'`, `'Y'`, `'Z'`], default `'NONE'`

mapping_y
    

Type:
    

enum in [`'NONE'`, `'X'`, `'Y'`, `'Z'`], default `'NONE'`

mapping_z
    

Type:
    

enum in [`'NONE'`, `'X'`, `'Y'`, `'Z'`], default `'NONE'`

max
    

Maximum value for clipping

Type:
    

[[mathutils.Vector]] of 3 items in [-inf, inf], default (0.0, 0.0, 0.0)

min
    

Minimum value for clipping

Type:
    

[[mathutils.Vector]] of 3 items in [-inf, inf], default (0.0, 0.0, 0.0)

rotation
    

Type:
    

[[mathutils.Euler]] rotation of 3 items in [-inf, inf], default (0.0, 0.0, 0.0)

scale
    

Type:
    

[[mathutils.Vector]] of 3 items in [-inf, inf], default (0.0, 0.0, 0.0)

translation
    

Type:
    

[[mathutils.Vector]] of 3 items in [-inf, inf], default (0.0, 0.0, 0.0)

use_max
    

Whether to use maximum clipping value

Type:
    

boolean, default False

use_min
    

Whether to use minimum clipping value

Type:
    

boolean, default False

vector_type
    

Type of vector that the mapping transforms

Type:
    

enum in [Mapping Type Items](../../bpy_types_enum_items/mapping_type_items.md#rna-enum-mapping-type-items), default `'POINT'`

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

  * [[ShaderNodeTexBrick.texture_mapping]]
  * [[ShaderNodeTexChecker.texture_mapping]]
  * [[ShaderNodeTexEnvironment.texture_mapping]]
  * [[ShaderNodeTexGabor.texture_mapping]]
  * [[ShaderNodeTexGradient.texture_mapping]]
  * [[ShaderNodeTexImage.texture_mapping]]

| 

  * [[ShaderNodeTexMagic.texture_mapping]]
  * [[ShaderNodeTexNoise.texture_mapping]]
  * [[ShaderNodeTexSky.texture_mapping]]
  * [[ShaderNodeTexVoronoi.texture_mapping]]
  * [[ShaderNodeTexWave.texture_mapping]]

  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
