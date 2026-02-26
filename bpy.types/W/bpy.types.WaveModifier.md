# WaveModifier(Modifier)

base classes — [[bpy_struct]], [[Modifier]]

_class _bpy.types.WaveModifier(_Modifier_)
    

Wave effect modifier

damping_time
    

Number of frames in which the wave damps out after it dies

Type:
    

float in [-1.04857e+06, 1.04857e+06], default 10.0

falloff_radius
    

Distance after which it fades out

Type:
    

float in [0, inf], default 0.0

height
    

Height of the wave

Type:
    

float in [-inf, inf], default 0.5

invert_vertex_group
    

Invert vertex group influence

Type:
    

boolean, default False

lifetime
    

Lifetime of the wave in frames, zero means infinite

Type:
    

float in [-1.04857e+06, 1.04857e+06], default 0.0

narrowness
    

Distance between the top and the base of a wave, the higher the value, the more narrow the wave

Type:
    

float in [0, inf], default 1.5

speed
    

Speed of the wave, towards the starting point when negative

Type:
    

float in [-inf, inf], default 0.25

start_position_object
    

Object which defines the wave center

Type:
    

[[Object]]

start_position_x
    

X coordinate of the start position

Type:
    

float in [-inf, inf], default 0.0

start_position_y
    

Y coordinate of the start position

Type:
    

float in [-inf, inf], default 0.0

texture
    

Type:
    

[[Texture]]

texture_coords
    

  * `LOCAL` Local – Use the local coordinate system for the texture coordinates.

  * `GLOBAL` Global – Use the global coordinate system for the texture coordinates.

  * `OBJECT` Object – Use the linked object’s local coordinate system for the texture coordinates.

  * `UV` UV – Use UV coordinates for the texture coordinates.


Type:
    

enum in [`'LOCAL'`, `'GLOBAL'`, `'OBJECT'`, `'UV'`], default `'LOCAL'`

texture_coords_bone
    

Bone to set the texture coordinates

Type:
    

string, default “”, (never None)

texture_coords_object
    

Object to set the texture coordinates

Type:
    

[[Object]]

time_offset
    

Either the starting frame (for positive speed) or ending frame (for negative speed)

Type:
    

float in [-1.04857e+06, 1.04857e+06], default 0.0

use_cyclic
    

Cyclic wave effect

Type:
    

boolean, default True

use_normal
    

Displace along normals

Type:
    

boolean, default False

use_normal_x
    

Enable displacement along the X normal

Type:
    

boolean, default True

use_normal_y
    

Enable displacement along the Y normal

Type:
    

boolean, default True

use_normal_z
    

Enable displacement along the Z normal

Type:
    

boolean, default True

use_x
    

X axis motion

Type:
    

boolean, default True

use_y
    

Y axis motion

Type:
    

boolean, default True

uv_layer
    

UV map name

Type:
    

string, default “”, (never None)

vertex_group
    

Vertex group name for modulating the wave

Type:
    

string, default “”, (never None)

width
    

Distance between the waves

Type:
    

float in [0, inf], default 1.5

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
