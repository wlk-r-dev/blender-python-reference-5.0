# Poselib Operators

bpy.ops.poselib.apply_pose_asset(_*_ , _asset_library_type ='LOCAL'_, _asset_library_identifier =''_, _relative_asset_identifier =''_, _blend_factor =1.0_, _flipped =False_)
    

Apply the given Pose Action to the rig

Parameters:
    

  * **asset_library_type** (enum in [Asset Library Type Items](../bpy_types_enum_items/asset_library_type_items.md#rna-enum-asset-library-type-items), (optional)) – Asset Library Type

  * **asset_library_identifier** (_string_ _,__(__optional_ _,__never None_ _)_) – Asset Library Identifier

  * **relative_asset_identifier** (_string_ _,__(__optional_ _,__never None_ _)_) – Relative Asset Identifier

  * **blend_factor** (_float in_ _[__-inf_ _,__inf_ _]__,__(__optional_ _)_) – Blend Factor, Amount that the pose is applied on top of the existing poses. A negative value will subtract the pose instead of adding it

  * **flipped** (_boolean_ _,__(__optional_ _)_) – Apply Flipped, When enabled, applies the pose flipped over the X-axis


bpy.ops.poselib.asset_delete()
    

Delete the selected Pose Asset

bpy.ops.poselib.asset_modify(_*_ , _mode ='ADJUST'_)
    

Update the selected pose asset in the asset library from the currently selected bones. The mode defines how the asset is updated

Parameters:
    

**mode** (enum in [`'ADJUST'`, `'REPLACE'`, `'ADD'`, `'REMOVE'`], (optional)) – 

Overwrite Mode, Specify which parts of the pose asset are overwritten

  * `ADJUST` Adjust – Update existing channels in the pose asset but don’t remove or add any channels.

  * `REPLACE` Replace with Selection – Completely replace all channels in the pose asset with the current selection.

  * `ADD` Add Selected Bones – Add channels of the selection to the pose asset. Existing channels will be updated.

  * `REMOVE` Remove Selected Bones – Remove channels of the selection from the pose asset.


bpy.ops.poselib.blend_pose_asset(_*_ , _asset_library_type ='LOCAL'_, _asset_library_identifier =''_, _relative_asset_identifier =''_, _blend_factor =0.0_, _flipped =False_, _release_confirm =False_)
    

Blend the given Pose Action to the rig

Parameters:
    

  * **asset_library_type** (enum in [Asset Library Type Items](../bpy_types_enum_items/asset_library_type_items.md#rna-enum-asset-library-type-items), (optional)) – Asset Library Type

  * **asset_library_identifier** (_string_ _,__(__optional_ _,__never None_ _)_) – Asset Library Identifier

  * **relative_asset_identifier** (_string_ _,__(__optional_ _,__never None_ _)_) – Relative Asset Identifier

  * **blend_factor** (_float in_ _[__-inf_ _,__inf_ _]__,__(__optional_ _)_) – Blend Factor, Amount that the pose is applied on top of the existing poses. A negative value will subtract the pose instead of adding it

  * **flipped** (_boolean_ _,__(__optional_ _)_) – Apply Flipped, When enabled, applies the pose flipped over the X-axis

  * **release_confirm** (_boolean_ _,__(__optional_ _)_) – Confirm on Release, Always confirm operation when releasing button


bpy.ops.poselib.copy_as_asset()
    

Create a new pose asset on the clipboard, to be pasted into an Asset Browser

File:
    

[addons_core/pose_library/operators.py:116](https://projects.blender.org/blender/blender/src/branch/main/scripts/addons_core/pose_library/operators.py#L116)

bpy.ops.poselib.create_pose_asset(_*_ , _pose_name =''_, _asset_library_reference =''_, _catalog_path =''_)
    

Create a new asset from the selected bones in the scene

Parameters:
    

  * **pose_name** (_string_ _,__(__optional_ _,__never None_ _)_) – Pose Name, Name for the new pose asset

  * **asset_library_reference** (_enum in_ _[__]__,__(__optional_ _)_) – Library, Asset library used to store the new pose

  * **catalog_path** (_string_ _,__(__optional_ _,__never None_ _)_) – Catalog, Catalog to use for the new asset


bpy.ops.poselib.paste_asset()
    

Paste the Asset that was previously copied using Copy As Asset

File:
    

[addons_core/pose_library/operators.py:190](https://projects.blender.org/blender/blender/src/branch/main/scripts/addons_core/pose_library/operators.py#L190)

bpy.ops.poselib.pose_asset_select_bones(_*_ , _select =True_, _flipped =False_)
    

Select those bones that are used in this pose

Parameters:
    

  * **select** (_boolean_ _,__(__optional_ _)_) – Select

  * **flipped** (_boolean_ _,__(__optional_ _)_) – Flipped


File:
    

[addons_core/pose_library/operators.py:228](https://projects.blender.org/blender/blender/src/branch/main/scripts/addons_core/pose_library/operators.py#L228)

bpy.ops.poselib.restore_previous_action()
    

Switch back to the previous Action, after creating a pose asset

File:
    

[addons_core/pose_library/operators.py:65](https://projects.blender.org/blender/blender/src/branch/main/scripts/addons_core/pose_library/operators.py#L65)
  *[*]: Keyword-only parameters separator (PEP 3102)
