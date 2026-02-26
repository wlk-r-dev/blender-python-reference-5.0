# ShapeKey(bpy_struct)

base class — [`bpy_struct`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct "bpy.types.bpy_struct")

_class _bpy.types.ShapeKey(_bpy_struct_)
    

Shape key in a shape keys data-block

data
    

Type:
    

[`bpy_prop_collection`](../_other/bpy.types.bpy_prop_collection.md#bpy.types.bpy_prop_collection "bpy.types.bpy_prop_collection") of [`UnknownType`](../U/bpy.types.UnknownType.md#bpy.types.UnknownType "bpy.types.UnknownType"), (readonly)

frame
    

Frame for absolute keys

Type:
    

float in [-inf, inf], default 0.0, (readonly)

interpolation
    

Interpolation type for absolute shape keys

Type:
    

enum in [`'KEY_LINEAR'`, `'KEY_CARDINAL'`, `'KEY_CATMULL_ROM'`, `'KEY_BSPLINE'`], default `'KEY_LINEAR'`

lock_shape
    

Protect the shape key from accidental sculpting and editing

Type:
    

boolean, default False

mute
    

Toggle this shape key

Type:
    

boolean, default False

name
    

Name of Shape Key

Type:
    

string, default “”, (never None)

points
    

Optimized access to shape keys point data, when using foreach_get/foreach_set accessors. Warning: Does not support legacy Curve shape keys.

Type:
    

[`bpy_prop_collection`](../_other/bpy.types.bpy_prop_collection.md#bpy.types.bpy_prop_collection "bpy.types.bpy_prop_collection") of [`ShapeKeyPoint`](bpy.types.ShapeKeyPoint.md#bpy.types.ShapeKeyPoint "bpy.types.ShapeKeyPoint"), (readonly)

relative_key
    

Shape used as a relative key

Type:
    

`ShapeKey`, (never None)

slider_max
    

Maximum for slider

Type:
    

float in [-10, 10], default 1.0

slider_min
    

Minimum for slider

Type:
    

float in [-10, 10], default 0.0

value
    

Value of shape key at the current frame

Type:
    

float in [0, 1], default 1.0

vertex_group
    

Vertex weight group, to blend with basis shape

Type:
    

string, default “”, (never None)

normals_vertex_get()
    

Compute local space vertices’ normals for this shape key

Returns:
    

normals

Return type:
    

float in [-1, 1]

normals_polygon_get()
    

Compute local space faces’ normals for this shape key

Returns:
    

normals

Return type:
    

float in [-1, 1]

normals_split_get()
    

Compute local space face corners’ normals for this shape key

Returns:
    

normals

Return type:
    

float in [-1, 1]

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

  * [`ClothSettings.rest_shape_key`](../C/bpy.types.ClothSettings.md#bpy.types.ClothSettings.rest_shape_key "bpy.types.ClothSettings.rest_shape_key")
  * [`Key.key_blocks`](../K/bpy.types.Key.md#bpy.types.Key.key_blocks "bpy.types.Key.key_blocks")
  * [`Key.reference_key`](../K/bpy.types.Key.md#bpy.types.Key.reference_key "bpy.types.Key.reference_key")
  * [`Object.active_shape_key`](../O/bpy.types.Object.md#bpy.types.Object.active_shape_key "bpy.types.Object.active_shape_key")

| 

  * [`Object.shape_key_add`](../O/bpy.types.Object.md#bpy.types.Object.shape_key_add "bpy.types.Object.shape_key_add")
  * [`Object.shape_key_remove`](../O/bpy.types.Object.md#bpy.types.Object.shape_key_remove "bpy.types.Object.shape_key_remove")
  * `ShapeKey.relative_key`

  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
