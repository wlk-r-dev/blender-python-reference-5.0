# PivotConstraint(Constraint)

base classes — [[bpy_struct]], [[Constraint]]

_class _bpy.types.PivotConstraint(_Constraint_)
    

Rotate around a different point

head_tail
    

Target along length of bone: Head is 0, Tail is 1

Type:
    

float in [0, 1], default 0.0

offset
    

Offset of pivot from target (when set), or from owner’s location (when Fixed Position is off), or the absolute pivot point

Type:
    

[[mathutils.Vector]] of 3 items in [-inf, inf], default (0.0, 0.0, 0.0)

rotation_range
    

Rotation range on which pivoting should occur

  * `ALWAYS_ACTIVE` Always – Use the pivot point in every rotation.

  * `NX` -X Rotation – Use the pivot point in the negative rotation range around the X-axis.

  * `NY` -Y Rotation – Use the pivot point in the negative rotation range around the Y-axis.

  * `NZ` -Z Rotation – Use the pivot point in the negative rotation range around the Z-axis.

  * `X` X Rotation – Use the pivot point in the positive rotation range around the X-axis.

  * `Y` Y Rotation – Use the pivot point in the positive rotation range around the Y-axis.

  * `Z` Z Rotation – Use the pivot point in the positive rotation range around the Z-axis.


Type:
    

enum in [`'ALWAYS_ACTIVE'`, `'NX'`, `'NY'`, `'NZ'`, `'X'`, `'Y'`, `'Z'`], default `'NX'`

subtarget
    

Type:
    

string, default “”, (never None)

target
    

Target Object, defining the position of the pivot when defined

Type:
    

[[Object]]

use_bbone_shape
    

Follow shape of B-Bone segments when calculating Head/Tail position

Type:
    

boolean, default False

use_relative_location
    

Offset will be an absolute point in space instead of relative to the target

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
