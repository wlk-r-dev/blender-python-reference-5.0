# GreasePencilLengthModifier(Modifier)

base classes — [[bpy_struct]], [[Modifier]]

_class _bpy.types.GreasePencilLengthModifier(_Modifier_)
    

Stretch or shrink strokes

end_factor
    

Added length to the end of each stroke relative to its length

Type:
    

float in [-inf, inf], default 0.1

end_length
    

Absolute added length to the end of each stroke

Type:
    

float in [-inf, inf], default 0.1

invert_curvature
    

Invert the curvature of the stroke’s extension

Type:
    

boolean, default False

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

layer_pass_filter
    

Layer pass filter

Type:
    

int in [0, 100], default 0

material_filter
    

Material used for filtering

Type:
    

[[Material]]

material_pass_filter
    

Material pass

Type:
    

int in [0, 100], default 0

max_angle
    

Ignore points on the stroke that deviate from their neighbors by more than this angle when determining the extrapolation shape

Type:
    

float in [0, 3.14159], default 2.96706

mode
    

Mode to define length

  * `RELATIVE` Relative – Length in ratio to the stroke’s length.

  * `ABSOLUTE` Absolute – Length in geometry space.


Type:
    

enum in [`'RELATIVE'`, `'ABSOLUTE'`], default `'RELATIVE'`

open_curvature_panel
    

Type:
    

boolean, default False

open_influence_panel
    

Type:
    

boolean, default False

open_random_panel
    

Type:
    

boolean, default False

overshoot_factor
    

Defines what portion of the stroke is used for the calculation of the extension

Type:
    

float in [0, 1], default 0.1

point_density
    

Multiplied by Start/End for the total added point count

Type:
    

float in [0.1, 1000], default 30.0

random_end_factor
    

Size of random length added to the end of each stroke

Type:
    

float in [-inf, inf], default 0.0

random_offset
    

Smoothly offset each stroke’s random value

Type:
    

float in [-inf, inf], default 0.0

random_start_factor
    

Size of random length added to the start of each stroke

Type:
    

float in [-inf, inf], default 0.0

seed
    

Random seed

Type:
    

int in [0, inf], default 0

segment_influence
    

Factor to determine how much the length of the individual segments should influence the final computed curvature. Higher factors makes small segments influence the overall curvature less.

Type:
    

float in [-2, 3], default 0.0

start_factor
    

Added length to the start of each stroke relative to its length

Type:
    

float in [-inf, inf], default 0.1

start_length
    

Absolute added length to the start of each stroke

Type:
    

float in [-inf, inf], default 0.1

step
    

Number of frames between randomization steps

Type:
    

int in [1, 100], default 4

tree_node_filter
    

Layer name

Type:
    

string, default “”, (never None)

use_curvature
    

Follow the curvature of the stroke

Type:
    

boolean, default True

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

use_random
    

Use random values over time

Type:
    

boolean, default False

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
