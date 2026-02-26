# GreasePencilTextureModifier(Modifier)

base classes — [[bpy_struct]], [[Modifier]]

_class _bpy.types.GreasePencilTextureModifier(_Modifier_)
    

Transform stroke texture coordinates Modifier

alignment_rotation
    

Additional rotation applied to dots and square strokes

Type:
    

float in [-1.5708, 1.5708], default 0.0

fill_offset
    

Additional offset of the fill UV

Type:
    

[[mathutils.Vector]] of 2 items in [-inf, inf], default (0.0, 0.0)

fill_rotation
    

Additional rotation of the fill UV

Type:
    

float in [-inf, inf], default 0.0

fill_scale
    

Additional scale of the fill UV

Type:
    

float in [0.01, 100], default 1.0

fit_method
    

  * `CONSTANT_LENGTH` Constant Length – Keep the texture at a constant length regardless of the length of each stroke.

  * `FIT_STROKE` Stroke Length – Scale the texture to fit the length of each stroke.


Type:
    

enum in [`'CONSTANT_LENGTH'`, `'FIT_STROKE'`], default `'CONSTANT_LENGTH'`

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

mode
    

  * `STROKE` Stroke – Manipulate only stroke texture coordinates.

  * `FILL` Fill – Manipulate only fill texture coordinates.

  * `STROKE_AND_FILL` Stroke & Fill – Manipulate both stroke and fill texture coordinates.


Type:
    

enum in [`'STROKE'`, `'FILL'`, `'STROKE_AND_FILL'`], default `'STROKE'`

open_influence_panel
    

Type:
    

boolean, default False

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

uv_offset
    

Offset value to add to stroke UVs

Type:
    

float in [-inf, inf], default 0.0

uv_scale
    

Factor to scale the UVs

Type:
    

float in [0, inf], default 1.0

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
