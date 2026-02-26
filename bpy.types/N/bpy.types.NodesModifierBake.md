# NodesModifierBake(bpy_struct)

base class — [[bpy_struct]]

_class _bpy.types.NodesModifierBake(_bpy_struct_)
    

bake_id
    

Identifier for this bake which remains unchanged even when the bake node is renamed, grouped or ungrouped

Type:
    

int in [-inf, inf], default 0, (readonly)

bake_mode
    

  * `ANIMATION` Animation – Bake a frame range.

  * `STILL` Still – Bake a single frame.


Type:
    

enum in [`'ANIMATION'`, `'STILL'`], default `'ANIMATION'`

bake_target
    

Where to store the baked data

  * `INHERIT` Inherit from Modifier – Use setting from the modifier.

  * `PACKED` Packed – Pack the baked data into the .blend file.

  * `DISK` Disk – Store the baked data in a directory on disk.


Type:
    

enum in [`'INHERIT'`, `'PACKED'`, `'DISK'`], default `'INHERIT'`

data_blocks
    

Type:
    

[[NodesModifierBakeDataBlocks]] [[bpy_prop_collection]] of [[NodesModifierDataBlock]], (readonly)

directory
    

Location on disk where the bake data is stored

Type:
    

string, default “”, (never None, blend relative `//` prefix supported)

frame_end
    

Frame where the baking ends

Type:
    

int in [-inf, inf], default 0

frame_start
    

Frame where the baking starts

Type:
    

int in [-inf, inf], default 0

node
    

Bake node or simulation output node that corresponds to this bake. This node may be deeply nested in the modifier node group. It can be none in some cases like missing linked data blocks.

Type:
    

[[Node]], (readonly)

use_custom_path
    

Specify a path where the baked data should be stored manually

Type:
    

boolean, default False

use_custom_simulation_frame_range
    

Override the simulation frame range from the scene

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

  * [[NodesModifier.bakes]]

| 


  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
