# VertexWeightProximityModifier(Modifier)

base classes — [`bpy_struct`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct "bpy.types.bpy_struct"), [`Modifier`](../M/bpy.types.Modifier.md#bpy.types.Modifier "bpy.types.Modifier")

_class _bpy.types.VertexWeightProximityModifier(_Modifier_)
    

Set the weights of vertices in a group from a target object’s distance

falloff_type
    

How weights are mapped to their new values

  * `LINEAR` Linear – Null action.

  * `CURVE` Custom Curve.

  * `SHARP` Sharp.

  * `SMOOTH` Smooth.

  * `ROOT` Root.

  * `ICON_SPHERECURVE` Sphere.

  * `RANDOM` Random.

  * `STEP` Median Step – Map all values below 0.5 to 0.0, and all others to 1.0.


Type:
    

enum in [`'LINEAR'`, `'CURVE'`, `'SHARP'`, `'SMOOTH'`, `'ROOT'`, `'ICON_SPHERECURVE'`, `'RANDOM'`, `'STEP'`], default `'LINEAR'`

invert_falloff
    

Invert the resulting falloff weight

Type:
    

boolean, default False

invert_mask_vertex_group
    

Invert vertex group mask influence

Type:
    

boolean, default False

map_curve
    

Custom mapping curve

Type:
    

[`CurveMapping`](../C/bpy.types.CurveMapping.md#bpy.types.CurveMapping "bpy.types.CurveMapping"), (readonly)

mask_constant
    

Global influence of current modifications on vgroup

Type:
    

float in [-inf, inf], default 1.0

mask_tex_map_bone
    

Which bone to take texture coordinates from

Type:
    

string, default “”, (never None)

mask_tex_map_object
    

Which object to take texture coordinates from

Type:
    

[`Object`](../O/bpy.types.Object.md#bpy.types.Object "bpy.types.Object")

mask_tex_mapping
    

Which texture coordinates to use for mapping

  * `LOCAL` Local – Use local generated coordinates.

  * `GLOBAL` Global – Use global coordinates.

  * `OBJECT` Object – Use local generated coordinates of another object.

  * `UV` UV – Use coordinates from a UV layer.


Type:
    

enum in [`'LOCAL'`, `'GLOBAL'`, `'OBJECT'`, `'UV'`], default `'LOCAL'`

mask_tex_use_channel
    

Which texture channel to use for masking

Type:
    

enum in [`'INT'`, `'RED'`, `'GREEN'`, `'BLUE'`, `'HUE'`, `'SAT'`, `'VAL'`, `'ALPHA'`], default `'INT'`

mask_tex_uv_layer
    

UV map name

Type:
    

string, default “”, (never None)

mask_texture
    

Masking texture

Type:
    

[`Texture`](../T/bpy.types.Texture.md#bpy.types.Texture "bpy.types.Texture")

mask_vertex_group
    

Masking vertex group name

Type:
    

string, default “”, (never None)

max_dist
    

Distance mapping to weight 1.0

Type:
    

float in [0, inf], default 1.0

min_dist
    

Distance mapping to weight 0.0

Type:
    

float in [0, inf], default 0.0

normalize
    

Normalize the resulting weights (otherwise they are only clamped within 0.0 to 1.0 range)

Type:
    

boolean, default False

proximity_geometry
    

Use the shortest computed distance to target object’s geometry as weight

  * `VERTEX` Vertex – Compute distance to nearest vertex.

  * `EDGE` Edge – Compute distance to nearest edge.

  * `FACE` Face – Compute distance to nearest face.


Type:
    

enum set in {`'VERTEX'`, `'EDGE'`, `'FACE'`}, default {`'FACE'`}

proximity_mode
    

Which distances to target object to use

  * `OBJECT` Object – Use distance between affected and target objects.

  * `GEOMETRY` Geometry – Use distance between affected object’s vertices and target object, or target object’s geometry.


Type:
    

enum in [`'OBJECT'`, `'GEOMETRY'`], default `'GEOMETRY'`

target
    

Object to calculate vertices distances from

Type:
    

[`Object`](../O/bpy.types.Object.md#bpy.types.Object "bpy.types.Object")

vertex_group
    

Vertex group name

Type:
    

string, default “”, (never None)

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
