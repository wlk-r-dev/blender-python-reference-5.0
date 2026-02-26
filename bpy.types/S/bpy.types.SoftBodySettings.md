# SoftBodySettings(bpy_struct)

base class — [`bpy_struct`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct "bpy.types.bpy_struct")

_class _bpy.types.SoftBodySettings(_bpy_struct_)
    

Soft body simulation settings for an object

aero
    

Make edges ‘sail’

Type:
    

int in [0, 30000], default 0

aerodynamics_type
    

Method of calculating aerodynamic interaction

  * `SIMPLE` Simple – Edges receive a drag force from surrounding media.

  * `LIFT_FORCE` Lift Force – Edges receive a lift force when passing through surrounding media.


Type:
    

enum in [`'SIMPLE'`, `'LIFT_FORCE'`], default `'SIMPLE'`

ball_damp
    

Blending to inelastic collision

Type:
    

float in [0.001, 1], default 0.0

ball_size
    

Absolute ball size or factor if not manually adjusted

Type:
    

float in [-10, 10], default 0.0

ball_stiff
    

Ball inflating pressure

Type:
    

float in [0.001, 100], default 0.0

bend
    

Bending Stiffness

Type:
    

float in [0, 10], default 0.0

choke
    

‘Viscosity’ inside collision target

Type:
    

int in [0, 100], default 0

collision_collection
    

Limit colliders to this collection

Type:
    

[`Collection`](../C/bpy.types.Collection.md#bpy.types.Collection "bpy.types.Collection")

collision_type
    

Choose Collision Type

  * `MANUAL` Manual – Manual adjust.

  * `AVERAGE` Average – Average Spring length * Ball Size.

  * `MINIMAL` Minimal – Minimal Spring length * Ball Size.

  * `MAXIMAL` Maximal – Maximal Spring length * Ball Size.

  * `MINMAX` AvMinMax – (Min+Max)/2 * Ball Size.


Type:
    

enum in [`'MANUAL'`, `'AVERAGE'`, `'MINIMAL'`, `'MAXIMAL'`, `'MINMAX'`], default `'MANUAL'`

damping
    

Edge spring friction

Type:
    

float in [0, 50], default 0.0

effector_weights
    

Type:
    

[`EffectorWeights`](../E/bpy.types.EffectorWeights.md#bpy.types.EffectorWeights "bpy.types.EffectorWeights"), (readonly)

error_threshold
    

The Runge-Kutta ODE solver error limit, low value gives more precision, high values speed

Type:
    

float in [0.001, 10], default 0.0

friction
    

General media friction for point movements

Type:
    

float in [0, 50], default 0.0

fuzzy
    

Fuzziness while on collision, high values make collision handling faster but less stable

Type:
    

int in [1, 100], default 0

goal_default
    

Default Goal (vertex target position) value

Type:
    

float in [0, 1], default 0.0

goal_friction
    

Goal (vertex target position) friction

Type:
    

float in [0, 50], default 0.0

goal_max
    

Goal maximum, vertex weights are scaled to match this range

Type:
    

float in [0, 1], default 0.0

goal_min
    

Goal minimum, vertex weights are scaled to match this range

Type:
    

float in [0, 1], default 0.0

goal_spring
    

Goal (vertex target position) spring stiffness

Type:
    

float in [0, 0.999], default 0.0

gravity
    

Apply gravitation to point movement

Type:
    

float in [-10, 10], default 0.0

location_mass_center
    

Location of center of mass

Type:
    

[`mathutils.Vector`](mathutils.md#mathutils.Vector "mathutils.Vector") of 3 items in [-inf, inf], default (0.0, 0.0, 0.0)

mass
    

General Mass value

Type:
    

float in [0, 50000], default 0.0

plastic
    

Permanent deform

Type:
    

int in [0, 100], default 0

pull
    

Edge spring stiffness when longer than rest length

Type:
    

float in [0, 0.999], default 0.0

push
    

Edge spring stiffness when shorter than rest length

Type:
    

float in [0, 0.999], default 0.0

rotation_estimate
    

Estimated rotation matrix

Type:
    

[`mathutils.Matrix`](mathutils.md#mathutils.Matrix "mathutils.Matrix") of 3 * 3 items in [-inf, inf], default ((0.0, 0.0, 0.0), (0.0, 0.0, 0.0), (0.0, 0.0, 0.0))

scale_estimate
    

Estimated scale matrix

Type:
    

[`mathutils.Matrix`](mathutils.md#mathutils.Matrix "mathutils.Matrix") of 3 * 3 items in [-inf, inf], default ((0.0, 0.0, 0.0), (0.0, 0.0, 0.0), (0.0, 0.0, 0.0))

shear
    

Shear Stiffness

Type:
    

float in [0, 1], default 0.0

speed
    

Tweak timing for physics to control frequency and speed

Type:
    

float in [0.01, 100], default 0.0

spring_length
    

Alter spring length to shrink/blow up (unit %) 0 to disable

Type:
    

int in [0, 200], default 0

step_max
    

Maximal # solver steps/frame

Type:
    

int in [0, 30000], default 0

step_min
    

Minimal # solver steps/frame

Type:
    

int in [0, 30000], default 0

use_auto_step
    

Use velocities for automagic step sizes

Type:
    

boolean, default False

use_diagnose
    

Turn on SB diagnose console prints

Type:
    

boolean, default False

use_edge_collision
    

Edges collide too

Type:
    

boolean, default False

use_edges
    

Use Edges as springs

Type:
    

boolean, default False

use_estimate_matrix
    

Store the estimated transforms in the soft body settings

Type:
    

boolean, default False

use_face_collision
    

Faces collide too, can be very slow

Type:
    

boolean, default False

use_goal
    

Define forces for vertices to stick to animated position

Type:
    

boolean, default False

use_self_collision
    

Enable naive vertex ball self collision

Type:
    

boolean, default False

use_stiff_quads
    

Add diagonal springs on 4-gons

Type:
    

boolean, default False

vertex_group_goal
    

Control point weight values

Type:
    

string, default “”, (never None)

vertex_group_mass
    

Control point mass values

Type:
    

string, default “”, (never None)

vertex_group_spring
    

Control point spring strength values

Type:
    

string, default “”, (never None)

_classmethod _bl_rna_get_subclass(_id_ , _default =None_, _/_)
    

Parameters:
    

**id** (_str_) – The RNA type identifier.

Returns:
    

The RNA type or default when not found.

Return type:
    

[`bpy.types.Struct`](bpy.types.Struct.md#bpy.types.Struct "bpy.types.Struct") subclass

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

  * [`Object.soft_body`](../O/bpy.types.Object.md#bpy.types.Object.soft_body "bpy.types.Object.soft_body")

| 

  * [`SoftBodyModifier.settings`](bpy.types.SoftBodyModifier.md#bpy.types.SoftBodyModifier.settings "bpy.types.SoftBodyModifier.settings")

  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
