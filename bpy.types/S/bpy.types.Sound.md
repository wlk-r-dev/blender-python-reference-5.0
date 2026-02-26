# Sound(ID)

base classes — [[bpy_struct]], [[ID]]

_class _bpy.types.Sound(_ID_)
    

Sound data-block referencing an external or packed sound file

channels
    

Definition of audio channels

  * `INVALID` Invalid – Invalid.

  * `MONO` Mono – Mono.

  * `STEREO` Stereo – Stereo.

  * `STEREO_LFE` Stereo LFE – Stereo FX.

  * `CHANNELS_4` 4 Channels – 4 Channels.

  * `CHANNELS_5` 5 Channels – 5 Channels.

  * `SURROUND_51` 5.1 Surround – 5.1 Surround.

  * `SURROUND_61` 6.1 Surround – 6.1 Surround.

  * `SURROUND_71` 7.1 Surround – 7.1 Surround.


Type:
    

enum in [`'INVALID'`, `'MONO'`, `'STEREO'`, `'STEREO_LFE'`, `'CHANNELS_4'`, `'CHANNELS_5'`, `'SURROUND_51'`, `'SURROUND_61'`, `'SURROUND_71'`], default `'INVALID'`, (readonly)

filepath
    

Sound sample file used by this Sound data-block

Type:
    

string, default “”, (never None, blend relative `//` prefix supported)

packed_file
    

Type:
    

[[PackedFile]], (readonly)

samplerate
    

Sample rate of the audio in Hz

Type:
    

int in [-inf, inf], default 0, (readonly)

use_memory_cache
    

The sound file is decoded and loaded into RAM

Type:
    

boolean, default False

use_mono
    

If the file contains multiple audio channels they are rendered to a single one

Type:
    

boolean, default False

factory
    

The aud.Factory object of the sound.

(readonly)

pack()
    

Pack the sound into the current blend file

unpack(_*_ , _method ='USE_LOCAL'_)
    

Unpack the sound to the samples filename

Parameters:
    

**method** (enum in [Unpack Method Items](../../bpy_types_enum_items/unpack_method_items.md#rna-enum-unpack-method-items), (optional)) – method, How to unpack

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
  * [[ID.name]]
  * [[ID.name_full]]
  * [[ID.id_type]]
  * [[ID.session_uid]]
  * [[ID.is_evaluated]]
  * [[ID.original]]
  * [[ID.users]]
  * [[ID.use_fake_user]]
  * [[ID.use_extra_user]]
  * [[ID.is_embedded_data]]

| 

  * [[ID.is_linked_packed]]
  * [[ID.is_missing]]
  * [[ID.is_runtime_data]]
  * [[ID.is_editable]]
  * [[ID.tag]]
  * [[ID.is_library_indirect]]
  * [[ID.library]]
  * [[ID.library_weak_reference]]
  * [[ID.asset_data]]
  * [[ID.override_library]]
  * [[ID.preview]]

  
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
  * [[bpy_struct.path_resolve]]
  * [[bpy_struct.pop]]
  * [[bpy_struct.property_overridable_library_set]]
  * [[bpy_struct.property_unset]]
  * [[bpy_struct.rna_ancestors]]

| 

  * [[bpy_struct.type_recast]]
  * [[bpy_struct.values]]
  * [[ID.bl_system_properties_get]]
  * [[ID.rename]]
  * [[ID.evaluated_get]]
  * [[ID.copy]]
  * [[ID.asset_mark]]
  * [[ID.asset_clear]]
  * [[ID.asset_generate_preview]]
  * [[ID.override_create]]
  * [[ID.override_hierarchy_create]]
  * [[ID.user_clear]]
  * [[ID.user_remap]]
  * [[ID.make_local]]
  * [[ID.user_of_id]]
  * [[ID.animation_data_create]]
  * [[ID.animation_data_clear]]
  * [[ID.update_tag]]
  * [[ID.preview_ensure]]
  * [[ID.bl_rna_get_subclass]]
  * [[ID.bl_rna_get_subclass_py]]

  
---|---  
  
## References

  * [[BlendData.sounds]]
  * [[BlendDataSounds.load]]
  * [[BlendDataSounds.remove]]

| 

  * [[SoundStrip.sound]]
  * [[Speaker.sound]]

  
---|---
  *[*]: Keyword-only parameters separator (PEP 3102)
  *[/]: Positional-only parameter separator (PEP 570)
