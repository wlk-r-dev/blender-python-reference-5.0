# VertexWeightMixModifier(Modifier)

base classes — [[bpy_struct]], [[Modifier]]

_class _bpy.types.VertexWeightMixModifier(_Modifier_)
    

Mix the weights of two vertex groups

default_weight_a
    

Default weight a vertex will have if it is not in the first A vgroup

Type:
    

float in [0, 1], default 0.0

default_weight_b
    

Default weight a vertex will have if it is not in the second B vgroup

Type:
    

float in [0, 1], default 0.0

invert_mask_vertex_group
    

Invert vertex group mask influence

Type:
    

boolean, default False

invert_vertex_group_a
    

Invert the influence of vertex group A

Type:
    

boolean, default False

invert_vertex_group_b
    

Invert the influence of vertex group B

Type:
    

boolean, default False

mask_constant
    

Global influence of current modifications on vgroup

Type:
    

float in [-inf, inf], default 1.0

mask_tex_map_bone
    

Which bone to take texture coordinates from

Type:
    

string, default “”, (never None)

mask_tex_map_object
    

Which object to take texture coordinates from

Type:
    

[[Object]]

mask_tex_mapping
    

Which texture coordinates to use for mapping

  * `LOCAL` Local – Use local generated coordinates.

  * `GLOBAL` Global – Use global coordinates.

  * `OBJECT` Object – Use local generated coordinates of another object.

  * `UV` UV – Use coordinates from a UV layer.


Type:
    

enum in [`'LOCAL'`, `'GLOBAL'`, `'OBJECT'`, `'UV'`], default `'LOCAL'`

mask_tex_use_channel
    

Which texture channel to use for masking

Type:
    

enum in [`'INT'`, `'RED'`, `'GREEN'`, `'BLUE'`, `'HUE'`, `'SAT'`, `'VAL'`, `'ALPHA'`], default `'INT'`

mask_tex_uv_layer
    

UV map name

Type:
    

string, default “”, (never None)

mask_texture
    

Masking texture

Type:
    

[[Texture]]

mask_vertex_group
    

Masking vertex group name

Type:
    

string, default “”, (never None)

mix_mode
    

How weights from vgroup B affect weights of vgroup A

  * `SET` Replace – Replace VGroup A’s weights by VGroup B’s ones.

  * `ADD` Add – Add VGroup B’s weights to VGroup A’s ones.

  * `SUB` Subtract – Subtract VGroup B’s weights from VGroup A’s ones.

  * `MUL` Multiply – Multiply VGroup A’s weights by VGroup B’s ones.

  * `DIV` Divide – Divide VGroup A’s weights by VGroup B’s ones.

  * `DIF` Difference – Difference between VGroup A’s and VGroup B’s weights.

  * `AVG` Average – Average value of VGroup A’s and VGroup B’s weights.

  * `MIN` Minimum – Minimum of VGroup A’s and VGroup B’s weights.

  * `MAX` Maximum – Maximum of VGroup A’s and VGroup B’s weights.


Type:
    

enum in [`'SET'`, `'ADD'`, `'SUB'`, `'MUL'`, `'DIV'`, `'DIF'`, `'AVG'`, `'MIN'`, `'MAX'`], default `'SET'`

mix_set
    

Which vertices should be affected

  * `ALL` All – Affect all vertices (might add some to VGroup A).

  * `A` VGroup A – Affect vertices in VGroup A.

  * `B` VGroup B – Affect vertices in VGroup B (might add some to VGroup A).

  * `OR` VGroup A or B – Affect vertices in at least one of both VGroups (might add some to VGroup A).

  * `AND` VGroup A and B – Affect vertices in both groups.


Type:
    

enum in [`'ALL'`, `'A'`, `'B'`, `'OR'`, `'AND'`], default `'AND'`

normalize
    

Normalize the resulting weights (otherwise they are only clamped within 0.0 to 1.0 range)

Type:
    

boolean, default False

vertex_group_a
    

First vertex group name

Type:
    

string, default “”, (never None)

vertex_group_b
    

Second vertex group name

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
