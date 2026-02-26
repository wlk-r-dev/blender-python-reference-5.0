# Strip(bpy_struct)

base class — [[bpy_struct]]

subclasses — [[EffectStrip]], [[ImageStrip]], [[MaskStrip]], [[MetaStrip]], [[MovieClipStrip]], [[MovieStrip]], [[SceneStrip]], [[SoundStrip]]

_class _bpy.types.Strip(_bpy_struct_)
    

Sequence strip in the sequence editor

blend_alpha
    

Percentage of how much the strip’s colors affect other strips

Type:
    

float in [0, 1], default 1.0

blend_type
    

Method for controlling how the strip combines with other strips

Type:
    

enum in [`'REPLACE'`, `'CROSS'`, `'DARKEN'`, `'MULTIPLY'`, `'BURN'`, `'LINEAR_BURN'`, `'LIGHTEN'`, `'SCREEN'`, `'DODGE'`, `'ADD'`, `'OVERLAY'`, `'SOFT_LIGHT'`, `'HARD_LIGHT'`, `'VIVID_LIGHT'`, `'LINEAR_LIGHT'`, `'PIN_LIGHT'`, `'DIFFERENCE'`, `'EXCLUSION'`, `'SUBTRACT'`, `'HUE'`, `'SATURATION'`, `'COLOR'`, `'VALUE'`, `'ALPHA_OVER'`, `'ALPHA_UNDER'`, `'GAMMA_CROSS'`], default `'ALPHA_OVER'`

channel
    

Y position of the sequence strip

Type:
    

int in [1, 128], default 0

color_tag
    

Color tag for a strip

Type:
    

