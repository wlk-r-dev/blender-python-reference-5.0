# GreasePencilNoiseModifier(Modifier)

base classes — [[bpy_struct]], [[Modifier]]

_class _bpy.types.GreasePencilNoiseModifier(_Modifier_)
    

Noise effect modifier

custom_curve
    

Custom curve to apply effect

Type:
    

[[CurveMapping]], (readonly)

factor
    

Amount of noise to apply

Type:
    

float in [0, inf], default 0.5

factor_strength
    

Amount of noise to apply to opacity

Type:
    

float in [0, inf], default 0.0

factor_thickness
    

Amount of noise to apply to thickness

Type:
    

float in [0, inf], default 0.0

factor_uvs
    

Amount of noise to apply to UV rotation

Type:
    

float in [0, inf], default 0.0

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

material_filter
    

Material used for filtering

Type:
    

[[Material]]

material_pass_filter
    

Material pass

Type:
    

int in [0, 100], default 0

noise_offset
    

Offset the noise along the strokes

Type:
    

float in [0, inf], default 0.0

noise_scale
    

Scale the noise frequency

Type:
    

float in [0, 1], default 0.0

open_influence_panel
    

Type:
    

boolean, default False

open_random_panel
    

Type:
    

boolean, default False

random_mode
    

Where to perform randomization

  * `STEP` Steps – Randomize every number of frames.

  * `KEYFRAME` Keyframes – Randomize on keyframes only.


Type:
    

enum in [`'STEP'`, `'KEYFRAME'`], default `'STEP'`

seed
    

Random seed

Type:
    

int in [0, inf], default 1

step
    

Number of frames between randomization steps

Type:
    

int in [1, 100], default 4

tree_node_filter
    

Layer name

Type:
    

string, default “”, (never None)

use_custom_curve
    

Use a custom curve to define a factor along the strokes

Type:
    

boolean, default False

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
    

boolean, default True

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
