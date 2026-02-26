# UnifiedPaintSettings(bpy_struct)

base class — [[bpy_struct]]

_class _bpy.types.UnifiedPaintSettings(_bpy_struct_)
    

Overrides for some of the active brush’s settings

color
    

Type:
    

[[mathutils.Color]] of 3 items in [0, 1], default (0.0, 0.0, 0.0)

hue_jitter
    

Color jitter effect on hue

Type:
    

float in [0, 1], default 0.0

input_samples
    

Number of input samples to average together to smooth the brush stroke

Type:
    

int in [1, 64], default 1

saturation_jitter
    

Color jitter effect on saturation

Type:
    

float in [0, 1], default 0.0

secondary_color
    

Type:
    

[[mathutils.Color]] of 3 items in [0, 1], default (1.0, 1.0, 1.0)

size
    

Diameter of the brush

Type:
    

int in [1, 10000], default 100

strength
    

How powerful the effect of the brush is when applied

Type:
    

float in [0, 10], default 0.5

unprojected_size
    

Diameter of brush in Blender units

Type:
    

float in [0.001, inf], default 0.58

use_color_jitter
    

Jitter brush color

Type:
    

boolean, default False

use_locked_size
    

Measure brush size relative to the view or the scene

  * `VIEW` View – Measure brush size relative to the view.

  * `SCENE` Scene – Measure brush size relative to the scene.


Type:
    

enum in [`'VIEW'`, `'SCENE'`], default `'VIEW'`

use_random_press_hue
    

Use pressure to modulate randomness

Type:
    

boolean, default False

use_random_press_sat
    

Use pressure to modulate randomness

Type:
    

boolean, default False

use_random_press_val
    

Use pressure to modulate randomness

Type:
    

boolean, default False

use_stroke_random_hue
    

Use randomness at stroke level

Type:
    

boolean, default False

use_stroke_random_sat
    

Use randomness at stroke level

Type:
    

boolean, default False

use_stroke_random_val
    

Use randomness at stroke level

Type:
    

boolean, default False

use_unified_color
    

Instead of per-brush color, the color is shared across brushes

Type:
    

boolean, default True

use_unified_input_samples
    

Instead of per-brush input samples, the value is shared across brushes

Type:
    

boolean, default False

use_unified_size
    

Instead of per-brush size, the size is shared across brushes

Type:
    

boolean, default True

use_unified_strength
    

Instead of per-brush strength, the strength is shared across brushes

Type:
    

boolean, default False

use_unified_weight
    

Instead of per-brush weight, the weight is shared across brushes

Type:
    

boolean, default False

value_jitter
    

Color jitter effect on value

Type:
    

float in [0, 1], default 0.0

weight
    

Weight to assign in vertex groups

Type:
    

float in [0, 1], default 0.5

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

| 


  
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

| 

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
  * [[bpy_struct.type_recast]]
  * [[bpy_struct.values]]

  
---|---  
  
## References

  * [[Paint.unified_paint_settings]]

| 


  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
