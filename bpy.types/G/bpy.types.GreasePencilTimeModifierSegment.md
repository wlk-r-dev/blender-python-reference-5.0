# GreasePencilTimeModifierSegment(bpy_struct)

base class — [[bpy_struct]]

_class _bpy.types.GreasePencilTimeModifierSegment(_bpy_struct_)
    

Configuration for a single dash segment

name
    

Name of the dash segment

Type:
    

string, default “”, (never None)

segment_end
    

Last frame of the segment

Type:
    

int in [0, 32767], default 2

segment_mode
    

  * `NORMAL` Regular – Apply offset in usual animation direction.

  * `REVERSE` Reverse – Apply offset in reverse animation direction.

  * `PINGPONG` Ping Pong – Loop back and forth.


Type:
    

enum in [`'NORMAL'`, `'REVERSE'`, `'PINGPONG'`], default `'NORMAL'`

segment_repeat
    

Number of cycle repeats

Type:
    

int in [1, 32767], default 1

segment_start
    

First frame of the segment

Type:
    

int in [0, 32767], default 1

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

  * [[GreasePencilTimeModifier.segments]]

| 


  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
