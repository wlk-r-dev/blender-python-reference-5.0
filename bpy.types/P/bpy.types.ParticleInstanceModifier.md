# ParticleInstanceModifier(Modifier)

base classes — [[bpy_struct]], [[Modifier]]

_class _bpy.types.ParticleInstanceModifier(_Modifier_)
    

Particle system instancing modifier

axis
    

Pole axis for rotation

Type:
    

enum in [Axis Xyz Items](../../bpy_types_enum_items/axis_xyz_items.md#rna-enum-axis-xyz-items), default `'Z'`

index_layer_name
    

Custom data layer name for the index

Type:
    

string, default “”, (never None)

object
    

Object that has the particle system

Type:
    

[[Object]]

particle_amount
    

Amount of particles to use for instancing

Type:
    

float in [0, 1], default 1.0

particle_offset
    

Relative offset of particles to use for instancing, to avoid overlap of multiple instances

Type:
    

float in [0, 1], default 0.0

particle_system
    

Type:
    

[[ParticleSystem]]

particle_system_index
    

Type:
    

int in [1, 32767], default 1

position
    

Position along path

Type:
    

float in [0, 1], default 1.0

random_position
    

Randomize position along path

Type:
    

float in [0, 1], default 0.0

random_rotation
    

Randomize rotation around path

Type:
    

float in [0, 1], default 0.0

rotation
    

Rotation around path

Type:
    

float in [0, 1], default 0.0

show_alive
    

Show instances when particles are alive

Type:
    

boolean, default True

show_dead
    

Show instances when particles are dead

Type:
    

boolean, default True

show_unborn
    

Show instances when particles are unborn

Type:
    

boolean, default True

space
    

Space to use for copying mesh data

  * `LOCAL` Local – Use offset from the particle object in the instance object.

  * `WORLD` World – Use world space offset in the instance object.


Type:
    

enum in [`'LOCAL'`, `'WORLD'`], default `'WORLD'`

use_children
    

Create instances from child particles

Type:
    

boolean, default False

use_normal
    

Create instances from normal particles

Type:
    

boolean, default True

use_path
    

Create instances along particle paths

Type:
    

boolean, default False

use_preserve_shape
    

Don’t stretch the object

Type:
    

boolean, default False

use_size
    

Use particle size to scale the instances

Type:
    

boolean, default False

value_layer_name
    

Custom data layer name for the randomized value

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
