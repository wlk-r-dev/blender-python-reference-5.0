# ParticleSettings(ID)

base classes — [[bpy_struct]], [[ID]]

_class _bpy.types.ParticleSettings(_ID_)
    

Particle settings, reusable by multiple particle systems

active_instanceweight
    

Type:
    

[[ParticleDupliWeight]], (readonly)

active_instanceweight_index
    

Type:
    

int in [0, inf], default 0

active_texture
    

Active texture slot being displayed

Type:
    

[[Texture]]

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
    

[[AnimData]], (readonly)

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
    

[[BoidSettings]], (readonly)

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
    

[[CurveMapping]], (readonly)

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
    

[[Collection]]

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
    

[[EffectorWeights]], (readonly)

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
    

[[SPHFluidSettings]], (readonly)

force_field_1
    

Type:
    

[[FieldSettings]], (readonly)

force_field_2
    

Type:
    

[[FieldSettings]], (readonly)

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
    

[[Collection]]

instance_object
    

Show this object in place of particles

Type:
    

[[Object]]

instance_weights
    

Weights for all of the objects in the instance collection

Type:
    

[[bpy_prop_collection]] of [[ParticleDupliWeight]], (readonly)

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
    

[[mathutils.Vector]] of 3 items in [-200, 200], default (0.0, 0.0, 0.0)

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
    

[[CurveMapping]], (readonly)

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
    

[[ParticleSettingsTextureSlots]] [[bpy_prop_collection]] of [[ParticleSettingsTextureSlot]], (readonly)

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
    

[[CurveMapping]], (readonly)

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
  * [[ID.name]]
  * [[ID.name_full]]
  * [[ID.id_type]]
  * [[ID.session_uid]]
  * [[ID.is_evaluated]]
  * [[ID.original]]
  * [[ID.users]]
  * [[ID.use_fake_user]]
  * [[ID.use_extra_user]]
  * [[ID.is_embedded_data]]

| 

  * [[ID.is_linked_packed]]
  * [[ID.is_missing]]
  * [[ID.is_runtime_data]]
  * [[ID.is_editable]]
  * [[ID.tag]]
  * [[ID.is_library_indirect]]
  * [[ID.library]]
  * [[ID.library_weak_reference]]
  * [[ID.asset_data]]
  * [[ID.override_library]]
  * [[ID.preview]]

  
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
  * [[bpy_struct.keyframe_insert]]
  * [[bpy_struct.keys]]
  * [[bpy_struct.path_from_id]]
  * [[bpy_struct.path_from_module]]
  * [[bpy_struct.path_resolve]]
  * [[bpy_struct.pop]]
  * [[bpy_struct.property_overridable_library_set]]
  * [[bpy_struct.property_unset]]
  * [[bpy_struct.rna_ancestors]]

| 

  * [[bpy_struct.type_recast]]
  * [[bpy_struct.values]]
  * [[ID.bl_system_properties_get]]
  * [[ID.rename]]
  * [[ID.evaluated_get]]
  * [[ID.copy]]
  * [[ID.asset_mark]]
  * [[ID.asset_clear]]
  * [[ID.asset_generate_preview]]
  * [[ID.override_create]]
  * [[ID.override_hierarchy_create]]
  * [[ID.user_clear]]
  * [[ID.user_remap]]
  * [[ID.make_local]]
  * [[ID.user_of_id]]
  * [[ID.animation_data_create]]
  * [[ID.animation_data_clear]]
  * [[ID.update_tag]]
  * [[ID.preview_ensure]]
  * [[ID.bl_rna_get_subclass]]
  * [[ID.bl_rna_get_subclass_py]]

  
---|---  
  
## References

  * [[bpy.context.particle_settings]]
  * [[BlendData.particles]]
  * [[BlendDataParticles.new]]

| 

  * [[BlendDataParticles.remove]]
  * [[ParticleSystem.settings]]

  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
