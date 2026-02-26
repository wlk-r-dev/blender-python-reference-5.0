# VolumeGrid(bpy_struct)

base class — [[bpy_struct]]

_class _bpy.types.VolumeGrid(_bpy_struct_)
    

3D volume grid

channels
    

Number of dimensions of the grid data type

Type:
    

int in [0, inf], default 0, (readonly)

data_type
    

Data type of voxel values

Type:
    

enum in [Volume Grid Data Type Items](../../bpy_types_enum_items/volume_grid_data_type_items.md#rna-enum-volume-grid-data-type-items), default `'UNKNOWN'`, (readonly)

is_loaded
    

Grid tree is loaded in memory

Type:
    

boolean, default False, (readonly)

matrix_object
    

Transformation matrix from voxel index to object space

Type:
    

[[mathutils.Matrix]] of 4 * 4 items in [-inf, inf], default ((0.0, 0.0, 0.0, 0.0), (0.0, 0.0, 0.0, 0.0), (0.0, 0.0, 0.0, 0.0), (0.0, 0.0, 0.0, 0.0)), (readonly)

name
    

Volume grid name

Type:
    

string, default “”, (readonly, never None)

load()
    

Load grid tree from file

Returns:
    

True if grid tree was successfully loaded

Return type:
    

boolean

unload()
    

Unload grid tree and voxel data from memory, leaving only metadata

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

  * [[Volume.grids]]

| 


  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
