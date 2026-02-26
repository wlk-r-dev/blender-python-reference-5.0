# SoundStrip(Strip)

base classes — [[bpy_struct]], [[Strip]]

_class _bpy.types.SoundStrip(_Strip_)
    

Sequence strip defining a sound to be played over a period of time

animation_offset_end
    

Animation end offset (trim end)

Type:
    

int in [0, inf], default 0

animation_offset_start
    

Animation start offset (trim start)

Type:
    

int in [0, inf], default 0

pan
    

Playback panning of the sound (only for Mono sources)

Type:
    

float in [-inf, inf], default 0.0

pitch_correction
    

Maintain the original pitch of the audio when changing playback speed

Type:
    

boolean, default False

retiming_keys
    

Type:
    

[[RetimingKeys]] [[bpy_prop_collection]] of [[RetimingKey]], (readonly)

show_waveform
    

Display the audio waveform inside the strip

Type:
    

boolean, default False

sound
    

Sound data-block used by this strip

Type:
    

[[Sound]]

sound_offset
    

Offset of the sound from the beginning of the strip, expressed in seconds

Type:
    

float in [-inf, inf], default 0.0

volume
    

Playback volume of the sound

Type:
    

float in [0, 100], default 1.0

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
  * [[Strip.name]]
  * [[Strip.type]]
  * [[Strip.select]]
  * [[Strip.select_left_handle]]
  * [[Strip.select_right_handle]]
  * [[Strip.mute]]
  * [[Strip.lock]]
  * [[Strip.frame_final_duration]]
  * [[Strip.frame_duration]]
  * [[Strip.frame_start]]
  * [[Strip.frame_final_start]]

| 

  * [[Strip.frame_final_end]]
  * [[Strip.frame_offset_start]]
  * [[Strip.frame_offset_end]]
  * [[Strip.channel]]
  * [[Strip.use_linear_modifiers]]
  * [[Strip.blend_type]]
  * [[Strip.blend_alpha]]
  * [[Strip.effect_fader]]
  * [[Strip.use_default_fade]]
  * [[Strip.color_tag]]
  * [[Strip.modifiers]]
  * [[Strip.show_retiming_keys]]

  
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
  * [[bpy_struct.keyframe_insert]]
  * [[bpy_struct.keys]]
  * [[bpy_struct.path_from_id]]
  * [[bpy_struct.path_from_module]]

| 

  * [[bpy_struct.path_resolve]]
  * [[bpy_struct.pop]]
  * [[bpy_struct.property_overridable_library_set]]
  * [[bpy_struct.property_unset]]
  * [[bpy_struct.rna_ancestors]]
  * [[bpy_struct.type_recast]]
  * [[bpy_struct.values]]
  * [[Strip.bl_system_properties_get]]
  * [[Strip.strip_elem_from_frame]]
  * [[Strip.swap]]
  * [[Strip.move_to_meta]]
  * [[Strip.parent_meta]]
  * [[Strip.invalidate_cache]]
  * [[Strip.split]]
  * [[Strip.bl_rna_get_subclass]]
  * [[Strip.bl_rna_get_subclass_py]]

  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
