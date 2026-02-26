# RigidBodyWorld(bpy_struct)

base class — [[bpy_struct]]

_class _bpy.types.RigidBodyWorld(_bpy_struct_)
    

Self-contained rigid body simulation environment and settings

collection
    

Collection containing objects participating in this simulation

Type:
    

[[Collection]]

constraints
    

Collection containing rigid body constraint objects

Type:
    

[[Collection]]

effector_weights
    

Type:
    

[[EffectorWeights]], (readonly)

enabled
    

Simulation will be evaluated

Type:
    

boolean, default False

point_cache
    

Type:
    

[[PointCache]], (readonly, never None)

solver_iterations
    

Number of constraint solver iterations made per simulation step (higher values are more accurate but slower)

Type:
    

int in [1, 1000], default 10

substeps_per_frame
    

Number of simulation steps taken per frame (higher values are more accurate but slower)

Type:
    

int in [1, 32767], default 10

time_scale
    

Change the speed of the simulation

Type:
    

float in [0, 100], default 1.0

use_split_impulse
    

Reduce extra velocity that can build up when objects collide (lowers simulation stability a little so use only when necessary)

Type:
    

boolean, default False

convex_sweep_test(_object_ , _start_ , _end_)
    

Sweep test convex rigidbody against the current rigidbody world

Parameters:
    

**object** ([[Object]], (never None)) – Rigidbody object with a convex collision shape

Returns:
    

`object_location`, The hit location of this sweep test, [[mathutils.Vector]] of 3 items in [-inf, inf]

`hitpoint`, The hit location of this sweep test, [[mathutils.Vector]] of 3 items in [-inf, inf]

`normal`, The face normal at the sweep test hit location, [[mathutils.Vector]] of 3 items in [-inf, inf]

`has_hit`, If the function has found collision point, value is 1, otherwise 0, int in [-inf, inf]

Return type:
    

([[mathutils.Vector]] of 3 items in [-inf, inf], [[mathutils.Vector]] of 3 items in [-inf, inf], [[mathutils.Vector]] of 3 items in [-inf, inf], int in [-inf, inf])

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

  * [[Scene.rigidbody_world]]

| 


  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
