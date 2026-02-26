# GreasePencilBuildModifier(Modifier)

base classes — [[bpy_struct]], [[Modifier]]

_class _bpy.types.GreasePencilBuildModifier(_Modifier_)
    

Animate strokes appearing and disappearing

concurrent_time_alignment
    

How should strokes start to appear/disappear

  * `START` Align Start – All strokes start at same time (i.e. short strokes finish earlier).

  * `END` Align End – All strokes end at same time (i.e. short strokes start later).


Type:
    

enum in [`'START'`, `'END'`], default `'START'`

fade_factor
    

Defines how much of the stroke is fading in/out

Type:
    

float in [0, 1], default 0.0

fade_opacity_strength
    

How much strength fading applies on top of stroke opacity

Type:
    

float in [0, 1], default 0.0

fade_thickness_strength
    

How much strength fading applies on top of stroke thickness

Type:
    

float in [0, 1], default 0.0

frame_end
    

End Frame (when Restrict Frame Range is enabled)

Type:
    

float in [-1.04857e+06, 1.04857e+06], default 125.0

frame_start
    

Start Frame (when Restrict Frame Range is enabled)

Type:
    

float in [-1.04857e+06, 1.04857e+06], default 1.0

invert_layer_filter
    

Invert layer filter

Type:
    

boolean, default False

invert_layer_pass_filter
    

Invert layer pass filter

Type:
    

boolean, default False

invert_material_filter
    

Invert material filter

Type:
    

boolean, default False

invert_material_pass_filter
    

Invert material pass filter

Type:
    

boolean, default False

layer_pass_filter
    

Layer pass filter

Type:
    

int in [0, 100], default 0

length
    

Maximum number of frames that the build effect can run for (unless another GP keyframe occurs before this time has elapsed)

Type:
    

float in [1, 1.04857e+06], default 100.0

material_filter
    

Material used for filtering

Type:
    

[[Material]]

material_pass_filter
    

Material pass

Type:
    

int in [0, 100], default 0

mode
    

How strokes are being built

  * `SEQUENTIAL` Sequential – Strokes appear/disappear one after the other, but only a single one changes at a time.

  * `CONCURRENT` Concurrent – Multiple strokes appear/disappear at once.

  * `ADDITIVE` Additive – Builds only new strokes (assuming ‘additive’ drawing).


Type:
    

enum in [`'SEQUENTIAL'`, `'CONCURRENT'`, `'ADDITIVE'`], default `'SEQUENTIAL'`

object
    

Object used as build starting position

Type:
    

[[Object]]

open_fading_panel
    

Type:
    

boolean, default False

open_frame_range_panel
    

Type:
    

boolean, default False

open_influence_panel
    

Type:
    

boolean, default False

percentage_factor
    

Defines how much of the stroke is visible

Type:
    

float in [0, 1], default 0.0

speed_factor
    

Multiply recorded drawing speed by a factor

Type:
    

float in [0, 100], default 1.2

speed_maxgap
    

The maximum gap between strokes in seconds

Type:
    

float in [0, 100], default 0.5

start_delay
    

Number of frames after each GP keyframe before the modifier has any effect

Type:
    

float in [0, 1.04857e+06], default 0.0

target_vertex_group
    

Output Vertex group

Type:
    

string, default “”, (never None)

time_mode
    

Use drawing speed, a number of frames, or a manual factor to build strokes

  * `DRAWSPEED` Natural Drawing Speed – Use recorded speed multiplied by a factor.

  * `FRAMES` Number of Frames – Set a fixed number of frames for all build animations.

  * `PERCENTAGE` Percentage Factor – Set a manual percentage to build.


Type:
    

enum in [`'DRAWSPEED'`, `'FRAMES'`, `'PERCENTAGE'`], default `'FRAMES'`

transition
    

How are strokes animated (i.e. are they appearing or disappearing)

  * `GROW` Grow – Show points in the order they occur in each stroke (e.g. for animating lines being drawn).

  * `SHRINK` Shrink – Hide points from the end of each stroke to the start (e.g. for animating lines being erased).

  * `FADE` Vanish – Hide points in the order they occur in each stroke (e.g. for animating ink fading or vanishing after getting drawn).


Type:
    

enum in [`'GROW'`, `'SHRINK'`, `'FADE'`], default `'GROW'`

tree_node_filter
    

Layer name

Type:
    

string, default “”, (never None)

use_fading
    

Fade out strokes instead of directly cutting off

Type:
    

boolean, default False

use_layer_group_filter
    

Filter by layer group name

Type:
    

boolean, default False

use_layer_pass_filter
    

Use layer pass filter

Type:
    

boolean, default False

use_material_pass_filter
    

Use material pass filter

Type:
    

boolean, default False

use_percentage
    

Use a percentage factor to determine the visible points

Type:
    

boolean, default False

use_restrict_frame_range
    

Only modify strokes during the specified frame range

Type:
    

boolean, default False

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
