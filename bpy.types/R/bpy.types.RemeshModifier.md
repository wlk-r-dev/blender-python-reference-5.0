# RemeshModifier(Modifier)

base classes — [[bpy_struct]], [[Modifier]]

_class _bpy.types.RemeshModifier(_Modifier_)
    

Generate a new surface with regular topology that follows the shape of the input mesh

adaptivity
    

Reduces the final face count by simplifying geometry where detail is not needed, generating triangles. A value greater than 0 disables Fix Poles.

Type:
    

float in [-inf, inf], default 0.0

mode
    

  * `BLOCKS` Blocks – Output a blocky surface with no smoothing.

  * `SMOOTH` Smooth – Output a smooth surface with no sharp-features detection.

  * `SHARP` Sharp – Output a surface that reproduces sharp edges and corners from the input mesh.

  * `VOXEL` Voxel – Output a mesh corresponding to the volume of the original mesh.


Type:
    

enum in [`'BLOCKS'`, `'SMOOTH'`, `'SHARP'`, `'VOXEL'`], default `'VOXEL'`

octree_depth
    

Resolution of the octree; higher values give finer details

Type:
    

int in [1, 24], default 4

scale
    

The ratio of the largest dimension of the model over the size of the grid

Type:
    

float in [0, 0.99], default 0.9

sharpness
    

Tolerance for outliers; lower values filter noise while higher values will reproduce edges closer to the input

Type:
    

float in [-inf, inf], default 1.0

threshold
    

If removing disconnected pieces, minimum size of components to preserve as a ratio of the number of polygons in the largest component

Type:
    

float in [0, 1], default 1.0

use_remove_disconnected
    

Type:
    

boolean, default True

use_smooth_shade
    

Output faces with smooth shading rather than flat shaded

Type:
    

boolean, default False

voxel_size
    

Size of the voxel in object space used for volume evaluation. Lower values preserve finer details.

Type:
    

float in [0, inf], default 0.1

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
