# ParticleSettings(ID)

base classes — [`bpy_struct`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct "bpy.types.bpy_struct"), [`ID`](../I/bpy.types.ID.md#bpy.types.ID "bpy.types.ID")

_class _bpy.types.ParticleSettings(_ID_)
    

Particle settings, reusable by multiple particle systems

active_instanceweight
    

Type:
    

[`ParticleDupliWeight`](bpy.types.ParticleDupliWeight.md#bpy.types.ParticleDupliWeight "bpy.types.ParticleDupliWeight"), (readonly)

active_instanceweight_index
    

Type:
    

int in [0, inf], default 0

active_texture
    

Active texture slot being displayed

Type:
    

[`Texture`](../T/bpy.types.Texture.md#bpy.types.Texture "bpy.types.Texture")

active_texture_index
    

Index of active texture slot

Type:
    

int in [0, 17], default 0

adaptive_angle
    

How many degrees path has to curve to make another render segment

Type:
    

int in [0, 45], default 5

adaptive_pixel
    

How many pixels path has to cover to make another render segment

Type:
    

int in [0, 50], default 3

angular_velocity_factor
    

Angular velocity amount (in radians per second)

Type:
    

float in [-200, 200], default 0.0

angular_velocity_mode
    

What axis is used to change particle rotation with time

Type:
    

enum in [`'NONE'`, `'VELOCITY'`, `'HORIZONTAL'`, `'VERTICAL'`, `'GLOBAL_X'`, `'GLOBAL_Y'`, `'GLOBAL_Z'`, `'RAND'`], default `'VELOCITY'`

animation_data
    

Animation data for this data-block

Type:
    

[`AnimData`](../A/bpy.types.AnimData.md#bpy.types.AnimData "bpy.types.AnimData"), (readonly)

apply_effector_to_children
    

Apply effectors to children

Type:
    

boolean, default False

apply_guide_to_children
    

Type:
    

boolean, default False

bending_random
    

Random stiffness of hairs

Type:
    

float in [0, 1], default 0.0

boids
    

Type:
    

[`BoidSettings`](../B/bpy.types.BoidSettings.md#bpy.types.BoidSettings "bpy.types.BoidSettings"), (readonly)

branch_threshold
    

Threshold of branching

Type:
    

float in [0, 1], default 0.0

brownian_factor
    

Amount of random, erratic particle movement

Type:
    

float in [0, 200], default 0.0

child_length
    

Length of child paths

Type:
    

float in [0, 1], default 1.0

child_length_threshold
    

Amount of particles left untouched by child path length

Type:
    

float in [0, 1], default 0.0

child_parting_factor
    

Create parting in the children based on parent strands

Type:
    

float in [0, 1], default 0.0

child_parting_max
    

Maximum root to tip angle (tip distance/root distance for long hair)

Type:
    

float in [0, 180], default 0.0

child_parting_min
    

Minimum root to tip angle (tip distance/root distance for long hair)

Type:
    

float in [0, 180], default 0.0

child_percent
    

Number of children per parent

Type:
    

int in [0, 100000], default 10

child_radius
    

Radius of children around parent

Type:
    

float in [0, 100000], default 0.2

child_roundness
    

Roundness of children around parent

Type:
    

float in [0, 1], default 0.0

child_size
    

A multiplier for the child particle size

Type:
    

float in [0.001, 100000], default 1.0

child_size_random
    

Random variation to the size of the child particles

Type:
    

float in [0, 1], default 0.0

child_type
    

Create child particles

Type:
    

enum in [`'NONE'`, `'SIMPLE'`, `'INTERPOLATED'`], default `'NONE'`

clump_curve
    

Curve defining clump tapering

Type:
    

[`CurveMapping`](../C/bpy.types.CurveMapping.md#bpy.types.CurveMapping "bpy.types.CurveMapping"), (readonly)

clump_factor
    

Amount of clumping

Type:
    

float in [-1, 1], default 0.0

clump_noise_size
    

Size of clump noise

Type:
    

float in [1e-05, 100000], default 1.0

clump_shape
    

Shape of clumping

Type:
    

float in [-0.999, 0.999], default 0.0

collision_collection
    

Limit colliders to this collection

Type:
    

[`Collection`](../C/bpy.types.Collection.md#bpy.types.Collection "bpy.types.Collection")

color_maximum
    

Maximum length of the particle color vector

Type:
    

float in [0.01, 100], default 1.0

count
    

Total number of particles

Type:
    

int in [0, inf], default 1000

courant_target
    

The relative distance a particle can move before requiring more subframes (target Courant number); 0.01 to 0.3 is the recommended range

Type:
    

float in [0.0001, 10], default 0.2

create_long_hair_children
    

Calculate children that suit long hair well

Type:
    

boolean, default False

damping
    

Amount of damping

Type:
    

float in [0, 1], default 0.0

display_color
    

Display additional particle data as a color

Type:
    

enum in [`'NONE'`, `'MATERIAL'`, `'VELOCITY'`, `'ACCELERATION'`], default `'MATERIAL'`

display_method
    

How particles are displayed in viewport

Type:
    

enum in [`'NONE'`, `'RENDER'`, `'DOT'`, `'CIRC'`, `'CROSS'`, `'AXIS'`], default `'RENDER'`

display_percentage
    

Percentage of particles to display in 3D view

Type:
    

int in [0, 100], default 100

display_size
    

Size of particles on viewport

Type:
    

float in [0, 1000], default 0.1

display_step
    

How many steps paths are displayed with (power of 2)

Type:
    

int in [0, 10], default 2

distribution
    

How to distribute particles on selected element

Type:
    

enum in [`'JIT'`, `'RAND'`, `'GRID'`], default `'JIT'`

drag_factor
    

Amount of air drag

Type:
    

float in [0, 1], default 0.0

effect_hair
    

Hair stiffness for effectors

Type:
    

float in [0, 1], default 0.0

effector_amount
    

How many particles are effectors (0 is all particles)

Type:
    

int in [0, 10000], default 0

effector_weights
    

Type:
    

[`EffectorWeights`](../E/bpy.types.EffectorWeights.md#bpy.types.EffectorWeights "bpy.types.EffectorWeights"), (readonly)

emit_from
    

Where to emit particles from

Type:
    

enum in [`'VERT'`, `'FACE'`, `'VOLUME'`], default `'FACE'`

factor_random
    

Give the starting velocity a random variation

Type:
    

float in [0, 200], default 0.0

fluid
    

Type:
    

[`SPHFluidSettings`](../S/bpy.types.SPHFluidSettings.md#bpy.types.SPHFluidSettings "bpy.types.SPHFluidSettings"), (readonly)

force_field_1
    

Type:
    

[`FieldSettings`](../F/bpy.types.FieldSettings.md#bpy.types.FieldSettings "bpy.types.FieldSettings"), (readonly)

force_field_2
    

Type:
    

[`FieldSettings`](../F/bpy.types.FieldSettings.md#bpy.types.FieldSettings "bpy.types.FieldSettings"), (readonly)

frame_end
    

Frame number to stop emitting particles

Type:
    

float in [-1.04857e+06, 1.04857e+06], default 200.0

frame_start
    

Frame number to start emitting particles

Type:
    

float in [-1.04857e+06, 1.04857e+06], default 1.0

grid_random
    

Add random offset to the grid locations

Type:
    

float in [0, 1], default 0.0

grid_resolution
    

The resolution of the particle grid

Type:
    

int in [1, 250], default 10

hair_length
    

Length of the hair

Type:
    

float in [0, 1000], default 0.0

hair_step
    

Number of hair segments

Type:
    

int in [2, 32767], default 5

hexagonal_grid
    

Create the grid in a hexagonal pattern

Type:
    

boolean, default False

instance_collection
    

Show objects in this collection in place of particles

Type:
    

[`Collection`](../C/bpy.types.Collection.md#bpy.types.Collection "bpy.types.Collection")

instance_object
    

Show this object in place of particles

Type:
    

[`Object`](../O/bpy.types.Object.md#bpy.types.Object "bpy.types.Object")

instance_weights
    

Weights for all of the objects in the instance collection

Type:
    

[`bpy_prop_collection`](../_other/bpy.types.bpy_prop_collection.md#bpy.types.bpy_prop_collection "bpy.types.bpy_prop_collection") of [`ParticleDupliWeight`](bpy.types.ParticleDupliWeight.md#bpy.types.ParticleDupliWeight "bpy.types.ParticleDupliWeight"), (readonly)

integrator
    

Algorithm used to calculate physics, from the fastest to the most stable and accurate: Midpoint, Euler, Verlet, RK4

Type:
    

enum in [`'EULER'`, `'VERLET'`, `'MIDPOINT'`, `'RK4'`], default `'MIDPOINT'`

invert_grid
    

Invert what is considered object and what is not

Type:
    

boolean, default False

is_fluid
    

Particles were created by a fluid simulation

Type:
    

boolean, default False, (readonly)

jitter_factor
    

Amount of jitter applied to the sampling

Type:
    

float in [0, 2], default 1.0

keyed_loops
    

Number of times the keys are looped

Type:
    

int in [1, 10000], default 1

keys_step
    

Type:
    

int in [0, 32767], default 5

kink
    

Type of periodic offset on the path

Type:
    

enum in [`'NO'`, `'CURL'`, `'RADIAL'`, `'WAVE'`, `'BRAID'`, `'SPIRAL'`], default `'NO'`

kink_amplitude
    

The amplitude of the offset

Type:
    

float in [-100000, 100000], default 0.2

kink_amplitude_clump
    

How much clump affects kink amplitude

Type:
    

float in [0, 1], default 1.0

kink_amplitude_random
    

Random variation of the amplitude

Type:
    

float in [0, 1], default 0.0

kink_axis
    

Which axis to use for offset

Type:
    

enum in [Axis Xyz Items](../../bpy_types_enum_items/axis_xyz_items.md#rna-enum-axis-xyz-items), default `'Z'`

kink_axis_random
    

Random variation of the orientation

Type:
    

float in [0, 1], default 0.0

kink_extra_steps
    

Extra steps for resolution of special kink features

Type:
    

int in [1, inf], default 4

kink_flat
    

How flat the hairs are

Type:
    

float in [0, 1], default 0.0

kink_frequency
    

The frequency of the offset (1/total length)

Type:
    

float in [-100000, 100000], default 2.0

kink_shape
    

Adjust the offset to the beginning/end

Type:
    

float in [-0.999, 0.999], default 0.0

length_random
    

Give path length a random variation

Type:
    

float in [0, 1], default 0.0

lifetime
    

Life span of the particles

Type:
    

float in [1, 1.04857e+06], default 50.0

lifetime_random
    

Give the particle life a random variation

Type:
    

float in [0, 1], default 0.0

line_length_head
    

Length of the line’s head

Type:
    

float in [0, 100000], default 0.0

line_length_tail
    

Length of the line’s tail

Type:
    

float in [0, 100000], default 0.0

lock_boids_to_surface
    

Constrain boids to a surface

Type:
    

boolean, default False

mass
    

Mass of the particles

Type:
    

float in [1e-08, 100000], default 1.0

material
    

Index of material slot used for rendering particles

Type:
    

int in [1, 32767], default 1

material_slot
    

Material slot used for rendering particles

Type:
    

enum in [`'DEFAULT'`], default `'DEFAULT'`

normal_factor
    

Let the surface normal give the particle a starting velocity

Type:
    

float in [-1000, 1000], default 1.0

object_align_factor
    

Let the emitter object orientation give the particle a starting velocity

Type:
    

[`mathutils.Vector`](mathutils.md#mathutils.Vector "mathutils.Vector") of 3 items in [-200, 200], default (0.0, 0.0, 0.0)

object_factor
    

Let the object give the particle a starting velocity

Type:
    

float in [-200, 200], default 0.0

particle_factor
    

Let the target particle give the particle a starting velocity

Type:
    

float in [-200, 200], default 0.0

particle_size
    

The size of the particles

Type:
    

float in [0.001, 100000], default 0.05

path_end
    

End time of path

Type:
    

float in [-inf, inf], default 1.0

path_start
    

Starting time of path

Type:
    

float in [-inf, inf], default 0.0

phase_factor
    

Rotation around the chosen orientation axis

Type:
    

float in [-1, 1], default 0.0

phase_factor_random
    

Randomize rotation around the chosen orientation axis

Type:
    

float in [0, 2], default 0.0

physics_type
    

Particle physics type

Type:
    

enum in [`'NO'`, `'NEWTON'`, `'KEYED'`, `'BOIDS'`, `'FLUID'`], default `'NEWTON'`

radius_scale
    

Multiplier of diameter properties

Type:
    

float in [0, inf], default 0.01

react_event
    

The event of target particles to react on

Type:
    

enum in [`'DEATH'`, `'COLLIDE'`, `'NEAR'`], default `'DEATH'`

reactor_factor
    

Let the vector away from the target particle’s location give the particle a starting velocity

Type:
    

float in [-10, 10], default 0.0

render_step
    

How many steps paths are rendered with (power of 2)

Type:
    

int in [0, 20], default 3

render_type
    

How particles are rendered

Type:
    

enum in [`'NONE'`, `'HALO'`, `'LINE'`, `'PATH'`, `'OBJECT'`, `'COLLECTION'`], default `'HALO'`

rendered_child_count
    

Number of children per parent for rendering

Type:
    

int in [0, 100000], default 100

root_radius
    

Strand diameter width at the root

Type:
    

float in [0, inf], default 1.0

rotation_factor_random
    

Randomize particle orientation

Type:
    

float in [0, 1], default 0.0

rotation_mode
    

Particle orientation axis (does not affect Explode modifier’s results)

Type:
    

enum in [`'NONE'`, `'NOR'`, `'NOR_TAN'`, `'VEL'`, `'GLOB_X'`, `'GLOB_Y'`, `'GLOB_Z'`, `'OB_X'`, `'OB_Y'`, `'OB_Z'`], default `'VEL'`

roughness_1
    

Amount of location dependent roughness

Type:
    

float in [0, 100000], default 0.0

roughness_1_size
    

Size of location dependent roughness

Type:
    

float in [0.01, 100000], default 1.0

roughness_2
    

Amount of random roughness

Type:
    

float in [0, 100000], default 0.0

roughness_2_size
    

Size of random roughness

Type:
    

float in [0.01, 100000], default 1.0

roughness_2_threshold
    

Amount of particles left untouched by random roughness

Type:
    

float in [0, 1], default 0.0

roughness_curve
    

Curve defining roughness

Type:
    

[`CurveMapping`](../C/bpy.types.CurveMapping.md#bpy.types.CurveMapping "bpy.types.CurveMapping"), (readonly)

roughness_end_shape
    

Shape of endpoint roughness

Type:
    

float in [0, 10], default 1.0

roughness_endpoint
    

Amount of endpoint roughness

Type:
    

float in [0, 100000], default 0.0

shape
    

Strand shape parameter

Type:
    

float in [-1, 1], default 0.0

show_guide_hairs
    

Show guide hairs

Type:
    

boolean, default False

show_hair_grid
    

Show hair simulation grid

Type:
    

boolean, default False

show_health
    

Display boid health

Type:
    

boolean, default False

show_number
    

Show particle number

Type:
    

boolean, default False

show_size
    

Show particle size

Type:
    

boolean, default False

show_unborn
    

Show particles before they are emitted

Type:
    

boolean, default False

show_velocity
    

Show particle velocity

Type:
    

boolean, default False

size_random
    

Give the particle size a random variation

Type:
    

float in [0, 1], default 0.0

subframes
    

Subframes to simulate for improved stability and finer granularity simulations (dt = timestep / (subframes + 1))

Type:
    

int in [0, 1000], default 0

tangent_factor
    

Let the surface tangent give the particle a starting velocity

Type:
    

float in [-1000, 1000], default 0.0

tangent_phase
    

Rotate the surface tangent

Type:
    

float in [-1, 1], default 0.0

texture_slots
    

Texture slots defining the mapping and influence of textures

Type:
    

[`ParticleSettingsTextureSlots`](bpy.types.ParticleSettingsTextureSlots.md#bpy.types.ParticleSettingsTextureSlots "bpy.types.ParticleSettingsTextureSlots") [`bpy_prop_collection`](../_other/bpy.types.bpy_prop_collection.md#bpy.types.bpy_prop_collection "bpy.types.bpy_prop_collection") of [`ParticleSettingsTextureSlot`](bpy.types.ParticleSettingsTextureSlot.md#bpy.types.ParticleSettingsTextureSlot "bpy.types.ParticleSettingsTextureSlot"), (readonly)

time_tweak
    

A multiplier for physics timestep (1.0 means one frame = 1/25 seconds)

Type:
    

float in [0, 100], default 1.0

timestep
    

The simulation timestep per frame (seconds per frame)

Type:
    

float in [0.0001, 100], default 0.0

tip_radius
    

Strand diameter width at the tip

Type:
    

float in [0, inf], default 0.0

trail_count
    

Number of trail particles

Type:
    

int in [1, 100000], default 0

twist
    

Number of turns around parent along the strand

Type:
    

float in [-100000, 100000], default 0.0

twist_curve
    

Curve defining twist

Type:
    

[`CurveMapping`](../C/bpy.types.CurveMapping.md#bpy.types.CurveMapping "bpy.types.CurveMapping"), (readonly)

type
    

Particle type

Type:
    

enum in [`'EMITTER'`, `'HAIR'`], default `'EMITTER'`

use_absolute_path_time
    

Path timing is in absolute frames

Type:
    

boolean, default False

use_adaptive_subframes
    

Automatically set the number of subframes

Type:
    

boolean, default False

use_advanced_hair
    

Use full physics calculations for growing hair

Type:
    

boolean, default False

use_close_tip
    

Set tip radius to zero

Type:
    

boolean, default True

use_clump_curve
    

Use a curve to define clump tapering

Type:
    

boolean, default False

use_clump_noise
    

Create random clumps around the parent

Type:
    

boolean, default False

use_collection_count
    

Use object multiple times in the same collection

Type:
    

boolean, default False

use_collection_pick_random
    

Pick objects from collection randomly

Type:
    

boolean, default False

use_dead
    

Show particles after they have died

Type:
    

boolean, default False

use_die_on_collision
    

Particles die when they collide with a deflector object

Type:
    

boolean, default False

use_dynamic_rotation
    

Particle rotations are affected by collisions and effectors

Type:
    

boolean, default False

use_emit_random
    

Emit in random order of elements

Type:
    

boolean, default True

use_even_distribution
    

Use even distribution from faces based on face areas or edge lengths

Type:
    

boolean, default True

use_global_instance
    

Use object’s global coordinates for duplication

Type:
    

boolean, default False

use_hair_bspline
    

Interpolate hair using B-Splines

Type:
    

boolean, default False

use_modifier_stack
    

Emit particles from mesh with modifiers applied (must use same subdivision surface level for viewport and render for correct results)

Type:
    

boolean, default False

use_multiply_size_mass
    

Multiply mass by particle size

Type:
    

boolean, default False

use_parent_particles
    

Render parent particles

Type:
    

boolean, default False

use_react_multiple
    

React multiple times

Type:
    

boolean, default False

use_react_start_end
    

Give birth to unreacted particles eventually

Type:
    

boolean, default False

use_regrow_hair
    

Regrow hair for each frame

Type:
    

boolean, default False

use_render_adaptive
    

Display steps of the particle path

Type:
    

boolean, default False

use_rotation_instance
    

Use object’s rotation for duplication (global x-axis is aligned particle rotation axis)

Type:
    

boolean, default False

use_rotations
    

Calculate particle rotations

Type:
    

boolean, default False

use_roughness_curve
    

Use a curve to define roughness

Type:
    

boolean, default False

use_scale_instance
    

Use object’s scale for duplication

Type:
    

boolean, default True

use_self_effect
    

Particle effectors affect themselves

Type:
    

boolean, default False

use_size_deflect
    

Use particle’s size in deflection

Type:
    

boolean, default False

use_strand_primitive
    

Use the strand primitive for rendering

Type:
    

boolean, default False

use_twist_curve
    

Use a curve to define twist

Type:
    

boolean, default False

use_velocity_length
    

Multiply line length by particle speed

Type:
    

boolean, default False

use_whole_collection
    

Use whole collection at once

Type:
    

boolean, default False

userjit
    

Emission locations per face (0 = automatic)

Type:
    

int in [0, 1000], default 0

virtual_parents
    

Relative amount of virtual parents

Type:
    

float in [0, 1], default 0.0

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
  * [`ID.name`](../I/bpy.types.ID.md#bpy.types.ID.name "bpy.types.ID.name")
  * [`ID.name_full`](../I/bpy.types.ID.md#bpy.types.ID.name_full "bpy.types.ID.name_full")
  * [`ID.id_type`](../I/bpy.types.ID.md#bpy.types.ID.id_type "bpy.types.ID.id_type")
  * [`ID.session_uid`](../I/bpy.types.ID.md#bpy.types.ID.session_uid "bpy.types.ID.session_uid")
  * [`ID.is_evaluated`](../I/bpy.types.ID.md#bpy.types.ID.is_evaluated "bpy.types.ID.is_evaluated")
  * [`ID.original`](../I/bpy.types.ID.md#bpy.types.ID.original "bpy.types.ID.original")
  * [`ID.users`](../I/bpy.types.ID.md#bpy.types.ID.users "bpy.types.ID.users")
  * [`ID.use_fake_user`](../I/bpy.types.ID.md#bpy.types.ID.use_fake_user "bpy.types.ID.use_fake_user")
  * [`ID.use_extra_user`](../I/bpy.types.ID.md#bpy.types.ID.use_extra_user "bpy.types.ID.use_extra_user")
  * [`ID.is_embedded_data`](../I/bpy.types.ID.md#bpy.types.ID.is_embedded_data "bpy.types.ID.is_embedded_data")

| 

  * [`ID.is_linked_packed`](../I/bpy.types.ID.md#bpy.types.ID.is_linked_packed "bpy.types.ID.is_linked_packed")
  * [`ID.is_missing`](../I/bpy.types.ID.md#bpy.types.ID.is_missing "bpy.types.ID.is_missing")
  * [`ID.is_runtime_data`](../I/bpy.types.ID.md#bpy.types.ID.is_runtime_data "bpy.types.ID.is_runtime_data")
  * [`ID.is_editable`](../I/bpy.types.ID.md#bpy.types.ID.is_editable "bpy.types.ID.is_editable")
  * [`ID.tag`](../I/bpy.types.ID.md#bpy.types.ID.tag "bpy.types.ID.tag")
  * [`ID.is_library_indirect`](../I/bpy.types.ID.md#bpy.types.ID.is_library_indirect "bpy.types.ID.is_library_indirect")
  * [`ID.library`](../I/bpy.types.ID.md#bpy.types.ID.library "bpy.types.ID.library")
  * [`ID.library_weak_reference`](../I/bpy.types.ID.md#bpy.types.ID.library_weak_reference "bpy.types.ID.library_weak_reference")
  * [`ID.asset_data`](../I/bpy.types.ID.md#bpy.types.ID.asset_data "bpy.types.ID.asset_data")
  * [`ID.override_library`](../I/bpy.types.ID.md#bpy.types.ID.override_library "bpy.types.ID.override_library")
  * [`ID.preview`](../I/bpy.types.ID.md#bpy.types.ID.preview "bpy.types.ID.preview")

  
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
  * [`bpy_struct.keyframe_insert`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.keyframe_insert "bpy.types.bpy_struct.keyframe_insert")
  * [`bpy_struct.keys`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.keys "bpy.types.bpy_struct.keys")
  * [`bpy_struct.path_from_id`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.path_from_id "bpy.types.bpy_struct.path_from_id")
  * [`bpy_struct.path_from_module`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.path_from_module "bpy.types.bpy_struct.path_from_module")
  * [`bpy_struct.path_resolve`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.path_resolve "bpy.types.bpy_struct.path_resolve")
  * [`bpy_struct.pop`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.pop "bpy.types.bpy_struct.pop")
  * [`bpy_struct.property_overridable_library_set`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.property_overridable_library_set "bpy.types.bpy_struct.property_overridable_library_set")
  * [`bpy_struct.property_unset`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.property_unset "bpy.types.bpy_struct.property_unset")
  * [`bpy_struct.rna_ancestors`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.rna_ancestors "bpy.types.bpy_struct.rna_ancestors")

| 

  * [`bpy_struct.type_recast`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.type_recast "bpy.types.bpy_struct.type_recast")
  * [`bpy_struct.values`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.values "bpy.types.bpy_struct.values")
  * [`ID.bl_system_properties_get`](../I/bpy.types.ID.md#bpy.types.ID.bl_system_properties_get "bpy.types.ID.bl_system_properties_get")
  * [`ID.rename`](../I/bpy.types.ID.md#bpy.types.ID.rename "bpy.types.ID.rename")
  * [`ID.evaluated_get`](../I/bpy.types.ID.md#bpy.types.ID.evaluated_get "bpy.types.ID.evaluated_get")
  * [`ID.copy`](../I/bpy.types.ID.md#bpy.types.ID.copy "bpy.types.ID.copy")
  * [`ID.asset_mark`](../I/bpy.types.ID.md#bpy.types.ID.asset_mark "bpy.types.ID.asset_mark")
  * [`ID.asset_clear`](../I/bpy.types.ID.md#bpy.types.ID.asset_clear "bpy.types.ID.asset_clear")
  * [`ID.asset_generate_preview`](../I/bpy.types.ID.md#bpy.types.ID.asset_generate_preview "bpy.types.ID.asset_generate_preview")
  * [`ID.override_create`](../I/bpy.types.ID.md#bpy.types.ID.override_create "bpy.types.ID.override_create")
  * [`ID.override_hierarchy_create`](../I/bpy.types.ID.md#bpy.types.ID.override_hierarchy_create "bpy.types.ID.override_hierarchy_create")
  * [`ID.user_clear`](../I/bpy.types.ID.md#bpy.types.ID.user_clear "bpy.types.ID.user_clear")
  * [`ID.user_remap`](../I/bpy.types.ID.md#bpy.types.ID.user_remap "bpy.types.ID.user_remap")
  * [`ID.make_local`](../I/bpy.types.ID.md#bpy.types.ID.make_local "bpy.types.ID.make_local")
  * [`ID.user_of_id`](../I/bpy.types.ID.md#bpy.types.ID.user_of_id "bpy.types.ID.user_of_id")
  * [`ID.animation_data_create`](../I/bpy.types.ID.md#bpy.types.ID.animation_data_create "bpy.types.ID.animation_data_create")
  * [`ID.animation_data_clear`](../I/bpy.types.ID.md#bpy.types.ID.animation_data_clear "bpy.types.ID.animation_data_clear")
  * [`ID.update_tag`](../I/bpy.types.ID.md#bpy.types.ID.update_tag "bpy.types.ID.update_tag")
  * [`ID.preview_ensure`](../I/bpy.types.ID.md#bpy.types.ID.preview_ensure "bpy.types.ID.preview_ensure")
  * [`ID.bl_rna_get_subclass`](../I/bpy.types.ID.md#bpy.types.ID.bl_rna_get_subclass "bpy.types.ID.bl_rna_get_subclass")
  * [`ID.bl_rna_get_subclass_py`](../I/bpy.types.ID.md#bpy.types.ID.bl_rna_get_subclass_py "bpy.types.ID.bl_rna_get_subclass_py")

  
---|---  
  
## References

  * [`bpy.context.particle_settings`](../../bpy.context.md#bpy.context.particle_settings "bpy.context.particle_settings")
  * [`BlendData.particles`](../B/bpy.types.BlendData.md#bpy.types.BlendData.particles "bpy.types.BlendData.particles")
  * [`BlendDataParticles.new`](../B/bpy.types.BlendDataParticles.md#bpy.types.BlendDataParticles.new "bpy.types.BlendDataParticles.new")

| 

  * [`BlendDataParticles.remove`](../B/bpy.types.BlendDataParticles.md#bpy.types.BlendDataParticles.remove "bpy.types.BlendDataParticles.remove")
  * [`ParticleSystem.settings`](bpy.types.ParticleSystem.md#bpy.types.ParticleSystem.settings "bpy.types.ParticleSystem.settings")

  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
