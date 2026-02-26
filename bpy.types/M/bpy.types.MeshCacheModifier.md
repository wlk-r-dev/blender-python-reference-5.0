# MeshCacheModifier(Modifier)

base classes — [[bpy_struct]], [[Modifier]]

_class _bpy.types.MeshCacheModifier(_Modifier_)
    

Cache Mesh

cache_format
    

Type:
    

enum in [`'MDD'`, `'PC2'`], default `'MDD'`

deform_mode
    

  * `OVERWRITE` Overwrite – Replace vertex coordinates with cached values.

  * `INTEGRATE` Integrate – Integrate deformation from this modifier’s input with the mesh-cache coordinates (useful for shape keys).


Type:
    

enum in [`'OVERWRITE'`, `'INTEGRATE'`], default `'OVERWRITE'`

eval_factor
    

Evaluation time in seconds

Type:
    

float in [0, 1], default 0.0

eval_frame
    

The frame to evaluate (starting at 0)

Type:
    

float in [0, 1.04857e+06], default 0.0

eval_time
    

Evaluation time in seconds

Type:
    

float in [0, inf], default 0.0

factor
    

Influence of the deformation

Type:
    

float in [0, 1], default 1.0

filepath
    

Path to external displacements file

Type:
    

string, default “”, (never None, blend relative `//` prefix supported)

flip_axis
    

Type:
    

boolean array of 3 items, default (False, False, False)

forward_axis
    

Type:
    

enum in [Object Axis Items](../../bpy_types_enum_items/object_axis_items.md#rna-enum-object-axis-items), default `'POS_Y'`

frame_scale
    

Evaluation time in seconds

Type:
    

float in [0, 100], default 1.0

frame_start
    

Add this to the start frame

Type:
    

float in [-1.04857e+06, 1.04857e+06], default 0.0

interpolation
    

Type:
    

enum in [`'NONE'`, `'LINEAR'`], default `'LINEAR'`

invert_vertex_group
    

Invert vertex group influence

Type:
    

boolean, default False

play_mode
    

  * `SCENE` Scene – Use the time from the scene.

  * `CUSTOM` Custom – Use the modifier’s own time evaluation.


Type:
    

enum in [`'SCENE'`, `'CUSTOM'`], default `'SCENE'`

time_mode
    

Method to control playback time

  * `FRAME` Frame – Control playback using a frame-number (ignoring time FPS and start frame from the file).

  * `TIME` Time – Control playback using time in seconds.

  * `FACTOR` Factor – Control playback using a value between 0 and 1.


Type:
    

enum in [`'FRAME'`, `'TIME'`, `'FACTOR'`], default `'FRAME'`

up_axis
    

Type:
    

enum in [Object Axis Items](../../bpy_types_enum_items/object_axis_items.md#rna-enum-object-axis-items), default `'POS_Z'`

vertex_group
    

Name of the Vertex Group which determines the influence of the modifier per point

Type:
    

string, default “”, (never None)

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
  * [[Modifier.name]]
  * [[Modifier.type]]
  * [[Modifier.show_viewport]]
  * [[Modifier.show_render]]
  * [[Modifier.show_in_editmode]]
  * [[Modifier.show_on_cage]]

| 

  * [[Modifier.show_expanded]]
  * [[Modifier.is_active]]
  * [[Modifier.use_pin_to_last]]
  * [[Modifier.is_override_data]]
  * [[Modifier.use_apply_on_spline]]
  * [[Modifier.execution_time]]
  * [[Modifier.persistent_uid]]

  
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
  * [[bpy_struct.keyframe_delete]]

| 

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
  * [[Modifier.bl_rna_get_subclass]]
  * [[Modifier.bl_rna_get_subclass_py]]

  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
