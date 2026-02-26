# OceanModifier(Modifier)

base classes — [`bpy_struct`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct "bpy.types.bpy_struct"), [`Modifier`](../M/bpy.types.Modifier.md#bpy.types.Modifier "bpy.types.Modifier")

_class _bpy.types.OceanModifier(_Modifier_)
    

Simulate an ocean surface

bake_foam_fade
    

How much foam accumulates over time (baked ocean only)

Type:
    

float in [0, inf], default 0.98

choppiness
    

Choppiness of the wave’s crest (adds some horizontal component to the displacement)

Type:
    

float in [0, inf], default 1.0

damping
    

Damp reflected waves going in opposite direction to the wind

Type:
    

float in [0, 1], default 0.5

depth
    

Depth of the solid ground below the water surface

Type:
    

float in [-inf, inf], default 200.0

fetch_jonswap
    

This is the distance from a lee shore, called the fetch, or the distance over which the wind blows with constant velocity. Used by ‘JONSWAP’ and ‘TMA’ models.

Type:
    

float in [0, inf], default 120.0

filepath
    

Path to a folder to store external baked images

Type:
    

string, default “”, (never None, blend relative `//` prefix supported)

foam_coverage
    

Amount of generated foam

Type:
    

float in [-inf, inf], default 0.0

foam_layer_name
    

Name of the vertex color layer used for foam

Type:
    

string, default “”, (never None)

frame_end
    

End frame of the ocean baking

Type:
    

int in [-inf, inf], default 250

frame_start
    

Start frame of the ocean baking

Type:
    

int in [-inf, inf], default 1

geometry_mode
    

Method of modifying geometry

  * `GENERATE` Generate – Generate ocean surface geometry at the specified resolution.

  * `DISPLACE` Displace – Displace existing geometry according to simulation.


Type:
    

enum in [`'GENERATE'`, `'DISPLACE'`], default `'GENERATE'`

invert_spray
    

Invert the spray direction map

Type:
    

boolean, default False

is_cached
    

Whether the ocean is using cached data or simulating

Type:
    

boolean, default False, (readonly)

random_seed
    

Seed of the random generator

Type:
    

int in [0, inf], default 0

repeat_x
    

Repetitions of the generated surface in X

Type:
    

int in [1, 1024], default 1

repeat_y
    

Repetitions of the generated surface in Y

Type:
    

int in [1, 1024], default 1

resolution
    

Resolution of the generated surface for rendering and baking

Type:
    

int in [1, 1024], default 7

sharpen_peak_jonswap
    

Peak sharpening for ‘JONSWAP’ and ‘TMA’ models

Type:
    

float in [0, 1], default 0.0

size
    

Surface scale factor (does not affect the height of the waves)

Type:
    

float in [0, inf], default 1.0

spatial_size
    

Size of the simulation domain (in meters), and of the generated geometry (in BU)

Type:
    

int in [-inf, inf], default 50

spectrum
    

Spectrum to use

  * `PHILLIPS` Turbulent Ocean – Use for turbulent seas with foam.

  * `PIERSON_MOSKOWITZ` Established Ocean – Use for a large area, established ocean (Pierson-Moskowitz method).

  * `JONSWAP` Established Ocean (Sharp Peaks) – Use for established oceans (‘JONSWAP’, Pierson-Moskowitz method) with peak sharpening.

  * `TEXEL_MARSEN_ARSLOE` Shallow Water – Use for shallow water (‘JONSWAP’, ‘TMA’ - Texel-Marsen-Arsloe method).


Type:
    

enum in [`'PHILLIPS'`, `'PIERSON_MOSKOWITZ'`, `'JONSWAP'`, `'TEXEL_MARSEN_ARSLOE'`], default `'PHILLIPS'`

spray_layer_name
    

Name of the vertex color layer used for the spray direction map

Type:
    

string, default “”, (never None)

time
    

Current time of the simulation

Type:
    

float in [0, inf], default 1.0

use_foam
    

Generate foam mask as a vertex color channel

Type:
    

boolean, default False

use_normals
    

Output normals for bump mapping - disabling can speed up performance if it’s not needed

Type:
    

boolean, default False

use_spray
    

Generate map of spray direction as a vertex color channel

Type:
    

boolean, default False

viewport_resolution
    

Viewport resolution of the generated surface

Type:
    

int in [1, 1024], default 7

wave_alignment
    

How much the waves are aligned to each other

Type:
    

float in [0, 1], default 0.0

wave_direction
    

Main direction of the waves when they are (partially) aligned

Type:
    

float in [-inf, inf], default 0.0

wave_scale
    

Scale of the displacement effect

Type:
    

float in [0, inf], default 1.0

wave_scale_min
    

Shortest allowed wavelength

Type:
    

float in [0, inf], default 0.01

wind_velocity
    

Wind speed

Type:
    

float in [-inf, inf], default 30.0

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
