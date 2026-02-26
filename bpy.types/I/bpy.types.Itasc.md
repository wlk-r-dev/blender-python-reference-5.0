# Itasc(IKParam)

base classes — [`bpy_struct`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct "bpy.types.bpy_struct"), [`IKParam`](bpy.types.IKParam.md#bpy.types.IKParam "bpy.types.IKParam")

_class _bpy.types.Itasc(_IKParam_)
    

Parameters for the iTaSC IK solver

damping_epsilon
    

Singular value under which damping is progressively applied (higher values produce results with more stability, less reactivity)

Type:
    

float in [0, 1], default 0.0

damping_max
    

Maximum damping coefficient when singular value is nearly 0 (higher values produce results with more stability, less reactivity)

Type:
    

float in [0, 1], default 0.0

feedback
    

Feedback coefficient for error correction, average response time is 1/feedback

Type:
    

float in [0, 100], default 0.0

iterations
    

Maximum number of iterations for convergence in case of reiteration

Type:
    

int in [0, 1000], default 0

mode
    

  * `ANIMATION` Animation – Stateless solver computing pose starting from current action and non-IK constraints.

  * `SIMULATION` Simulation – State-full solver running in real-time context and ignoring actions and non-IK constraints.


Type:
    

enum in [`'ANIMATION'`, `'SIMULATION'`], default `'ANIMATION'`

precision
    

Precision of convergence in case of reiteration

Type:
    

float in [0, 0.1], default 0.0

reiteration_method
    

Defines if the solver is allowed to reiterate (converge until precision is met) on none, first or all frames

  * `NEVER` Never – The solver does not reiterate, not even on first frame (starts from rest pose).

  * `INITIAL` Initial – The solver reiterates (converges) on the first frame but not on subsequent frame.

  * `ALWAYS` Always – The solver reiterates (converges) on all frames.


Type:
    

enum in [`'NEVER'`, `'INITIAL'`, `'ALWAYS'`], default `'NEVER'`

solver
    

Solving method selection: automatic damping or manual damping

  * `SDLS` SDLS – Selective Damped Least Square.

  * `DLS` DLS – Damped Least Square with Numerical Filtering.


Type:
    

enum in [`'SDLS'`, `'DLS'`], default `'SDLS'`

step_count
    

Divide the frame interval into this many steps

Type:
    

int in [1, 50], default 0

step_max
    

Higher bound for timestep in second in case of automatic substeps

Type:
    

float in [0, 1], default 0.0

step_min
    

Lower bound for timestep in second in case of automatic substeps

Type:
    

float in [0, 0.1], default 0.0

translate_root_bones
    

Translate root (i.e. parentless) bones to the armature origin

Type:
    

boolean, default False

use_auto_step
    

Automatically determine the optimal number of steps for best performance/accuracy trade off

Type:
    

boolean, default False

velocity_max
    

Maximum joint velocity in radians/second

Type:
    

float in [0, 100], default 0.0

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

  * [`IKParam.ik_solver`](bpy.types.IKParam.md#bpy.types.IKParam.ik_solver "bpy.types.IKParam.ik_solver")

  
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

| 

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
  * [`IKParam.bl_rna_get_subclass`](bpy.types.IKParam.md#bpy.types.IKParam.bl_rna_get_subclass "bpy.types.IKParam.bl_rna_get_subclass")
  * [`IKParam.bl_rna_get_subclass_py`](bpy.types.IKParam.md#bpy.types.IKParam.bl_rna_get_subclass_py "bpy.types.IKParam.bl_rna_get_subclass_py")

  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
