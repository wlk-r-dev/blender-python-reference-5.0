# NlaStrip(bpy_struct)

base class — [`bpy_struct`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct "bpy.types.bpy_struct")

_class _bpy.types.NlaStrip(_bpy_struct_)
    

A container referencing an existing Action

action
    

Action referenced by this strip

Type:
    

[`Action`](../A/bpy.types.Action.md#bpy.types.Action "bpy.types.Action")

action_frame_end
    

Last frame from action to use

Type:
    

float in [-inf, inf], default 0.0

action_frame_start
    

First frame from action to use

Type:
    

float in [-inf, inf], default 0.0

action_slot
    

The slot identifies which sub-set of the Action is considered to be for this strip, and its name is used to find the right slot when assigning another Action

Type:
    

[`ActionSlot`](../A/bpy.types.ActionSlot.md#bpy.types.ActionSlot "bpy.types.ActionSlot")

action_slot_handle
    

A number that identifies which sub-set of the Action is considered to be for this NLA strip

Type:
    

int in [-inf, inf], default 0

action_suitable_slots
    

The list of action slots suitable for this NLA strip

Type:
    

[`bpy_prop_collection`](../_other/bpy.types.bpy_prop_collection.md#bpy.types.bpy_prop_collection "bpy.types.bpy_prop_collection") of [`ActionSlot`](../A/bpy.types.ActionSlot.md#bpy.types.ActionSlot "bpy.types.ActionSlot"), (readonly)

active
    

NLA Strip is active

Type:
    

boolean, default False, (readonly)

blend_in
    

Number of frames at start of strip to fade in influence

Type:
    

float in [-inf, inf], default 0.0

blend_out
    

Type:
    

float in [-inf, inf], default 0.0

blend_type
    

Method used for combining strip’s result with accumulated result

  * `REPLACE` Replace – The strip values replace the accumulated results by amount specified by influence.

  * `COMBINE` Combine – The strip values are combined with accumulated results by appropriately using addition, multiplication, or quaternion math, based on channel type.

  * `ADD` Add – Weighted result of strip is added to the accumulated results.

  * `SUBTRACT` Subtract – Weighted result of strip is removed from the accumulated results.

  * `MULTIPLY` Multiply – Weighted result of strip is multiplied with the accumulated results.


Type:
    

enum in [`'REPLACE'`, `'COMBINE'`, `'ADD'`, `'SUBTRACT'`, `'MULTIPLY'`], default `'REPLACE'`

extrapolation
    

Action to take for gaps past the strip extents

  * `NOTHING` Nothing – Strip has no influence past its extents.

  * `HOLD` Hold – Hold the first frame if no previous strips in track, and always hold last frame.

  * `HOLD_FORWARD` Hold Forward – Only hold last frame.


Type:
    

enum in [`'NOTHING'`, `'HOLD'`, `'HOLD_FORWARD'`], default `'HOLD'`

fcurves
    

F-Curves for controlling the strip’s influence and timing

Type:
    

[`NlaStripFCurves`](bpy.types.NlaStripFCurves.md#bpy.types.NlaStripFCurves "bpy.types.NlaStripFCurves") [`bpy_prop_collection`](../_other/bpy.types.bpy_prop_collection.md#bpy.types.bpy_prop_collection "bpy.types.bpy_prop_collection") of [`FCurve`](../F/bpy.types.FCurve.md#bpy.types.FCurve "bpy.types.FCurve"), (readonly)

frame_end
    

Type:
    

float in [-inf, inf], default 0.0

frame_end_raw
    

Same as frame_end, except that any value can be set, including ones that create an invalid state

Type:
    

float in [-inf, inf], default 0.0

frame_end_ui
    

End frame of the NLA strip. Note: changing this value also updates the value of the strip’s repeats or its action’s end frame. If only the end frame should be changed, see the “frame_end” property instead.

Type:
    

float in [-inf, inf], default 0.0

frame_start
    

Type:
    

float in [-inf, inf], default 0.0

frame_start_raw
    

Same as frame_start, except that any value can be set, including ones that create an invalid state

Type:
    

float in [-inf, inf], default 0.0

frame_start_ui
    

Start frame of the NLA strip. Note: changing this value also updates the value of the strip’s end frame. If only the start frame should be changed, see the “frame_start” property instead.

Type:
    

float in [-inf, inf], default 0.0

influence
    

Amount the strip contributes to the current result

Type:
    

float in [0, 1], default 0.0

last_slot_identifier
    

The identifier of the most recently assigned action slot. The slot identifies which sub-set of the Action is considered to be for this strip, and its identifier is used to find the right slot when assigning an Action.

Type:
    

string, default “”, (never None)

modifiers
    

Modifiers affecting all the F-Curves in the referenced Action

Type:
    

[`bpy_prop_collection`](../_other/bpy.types.bpy_prop_collection.md#bpy.types.bpy_prop_collection "bpy.types.bpy_prop_collection") of [`FModifier`](../F/bpy.types.FModifier.md#bpy.types.FModifier "bpy.types.FModifier"), (readonly)

mute
    

Disable NLA Strip evaluation

Type:
    

boolean, default False

name
    

Type:
    

string, default “”, (never None)

repeat
    

Number of times to repeat the action range

Type:
    

float in [0.1, 1000], default 1.0

scale
    

Scaling factor for action

Type:
    

float in [0.0001, 1000], default 1.0

select
    

NLA Strip is selected

Type:
    

boolean, default False

strip_time
    

Frame of referenced Action to evaluate

Type:
    

float in [-inf, inf], default 0.0

strips
    

NLA Strips that this strip acts as a container for (if it is of type Meta)

Type:
    

[`bpy_prop_collection`](../_other/bpy.types.bpy_prop_collection.md#bpy.types.bpy_prop_collection "bpy.types.bpy_prop_collection") of `NlaStrip`, (readonly)

type
    

Type of NLA Strip

  * `CLIP` Action Clip – NLA Strip references some Action.

  * `TRANSITION` Transition – NLA Strip ‘transitions’ between adjacent strips.

  * `META` Meta – NLA Strip acts as a container for adjacent strips.

  * `SOUND` Sound Clip – NLA Strip representing a sound event for speakers.


Type:
    

enum in [`'CLIP'`, `'TRANSITION'`, `'META'`, `'SOUND'`], default `'CLIP'`, (readonly)

use_animated_influence
    

Influence setting is controlled by an F-Curve rather than automatically determined

Type:
    

boolean, default False

use_animated_time
    

Strip time is controlled by an F-Curve rather than automatically determined

Type:
    

boolean, default False

use_animated_time_cyclic
    

Cycle the animated time within the action start and end

Type:
    

boolean, default False

use_auto_blend
    

Number of frames for Blending In/Out is automatically determined from overlapping strips

Type:
    

boolean, default False

use_reverse
    

NLA Strip is played back in reverse order (only when timing is automatically determined)

Type:
    

boolean, default False

use_sync_length
    

Update range of frames referenced from action after tweaking strip and its keyframes

Type:
    

boolean, default False

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

| 


  
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

| 

  * [`bpy_struct.keyframe_delete`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.keyframe_delete "bpy.types.bpy_struct.keyframe_delete")
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

  
---|---  
  
## References

  * [`bpy.context.active_nla_strip`](../../bpy.context.md#bpy.context.active_nla_strip "bpy.context.active_nla_strip")
  * [`bpy.context.selected_nla_strips`](../../bpy.context.md#bpy.context.selected_nla_strips "bpy.context.selected_nla_strips")
  * `NlaStrip.strips`

| 

  * [`NlaStrips.new`](bpy.types.NlaStrips.md#bpy.types.NlaStrips.new "bpy.types.NlaStrips.new")
  * [`NlaStrips.remove`](bpy.types.NlaStrips.md#bpy.types.NlaStrips.remove "bpy.types.NlaStrips.remove")
  * [`NlaTrack.strips`](bpy.types.NlaTrack.md#bpy.types.NlaTrack.strips "bpy.types.NlaTrack.strips")

  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
