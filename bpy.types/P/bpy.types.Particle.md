# Particle(bpy_struct)

base class — [[bpy_struct]]

_class _bpy.types.Particle(_bpy_struct_)
    

Particle in a particle system

alive_state
    

Type:
    

enum in [`'DEAD'`, `'UNBORN'`, `'ALIVE'`, `'DYING'`], default `'DEAD'`

angular_velocity
    

Type:
    

[[mathutils.Vector]] of 3 items in [-inf, inf], default (0.0, 0.0, 0.0)

birth_time
    

Type:
    

float in [-inf, inf], default 0.0

die_time
    

Type:
    

float in [-inf, inf], default 0.0

hair_keys
    

Type:
    

[[bpy_prop_collection]] of [[ParticleHairKey]], (readonly)

is_exist
    

Type:
    

boolean, default False, (readonly)

is_visible
    

Type:
    

boolean, default False, (readonly)

lifetime
    

Type:
    

float in [-inf, inf], default 0.0

location
    

Type:
    

[[mathutils.Vector]] of 3 items in [-inf, inf], default (0.0, 0.0, 0.0)

particle_keys
    

Type:
    

[[bpy_prop_collection]] of [[ParticleKey]], (readonly)

prev_angular_velocity
    

Type:
    

[[mathutils.Vector]] of 3 items in [-inf, inf], default (0.0, 0.0, 0.0)

prev_location
    

Type:
    

[[mathutils.Vector]] of 3 items in [-inf, inf], default (0.0, 0.0, 0.0)

prev_rotation
    

Type:
    

[[mathutils.Quaternion]] rotation of 4 items in [-inf, inf], default (0.0, 0.0, 0.0, 0.0)

prev_velocity
    

Type:
    

[[mathutils.Vector]] of 3 items in [-inf, inf], default (0.0, 0.0, 0.0)

rotation
    

Type:
    

[[mathutils.Quaternion]] rotation of 4 items in [-inf, inf], default (0.0, 0.0, 0.0, 0.0)

size
    

Type:
    

float in [-inf, inf], default 0.0

velocity
    

Type:
    

[[mathutils.Vector]] of 3 items in [-inf, inf], default (0.0, 0.0, 0.0)

uv_on_emitter(_modifier_)
    

Obtain UV coordinates for a particle on an evaluated mesh.

Parameters:
    

**modifier** ([[ParticleSystemModifier]], (never None)) – Particle modifier from an evaluated object

Returns:
    

uv

Return type:
    

[[mathutils.Vector]] of 2 items in [-inf, inf]

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

  * [[ParticleHairKey.co_object]]
  * [[ParticleHairKey.co_object_set]]
  * [[ParticleSystem.mcol_on_emitter]]

| 

  * [[ParticleSystem.particles]]
  * [[ParticleSystem.uv_on_emitter]]

  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
