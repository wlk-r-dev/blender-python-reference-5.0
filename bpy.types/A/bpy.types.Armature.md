# Armature(ID)

base classes — [[bpy_struct]], [[ID]]

_class _bpy.types.Armature(_ID_)
    

Armature data-block containing a hierarchy of bones, usually used for rigging characters

animation_data
    

Animation data for this data-block

Type:
    

[[AnimData]], (readonly)

axes_position
    

The position for the axes on the bone. Increasing the value moves it closer to the tip; decreasing moves it closer to the root.

Type:
    

float in [0, 1], default 0.0

bones
    

Type:
    

[[ArmatureBones]] [[bpy_prop_collection]] of [[Bone]], (readonly)

collections
    

Type:
    

[[BoneCollections]] [[bpy_prop_collection]] of [[BoneCollection]]

collections_all
    

List of all bone collections of the armature

Type:
    

[[bpy_prop_collection]] of [[BoneCollection]], (readonly)

display_type
    

  * `OCTAHEDRAL` Octahedral – Display bones as octahedral shape (default).

  * `STICK` Stick – Display bones as simple 2D lines with dots.

  * `BBONE` B-Bone – Display bones as boxes, showing subdivision and B-Splines.

  * `ENVELOPE` Envelope – Display bones as extruded spheres, showing deformation influence volume.

  * `WIRE` Wire – Display bones as thin wires, showing subdivision and B-Splines.


Type:
    

enum in [`'OCTAHEDRAL'`, `'STICK'`, `'BBONE'`, `'ENVELOPE'`, `'WIRE'`], default `'OCTAHEDRAL'`

edit_bones
    

Type:
    

[[ArmatureEditBones]] [[bpy_prop_collection]] of [[EditBone]], (readonly)

is_editmode
    

True when used in editmode

Type:
    

boolean, default False, (readonly)

pose_position
    

Show armature in binding pose or final posed state

  * `POSE` Pose Position – Show armature in posed state.

  * `REST` Rest Position – Show Armature in binding pose state (no posing possible).


Type:
    

enum in [`'POSE'`, `'REST'`], default `'POSE'`

relation_line_position
    

The start position of the relation lines from parent to child bones

  * `TAIL` Tail – Draw the relationship line from the parent tail to the child head.

  * `HEAD` Head – Draw the relationship line from the parent head to the child head.


Type:
    

enum in [`'TAIL'`, `'HEAD'`], default `'TAIL'`

show_axes
    

Display bone axes

Type:
    

boolean, default False

show_bone_colors
    

Display bone colors

Type:
    

boolean, default True

show_bone_custom_shapes
    

Display bones with their custom shapes

Type:
    

boolean, default True

show_names
    

Display bone names

Type:
    

boolean, default False

use_mirror_x
    

Apply changes to matching bone on opposite side of X-Axis

Type:
    

boolean, default False

transform(_matrix_)
    

Transform armature bones by a matrix

Parameters:
    

**matrix** ([[mathutils.Matrix]] of 4 * 4 items in [-inf, inf]) – Matrix

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
  * [[ID.name]]
  * [[ID.name_full]]
  * [[ID.id_type]]
  * [[ID.session_uid]]
  * [[ID.is_evaluated]]
  * [[ID.original]]
  * [[ID.users]]
  * [[ID.use_fake_user]]
  * [[ID.use_extra_user]]
  * [[ID.is_embedded_data]]

| 

  * [[ID.is_linked_packed]]
  * [[ID.is_missing]]
  * [[ID.is_runtime_data]]
  * [[ID.is_editable]]
  * [[ID.tag]]
  * [[ID.is_library_indirect]]
  * [[ID.library]]
  * [[ID.library_weak_reference]]
  * [[ID.asset_data]]
  * [[ID.override_library]]
  * [[ID.preview]]

  
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
  * [[bpy_struct.keyframe_insert]]
  * [[bpy_struct.keys]]
  * [[bpy_struct.path_from_id]]
  * [[bpy_struct.path_from_module]]
  * [[bpy_struct.path_resolve]]
  * [[bpy_struct.pop]]
  * [[bpy_struct.property_overridable_library_set]]
  * [[bpy_struct.property_unset]]
  * [[bpy_struct.rna_ancestors]]

| 

  * [[bpy_struct.type_recast]]
  * [[bpy_struct.values]]
  * [[ID.bl_system_properties_get]]
  * [[ID.rename]]
  * [[ID.evaluated_get]]
  * [[ID.copy]]
  * [[ID.asset_mark]]
  * [[ID.asset_clear]]
  * [[ID.asset_generate_preview]]
  * [[ID.override_create]]
  * [[ID.override_hierarchy_create]]
  * [[ID.user_clear]]
  * [[ID.user_remap]]
  * [[ID.make_local]]
  * [[ID.user_of_id]]
  * [[ID.animation_data_create]]
  * [[ID.animation_data_clear]]
  * [[ID.update_tag]]
  * [[ID.preview_ensure]]
  * [[ID.bl_rna_get_subclass]]
  * [[ID.bl_rna_get_subclass_py]]

  
---|---  
  
## References

  * [[bpy.context.armature]]
  * [[BlendData.armatures]]

| 

  * [[BlendDataArmatures.new]]
  * [[BlendDataArmatures.remove]]

  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
