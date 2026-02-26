# GeometryAttributeConstraint(Constraint)

base classes — [[bpy_struct]], [[Constraint]]

_class _bpy.types.GeometryAttributeConstraint(_Constraint_)
    

Create a constraint-based relationship with an attribute from geometry

apply_target_transform
    

Apply the target object’s world transform on top of the attribute’s transform

Type:
    

boolean, default False

attribute_name
    

Name of the attribute to retrieve the transform from

Type:
    

string, default “”, (never None)

data_type
    

Select data type of attribute

  * `VECTOR` Vector – Vector data type, affects position.

  * `QUATERNION` Quaternion – Quaternion data type, affects rotation.

  * `FLOAT4X4` 4x4 Matrix – 4x4 Matrix data type, affects transform.


Type:
    

enum in [`'VECTOR'`, `'QUATERNION'`, `'FLOAT4X4'`], default `'VECTOR'`

domain
    

Attribute domain

Type:
    

enum in [`'POINT'`, `'EDGE'`, `'FACE'`, `'FACE_CORNER'`, `'CURVE'`, `'INSTANCE'`], default `'POINT'`

mix_loc
    

Mix Location

Type:
    

boolean, default False

mix_mode
    

Specify how the copied and existing transformations are combined

  * `REPLACE` Replace – Replace the original transformation with the transform from the attribute.

  * `BEFORE_FULL` Before Original (Full) – Apply copied transformation before original, using simple matrix multiplication as if the constraint target is a parent in Full Inherit Scale mode. Will create shear when combining rotation and non-uniform scale..

  * `BEFORE_SPLIT` Before Original (Split Channels) – Apply copied transformation before original, handling location, rotation and scale separately, similar to a sequence of three Copy constraints.

  * `AFTER_FULL` After Original (Full) – Apply copied transformation after original, using simple matrix multiplication as if the constraint target is a child in Full Inherit Scale mode. Will create shear when combining rotation and non-uniform scale..

  * `AFTER_SPLIT` After Original (Split Channels) – Apply copied transformation after original, handling location, rotation and scale separately, similar to a sequence of three Copy constraints.


Type:
    

enum in [`'REPLACE'`, `'BEFORE_FULL'`, `'BEFORE_SPLIT'`, `'AFTER_FULL'`, `'AFTER_SPLIT'`], default `'REPLACE'`

mix_rot
    

Mix Rotation

Type:
    

boolean, default False

mix_scl
    

Mix Scale

Type:
    

boolean, default False

sample_index
    

Sample Index

Type:
    

int in [0, inf], default 0

target
    

Target geometry object

Type:
    

[[Object]]

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
