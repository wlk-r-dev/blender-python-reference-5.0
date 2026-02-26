# TransformConstraint(Constraint)

base classes — [`bpy_struct`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct "bpy.types.bpy_struct"), [`Constraint`](../C/bpy.types.Constraint.md#bpy.types.Constraint "bpy.types.Constraint")

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
    

[`Object`](../O/bpy.types.Object.md#bpy.types.Object "bpy.types.Object")

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
    

[`bpy.types.Struct`](../S/bpy.types.Struct.md#bpy.types.Struct "bpy.types.Struct") subclass

_classmethod _bl_rna_get_subclass_py(_id_ , _default =None_, _/_)
    

Parameters:
    

**id** (_str_) – The RNA type identifier.

Returns:
    

The class or default when not found.

Return type:
    

type

## Inherited Properties

  * [`bpy_struct.id_data`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.id_data "bpy.types.bpy_struct.id_data")
  * [`Constraint.name`](../C/bpy.types.Constraint.md#bpy.types.Constraint.name "bpy.types.Constraint.name")
  * [`Constraint.type`](../C/bpy.types.Constraint.md#bpy.types.Constraint.type "bpy.types.Constraint.type")
  * [`Constraint.is_override_data`](../C/bpy.types.Constraint.md#bpy.types.Constraint.is_override_data "bpy.types.Constraint.is_override_data")
  * [`Constraint.owner_space`](../C/bpy.types.Constraint.md#bpy.types.Constraint.owner_space "bpy.types.Constraint.owner_space")
  * [`Constraint.target_space`](../C/bpy.types.Constraint.md#bpy.types.Constraint.target_space "bpy.types.Constraint.target_space")
  * [`Constraint.space_object`](../C/bpy.types.Constraint.md#bpy.types.Constraint.space_object "bpy.types.Constraint.space_object")
  * [`Constraint.space_subtarget`](../C/bpy.types.Constraint.md#bpy.types.Constraint.space_subtarget "bpy.types.Constraint.space_subtarget")

| 

  * [`Constraint.mute`](../C/bpy.types.Constraint.md#bpy.types.Constraint.mute "bpy.types.Constraint.mute")
  * [`Constraint.enabled`](../C/bpy.types.Constraint.md#bpy.types.Constraint.enabled "bpy.types.Constraint.enabled")
  * [`Constraint.show_expanded`](../C/bpy.types.Constraint.md#bpy.types.Constraint.show_expanded "bpy.types.Constraint.show_expanded")
  * [`Constraint.is_valid`](../C/bpy.types.Constraint.md#bpy.types.Constraint.is_valid "bpy.types.Constraint.is_valid")
  * [`Constraint.active`](../C/bpy.types.Constraint.md#bpy.types.Constraint.active "bpy.types.Constraint.active")
  * [`Constraint.influence`](../C/bpy.types.Constraint.md#bpy.types.Constraint.influence "bpy.types.Constraint.influence")
  * [`Constraint.error_location`](../C/bpy.types.Constraint.md#bpy.types.Constraint.error_location "bpy.types.Constraint.error_location")
  * [`Constraint.error_rotation`](../C/bpy.types.Constraint.md#bpy.types.Constraint.error_rotation "bpy.types.Constraint.error_rotation")

  
---|---  
  
## Inherited Functions

  * [`bpy_struct.as_pointer`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.as_pointer "bpy.types.bpy_struct.as_pointer")
  * [`bpy_struct.driver_add`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.driver_add "bpy.types.bpy_struct.driver_add")
  * [`bpy_struct.driver_remove`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.driver_remove "bpy.types.bpy_struct.driver_remove")
  * [`bpy_struct.get`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.get "bpy.types.bpy_struct.get")
  * [`bpy_struct.id_properties_clear`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.id_properties_clear "bpy.types.bpy_struct.id_properties_clear")
  * [`bpy_struct.id_properties_ensure`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.id_properties_ensure "bpy.types.bpy_struct.id_properties_ensure")
  * [`bpy_struct.id_properties_ui`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.id_properties_ui "bpy.types.bpy_struct.id_properties_ui")
  * [`bpy_struct.is_property_hidden`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.is_property_hidden "bpy.types.bpy_struct.is_property_hidden")
  * [`bpy_struct.is_property_overridable_library`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.is_property_overridable_library "bpy.types.bpy_struct.is_property_overridable_library")
  * [`bpy_struct.is_property_readonly`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.is_property_readonly "bpy.types.bpy_struct.is_property_readonly")
  * [`bpy_struct.is_property_set`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.is_property_set "bpy.types.bpy_struct.is_property_set")
  * [`bpy_struct.items`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.items "bpy.types.bpy_struct.items")
  * [`bpy_struct.keyframe_delete`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.keyframe_delete "bpy.types.bpy_struct.keyframe_delete")

| 

  * [`bpy_struct.keyframe_insert`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.keyframe_insert "bpy.types.bpy_struct.keyframe_insert")
  * [`bpy_struct.keys`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.keys "bpy.types.bpy_struct.keys")
  * [`bpy_struct.path_from_id`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.path_from_id "bpy.types.bpy_struct.path_from_id")
  * [`bpy_struct.path_from_module`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.path_from_module "bpy.types.bpy_struct.path_from_module")
  * [`bpy_struct.path_resolve`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.path_resolve "bpy.types.bpy_struct.path_resolve")
  * [`bpy_struct.pop`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.pop "bpy.types.bpy_struct.pop")
  * [`bpy_struct.property_overridable_library_set`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.property_overridable_library_set "bpy.types.bpy_struct.property_overridable_library_set")
  * [`bpy_struct.property_unset`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.property_unset "bpy.types.bpy_struct.property_unset")
  * [`bpy_struct.rna_ancestors`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.rna_ancestors "bpy.types.bpy_struct.rna_ancestors")
  * [`bpy_struct.type_recast`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.type_recast "bpy.types.bpy_struct.type_recast")
  * [`bpy_struct.values`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.values "bpy.types.bpy_struct.values")
  * [`Constraint.bl_rna_get_subclass`](../C/bpy.types.Constraint.md#bpy.types.Constraint.bl_rna_get_subclass "bpy.types.Constraint.bl_rna_get_subclass")
  * [`Constraint.bl_rna_get_subclass_py`](../C/bpy.types.Constraint.md#bpy.types.Constraint.bl_rna_get_subclass_py "bpy.types.Constraint.bl_rna_get_subclass_py")

  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
