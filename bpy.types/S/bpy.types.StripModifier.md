# StripModifier(bpy_struct)

base class — [[bpy_struct]]

subclasses — [[BrightContrastModifier]], [[ColorBalanceModifier]], [[CurvesModifier]], [[HueCorrectModifier]], [[MaskStripModifier]], [[SequencerCompositorModifierData]], [[SequencerTonemapModifierData]], [[SoundEqualizerModifier]], [[WhiteBalanceModifier]]

_class _bpy.types.StripModifier(_bpy_struct_)
    

Modifier for sequence strip

enable
    

Enable this modifier

Type:
    

boolean, default False

input_mask_id
    

Mask ID used as mask input for the modifier

Type:
    

[[Mask]]

input_mask_strip
    

Strip used as mask input for the modifier

Type:
    

[[Strip]]

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

  * [[bpy.context.strip_modifier]]
  * [[Strip.modifiers]]
  * [[StripModifiers.active]]

| 

  * [[StripModifiers.new]]
  * [[StripModifiers.remove]]

  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
