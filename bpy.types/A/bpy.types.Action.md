# Action(ID)

base classes — [`bpy_struct`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct "bpy.types.bpy_struct"), [`ID`](../I/bpy.types.ID.md#bpy.types.ID "bpy.types.ID")

_class _bpy.types.Action(_ID_)
    

A collection of F-Curves for animation

curve_frame_range
    

The combined frame range of all F-Curves within this action

Type:
    

[`mathutils.Vector`](mathutils.md#mathutils.Vector "mathutils.Vector") of 2 items in [-inf, inf], default (0.0, 0.0), (readonly)

frame_end
    

The end frame of the manually set intended playback range

Type:
    

float in [-1.04857e+06, 1.04857e+06], default 0.0

frame_range
    

The intended playback frame range of this action, using the manually set range if available, or the combined frame range of all F-Curves within this action if not (assigning sets the manual frame range)

Type:
    

[`mathutils.Vector`](mathutils.md#mathutils.Vector "mathutils.Vector") of 2 items in [-inf, inf], default (0.0, 0.0)

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
    

[`ActionLayers`](bpy.types.ActionLayers.md#bpy.types.ActionLayers "bpy.types.ActionLayers") [`bpy_prop_collection`](../_other/bpy.types.bpy_prop_collection.md#bpy.types.bpy_prop_collection "bpy.types.bpy_prop_collection") of [`ActionLayer`](bpy.types.ActionLayer.md#bpy.types.ActionLayer "bpy.types.ActionLayer"), (readonly)

pose_markers
    

Markers specific to this action, for labeling poses

Type:
    

[`ActionPoseMarkers`](bpy.types.ActionPoseMarkers.md#bpy.types.ActionPoseMarkers "bpy.types.ActionPoseMarkers") [`bpy_prop_collection`](../_other/bpy.types.bpy_prop_collection.md#bpy.types.bpy_prop_collection "bpy.types.bpy_prop_collection") of [`TimelineMarker`](../T/bpy.types.TimelineMarker.md#bpy.types.TimelineMarker "bpy.types.TimelineMarker"), (readonly)

slots
    

The list of slots in this Action

Type:
    

[`ActionSlots`](bpy.types.ActionSlots.md#bpy.types.ActionSlots "bpy.types.ActionSlots") [`bpy_prop_collection`](../_other/bpy.types.bpy_prop_collection.md#bpy.types.bpy_prop_collection "bpy.types.bpy_prop_collection") of [`ActionSlot`](bpy.types.ActionSlot.md#bpy.types.ActionSlot "bpy.types.ActionSlot"), (readonly)

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
    

  * **datablock** ([`ID`](../I/bpy.types.ID.md#bpy.types.ID "bpy.types.ID"), (never None)) – The data-block animated by this action, for which to ensure the F-Curve exists. This action must already be assigned to the data-block

  * **data_path** (_string_ _,__(__never None_ _)_) – Data Path, F-Curve data path

  * **index** (_int in_ _[__0_ _,__inf_ _]__,__(__optional_ _)_) – Index, Array index

  * **group_name** (_string_ _,__(__optional_ _,__never None_ _)_) – Group Name, Name of the group for this F-Curve, if any. If the F-Curve already exists, this parameter is ignored


Returns:
    

The found or created F-Curve

Return type:
    

[`FCurve`](../F/bpy.types.FCurve.md#bpy.types.FCurve "bpy.types.FCurve")

flip_with_pose(_object_)
    

Flip the action around the X axis using a pose

Parameters:
    

**object** ([`Object`](../O/bpy.types.Object.md#bpy.types.Object "bpy.types.Object"), (never None)) – The reference armature object to use when flipping

_classmethod _bl_rna_get_subclass(_id_ , _default =None_, _/_)
    

Parameters:
    

**id** (_str_) – The RNA type identifier.

Returns:
    

The RNA type or default when not found.

Return type:
    

[`bpy.types.Struct`](../S/bpy.types.Struct.md#bpy.types.Struct "bpy.types.Struct") subclass

_classmethod _bl_rna_get_subclass_py(_id_ , _default =None_, _/_)
    

Parameters:
    

**id** (_str_) – The RNA type identifier.

Returns:
    

The class or default when not found.

Return type:
    

type

## Inherited Properties

  * [`bpy_struct.id_data`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.id_data "bpy.types.bpy_struct.id_data")
  * [`ID.name`](../I/bpy.types.ID.md#bpy.types.ID.name "bpy.types.ID.name")
  * [`ID.name_full`](../I/bpy.types.ID.md#bpy.types.ID.name_full "bpy.types.ID.name_full")
  * [`ID.id_type`](../I/bpy.types.ID.md#bpy.types.ID.id_type "bpy.types.ID.id_type")
  * [`ID.session_uid`](../I/bpy.types.ID.md#bpy.types.ID.session_uid "bpy.types.ID.session_uid")
  * [`ID.is_evaluated`](../I/bpy.types.ID.md#bpy.types.ID.is_evaluated "bpy.types.ID.is_evaluated")
  * [`ID.original`](../I/bpy.types.ID.md#bpy.types.ID.original "bpy.types.ID.original")
  * [`ID.users`](../I/bpy.types.ID.md#bpy.types.ID.users "bpy.types.ID.users")
  * [`ID.use_fake_user`](../I/bpy.types.ID.md#bpy.types.ID.use_fake_user "bpy.types.ID.use_fake_user")
  * [`ID.use_extra_user`](../I/bpy.types.ID.md#bpy.types.ID.use_extra_user "bpy.types.ID.use_extra_user")
  * [`ID.is_embedded_data`](../I/bpy.types.ID.md#bpy.types.ID.is_embedded_data "bpy.types.ID.is_embedded_data")

| 

  * [`ID.is_linked_packed`](../I/bpy.types.ID.md#bpy.types.ID.is_linked_packed "bpy.types.ID.is_linked_packed")
  * [`ID.is_missing`](../I/bpy.types.ID.md#bpy.types.ID.is_missing "bpy.types.ID.is_missing")
  * [`ID.is_runtime_data`](../I/bpy.types.ID.md#bpy.types.ID.is_runtime_data "bpy.types.ID.is_runtime_data")
  * [`ID.is_editable`](../I/bpy.types.ID.md#bpy.types.ID.is_editable "bpy.types.ID.is_editable")
  * [`ID.tag`](../I/bpy.types.ID.md#bpy.types.ID.tag "bpy.types.ID.tag")
  * [`ID.is_library_indirect`](../I/bpy.types.ID.md#bpy.types.ID.is_library_indirect "bpy.types.ID.is_library_indirect")
  * [`ID.library`](../I/bpy.types.ID.md#bpy.types.ID.library "bpy.types.ID.library")
  * [`ID.library_weak_reference`](../I/bpy.types.ID.md#bpy.types.ID.library_weak_reference "bpy.types.ID.library_weak_reference")
  * [`ID.asset_data`](../I/bpy.types.ID.md#bpy.types.ID.asset_data "bpy.types.ID.asset_data")
  * [`ID.override_library`](../I/bpy.types.ID.md#bpy.types.ID.override_library "bpy.types.ID.override_library")
  * [`ID.preview`](../I/bpy.types.ID.md#bpy.types.ID.preview "bpy.types.ID.preview")

  
---|---  
  
## Inherited Functions

  * [`bpy_struct.as_pointer`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.as_pointer "bpy.types.bpy_struct.as_pointer")
  * [`bpy_struct.driver_add`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.driver_add "bpy.types.bpy_struct.driver_add")
  * [`bpy_struct.driver_remove`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.driver_remove "bpy.types.bpy_struct.driver_remove")
  * [`bpy_struct.get`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.get "bpy.types.bpy_struct.get")
  * [`bpy_struct.id_properties_clear`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.id_properties_clear "bpy.types.bpy_struct.id_properties_clear")
  * [`bpy_struct.id_properties_ensure`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.id_properties_ensure "bpy.types.bpy_struct.id_properties_ensure")
  * [`bpy_struct.id_properties_ui`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.id_properties_ui "bpy.types.bpy_struct.id_properties_ui")
  * [`bpy_struct.is_property_hidden`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.is_property_hidden "bpy.types.bpy_struct.is_property_hidden")
  * [`bpy_struct.is_property_overridable_library`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.is_property_overridable_library "bpy.types.bpy_struct.is_property_overridable_library")
  * [`bpy_struct.is_property_readonly`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.is_property_readonly "bpy.types.bpy_struct.is_property_readonly")
  * [`bpy_struct.is_property_set`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.is_property_set "bpy.types.bpy_struct.is_property_set")
  * [`bpy_struct.items`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.items "bpy.types.bpy_struct.items")
  * [`bpy_struct.keyframe_delete`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.keyframe_delete "bpy.types.bpy_struct.keyframe_delete")
  * [`bpy_struct.keyframe_insert`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.keyframe_insert "bpy.types.bpy_struct.keyframe_insert")
  * [`bpy_struct.keys`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.keys "bpy.types.bpy_struct.keys")
  * [`bpy_struct.path_from_id`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.path_from_id "bpy.types.bpy_struct.path_from_id")
  * [`bpy_struct.path_from_module`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.path_from_module "bpy.types.bpy_struct.path_from_module")
  * [`bpy_struct.path_resolve`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.path_resolve "bpy.types.bpy_struct.path_resolve")
  * [`bpy_struct.pop`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.pop "bpy.types.bpy_struct.pop")
  * [`bpy_struct.property_overridable_library_set`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.property_overridable_library_set "bpy.types.bpy_struct.property_overridable_library_set")
  * [`bpy_struct.property_unset`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.property_unset "bpy.types.bpy_struct.property_unset")
  * [`bpy_struct.rna_ancestors`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.rna_ancestors "bpy.types.bpy_struct.rna_ancestors")

| 

  * [`bpy_struct.type_recast`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.type_recast "bpy.types.bpy_struct.type_recast")
  * [`bpy_struct.values`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.values "bpy.types.bpy_struct.values")
  * [`ID.bl_system_properties_get`](../I/bpy.types.ID.md#bpy.types.ID.bl_system_properties_get "bpy.types.ID.bl_system_properties_get")
  * [`ID.rename`](../I/bpy.types.ID.md#bpy.types.ID.rename "bpy.types.ID.rename")
  * [`ID.evaluated_get`](../I/bpy.types.ID.md#bpy.types.ID.evaluated_get "bpy.types.ID.evaluated_get")
  * [`ID.copy`](../I/bpy.types.ID.md#bpy.types.ID.copy "bpy.types.ID.copy")
  * [`ID.asset_mark`](../I/bpy.types.ID.md#bpy.types.ID.asset_mark "bpy.types.ID.asset_mark")
  * [`ID.asset_clear`](../I/bpy.types.ID.md#bpy.types.ID.asset_clear "bpy.types.ID.asset_clear")
  * [`ID.asset_generate_preview`](../I/bpy.types.ID.md#bpy.types.ID.asset_generate_preview "bpy.types.ID.asset_generate_preview")
  * [`ID.override_create`](../I/bpy.types.ID.md#bpy.types.ID.override_create "bpy.types.ID.override_create")
  * [`ID.override_hierarchy_create`](../I/bpy.types.ID.md#bpy.types.ID.override_hierarchy_create "bpy.types.ID.override_hierarchy_create")
  * [`ID.user_clear`](../I/bpy.types.ID.md#bpy.types.ID.user_clear "bpy.types.ID.user_clear")
  * [`ID.user_remap`](../I/bpy.types.ID.md#bpy.types.ID.user_remap "bpy.types.ID.user_remap")
  * [`ID.make_local`](../I/bpy.types.ID.md#bpy.types.ID.make_local "bpy.types.ID.make_local")
  * [`ID.user_of_id`](../I/bpy.types.ID.md#bpy.types.ID.user_of_id "bpy.types.ID.user_of_id")
  * [`ID.animation_data_create`](../I/bpy.types.ID.md#bpy.types.ID.animation_data_create "bpy.types.ID.animation_data_create")
  * [`ID.animation_data_clear`](../I/bpy.types.ID.md#bpy.types.ID.animation_data_clear "bpy.types.ID.animation_data_clear")
  * [`ID.update_tag`](../I/bpy.types.ID.md#bpy.types.ID.update_tag "bpy.types.ID.update_tag")
  * [`ID.preview_ensure`](../I/bpy.types.ID.md#bpy.types.ID.preview_ensure "bpy.types.ID.preview_ensure")
  * [`ID.bl_rna_get_subclass`](../I/bpy.types.ID.md#bpy.types.ID.bl_rna_get_subclass "bpy.types.ID.bl_rna_get_subclass")
  * [`ID.bl_rna_get_subclass_py`](../I/bpy.types.ID.md#bpy.types.ID.bl_rna_get_subclass_py "bpy.types.ID.bl_rna_get_subclass_py")

  
---|---  
  
## References

  * [`bpy.context.active_action`](../../bpy.context.md#bpy.context.active_action "bpy.context.active_action")
  * [`bpy.context.selected_editable_actions`](../../bpy.context.md#bpy.context.selected_editable_actions "bpy.context.selected_editable_actions")
  * [`bpy.context.selected_visible_actions`](../../bpy.context.md#bpy.context.selected_visible_actions "bpy.context.selected_visible_actions")
  * [`ActionConstraint.action`](bpy.types.ActionConstraint.md#bpy.types.ActionConstraint.action "bpy.types.ActionConstraint.action")
  * [`AnimData.action`](bpy.types.AnimData.md#bpy.types.AnimData.action "bpy.types.AnimData.action")
  * [`AnimData.action_tweak_storage`](bpy.types.AnimData.md#bpy.types.AnimData.action_tweak_storage "bpy.types.AnimData.action_tweak_storage")
  * [`BlendData.actions`](../B/bpy.types.BlendData.md#bpy.types.BlendData.actions "bpy.types.BlendData.actions")
  * [`BlendDataActions.new`](../B/bpy.types.BlendDataActions.md#bpy.types.BlendDataActions.new "bpy.types.BlendDataActions.new")

| 

  * [`BlendDataActions.remove`](../B/bpy.types.BlendDataActions.md#bpy.types.BlendDataActions.remove "bpy.types.BlendDataActions.remove")
  * `GLTF2_filter_action.action`
  * [`NlaStrip.action`](../N/bpy.types.NlaStrip.md#bpy.types.NlaStrip.action "bpy.types.NlaStrip.action")
  * [`NlaStrips.new`](../N/bpy.types.NlaStrips.md#bpy.types.NlaStrips.new "bpy.types.NlaStrips.new")
  * [`Pose.apply_pose_from_action`](../P/bpy.types.Pose.md#bpy.types.Pose.apply_pose_from_action "bpy.types.Pose.apply_pose_from_action")
  * [`Pose.backup_create`](../P/bpy.types.Pose.md#bpy.types.Pose.backup_create "bpy.types.Pose.backup_create")
  * [`Pose.blend_pose_from_action`](../P/bpy.types.Pose.md#bpy.types.Pose.blend_pose_from_action "bpy.types.Pose.blend_pose_from_action")
  * [`WindowManager.poselib_previous_action`](../W/bpy.types.WindowManager.md#bpy.types.WindowManager.poselib_previous_action "bpy.types.WindowManager.poselib_previous_action")

  
---|---
  *[*]: Keyword-only parameters separator (PEP 3102)
  *[/]: Positional-only parameter separator (PEP 570)
