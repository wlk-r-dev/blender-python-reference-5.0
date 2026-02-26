# CopyTransformsConstraint(Constraint)

base classes — [[bpy_struct]], [[Constraint]]

_class _bpy.types.CopyTransformsConstraint(_Constraint_)
    

Copy all the transforms of the target

head_tail
    

Target along length of bone: Head is 0, Tail is 1

Type:
    

float in [0, 1], default 0.0

mix_mode
    

Specify how the copied and existing transformations are combined

  * `REPLACE` Replace – Replace the original transformation with copied.

  * `BEFORE_FULL` Before Original (Full) – Apply copied transformation before original, using simple matrix multiplication as if the constraint target is a parent in Full Inherit Scale mode. Will create shear when combining rotation and non-uniform scale..

  * `BEFORE` Before Original (Aligned) – Apply copied transformation before original, as if the constraint target is a parent in Aligned Inherit Scale mode. This effectively uses Full for location and Split Channels for rotation and scale..

  * `BEFORE_SPLIT` Before Original (Split Channels) – Apply copied transformation before original, handling location, rotation and scale separately, similar to a sequence of three Copy constraints.

  * `AFTER_FULL` After Original (Full) – Apply copied transformation after original, using simple matrix multiplication as if the constraint target is a child in Full Inherit Scale mode. Will create shear when combining rotation and non-uniform scale..

  * `AFTER` After Original (Aligned) – Apply copied transformation after original, as if the constraint target is a child in Aligned Inherit Scale mode. This effectively uses Full for location and Split Channels for rotation and scale..

  * `AFTER_SPLIT` After Original (Split Channels) – Apply copied transformation after original, handling location, rotation and scale separately, similar to a sequence of three Copy constraints.


Type:
    

enum in [`'REPLACE'`, `'BEFORE_FULL'`, `'BEFORE'`, `'BEFORE_SPLIT'`, `'AFTER_FULL'`, `'AFTER'`, `'AFTER_SPLIT'`], default `'REPLACE'`

remove_target_shear
    

Remove shear from the target transformation before combining

Type:
    

boolean, default False

subtarget
    

Armature bone, mesh or lattice vertex group, …

Type:
    

string, default “”, (never None)

target
    

Target object

Type:
    

[[Object]]

use_bbone_shape
    

Follow shape of B-Bone segments when calculating Head/Tail position

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
  * [[Constraint.name]]
  * [[Constraint.type]]
  * [[Constraint.is_override_data]]
  * [[Constraint.owner_space]]
  * [[Constraint.target_space]]
  * [[Constraint.space_object]]
  * [[Constraint.space_subtarget]]

| 

  * [[Constraint.mute]]
  * [[Constraint.enabled]]
  * [[Constraint.show_expanded]]
  * [[Constraint.is_valid]]
  * [[Constraint.active]]
  * [[Constraint.influence]]
  * [[Constraint.error_location]]
  * [[Constraint.error_rotation]]

  
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
  * [[Constraint.bl_rna_get_subclass]]
  * [[Constraint.bl_rna_get_subclass_py]]

  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
