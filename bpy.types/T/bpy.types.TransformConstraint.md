# TransformConstraint(Constraint)

base classes — [[bpy_struct]], [[Constraint]]

_class _bpy.types.TransformConstraint(_Constraint_)
    

Map transformations of the target to the object

from_max_x
    

Top range of X axis source motion

Type:
    

float in [-inf, inf], default 0.0

from_max_x_rot
    

Top range of X axis source motion

Type:
    

float in [-inf, inf], default 0.0

from_max_x_scale
    

Top range of X axis source motion

Type:
    

float in [-inf, inf], default 0.0

from_max_y
    

Top range of Y axis source motion

Type:
    

float in [-inf, inf], default 0.0

from_max_y_rot
    

Top range of Y axis source motion

Type:
    

float in [-inf, inf], default 0.0

from_max_y_scale
    

Top range of Y axis source motion

Type:
    

float in [-inf, inf], default 0.0

from_max_z
    

Top range of Z axis source motion

Type:
    

float in [-inf, inf], default 0.0

from_max_z_rot
    

Top range of Z axis source motion

Type:
    

float in [-inf, inf], default 0.0

from_max_z_scale
    

Top range of Z axis source motion

Type:
    

float in [-inf, inf], default 0.0

from_min_x
    

Bottom range of X axis source motion

Type:
    

float in [-inf, inf], default 0.0

from_min_x_rot
    

Bottom range of X axis source motion

Type:
    

float in [-inf, inf], default 0.0

from_min_x_scale
    

Bottom range of X axis source motion

Type:
    

float in [-inf, inf], default 0.0

from_min_y
    

Bottom range of Y axis source motion

Type:
    

float in [-inf, inf], default 0.0

from_min_y_rot
    

Bottom range of Y axis source motion

Type:
    

float in [-inf, inf], default 0.0

from_min_y_scale
    

Bottom range of Y axis source motion

Type:
    

float in [-inf, inf], default 0.0

from_min_z
    

Bottom range of Z axis source motion

Type:
    

float in [-inf, inf], default 0.0

from_min_z_rot
    

Bottom range of Z axis source motion

Type:
    

float in [-inf, inf], default 0.0

from_min_z_scale
    

Bottom range of Z axis source motion

Type:
    

float in [-inf, inf], default 0.0

from_rotation_mode
    

Specify the type of rotation channels to use

Type:
    

enum in [Driver Target Rotation Mode Items](../../bpy_types_enum_items/driver_target_rotation_mode_items.md#rna-enum-driver-target-rotation-mode-items), default `'AUTO'`

map_from
    

The transformation type to use from the target

Type:
    

enum in [`'LOCATION'`, `'ROTATION'`, `'SCALE'`], default `'LOCATION'`

map_to
    

The transformation type to affect on the constrained object

Type:
    

enum in [`'LOCATION'`, `'ROTATION'`, `'SCALE'`], default `'LOCATION'`

map_to_x_from
    

The source axis constrained object’s X axis uses

Type:
    

enum in [Axis Xyz Items](../../bpy_types_enum_items/axis_xyz_items.md#rna-enum-axis-xyz-items), default `'X'`

map_to_y_from
    

The source axis constrained object’s Y axis uses

Type:
    

enum in [Axis Xyz Items](../../bpy_types_enum_items/axis_xyz_items.md#rna-enum-axis-xyz-items), default `'X'`

map_to_z_from
    

The source axis constrained object’s Z axis uses

Type:
    

enum in [Axis Xyz Items](../../bpy_types_enum_items/axis_xyz_items.md#rna-enum-axis-xyz-items), default `'X'`

mix_mode
    

Specify how to combine the new location with original

  * `REPLACE` Replace – Replace component values.

  * `ADD` Add – Add component values together.


Type:
    

enum in [`'REPLACE'`, `'ADD'`], default `'ADD'`

mix_mode_rot
    

Specify how to combine the new rotation with original

  * `REPLACE` Replace – Replace component values.

  * `ADD` Add – Add component values together.

  * `BEFORE` Before Original – Apply new rotation before original, as if it was on a parent.

  * `AFTER` After Original – Apply new rotation after original, as if it was on a child.


Type:
    

enum in [`'REPLACE'`, `'ADD'`, `'BEFORE'`, `'AFTER'`], default `'ADD'`

mix_mode_scale
    

Specify how to combine the new scale with original

  * `REPLACE` Replace – Replace component values.

  * `MULTIPLY` Multiply – Multiply component values together.


Type:
    

enum in [`'REPLACE'`, `'MULTIPLY'`], default `'REPLACE'`

subtarget
    

Armature bone, mesh or lattice vertex group, …

Type:
    

string, default “”, (never None)

target
    

Target object

Type:
    

[[Object]]

to_euler_order
    

Explicitly specify the output euler rotation order

  * `AUTO` Default – Euler using the default rotation order.

  * `XYZ` XYZ Euler – Euler using the XYZ rotation order.

  * `XZY` XZY Euler – Euler using the XZY rotation order.

  * `YXZ` YXZ Euler – Euler using the YXZ rotation order.

  * `YZX` YZX Euler – Euler using the YZX rotation order.

  * `ZXY` ZXY Euler – Euler using the ZXY rotation order.

  * `ZYX` ZYX Euler – Euler using the ZYX rotation order.


Type:
    

enum in [`'AUTO'`, `'XYZ'`, `'XZY'`, `'YXZ'`, `'YZX'`, `'ZXY'`, `'ZYX'`], default `'AUTO'`

to_max_x
    

Top range of X axis destination motion

Type:
    

float in [-inf, inf], default 0.0

to_max_x_rot
    

Top range of X axis destination motion

Type:
    

float in [-inf, inf], default 0.0

to_max_x_scale
    

Top range of X axis destination motion

Type:
    

float in [-inf, inf], default 0.0

to_max_y
    

Top range of Y axis destination motion

Type:
    

float in [-inf, inf], default 0.0

to_max_y_rot
    

Top range of Y axis destination motion

Type:
    

float in [-inf, inf], default 0.0

to_max_y_scale
    

Top range of Y axis destination motion

Type:
    

float in [-inf, inf], default 0.0

to_max_z
    

Top range of Z axis destination motion

Type:
    

float in [-inf, inf], default 0.0

to_max_z_rot
    

Top range of Z axis destination motion

Type:
    

float in [-inf, inf], default 0.0

to_max_z_scale
    

Top range of Z axis destination motion

Type:
    

float in [-inf, inf], default 0.0

to_min_x
    

Bottom range of X axis destination motion

Type:
    

float in [-inf, inf], default 0.0

to_min_x_rot
    

Bottom range of X axis destination motion

Type:
    

float in [-inf, inf], default 0.0

to_min_x_scale
    

Bottom range of X axis destination motion

Type:
    

float in [-inf, inf], default 0.0

to_min_y
    

Bottom range of Y axis destination motion

Type:
    

float in [-inf, inf], default 0.0

to_min_y_rot
    

Bottom range of Y axis destination motion

Type:
    

float in [-inf, inf], default 0.0

to_min_y_scale
    

Bottom range of Y axis destination motion

Type:
    

float in [-inf, inf], default 0.0

to_min_z
    

Bottom range of Z axis destination motion

Type:
    

float in [-inf, inf], default 0.0

to_min_z_rot
    

Bottom range of Z axis destination motion

Type:
    

float in [-inf, inf], default 0.0

to_min_z_scale
    

Bottom range of Z axis destination motion

Type:
    

float in [-inf, inf], default 0.0

use_motion_extrapolate
    

Extrapolate ranges

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
