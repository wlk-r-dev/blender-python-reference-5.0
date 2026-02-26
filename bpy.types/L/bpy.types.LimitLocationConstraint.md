# LimitLocationConstraint(Constraint)

base classes — [[bpy_struct]], [[Constraint]]

_class _bpy.types.LimitLocationConstraint(_Constraint_)
    

Limit the location of the constrained object

max_x
    

Highest X value to allow

Type:
    

float in [-inf, inf], default 0.0

max_y
    

Highest Y value to allow

Type:
    

float in [-inf, inf], default 0.0

max_z
    

Highest Z value to allow

Type:
    

float in [-inf, inf], default 0.0

min_x
    

Lowest X value to allow

Type:
    

float in [-inf, inf], default 0.0

min_y
    

Lowest Y value to allow

Type:
    

float in [-inf, inf], default 0.0

min_z
    

Lowest Z value to allow

Type:
    

float in [-inf, inf], default 0.0

use_max_x
    

Use the maximum X value

Type:
    

boolean, default False

use_max_y
    

Use the maximum Y value

Type:
    

boolean, default False

use_max_z
    

Use the maximum Z value

Type:
    

boolean, default False

use_min_x
    

Use the minimum X value

Type:
    

boolean, default False

use_min_y
    

Use the minimum Y value

Type:
    

boolean, default False

use_min_z
    

Use the minimum Z value

Type:
    

boolean, default False

use_transform_limit
    

Transform tools are affected by this constraint as well

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
  * [[Constraint.name]]
  * [[Constraint.type]]
  * [[Constraint.is_override_data]]
  * [[Constraint.owner_space]]
  * [[Constraint.target_space]]
  * [[Constraint.space_object]]
  * [[Constraint.space_subtarget]]

| 

  * [[Constraint.mute]]
  * [[Constraint.enabled]]
  * [[Constraint.show_expanded]]
  * [[Constraint.is_valid]]
  * [[Constraint.active]]
  * [[Constraint.influence]]
  * [[Constraint.error_location]]
  * [[Constraint.error_rotation]]

  
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
  * [[Constraint.bl_rna_get_subclass]]
  * [[Constraint.bl_rna_get_subclass_py]]

  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
