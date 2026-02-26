# Action(ID)

base classes — [[bpy_struct]], [[ID]]

_class _bpy.types.Action(_ID_)
    

A collection of F-Curves for animation

curve_frame_range
    

The combined frame range of all F-Curves within this action

Type:
    

[[mathutils.Vector]] of 2 items in [-inf, inf], default (0.0, 0.0), (readonly)

frame_end
    

The end frame of the manually set intended playback range

Type:
    

float in [-1.04857e+06, 1.04857e+06], default 0.0

frame_range
    

The intended playback frame range of this action, using the manually set range if available, or the combined frame range of all F-Curves within this action if not (assigning sets the manual frame range)

Type:
    

[[mathutils.Vector]] of 2 items in [-inf, inf], default (0.0, 0.0)

frame_start
    

The start frame of the manually set intended playback range

Type:
    

float in [-1.04857e+06, 1.04857e+06], default 0.0

is_action_layered
    

Return whether this is a layered Action. An empty Action is considered as both a ‘legacy’ and a ‘layered’ Action.

Type:
    

boolean, default False, (readonly)

is_action_legacy
    

Return whether this is a legacy Action. Legacy Actions have no layers or slots. An empty Action is considered as both a ‘legacy’ and a ‘layered’ Action. Since Blender 4.4 actions are automatically updated to layered actions, and thus this will only return True when the action is empty

Type:
    

boolean, default False, (readonly)

is_empty
    

False when there is any Layer, Slot, or legacy F-Curve

Type:
    

boolean, default False, (readonly)

layers
    

The list of layers that make up this Action

Type:
    

[[ActionLayers]] [[bpy_prop_collection]] of [[ActionLayer]], (readonly)

pose_markers
    

Markers specific to this action, for labeling poses

Type:
    

[[ActionPoseMarkers]] [[bpy_prop_collection]] of [[TimelineMarker]], (readonly)

slots
    

The list of slots in this Action

Type:
    

[[ActionSlots]] [[bpy_prop_collection]] of [[ActionSlot]], (readonly)

use_cyclic
    

The action is intended to be used as a cycle looping over its manually set playback frame range (enabling this does not automatically make it loop)

Type:
    

boolean, default False

use_frame_range
    

Manually specify the intended playback frame range for the action (this range is used by some tools, but does not affect animation evaluation)

Type:
    

boolean, default False

deselect_keys()
    

Deselects all keys of the Action. The selection status of F-Curves is unchanged.

fcurve_ensure_for_datablock(_datablock_ , _data_path_ , _*_ , _index =0_, _group_name =''_)
    

Ensure that an F-Curve exists, with the given data path and array index, for the given data-block. This action must already be assigned to the data-block. This function will also create the layer, keyframe strip, and action slot if necessary, and take care of assigning the action slot too

Parameters:
    

  * **datablock** ([[ID]], (never None)) – The data-block animated by this action, for which to ensure the F-Curve exists. This action must already be assigned to the data-block

  * **data_path** (_string_ _,__(__never None_ _)_) – Data Path, F-Curve data path

  * **index** (_int in_ _[__0_ _,__inf_ _]__,__(__optional_ _)_) – Index, Array index

  * **group_name** (_string_ _,__(__optional_ _,__never None_ _)_) – Group Name, Name of the group for this F-Curve, if any. If the F-Curve already exists, this parameter is ignored


Returns:
    

The found or created F-Curve

Return type:
    

[[FCurve]]

flip_with_pose(_object_)
    

Flip the action around the X axis using a pose

Parameters:
    

**object** ([[Object]], (never None)) – The reference armature object to use when flipping

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

  * [[bpy.context.active_action]]
  * [[bpy.context.selected_editable_actions]]
  * [[bpy.context.selected_visible_actions]]
  * [[ActionConstraint.action]]
  * [[AnimData.action]]
  * [[AnimData.action_tweak_storage]]
  * [[BlendData.actions]]
  * [[BlendDataActions.new]]

| 

  * [[BlendDataActions.remove]]
  * `GLTF2_filter_action.action`
  * [[NlaStrip.action]]
  * [[NlaStrips.new]]
  * [[Pose.apply_pose_from_action]]
  * [[Pose.backup_create]]
  * [[Pose.blend_pose_from_action]]
  * [[WindowManager.poselib_previous_action]]

  
---|---
  *[*]: Keyword-only parameters separator (PEP 3102)
  *[/]: Positional-only parameter separator (PEP 570)
