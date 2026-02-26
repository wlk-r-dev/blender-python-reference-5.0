# HookModifier(Modifier)

base classes — [`bpy_struct`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct "bpy.types.bpy_struct"), [`Modifier`](../M/bpy.types.Modifier.md#bpy.types.Modifier "bpy.types.Modifier")

_class _bpy.types.HookModifier(_Modifier_)
    

Hook modifier to modify the location of vertices

center
    

Center of the hook, used for falloff and display

Type:
    

[`mathutils.Vector`](mathutils.md#mathutils.Vector "mathutils.Vector") of 3 items in [-inf, inf], default (0.0, 0.0, 0.0)

falloff_curve
    

Custom falloff curve

Type:
    

[`CurveMapping`](../C/bpy.types.CurveMapping.md#bpy.types.CurveMapping "bpy.types.CurveMapping"), (readonly)

falloff_radius
    

If not zero, the distance from the hook where influence ends

Type:
    

float in [0, inf], default 0.0

falloff_type
    

Type:
    

enum in [`'NONE'`, `'CURVE'`, `'SMOOTH'`, `'SPHERE'`, `'ROOT'`, `'INVERSE_SQUARE'`, `'SHARP'`, `'LINEAR'`, `'CONSTANT'`], default `'SMOOTH'`

invert_vertex_group
    

Invert vertex group influence

Type:
    

boolean, default False

matrix_inverse
    

Reverse the transformation between this object and its target

Type:
    

[`mathutils.Matrix`](mathutils.md#mathutils.Matrix "mathutils.Matrix") of 4 * 4 items in [-inf, inf], default ((1.0, 0.0, 0.0, 0.0), (0.0, 1.0, 0.0, 0.0), (0.0, 0.0, 1.0, 0.0), (0.0, 0.0, 0.0, 1.0))

object
    

Parent Object for hook, also recalculates and clears offset

Type:
    

[`Object`](../O/bpy.types.Object.md#bpy.types.Object "bpy.types.Object")

strength
    

Relative force of the hook

Type:
    

float in [0, 1], default 1.0

subtarget
    

Name of Parent Bone for hook (if applicable), also recalculates and clears offset

Type:
    

string, default “”, (never None)

use_falloff_uniform
    

Compensate for non-uniform object scale

Type:
    

boolean, default False

vertex_group
    

Name of Vertex Group which determines influence of modifier per point

Type:
    

string, default “”, (never None)

vertex_indices
    

Indices of vertices bound to the modifier. For Bézier curves, handles count as additional vertices.

Type:
    

int array of 64 items in [0, inf], default (0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0), (readonly)

vertex_indices_set(_indices_)
    

Validates and assigns the array of vertex indices bound to the modifier

Parameters:
    

**indices** (_int array_ _of_ _64 items in_ _[__-inf_ _,__inf_ _]_) – Vertex Indices

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
  * [`Modifier.name`](../M/bpy.types.Modifier.md#bpy.types.Modifier.name "bpy.types.Modifier.name")
  * [`Modifier.type`](../M/bpy.types.Modifier.md#bpy.types.Modifier.type "bpy.types.Modifier.type")
  * [`Modifier.show_viewport`](../M/bpy.types.Modifier.md#bpy.types.Modifier.show_viewport "bpy.types.Modifier.show_viewport")
  * [`Modifier.show_render`](../M/bpy.types.Modifier.md#bpy.types.Modifier.show_render "bpy.types.Modifier.show_render")
  * [`Modifier.show_in_editmode`](../M/bpy.types.Modifier.md#bpy.types.Modifier.show_in_editmode "bpy.types.Modifier.show_in_editmode")
  * [`Modifier.show_on_cage`](../M/bpy.types.Modifier.md#bpy.types.Modifier.show_on_cage "bpy.types.Modifier.show_on_cage")

| 

  * [`Modifier.show_expanded`](../M/bpy.types.Modifier.md#bpy.types.Modifier.show_expanded "bpy.types.Modifier.show_expanded")
  * [`Modifier.is_active`](../M/bpy.types.Modifier.md#bpy.types.Modifier.is_active "bpy.types.Modifier.is_active")
  * [`Modifier.use_pin_to_last`](../M/bpy.types.Modifier.md#bpy.types.Modifier.use_pin_to_last "bpy.types.Modifier.use_pin_to_last")
  * [`Modifier.is_override_data`](../M/bpy.types.Modifier.md#bpy.types.Modifier.is_override_data "bpy.types.Modifier.is_override_data")
  * [`Modifier.use_apply_on_spline`](../M/bpy.types.Modifier.md#bpy.types.Modifier.use_apply_on_spline "bpy.types.Modifier.use_apply_on_spline")
  * [`Modifier.execution_time`](../M/bpy.types.Modifier.md#bpy.types.Modifier.execution_time "bpy.types.Modifier.execution_time")
  * [`Modifier.persistent_uid`](../M/bpy.types.Modifier.md#bpy.types.Modifier.persistent_uid "bpy.types.Modifier.persistent_uid")

  
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
  * [`Modifier.bl_rna_get_subclass`](../M/bpy.types.Modifier.md#bpy.types.Modifier.bl_rna_get_subclass "bpy.types.Modifier.bl_rna_get_subclass")
  * [`Modifier.bl_rna_get_subclass_py`](../M/bpy.types.Modifier.md#bpy.types.Modifier.bl_rna_get_subclass_py "bpy.types.Modifier.bl_rna_get_subclass_py")

  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
