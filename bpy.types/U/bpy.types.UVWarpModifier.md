# UVWarpModifier(Modifier)

base classes — [[bpy_struct]], [[Modifier]]

_class _bpy.types.UVWarpModifier(_Modifier_)
    

Add target position to UV coordinates

axis_u
    

Pole axis for rotation

Type:
    

enum in [Axis Xyz Items](../../bpy_types_enum_items/axis_xyz_items.md#rna-enum-axis-xyz-items), default `'X'`

axis_v
    

Pole axis for rotation

Type:
    

enum in [Axis Xyz Items](../../bpy_types_enum_items/axis_xyz_items.md#rna-enum-axis-xyz-items), default `'Y'`

bone_from
    

Bone defining offset

Type:
    

string, default “”, (never None)

bone_to
    

Bone defining offset

Type:
    

string, default “”, (never None)

center
    

Center point for rotate/scale

Type:
    

float array of 2 items in [-inf, inf], default (0.5, 0.5)

invert_vertex_group
    

Invert vertex group influence

Type:
    

boolean, default False

object_from
    

Object defining offset

Type:
    

[[Object]]

object_to
    

Object defining offset

Type:
    

[[Object]]

offset
    

2D Offset for the warp

Type:
    

float array of 2 items in [-inf, inf], default (0.0, 0.0)

rotation
    

2D Rotation for the warp

Type:
    

float in [-inf, inf], default 0.0

scale
    

2D Scale for the warp

Type:
    

float array of 2 items in [-inf, inf], default (1.0, 1.0)

uv_layer
    

UV map name

Type:
    

string, default “”, (never None)

vertex_group
    

Vertex group name

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
