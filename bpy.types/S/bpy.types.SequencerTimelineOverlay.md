# SequencerTimelineOverlay(bpy_struct)

base class — [[bpy_struct]]

_class _bpy.types.SequencerTimelineOverlay(_bpy_struct_)
    

show_fcurves
    

Display strip opacity/volume curve

Type:
    

boolean, default False

show_grid
    

Show vertical grid lines

Type:
    

boolean, default False

show_strip_duration
    

Type:
    

boolean, default False

show_strip_name
    

Type:
    

boolean, default False

show_strip_offset
    

Display strip in/out offsets

Type:
    

boolean, default False

show_strip_retiming
    

Display retiming keys on top of strips

Type:
    

boolean, default False

show_strip_source
    

Display path to source file, or name of source data-block

Type:
    

boolean, default False

show_strip_tag_color
    

Display the strip color tags in the sequencer

Type:
    

boolean, default False

show_thumbnails
    

Show strip thumbnails

Type:
    

boolean, default False

waveform_display_style
    

How Waveforms are displayed

  * `FULL_WAVEFORMS` Full – Display full waveform.

  * `HALF_WAVEFORMS` Half – Display upper half of the absolute value waveform.


Type:
    

enum in [`'FULL_WAVEFORMS'`, `'HALF_WAVEFORMS'`], default `'FULL_WAVEFORMS'`

waveform_display_type
    

How Waveforms are displayed

  * `ALL_WAVEFORMS` On – Display waveforms for all sound strips.

  * `DEFAULT_WAVEFORMS` Strip – Display waveforms depending on strip setting.

  * `NO_WAVEFORMS` Off – Don’t display waveforms for any sound strips.


Type:
    

enum in [`'ALL_WAVEFORMS'`, `'DEFAULT_WAVEFORMS'`, `'NO_WAVEFORMS'`], default `'DEFAULT_WAVEFORMS'`

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

  * [[SpaceSequenceEditor.timeline_overlay]]

| 


  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
