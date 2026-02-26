# FCurve(bpy_struct)

base class — [`bpy_struct`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct "bpy.types.bpy_struct")

_class _bpy.types.FCurve(_bpy_struct_)
    

F-Curve defining values of a period of time

array_index
    

Index to the specific property affected by F-Curve if applicable

Type:
    

int in [0, inf], default 0

auto_smoothing
    

Algorithm used to compute automatic handles

Type:
    

enum in [Fcurve Auto Smoothing Items](../../bpy_types_enum_items/fcurve_auto_smoothing_items.md#rna-enum-fcurve-auto-smoothing-items), default `'NONE'`

color
    

Color of the F-Curve in the Graph Editor

Type:
    

[`mathutils.Color`](mathutils.md#mathutils.Color "mathutils.Color") of 3 items in [0, 1], default (0.0, 0.0, 0.0)

color_mode
    

Method used to determine color of F-Curve in Graph Editor

  * `AUTO_RAINBOW` Auto Rainbow – Cycle through the rainbow, trying to give each curve a unique color.

  * `AUTO_RGB` Auto XYZ to RGB – Use axis colors for transform and color properties, and auto-rainbow for the rest.

  * `AUTO_YRGB` Auto WXYZ to YRGB – Use WXYZ axis colors for quaternion/axis-angle rotations, XYZ axis colors for other transform and color properties, and auto-rainbow for the rest.

  * `CUSTOM` User Defined – Use custom hand-picked color for F-Curve.


Type:
    

enum in [`'AUTO_RAINBOW'`, `'AUTO_RGB'`, `'AUTO_YRGB'`, `'CUSTOM'`], default `'AUTO_RAINBOW'`

data_path
    

RNA Path to property affected by F-Curve

Type:
    

string, default “”, (never None)

driver
    

Channel Driver (only set for Driver F-Curves)

Type:
    

[`Driver`](../D/bpy.types.Driver.md#bpy.types.Driver "bpy.types.Driver"), (readonly)

extrapolation
    

Method used for evaluating value of F-Curve outside first and last keyframes

  * `CONSTANT` Constant – Hold values of endpoint keyframes.

  * `LINEAR` Linear – Use slope of curve leading in/out of endpoint keyframes.


Type:
    

enum in [`'CONSTANT'`, `'LINEAR'`], default `'CONSTANT'`

group
    

Action Group that this F-Curve belongs to

Type:
    

[`ActionGroup`](../A/bpy.types.ActionGroup.md#bpy.types.ActionGroup "bpy.types.ActionGroup")

hide
    

F-Curve and its keyframes are hidden in the Graph Editor graphs

Type:
    

boolean, default False

is_empty
    

True if the curve contributes no animation due to lack of keyframes or useful modifiers, and should be deleted

Type:
    

boolean, default False, (readonly)

is_valid
    

False when F-Curve could not be evaluated in past, so should be skipped when evaluating

Type:
    

boolean, default False

keyframe_points
    

User-editable keyframes

Type:
    

[`FCurveKeyframePoints`](bpy.types.FCurveKeyframePoints.md#bpy.types.FCurveKeyframePoints "bpy.types.FCurveKeyframePoints") [`bpy_prop_collection`](../_other/bpy.types.bpy_prop_collection.md#bpy.types.bpy_prop_collection "bpy.types.bpy_prop_collection") of [`Keyframe`](../K/bpy.types.Keyframe.md#bpy.types.Keyframe "bpy.types.Keyframe"), (readonly)

lock
    

F-Curve’s settings cannot be edited

Type:
    

boolean, default False

modifiers
    

Modifiers affecting the shape of the F-Curve

Type:
    

[`FCurveModifiers`](bpy.types.FCurveModifiers.md#bpy.types.FCurveModifiers "bpy.types.FCurveModifiers") [`bpy_prop_collection`](../_other/bpy.types.bpy_prop_collection.md#bpy.types.bpy_prop_collection "bpy.types.bpy_prop_collection") of [`FModifier`](bpy.types.FModifier.md#bpy.types.FModifier "bpy.types.FModifier"), (readonly)

mute
    

Disable F-Curve evaluation

Type:
    

boolean, default False

sampled_points
    

Sampled animation data

Type:
    

[`bpy_prop_collection`](../_other/bpy.types.bpy_prop_collection.md#bpy.types.bpy_prop_collection "bpy.types.bpy_prop_collection") of [`FCurveSample`](bpy.types.FCurveSample.md#bpy.types.FCurveSample "bpy.types.FCurveSample"), (readonly)

select
    

F-Curve is selected for editing

Type:
    

boolean, default False

evaluate(_frame_)
    

Evaluate F-Curve

Parameters:
    

**frame** (_float in_ _[__-inf_ _,__inf_ _]_) – Frame, Evaluate F-Curve at given frame

Returns:
    

Value, Value of F-Curve specific frame

Return type:
    

float in [-inf, inf]

update()
    

Ensure keyframes are sorted in chronological order and handles are set correctly

range()
    

Get the time extents for F-Curve

Returns:
    

Range, Min/Max values

Return type:
    

[`mathutils.Vector`](mathutils.md#mathutils.Vector "mathutils.Vector") of 2 items in [-inf, inf]

update_autoflags(_data_)
    

Update FCurve flags set automatically from affected property (currently, integer/discrete flags set when the property is not a float)

Parameters:
    

**data** ([`AnyType`](../A/bpy.types.AnyType.md#bpy.types.AnyType "bpy.types.AnyType"), (never None)) – Data, Data containing the property controlled by given FCurve

convert_to_samples(_start_ , _end_)
    

Convert current FCurve from keyframes to sample points, if necessary

Parameters:
    

  * **start** (_int in_ _[__-1048574_ _,__1048574_ _]_) – Start Frame

  * **end** (_int in_ _[__-1048574_ _,__1048574_ _]_) – End Frame


convert_to_keyframes(_start_ , _end_)
    

Convert current FCurve from sample points to keyframes (linear interpolation), if necessary

Parameters:
    

  * **start** (_int in_ _[__-1048574_ _,__1048574_ _]_) – Start Frame

  * **end** (_int in_ _[__-1048574_ _,__1048574_ _]_) – End Frame


bake(_start_ , _end_ , _*_ , _step =1.0_, _remove ='IN_RANGE'_)
    

Place keys at even intervals on the existing curve.

Parameters:
    

  * **start** (_int in_ _[__-1048574_ _,__1048574_ _]_) – Start Frame, Frame at which to start baking

  * **end** (_int in_ _[__-1048574_ _,__1048574_ _]_) – End Frame, Frame at which to end baking (inclusive)

  * **step** (_float in_ _[__0.01_ _,__inf_ _]__,__(__optional_ _)_) – Step, At which interval to add keys

  * **remove** (enum in [`'NONE'`, `'IN_RANGE'`, `'OUT_RANGE'`, `'ALL'`], (optional)) – 

Remove Options, Choose which keys should be automatically removed by the bake

    * `NONE` None – Keep all keys.

    * `IN_RANGE` In Range – Remove all keys within the defined range.

    * `OUT_RANGE` Outside Range – Remove all keys outside the defined range.

    * `ALL` All – Remove all existing keys.


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

  * [`bpy.context.active_editable_fcurve`](../../bpy.context.md#bpy.context.active_editable_fcurve "bpy.context.active_editable_fcurve")
  * [`bpy.context.editable_fcurves`](../../bpy.context.md#bpy.context.editable_fcurves "bpy.context.editable_fcurves")
  * [`bpy.context.selected_editable_fcurves`](../../bpy.context.md#bpy.context.selected_editable_fcurves "bpy.context.selected_editable_fcurves")
  * [`bpy.context.selected_visible_fcurves`](../../bpy.context.md#bpy.context.selected_visible_fcurves "bpy.context.selected_visible_fcurves")
  * [`bpy.context.visible_fcurves`](../../bpy.context.md#bpy.context.visible_fcurves "bpy.context.visible_fcurves")
  * [`Action.fcurve_ensure_for_datablock`](../A/bpy.types.Action.md#bpy.types.Action.fcurve_ensure_for_datablock "bpy.types.Action.fcurve_ensure_for_datablock")
  * [`ActionChannelbag.fcurves`](../A/bpy.types.ActionChannelbag.md#bpy.types.ActionChannelbag.fcurves "bpy.types.ActionChannelbag.fcurves")
  * [`ActionChannelbagFCurves.ensure`](../A/bpy.types.ActionChannelbagFCurves.md#bpy.types.ActionChannelbagFCurves.ensure "bpy.types.ActionChannelbagFCurves.ensure")
  * [`ActionChannelbagFCurves.find`](../A/bpy.types.ActionChannelbagFCurves.md#bpy.types.ActionChannelbagFCurves.find "bpy.types.ActionChannelbagFCurves.find")
  * [`ActionChannelbagFCurves.new`](../A/bpy.types.ActionChannelbagFCurves.md#bpy.types.ActionChannelbagFCurves.new "bpy.types.ActionChannelbagFCurves.new")
  * [`ActionChannelbagFCurves.new_from_fcurve`](../A/bpy.types.ActionChannelbagFCurves.md#bpy.types.ActionChannelbagFCurves.new_from_fcurve "bpy.types.ActionChannelbagFCurves.new_from_fcurve")

| 

  * [`ActionChannelbagFCurves.new_from_fcurve`](../A/bpy.types.ActionChannelbagFCurves.md#bpy.types.ActionChannelbagFCurves.new_from_fcurve "bpy.types.ActionChannelbagFCurves.new_from_fcurve")
  * [`ActionChannelbagFCurves.remove`](../A/bpy.types.ActionChannelbagFCurves.md#bpy.types.ActionChannelbagFCurves.remove "bpy.types.ActionChannelbagFCurves.remove")
  * [`ActionGroup.channels`](../A/bpy.types.ActionGroup.md#bpy.types.ActionGroup.channels "bpy.types.ActionGroup.channels")
  * [`AnimData.drivers`](../A/bpy.types.AnimData.md#bpy.types.AnimData.drivers "bpy.types.AnimData.drivers")
  * [`AnimDataDrivers.find`](../A/bpy.types.AnimDataDrivers.md#bpy.types.AnimDataDrivers.find "bpy.types.AnimDataDrivers.find")
  * [`AnimDataDrivers.from_existing`](../A/bpy.types.AnimDataDrivers.md#bpy.types.AnimDataDrivers.from_existing "bpy.types.AnimDataDrivers.from_existing")
  * [`AnimDataDrivers.from_existing`](../A/bpy.types.AnimDataDrivers.md#bpy.types.AnimDataDrivers.from_existing "bpy.types.AnimDataDrivers.from_existing")
  * [`AnimDataDrivers.new`](../A/bpy.types.AnimDataDrivers.md#bpy.types.AnimDataDrivers.new "bpy.types.AnimDataDrivers.new")
  * [`AnimDataDrivers.remove`](../A/bpy.types.AnimDataDrivers.md#bpy.types.AnimDataDrivers.remove "bpy.types.AnimDataDrivers.remove")
  * [`NlaStrip.fcurves`](../N/bpy.types.NlaStrip.md#bpy.types.NlaStrip.fcurves "bpy.types.NlaStrip.fcurves")
  * [`NlaStripFCurves.find`](../N/bpy.types.NlaStripFCurves.md#bpy.types.NlaStripFCurves.find "bpy.types.NlaStripFCurves.find")

  
---|---
  *[*]: Keyword-only parameters separator (PEP 3102)
  *[/]: Positional-only parameter separator (PEP 570)
