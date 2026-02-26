# SPHFluidSettings(bpy_struct)

base class — [[bpy_struct]]

_class _bpy.types.SPHFluidSettings(_bpy_struct_)
    

Settings for particle fluids physics

buoyancy
    

Artificial buoyancy force in negative gravity direction based on pressure differences inside the fluid

Type:
    

float in [0, 10], default 0.0

fluid_radius
    

Fluid interaction radius

Type:
    

float in [0, 20], default 0.0

linear_viscosity
    

Linear viscosity

Type:
    

float in [0, 100], default 0.0

plasticity
    

How much the spring rest length can change after the elastic limit is crossed

Type:
    

float in [0, 100], default 0.0

repulsion
    

How strongly the fluid tries to keep from clustering (factor of stiffness)

Type:
    

float in [0, 100], default 0.0

rest_density
    

Fluid rest density

Type:
    

float in [0, 10000], default 0.0

rest_length
    

Spring rest length (factor of particle radius)

Type:
    

float in [0, 2], default 0.0

solver
    

The code used to calculate internal forces on particles

  * `DDR` Double-Density – An artistic solver with strong surface tension effects (original).

  * `CLASSICAL` Classical – A more physically-accurate solver.


Type:
    

enum in [`'DDR'`, `'CLASSICAL'`], default `'DDR'`

spring_force
    

Spring force

Type:
    

float in [0, 100], default 0.0

spring_frames
    

Create springs for this number of frames since particles birth (0 is always)

Type:
    

int in [0, 100], default 0

stiff_viscosity
    

Creates viscosity for expanding fluid

Type:
    

float in [0, 100], default 0.0

stiffness
    

How incompressible the fluid is (speed of sound)

Type:
    

float in [0, 1000], default 0.0

use_factor_density
    

Density is calculated as a factor of default density (depends on particle size)

Type:
    

boolean, default False

use_factor_radius
    

Interaction radius is a factor of 4 * particle size

Type:
    

boolean, default False

use_factor_repulsion
    

Repulsion is a factor of stiffness

Type:
    

boolean, default False

use_factor_rest_length
    

Spring rest length is a factor of 2 * particle size

Type:
    

boolean, default False

use_factor_stiff_viscosity
    

Stiff viscosity is a factor of normal viscosity

Type:
    

boolean, default False

use_initial_rest_length
    

Use the initial length as spring rest length instead of 2 * particle size

Type:
    

boolean, default False

use_viscoelastic_springs
    

Use viscoelastic springs instead of Hooke’s springs

Type:
    

boolean, default False

yield_ratio
    

How much the spring has to be stretched/compressed in order to change its rest length

Type:
    

float in [0, 1], default 0.0

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

  * [[ParticleSettings.fluid]]

| 


  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
