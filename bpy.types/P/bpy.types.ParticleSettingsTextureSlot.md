# ParticleSettingsTextureSlot(TextureSlot)

base classes — [[bpy_struct]], [[TextureSlot]]

_class _bpy.types.ParticleSettingsTextureSlot(_TextureSlot_)
    

Texture slot for textures in a Particle Settings data-block

clump_factor
    

Amount texture affects child clump

Type:
    

float in [-inf, inf], default 1.0

damp_factor
    

Amount texture affects particle damping

Type:
    

float in [-inf, inf], default 1.0

density_factor
    

Amount texture affects particle density

Type:
    

float in [-inf, inf], default 1.0

field_factor
    

Amount texture affects particle force fields

Type:
    

float in [-inf, inf], default 1.0

gravity_factor
    

Amount texture affects particle gravity

Type:
    

float in [-inf, inf], default 1.0

kink_amp_factor
    

Amount texture affects child kink amplitude

Type:
    

float in [-inf, inf], default 1.0

kink_freq_factor
    

Amount texture affects child kink frequency

Type:
    

float in [-inf, inf], default 1.0

length_factor
    

Amount texture affects child hair length

Type:
    

float in [-inf, inf], default 1.0

life_factor
    

Amount texture affects particle life time

Type:
    

float in [-inf, inf], default 1.0

mapping
    

  * `FLAT` Flat – Map X and Y coordinates directly.

  * `CUBE` Cube – Map using the normal vector.

  * `TUBE` Tube – Map with Z as central axis.

  * `SPHERE` Sphere – Map with Z as central axis.


Type:
    

enum in [`'FLAT'`, `'CUBE'`, `'TUBE'`, `'SPHERE'`], default `'FLAT'`

mapping_x
    

Type:
    

enum in [`'NONE'`, `'X'`, `'Y'`, `'Z'`], default `'X'`

mapping_y
    

Type:
    

enum in [`'NONE'`, `'X'`, `'Y'`, `'Z'`], default `'Y'`

mapping_z
    

Type:
    

enum in [`'NONE'`, `'X'`, `'Y'`, `'Z'`], default `'Z'`

object
    

Object to use for mapping with Object texture coordinates

Type:
    

[[Object]]

rough_factor
    

Amount texture affects child roughness

Type:
    

float in [-inf, inf], default 1.0

size_factor
    

Amount texture affects physical particle size

Type:
    

float in [-inf, inf], default 1.0

texture_coords
    

Texture coordinates used to map the texture onto the background

  * `GLOBAL` Global – Use global coordinates for the texture coordinates.

  * `OBJECT` Object – Use linked object’s coordinates for texture coordinates.

  * `UV` UV – Use UV coordinates for texture coordinates.

  * `ORCO` Generated – Use the original undeformed coordinates of the object.

  * `STRAND` Strand / Particle – Use normalized strand texture coordinate (1D) or particle age (X) and trail position (Y).


Type:
    

enum in [`'GLOBAL'`, `'OBJECT'`, `'UV'`, `'ORCO'`, `'STRAND'`], default `'UV'`

time_factor
    

Amount texture affects particle emission time

Type:
    

float in [-inf, inf], default 1.0

twist_factor
    

Amount texture affects child twist

Type:
    

float in [-inf, inf], default 1.0

use_map_clump
    

Affect the child clumping

Type:
    

boolean, default False

use_map_damp
    

Affect the particle velocity damping

Type:
    

boolean, default False

use_map_density
    

Affect the density of the particles

Type:
    

boolean, default False

use_map_field
    

Affect the particle force fields

Type:
    

boolean, default False

use_map_gravity
    

Affect the particle gravity

Type:
    

boolean, default False

use_map_kink_amp
    

Affect the child kink amplitude

Type:
    

boolean, default False

use_map_kink_freq
    

Affect the child kink frequency

Type:
    

boolean, default False

use_map_length
    

Affect the child hair length

Type:
    

boolean, default False

use_map_life
    

Affect the life time of the particles

Type:
    

boolean, default False

use_map_rough
    

Affect the child rough

Type:
    

boolean, default False

use_map_size
    

Affect the particle size

Type:
    

boolean, default False

use_map_time
    

Affect the emission time of the particles

Type:
    

boolean, default True

use_map_twist
    

Affect the child twist

Type:
    

boolean, default False

use_map_velocity
    

Affect the particle initial velocity

Type:
    

boolean, default False

uv_layer
    

UV map to use for mapping with UV texture coordinates

Type:
    

string, default “”, (never None)

velocity_factor
    

Amount texture affects particle initial velocity

Type:
    

float in [-inf, inf], default 1.0

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
  * [[TextureSlot.texture]]
  * [[TextureSlot.name]]
  * [[TextureSlot.offset]]
  * [[TextureSlot.scale]]

| 

  * [[TextureSlot.color]]
  * [[TextureSlot.blend_type]]
  * [[TextureSlot.default_value]]
  * [[TextureSlot.output_node]]

  
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
  * [[TextureSlot.bl_rna_get_subclass]]
  * [[TextureSlot.bl_rna_get_subclass_py]]

  
---|---  
  
## References

  * [[ParticleSettings.texture_slots]]
  * [[ParticleSettingsTextureSlots.add]]

| 

  * [[ParticleSettingsTextureSlots.create]]

  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
