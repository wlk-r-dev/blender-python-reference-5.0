# TexMapping(bpy_struct)

base class — [`bpy_struct`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct "bpy.types.bpy_struct")

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
    

[`mathutils.Vector`](mathutils.md#mathutils.Vector "mathutils.Vector") of 3 items in [-inf, inf], default (0.0, 0.0, 0.0)

min
    

Minimum value for clipping

Type:
    

[`mathutils.Vector`](mathutils.md#mathutils.Vector "mathutils.Vector") of 3 items in [-inf, inf], default (0.0, 0.0, 0.0)

rotation
    

Type:
    

[`mathutils.Euler`](mathutils.md#mathutils.Euler "mathutils.Euler") rotation of 3 items in [-inf, inf], default (0.0, 0.0, 0.0)

scale
    

Type:
    

[`mathutils.Vector`](mathutils.md#mathutils.Vector "mathutils.Vector") of 3 items in [-inf, inf], default (0.0, 0.0, 0.0)

translation
    

Type:
    

[`mathutils.Vector`](mathutils.md#mathutils.Vector "mathutils.Vector") of 3 items in [-inf, inf], default (0.0, 0.0, 0.0)

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
    

[`bpy.types.Struct`](../S/bpy.types.Struct.md#bpy.types.Struct "bpy.types.Struct") subclass

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

  * [`ShaderNodeTexBrick.texture_mapping`](../S/bpy.types.ShaderNodeTexBrick.md#bpy.types.ShaderNodeTexBrick.texture_mapping "bpy.types.ShaderNodeTexBrick.texture_mapping")
  * [`ShaderNodeTexChecker.texture_mapping`](../S/bpy.types.ShaderNodeTexChecker.md#bpy.types.ShaderNodeTexChecker.texture_mapping "bpy.types.ShaderNodeTexChecker.texture_mapping")
  * [`ShaderNodeTexEnvironment.texture_mapping`](../S/bpy.types.ShaderNodeTexEnvironment.md#bpy.types.ShaderNodeTexEnvironment.texture_mapping "bpy.types.ShaderNodeTexEnvironment.texture_mapping")
  * [`ShaderNodeTexGabor.texture_mapping`](../S/bpy.types.ShaderNodeTexGabor.md#bpy.types.ShaderNodeTexGabor.texture_mapping "bpy.types.ShaderNodeTexGabor.texture_mapping")
  * [`ShaderNodeTexGradient.texture_mapping`](../S/bpy.types.ShaderNodeTexGradient.md#bpy.types.ShaderNodeTexGradient.texture_mapping "bpy.types.ShaderNodeTexGradient.texture_mapping")
  * [`ShaderNodeTexImage.texture_mapping`](../S/bpy.types.ShaderNodeTexImage.md#bpy.types.ShaderNodeTexImage.texture_mapping "bpy.types.ShaderNodeTexImage.texture_mapping")

| 

  * [`ShaderNodeTexMagic.texture_mapping`](../S/bpy.types.ShaderNodeTexMagic.md#bpy.types.ShaderNodeTexMagic.texture_mapping "bpy.types.ShaderNodeTexMagic.texture_mapping")
  * [`ShaderNodeTexNoise.texture_mapping`](../S/bpy.types.ShaderNodeTexNoise.md#bpy.types.ShaderNodeTexNoise.texture_mapping "bpy.types.ShaderNodeTexNoise.texture_mapping")
  * [`ShaderNodeTexSky.texture_mapping`](../S/bpy.types.ShaderNodeTexSky.md#bpy.types.ShaderNodeTexSky.texture_mapping "bpy.types.ShaderNodeTexSky.texture_mapping")
  * [`ShaderNodeTexVoronoi.texture_mapping`](../S/bpy.types.ShaderNodeTexVoronoi.md#bpy.types.ShaderNodeTexVoronoi.texture_mapping "bpy.types.ShaderNodeTexVoronoi.texture_mapping")
  * [`ShaderNodeTexWave.texture_mapping`](../S/bpy.types.ShaderNodeTexWave.md#bpy.types.ShaderNodeTexWave.texture_mapping "bpy.types.ShaderNodeTexWave.texture_mapping")

  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
