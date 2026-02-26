# CollisionSettings(bpy_struct)

base class — [[bpy_struct]]

_class _bpy.types.CollisionSettings(_bpy_struct_)
    

Collision settings for object in physics simulation

absorption
    

How much of effector force gets lost during collision with this object (in percent)

Type:
    

float in [0, 1], default 0.0

cloth_friction
    

Friction for cloth collisions

Type:
    

float in [0, 80], default 0.0

damping
    

Amount of damping during collision

Type:
    

float in [0, 1], default 0.0

damping_factor
    

Amount of damping during particle collision

Type:
    

float in [0, 1], default 0.0

damping_random
    

Random variation of damping

Type:
    

float in [0, 1], default 0.0

friction_factor
    

Amount of friction during particle collision

Type:
    

float in [0, 1], default 0.0

friction_random
    

Random variation of friction

Type:
    

float in [0, 1], default 0.0

permeability
    

Chance that the particle will pass through the mesh

Type:
    

float in [0, 1], default 0.0

stickiness
    

Amount of stickiness to surface collision

Type:
    

float in [0, 10], default 0.0

thickness_inner
    

Inner face thickness (only used by softbodies)

Type:
    

float in [0.001, 1], default 0.0

thickness_outer
    

Outer face thickness

Type:
    

float in [0.001, 1], default 0.0

use
    

Enable this object as a collider for physics systems

Type:
    

boolean, default False

use_culling
    

Cloth collision acts with respect to the collider normals (improves penetration recovery)

Type:
    

boolean, default False

use_normal
    

Cloth collision impulses act in the direction of the collider normals (more reliable in some cases)

Type:
    

boolean, default False

use_particle_kill
    

Kill collided particles

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

  * [[CollisionModifier.settings]]

| 

  * [[Object.collision]]

  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
