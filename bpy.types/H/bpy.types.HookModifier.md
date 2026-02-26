# HookModifier(Modifier)

base classes — [[bpy_struct]], [[Modifier]]

_class _bpy.types.HookModifier(_Modifier_)
    

Hook modifier to modify the location of vertices

center
    

Center of the hook, used for falloff and display

Type:
    

[[mathutils.Vector]] of 3 items in [-inf, inf], default (0.0, 0.0, 0.0)

falloff_curve
    

Custom falloff curve

Type:
    

[[CurveMapping]], (readonly)

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
    

[[mathutils.Matrix]] of 4 * 4 items in [-inf, inf], default ((1.0, 0.0, 0.0, 0.0), (0.0, 1.0, 0.0, 0.0), (0.0, 0.0, 1.0, 0.0), (0.0, 0.0, 0.0, 1.0))

object
    

Parent Object for hook, also recalculates and clears offset

Type:
    

[[Object]]

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
