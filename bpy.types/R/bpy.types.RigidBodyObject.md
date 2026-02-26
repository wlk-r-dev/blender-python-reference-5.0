# RigidBodyObject(bpy_struct)

base class — [[bpy_struct]]

_class _bpy.types.RigidBodyObject(_bpy_struct_)
    

Settings for object participating in Rigid Body Simulation

angular_damping
    

Amount of angular velocity that is lost over time

Type:
    

float in [0, 1], default 0.1

collision_collections
    

Collision collections rigid body belongs to

Type:
    

boolean array of 20 items, default (False, False, False, False, False, False, False, False, False, False, False, False, False, False, False, False, False, False, False, False)

collision_margin
    

Threshold of distance near surface where collisions are still considered (best results when non-zero)

Type:
    

float in [0, 1], default 0.04

collision_shape
    

Collision Shape of object in Rigid Body Simulations

Type:
    

enum in [Rigidbody Object Shape Items](../../bpy_types_enum_items/rigidbody_object_shape_items.md#rna-enum-rigidbody-object-shape-items), default `'BOX'`

deactivate_angular_velocity
    

Angular Velocity below which simulation stops simulating object

Type:
    

float in [0, inf], default 0.5

deactivate_linear_velocity
    

Linear Velocity below which simulation stops simulating object

Type:
    

float in [0, inf], default 0.4

enabled
    

Rigid Body actively participates to the simulation

Type:
    

boolean, default False

friction
    

Resistance of object to movement

Type:
    

float in [0, inf], default 0.5

kinematic
    

Allow rigid body to be controlled by the animation system

Type:
    

boolean, default False

linear_damping
    

Amount of linear velocity that is lost over time

Type:
    

float in [0, 1], default 0.04

mass
    

How much the object ‘weighs’ irrespective of gravity

Type:
    

float in [0.001, inf], default 1.0

mesh_source
    

Source of the mesh used to create collision shape

  * `BASE` Base – Base mesh.

  * `DEFORM` Deform – Deformations (shape keys, deform modifiers).

  * `FINAL` Final – All modifiers.


Type:
    

enum in [`'BASE'`, `'DEFORM'`, `'FINAL'`], default `'BASE'`

restitution
    

Tendency of object to bounce after colliding with another (0 = stays still, 1 = perfectly elastic)

Type:
    

float in [0, inf], default 0.0

type
    

Role of object in Rigid Body Simulations

Type:
    

enum in [Rigidbody Object Type Items](../../bpy_types_enum_items/rigidbody_object_type_items.md#rna-enum-rigidbody-object-type-items), default `'ACTIVE'`

use_deactivation
    

Enable deactivation of resting rigid bodies (increases performance and stability but can cause glitches)

Type:
    

boolean, default True

use_deform
    

Rigid body deforms during simulation

Type:
    

boolean, default False

use_margin
    

Use custom collision margin (some shapes will have a visible gap around them)

Type:
    

boolean, default False

use_start_deactivated
    

Deactivate rigid body at the start of the simulation

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

| 


  
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

| 

  * [[bpy_struct.keyframe_delete]]
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

  
---|---  
  
## References

  * [[Object.rigid_body]]

| 


  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
