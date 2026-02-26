# GreasePencilFrame(bpy_struct)

base class — [[bpy_struct]]

_class _bpy.types.GreasePencilFrame(_bpy_struct_)
    

A Grease Pencil keyframe

drawing
    

A Grease Pencil drawing

Type:
    

[[GreasePencilDrawing]]

frame_number
    

The frame number in the scene

Type:
    

int in [-1048574, 1048574], default 0, (readonly)

keyframe_type
    

Type of keyframe

  * `KEYFRAME` Keyframe – Normal keyframe, e.g. for key poses.

  * `BREAKDOWN` Breakdown – A breakdown pose, e.g. for transitions between key poses.

  * `MOVING_HOLD` Moving Hold – A keyframe that is part of a moving hold.

  * `EXTREME` Extreme – An ‘extreme’ pose, or some other purpose as needed.

  * `JITTER` Jitter – A filler or baked keyframe for keying on ones, or some other purpose as needed.

  * `GENERATED` Generated – A key generated automatically by a tool, not manually created.


Type:
    

enum in [`'KEYFRAME'`, `'BREAKDOWN'`, `'MOVING_HOLD'`, `'EXTREME'`, `'JITTER'`, `'GENERATED'`], default `'KEYFRAME'`

select
    

Frame Selection in the Dope Sheet

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

  * [[GreasePencilFrames.copy]]
  * [[GreasePencilFrames.move]]
  * [[GreasePencilFrames.new]]

| 

  * [[GreasePencilLayer.current_frame]]
  * [[GreasePencilLayer.frames]]
  * [[GreasePencilLayer.get_frame_at]]

  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
