# RigidBodyConstraint(bpy_struct)

base class — [`bpy_struct`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct "bpy.types.bpy_struct")

_class _bpy.types.RigidBodyConstraint(_bpy_struct_)
    

Constraint influencing Objects inside Rigid Body Simulation

breaking_threshold
    

Impulse threshold that must be reached for the constraint to break

Type:
    

float in [0, inf], default 10.0

disable_collisions
    

Disable collisions between constrained rigid bodies

Type:
    

boolean, default False

enabled
    

Enable this constraint

Type:
    

boolean, default False

limit_ang_x_lower
    

Lower limit of X axis rotation

Type:
    

float in [-6.28319, 6.28319], default -0.785398

limit_ang_x_upper
    

Upper limit of X axis rotation

Type:
    

float in [-6.28319, 6.28319], default 0.785398

limit_ang_y_lower
    

Lower limit of Y axis rotation

Type:
    

float in [-6.28319, 6.28319], default -0.785398

limit_ang_y_upper
    

Upper limit of Y axis rotation

Type:
    

float in [-6.28319, 6.28319], default 0.785398

limit_ang_z_lower
    

Lower limit of Z axis rotation

Type:
    

float in [-6.28319, 6.28319], default -0.785398

limit_ang_z_upper
    

Upper limit of Z axis rotation

Type:
    

float in [-6.28319, 6.28319], default 0.785398

limit_lin_x_lower
    

Lower limit of X axis translation

Type:
    

float in [-inf, inf], default -1.0

limit_lin_x_upper
    

Upper limit of X axis translation

Type:
    

float in [-inf, inf], default 1.0

limit_lin_y_lower
    

Lower limit of Y axis translation

Type:
    

float in [-inf, inf], default -1.0

limit_lin_y_upper
    

Upper limit of Y axis translation

Type:
    

float in [-inf, inf], default 1.0

limit_lin_z_lower
    

Lower limit of Z axis translation

Type:
    

float in [-inf, inf], default -1.0

limit_lin_z_upper
    

Upper limit of Z axis translation

Type:
    

float in [-inf, inf], default 1.0

motor_ang_max_impulse
    

Maximum angular motor impulse

Type:
    

float in [0, inf], default 1.0

motor_ang_target_velocity
    

Target angular motor velocity

Type:
    

float in [-inf, inf], default 1.0

motor_lin_max_impulse
    

Maximum linear motor impulse

Type:
    

float in [0, inf], default 1.0

motor_lin_target_velocity
    

Target linear motor velocity

Type:
    

float in [-inf, inf], default 1.0

object1
    

First Rigid Body Object to be constrained

Type:
    

[`Object`](../O/bpy.types.Object.md#bpy.types.Object "bpy.types.Object")

object2
    

Second Rigid Body Object to be constrained

Type:
    

[`Object`](../O/bpy.types.Object.md#bpy.types.Object "bpy.types.Object")

solver_iterations
    

Number of constraint solver iterations made per simulation step (higher values are more accurate but slower)

Type:
    

int in [1, 1000], default 10

spring_damping_ang_x
    

Damping on the X rotational axis

Type:
    

float in [0, inf], default 0.5

spring_damping_ang_y
    

Damping on the Y rotational axis

Type:
    

float in [0, inf], default 0.5

spring_damping_ang_z
    

Damping on the Z rotational axis

Type:
    

float in [0, inf], default 0.5

spring_damping_x
    

Damping on the X axis

Type:
    

float in [0, inf], default 0.5

spring_damping_y
    

Damping on the Y axis

Type:
    

float in [0, inf], default 0.5

spring_damping_z
    

Damping on the Z axis

Type:
    

float in [0, inf], default 0.5

spring_stiffness_ang_x
    

Stiffness on the X rotational axis

Type:
    

float in [0, inf], default 10.0

spring_stiffness_ang_y
    

Stiffness on the Y rotational axis

Type:
    

float in [0, inf], default 10.0

spring_stiffness_ang_z
    

Stiffness on the Z rotational axis

Type:
    

float in [0, inf], default 10.0

spring_stiffness_x
    

Stiffness on the X axis

Type:
    

float in [0, inf], default 10.0

spring_stiffness_y
    

Stiffness on the Y axis

Type:
    

float in [0, inf], default 10.0

spring_stiffness_z
    

Stiffness on the Z axis

Type:
    

float in [0, inf], default 10.0

spring_type
    

Which implementation of spring to use

  * `SPRING1` Blender 2.7 – Spring implementation used in Blender 2.7. Damping is capped at 1.0.

  * `SPRING2` Blender 2.8 – New implementation available since 2.8.


Type:
    

enum in [`'SPRING1'`, `'SPRING2'`], default `'SPRING1'`

type
    

Type of Rigid Body Constraint

Type:
    

enum in [Rigidbody Constraint Type Items](../../bpy_types_enum_items/rigidbody_constraint_type_items.md#rna-enum-rigidbody-constraint-type-items), default `'POINT'`

use_breaking
    

Constraint can be broken if it receives an impulse above the threshold

Type:
    

boolean, default False

use_limit_ang_x
    

Limit rotation around X axis

Type:
    

boolean, default False

use_limit_ang_y
    

Limit rotation around Y axis

Type:
    

boolean, default False

use_limit_ang_z
    

Limit rotation around Z axis

Type:
    

boolean, default False

use_limit_lin_x
    

Limit translation on X axis

Type:
    

boolean, default False

use_limit_lin_y
    

Limit translation on Y axis

Type:
    

boolean, default False

use_limit_lin_z
    

Limit translation on Z axis

Type:
    

boolean, default False

use_motor_ang
    

Enable angular motor

Type:
    

boolean, default False

use_motor_lin
    

Enable linear motor

Type:
    

boolean, default False

use_override_solver_iterations
    

Override the number of solver iterations for this constraint

Type:
    

boolean, default False

use_spring_ang_x
    

Enable spring on X rotational axis

Type:
    

boolean, default False

use_spring_ang_y
    

Enable spring on Y rotational axis

Type:
    

boolean, default False

use_spring_ang_z
    

Enable spring on Z rotational axis

Type:
    

boolean, default False

use_spring_x
    

Enable spring on X axis

Type:
    

boolean, default False

use_spring_y
    

Enable spring on Y axis

Type:
    

boolean, default False

use_spring_z
    

Enable spring on Z axis

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

| 


  
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

| 

  * [`bpy_struct.keyframe_delete`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.keyframe_delete "bpy.types.bpy_struct.keyframe_delete")
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

  
---|---  
  
## References

  * [`Object.rigid_body_constraint`](../O/bpy.types.Object.md#bpy.types.Object.rigid_body_constraint "bpy.types.Object.rigid_body_constraint")

| 


  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
