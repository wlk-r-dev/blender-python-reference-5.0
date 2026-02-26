# GreasePencilTimeModifier(Modifier)

base classes — [[bpy_struct]], [[Modifier]]

_class _bpy.types.GreasePencilTimeModifier(_Modifier_)
    

Offset keyframes

frame_end
    

Final frame of the range

Type:
    

int in [0, 1048574], default 250

frame_scale
    

Evaluation time in seconds

Type:
    

float in [0.001, 100], default 1.0

frame_start
    

First frame of the range

Type:
    

int in [0, 1048574], default 1

invert_layer_filter
    

Invert layer filter

Type:
    

boolean, default False

invert_layer_pass_filter
    

Invert layer pass filter

Type:
    

boolean, default False

layer_pass_filter
    

Layer pass filter

Type:
    

int in [0, 100], default 0

mode
    

  * `NORMAL` Regular – Apply offset in usual animation direction.

  * `REVERSE` Reverse – Apply offset in reverse animation direction.

  * `FIX` Fixed Frame – Keep frame and do not change with time.

  * `PINGPONG` Ping Pong – Loop back and forth starting in reverse.

  * `CHAIN` Chain – List of chained animation segments.


Type:
    

enum in [`'NORMAL'`, `'REVERSE'`, `'FIX'`, `'PINGPONG'`, `'CHAIN'`], default `'NORMAL'`

offset
    

Number of frames to offset original keyframe number or frame to fix

Type:
    

int in [-32768, 32767], default 1

open_custom_range_panel
    

Type:
    

boolean, default False

open_influence_panel
    

Type:
    

boolean, default False

segment_active_index
    

Active index in the segment list

Type:
    

int in [0, inf], default 0

segments
    

Type:
    

[[bpy_prop_collection]] of [[GreasePencilTimeModifierSegment]], (readonly)

tree_node_filter
    

Layer name

Type:
    

string, default “”, (never None)

use_custom_frame_range
    

Define a custom range of frames to use in modifier

Type:
    

boolean, default False

use_keep_loop
    

Retiming end frames and move to start of animation to keep loop

Type:
    

boolean, default True

use_layer_group_filter
    

Filter by layer group name

Type:
    

boolean, default False

use_layer_pass_filter
    

Use layer pass filter

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
