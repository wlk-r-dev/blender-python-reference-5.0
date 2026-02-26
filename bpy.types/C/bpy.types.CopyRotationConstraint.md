# CopyRotationConstraint(Constraint)

base classes — [[bpy_struct]], [[Constraint]]

_class _bpy.types.CopyRotationConstraint(_Constraint_)
    

Copy the rotation of the target

euler_order
    

Explicitly specify the euler rotation order

  * `AUTO` Default – Euler using the default rotation order.

  * `XYZ` XYZ Euler – Euler using the XYZ rotation order.

  * `XZY` XZY Euler – Euler using the XZY rotation order.

  * `YXZ` YXZ Euler – Euler using the YXZ rotation order.

  * `YZX` YZX Euler – Euler using the YZX rotation order.

  * `ZXY` ZXY Euler – Euler using the ZXY rotation order.

  * `ZYX` ZYX Euler – Euler using the ZYX rotation order.


Type:
    

enum in [`'AUTO'`, `'XYZ'`, `'XZY'`, `'YXZ'`, `'YZX'`, `'ZXY'`, `'ZYX'`], default `'AUTO'`

invert_x
    

Invert the X rotation

Type:
    

boolean, default False

invert_y
    

Invert the Y rotation

Type:
    

boolean, default False

invert_z
    

Invert the Z rotation

Type:
    

boolean, default False

mix_mode
    

Specify how the copied and existing rotations are combined

  * `REPLACE` Replace – Replace the original rotation with copied.

  * `ADD` Add – Add euler component values together.

  * `BEFORE` Before Original – Apply copied rotation before original, as if the constraint target is a parent.

  * `AFTER` After Original – Apply copied rotation after original, as if the constraint target is a child.

  * `OFFSET` Offset (Legacy) – Combine rotations like the original Offset checkbox. Does not work well for multiple axis rotations..


Type:
    

enum in [`'REPLACE'`, `'ADD'`, `'BEFORE'`, `'AFTER'`, `'OFFSET'`], default `'REPLACE'`

subtarget
    

Armature bone, mesh or lattice vertex group, …

Type:
    

string, default “”, (never None)

target
    

Target object

Type:
    

[[Object]]

use_offset
    

DEPRECATED: Add original rotation into copied rotation

Type:
    

boolean, default False

use_x
    

Copy the target’s X rotation

Type:
    

boolean, default False

use_y
    

Copy the target’s Y rotation

Type:
    

boolean, default False

use_z
    

Copy the target’s Z rotation

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
