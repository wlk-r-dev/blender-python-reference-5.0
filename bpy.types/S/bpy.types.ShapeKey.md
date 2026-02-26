# ShapeKey(bpy_struct)

base class — [[bpy_struct]]

_class _bpy.types.ShapeKey(_bpy_struct_)
    

Shape key in a shape keys data-block

data
    

Type:
    

[[bpy_prop_collection]] of [[UnknownType]], (readonly)

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
    

[[bpy_prop_collection]] of [[ShapeKeyPoint]], (readonly)

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

  * [[ClothSettings.rest_shape_key]]
  * [[Key.key_blocks]]
  * [[Key.reference_key]]
  * [[Object.active_shape_key]]

| 

  * [[Object.shape_key_add]]
  * [[Object.shape_key_remove]]
  * `ShapeKey.relative_key`

  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
