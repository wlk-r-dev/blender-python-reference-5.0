# GreasePencilOffsetModifier(Modifier)

base classes — [[bpy_struct]], [[Modifier]]

_class _bpy.types.GreasePencilOffsetModifier(_Modifier_)
    

invert_layer_filter
    

Invert layer filter

Type:
    

boolean, default False

invert_layer_pass_filter
    

Invert layer pass filter

Type:
    

boolean, default False

invert_material_filter
    

Invert material filter

Type:
    

boolean, default False

invert_material_pass_filter
    

Invert material pass filter

Type:
    

boolean, default False

invert_vertex_group
    

Invert vertex group weights

Type:
    

boolean, default False

layer_pass_filter
    

Layer pass filter

Type:
    

int in [0, 100], default 0

location
    

Values for change location

Type:
    

[[mathutils.Vector]] of 3 items in [-inf, inf], default (0.0, 0.0, 0.0)

material_filter
    

Material used for filtering

Type:
    

[[Material]]

material_pass_filter
    

Material pass

Type:
    

int in [0, 100], default 0

offset_mode
    

  * `RANDOM` Random – Randomize stroke offset.

  * `LAYER` Layer – Offset layers by the same factor.

  * `STROKE` Stroke – Offset strokes by the same factor based on stroke draw order.

  * `MATERIAL` Material – Offset materials by the same factor.


Type:
    

enum in [`'RANDOM'`, `'LAYER'`, `'STROKE'`, `'MATERIAL'`], default `'RANDOM'`

open_general_panel
    

Type:
    

boolean, default False

open_influence_panel
    

Type:
    

boolean, default False

rotation
    

Values for changes in rotation

Type:
    

[[mathutils.Euler]] rotation of 3 items in [-inf, inf], default (0.0, 0.0, 0.0)

scale
    

Values for changes in scale

Type:
    

[[mathutils.Vector]] of 3 items in [-inf, inf], default (0.0, 0.0, 0.0)

seed
    

Random seed

Type:
    

int in [0, inf], default 0

stroke_location
    

Value for changes in location

Type:
    

[[mathutils.Vector]] of 3 items in [-inf, inf], default (0.0, 0.0, 0.0)

stroke_rotation
    

Value for changes in rotation

Type:
    

[[mathutils.Euler]] rotation of 3 items in [-inf, inf], default (0.0, 0.0, 0.0)

stroke_scale
    

Value for changes in scale

Type:
    

[[mathutils.Vector]] of 3 items in [-inf, inf], default (0.0, 0.0, 0.0)

stroke_start_offset
    

Offset starting point

Type:
    

int in [0, inf], default 0

stroke_step
    

Number of elements that will be grouped

Type:
    

int in [1, 500], default 1

tree_node_filter
    

Layer name

Type:
    

string, default “”, (never None)

use_layer_group_filter
    

Filter by layer group name

Type:
    

boolean, default False

use_layer_pass_filter
    

Use layer pass filter

Type:
    

boolean, default False

use_material_pass_filter
    

Use material pass filter

Type:
    

boolean, default False

use_uniform_random_scale
    

Use the same random seed for each scale axis for a uniform scale

Type:
    

boolean, default False

vertex_group_name
    

Vertex group name for modulating the deform

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
