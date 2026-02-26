# StripModifier(bpy_struct)

base class — [`bpy_struct`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct "bpy.types.bpy_struct")

subclasses — [`BrightContrastModifier`](../B/bpy.types.BrightContrastModifier.md#bpy.types.BrightContrastModifier "bpy.types.BrightContrastModifier"), [`ColorBalanceModifier`](../C/bpy.types.ColorBalanceModifier.md#bpy.types.ColorBalanceModifier "bpy.types.ColorBalanceModifier"), [`CurvesModifier`](../C/bpy.types.CurvesModifier.md#bpy.types.CurvesModifier "bpy.types.CurvesModifier"), [`HueCorrectModifier`](../H/bpy.types.HueCorrectModifier.md#bpy.types.HueCorrectModifier "bpy.types.HueCorrectModifier"), [`MaskStripModifier`](../M/bpy.types.MaskStripModifier.md#bpy.types.MaskStripModifier "bpy.types.MaskStripModifier"), [`SequencerCompositorModifierData`](bpy.types.SequencerCompositorModifierData.md#bpy.types.SequencerCompositorModifierData "bpy.types.SequencerCompositorModifierData"), [`SequencerTonemapModifierData`](bpy.types.SequencerTonemapModifierData.md#bpy.types.SequencerTonemapModifierData "bpy.types.SequencerTonemapModifierData"), [`SoundEqualizerModifier`](bpy.types.SoundEqualizerModifier.md#bpy.types.SoundEqualizerModifier "bpy.types.SoundEqualizerModifier"), [`WhiteBalanceModifier`](../W/bpy.types.WhiteBalanceModifier.md#bpy.types.WhiteBalanceModifier "bpy.types.WhiteBalanceModifier")

_class _bpy.types.StripModifier(_bpy_struct_)
    

Modifier for sequence strip

enable
    

Enable this modifier

Type:
    

boolean, default False

input_mask_id
    

Mask ID used as mask input for the modifier

Type:
    

[`Mask`](../M/bpy.types.Mask.md#bpy.types.Mask "bpy.types.Mask")

input_mask_strip
    

Strip used as mask input for the modifier

Type:
    

[`Strip`](bpy.types.Strip.md#bpy.types.Strip "bpy.types.Strip")

input_mask_type
    

Type of input data used for mask

  * `STRIP` Strip – Use sequencer strip as mask input.

  * `ID` Mask – Use mask ID as mask input.


Type:
    

enum in [`'STRIP'`, `'ID'`], default `'STRIP'`

is_active
    

This modifier is active

Type:
    

boolean, default False

mask_time
    

Time to use for the Mask animation

  * `RELATIVE` Relative – Mask animation is offset to start of strip.

  * `ABSOLUTE` Absolute – Mask animation is in sync with scene frame.


Type:
    

enum in [`'RELATIVE'`, `'ABSOLUTE'`], default `'RELATIVE'`

mute
    

Mute this modifier

Type:
    

boolean, default False

name
    

Type:
    

string, default “”, (never None)

show_expanded
    

Mute expanded settings for the modifier

Type:
    

boolean, default False

type
    

Type:
    

enum in [Strip Modifier Type Items](../../bpy_types_enum_items/strip_modifier_type_items.md#rna-enum-strip-modifier-type-items), default `'BRIGHT_CONTRAST'`, (readonly)

_classmethod _bl_rna_get_subclass(_id_ , _default =None_, _/_)
    

Parameters:
    

**id** (_str_) – The RNA type identifier.

Returns:
    

The RNA type or default when not found.

Return type:
    

[`bpy.types.Struct`](bpy.types.Struct.md#bpy.types.Struct "bpy.types.Struct") subclass

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

  * [`bpy.context.strip_modifier`](../../bpy.context.md#bpy.context.strip_modifier "bpy.context.strip_modifier")
  * [`Strip.modifiers`](bpy.types.Strip.md#bpy.types.Strip.modifiers "bpy.types.Strip.modifiers")
  * [`StripModifiers.active`](bpy.types.StripModifiers.md#bpy.types.StripModifiers.active "bpy.types.StripModifiers.active")

| 

  * [`StripModifiers.new`](bpy.types.StripModifiers.md#bpy.types.StripModifiers.new "bpy.types.StripModifiers.new")
  * [`StripModifiers.remove`](bpy.types.StripModifiers.md#bpy.types.StripModifiers.remove "bpy.types.StripModifiers.remove")

  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