enum in [Strip Color Items](../../bpy_types_enum_items/strip_color_items.md#rna-enum-strip-color-items), default `'COLOR_01'`

effect_fader
    

Custom fade value

Type:
    

float in [0, 1], default 0.0

frame_duration
    

The length of the contents of this strip before the handles are applied

Type:
    

int in [1, 1048574], default 0, (readonly)

frame_final_duration
    

The length of the contents of this strip after the handles are applied

Type:
    

int in [1, 1048574], default 0

frame_final_end
    

End frame displayed in the sequence editor after offsets are applied

Type:
    

int in [-inf, inf], default 0

frame_final_start
    

Start frame displayed in the sequence editor after offsets are applied, setting this is equivalent to moving the handle, not the actual start frame

Type:
    

int in [-inf, inf], default 0

frame_offset_end
    

Type:
    

float in [-inf, inf], default 0.0

frame_offset_start
    

Type:
    

float in [-inf, inf], default 0.0

frame_start
    

X position where the strip begins

Type:
    

float in [-inf, inf], default 0.0

lock
    

Lock strip so that it cannot be transformed

Type:
    

boolean, default False

modifiers
    

Modifiers affecting this strip

Type:
    

[[StripModifiers]] [[bpy_prop_collection]] of [[StripModifier]], (readonly)

mute
    

Disable strip so that it cannot be viewed in the output

Type:
    

boolean, default False

name
    

Type:
    

string, default “”, (never None)

select
    

Type:
    

boolean, default False

select_left_handle
    

Type:
    

boolean, default False

select_right_handle
    

Type:
    

boolean, default False

show_retiming_keys
    

Show retiming keys, so they can be moved

Type:
    

boolean, default False

type
    

Type:
    

enum in [`'IMAGE'`, `'META'`, `'SCENE'`, `'MOVIE'`, `'MOVIECLIP'`, `'MASK'`, `'SOUND'`, `'CROSS'`, `'ADD'`, `'SUBTRACT'`, `'ALPHA_OVER'`, `'ALPHA_UNDER'`, `'GAMMA_CROSS'`, `'MULTIPLY'`, `'WIPE'`, `'GLOW'`, `'COLOR'`, `'SPEED'`, `'MULTICAM'`, `'ADJUSTMENT'`, `'GAUSSIAN_BLUR'`, `'TEXT'`, `'COLORMIX'`], default `'IMAGE'`, (readonly)

use_default_fade
    

Fade effect using the built-in default (usually makes the transition as long as the effect strip)

Type:
    

boolean, default False

use_linear_modifiers
    

Calculate modifiers in linear space instead of sequencer’s space

Type:
    

boolean, default False

bl_system_properties_get(_*_ , _do_create =False_)
    

DEBUG ONLY. Internal access to runtime-defined RNA data storage, intended solely for testing and debugging purposes. Do not access it in regular scripting work, and in particular, do not assume that it contains writable data

Parameters:
    

**do_create** (_boolean_ _,__(__optional_ _)_) – Ensure that system properties are created if they do not exist yet

Returns:
    

The system properties root container, or None if there are no system properties stored in this data yet, and its creation was not requested

Return type:
    

[[PropertyGroup]]

strip_elem_from_frame(_frame_)
    

Return the strip element from a given frame or None

Parameters:
    

**frame** (_int in_ _[__-1048574_ _,__1048574_ _]_) – Frame, The frame to get the strip element from

Returns:
    

strip element of the current frame

Return type:
    

[[StripElement]]

swap(_other_)
    

swap

Parameters:
    

**other** (`Strip`, (never None)) – Other

move_to_meta(_meta_sequence_)
    

move_to_meta

Parameters:
    

**meta_sequence** (`Strip`, (never None)) – Destination Meta Strip, Meta to move the strip into

parent_meta()
    

Parent meta

Returns:
    

Parent Meta

Return type:
    

`Strip`

invalidate_cache(_type_)
    

Invalidate cached images for strip and all dependent strips

Parameters:
    

**type** (enum in [`'RAW'`, `'COMPOSITE'`], (never None)) – Type, Cache Type

split(_frame_ , _split_method_ , _*_ , _ignore_connections =False_)
    

Split Strip

Parameters:
    

  * **frame** (_int in_ _[__-inf_ _,__inf_ _]_) – Frame where to split the strip

  * **ignore_connections** (_boolean_ _,__(__optional_ _)_) – Don’t propagate split to connected strips


Returns:
    

Right side Strip

Return type:
    

`Strip`

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

  * [[bpy.context.active_strip]]
  * [[bpy.context.selected_editable_strips]]
  * [[bpy.context.selected_strips]]
  * [[bpy.context.strip]]
  * [[bpy.context.strips]]
  * [[AddStrip.input_1]]
  * [[AddStrip.input_2]]
  * [[AlphaOverStrip.input_1]]
  * [[AlphaOverStrip.input_2]]
  * [[AlphaUnderStrip.input_1]]
  * [[AlphaUnderStrip.input_2]]
  * [[ColorMixStrip.input_1]]
  * [[ColorMixStrip.input_2]]
  * [[CrossStrip.input_1]]
  * [[CrossStrip.input_2]]
  * [[GammaCrossStrip.input_1]]
  * [[GammaCrossStrip.input_2]]
  * [[GaussianBlurStrip.input_1]]
  * [[GlowStrip.input_1]]
  * [[MetaStrip.strips]]
  * [[MultiplyStrip.input_1]]
  * [[MultiplyStrip.input_2]]
  * [[SequenceEditor.active_strip]]
  * [[SequenceEditor.display_stack]]
  * [[SequenceEditor.meta_stack]]
  * [[SequenceEditor.strips]]
  * [[SequenceEditor.strips_all]]
  * [[SpeedControlStrip.input_1]]
  * `Strip.move_to_meta`
  * `Strip.parent_meta`

| 

  * `Strip.split`
  * `Strip.swap`
  * [[StripModifier.input_mask_strip]]
  * [[StripsMeta.new_clip]]
  * [[StripsMeta.new_effect]]
  * [[StripsMeta.new_effect]]
  * [[StripsMeta.new_effect]]
  * [[StripsMeta.new_image]]
  * [[StripsMeta.new_mask]]
  * [[StripsMeta.new_meta]]
  * [[StripsMeta.new_movie]]
  * [[StripsMeta.new_scene]]
  * [[StripsMeta.new_sound]]
  * [[StripsMeta.remove]]
  * [[StripsTopLevel.new_clip]]
  * [[StripsTopLevel.new_effect]]
  * [[StripsTopLevel.new_effect]]
  * [[StripsTopLevel.new_effect]]
  * [[StripsTopLevel.new_image]]
  * [[StripsTopLevel.new_mask]]
  * [[StripsTopLevel.new_meta]]
  * [[StripsTopLevel.new_movie]]
  * [[StripsTopLevel.new_scene]]
  * [[StripsTopLevel.new_sound]]
  * [[StripsTopLevel.remove]]
  * [[SubtractStrip.input_1]]
  * [[SubtractStrip.input_2]]
  * [[WipeStrip.input_1]]
  * [[WipeStrip.input_2]]

  
---|---
  *[*]: Keyword-only parameters separator (PEP 3102)
  *[/]: Positional-only parameter separator (PEP 570)
