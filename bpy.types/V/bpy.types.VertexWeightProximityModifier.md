# VertexWeightProximityModifier(Modifier)

base classes — [[bpy_struct]], [[Modifier]]

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
    

[[CurveMapping]], (readonly)

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
    

[[Object]]

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
    

[[Texture]]

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
    

[[Object]]

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
