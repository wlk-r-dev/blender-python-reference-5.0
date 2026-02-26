# VolumeToMeshModifier(Modifier)

base classes — [[bpy_struct]], [[Modifier]]

_class _bpy.types.VolumeToMeshModifier(_Modifier_)
    

adaptivity
    

Reduces the final face count by simplifying geometry where detail is not needed

Type:
    

float in [0, 1], default 0.0

grid_name
    

Grid in the volume object that is converted to a mesh

Type:
    

string, default “”, (never None)

object
    

Object

Type:
    

[[Object]]

resolution_mode
    

Mode for how the desired voxel size is specified

  * `GRID` Grid – Use resolution of the volume grid.

  * `VOXEL_AMOUNT` Voxel Amount – Desired number of voxels along one axis.

  * `VOXEL_SIZE` Voxel Size – Desired voxel side length.


Type:
    

enum in [`'GRID'`, `'VOXEL_AMOUNT'`, `'VOXEL_SIZE'`], default `'GRID'`

threshold
    

Voxels with a larger value are inside the generated mesh

Type:
    

float in [0, inf], default 0.0

use_smooth_shade
    

Output faces with smooth shading rather than flat shaded

Type:
    

boolean, default False

voxel_amount
    

Approximate number of voxels along one axis

Type:
    

int in [0, inf], default 0

voxel_size
    

Smaller values result in a higher resolution output

Type:
    

float in [0, inf], default 0.0

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
  * [[Modifier.name]]
  * [[Modifier.type]]
  * [[Modifier.show_viewport]]
  * [[Modifier.show_render]]
  * [[Modifier.show_in_editmode]]
  * [[Modifier.show_on_cage]]

| 

  * [[Modifier.show_expanded]]
  * [[Modifier.is_active]]
  * [[Modifier.use_pin_to_last]]
  * [[Modifier.is_override_data]]
  * [[Modifier.use_apply_on_spline]]
  * [[Modifier.execution_time]]
  * [[Modifier.persistent_uid]]

  
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

| 

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
  * [[Modifier.bl_rna_get_subclass]]
  * [[Modifier.bl_rna_get_subclass_py]]

  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
