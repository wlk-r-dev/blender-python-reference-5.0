# CastModifier(Modifier)

base classes — [[bpy_struct]], [[Modifier]]

_class _bpy.types.CastModifier(_Modifier_)
    

Modifier to cast to other shapes

cast_type
    

Target object shape

Type:
    

enum in [`'SPHERE'`, `'CYLINDER'`, `'CUBOID'`], default `'SPHERE'`

factor
    

Type:
    

float in [-inf, inf], default 0.5

invert_vertex_group
    

Invert vertex group influence

Type:
    

boolean, default False

object
    

Control object: if available, its location determines the center of the effect

Type:
    

[[Object]]

radius
    

Only deform vertices within this distance from the center of the effect (leave as 0 for infinite.)

Type:
    

float in [0, inf], default 0.0

size
    

Size of projection shape (leave as 0 for auto)

Type:
    

float in [0, inf], default 0.0

use_radius_as_size
    

Use radius as size of projection shape (0 = auto)

Type:
    

boolean, default True

use_transform
    

Use object transform to control projection shape

Type:
    

boolean, default False

use_x
    

Type:
    

boolean, default True

use_y
    

Type:
    

boolean, default True

use_z
    

Type:
    

boolean, default True

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
