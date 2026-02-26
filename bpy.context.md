# Context Access (bpy.context)

The context members available depend on the area of Blender which is currently being accessed.

Note that all context values are read-only, but may be modified through the data API or by running operators.

## Global Context

These properties are available in any contexts.

bpy.context.area
    

Type:
    

[`bpy.types.Area`](bpy.types/A/bpy.types.Area.md#bpy.types.Area "bpy.types.Area"), (readonly)

bpy.context.asset
    

Type:
    

[`bpy.types.AssetRepresentation`](bpy.types/A/bpy.types.AssetRepresentation.md#bpy.types.AssetRepresentation "bpy.types.AssetRepresentation"), (readonly)

bpy.context.blend_data
    

Type:
    

[`bpy.types.BlendData`](bpy.types/B/bpy.types.BlendData.md#bpy.types.BlendData "bpy.types.BlendData"), (readonly)

bpy.context.collection
    

Type:
    

[`bpy.types.Collection`](bpy.types/C/bpy.types.Collection.md#bpy.types.Collection "bpy.types.Collection"), (readonly)

bpy.context.engine
    

Type:
    

string, default “”, (readonly, never None)

bpy.context.gizmo_group
    

Type:
    

[`bpy.types.GizmoGroup`](bpy.types/G/bpy.types.GizmoGroup.md#bpy.types.GizmoGroup "bpy.types.GizmoGroup"), (readonly)

bpy.context.layer_collection
    

Type:
    

[`bpy.types.LayerCollection`](bpy.types/L/bpy.types.LayerCollection.md#bpy.types.LayerCollection "bpy.types.LayerCollection"), (readonly)

bpy.context.mode
    

Type:
    

enum in [Context Mode Items](bpy_types_enum_items/context_mode_items.md#rna-enum-context-mode-items), default `'EDIT_MESH'`, (readonly)

bpy.context.preferences
    

Type:
    

[`bpy.types.Preferences`](bpy.types/P/bpy.types.Preferences.md#bpy.types.Preferences "bpy.types.Preferences"), (readonly)

bpy.context.region
    

Type:
    

[`bpy.types.Region`](bpy.types/R/bpy.types.Region.md#bpy.types.Region "bpy.types.Region"), (readonly)

bpy.context.region_data
    

Type:
    

[`bpy.types.RegionView3D`](bpy.types/R/bpy.types.RegionView3D.md#bpy.types.RegionView3D "bpy.types.RegionView3D"), (readonly)

bpy.context.region_popup
    

The temporary region for pop-ups (including menus and pop-overs)

Type:
    

[`bpy.types.Region`](bpy.types/R/bpy.types.Region.md#bpy.types.Region "bpy.types.Region"), (readonly)

bpy.context.scene
    

Type:
    

[`bpy.types.Scene`](bpy.types/S/bpy.types.Scene.md#bpy.types.Scene "bpy.types.Scene"), (readonly)

bpy.context.screen
    

Type:
    

[`bpy.types.Screen`](bpy.types/S/bpy.types.Screen.md#bpy.types.Screen "bpy.types.Screen"), (readonly)

bpy.context.space_data
    

The current space, may be None in background-mode, when the cursor is outside the window or when using menu-search

Type:
    

[`bpy.types.Space`](bpy.types/S/bpy.types.Space.md#bpy.types.Space "bpy.types.Space"), (readonly)

bpy.context.tool_settings
    

Type:
    

[`bpy.types.ToolSettings`](bpy.types/T/bpy.types.ToolSettings.md#bpy.types.ToolSettings "bpy.types.ToolSettings"), (readonly)

bpy.context.view_layer
    

Type:
    

[`bpy.types.ViewLayer`](bpy.types/V/bpy.types.ViewLayer.md#bpy.types.ViewLayer "bpy.types.ViewLayer"), (readonly)

bpy.context.window
    

Type:
    

[`bpy.types.Window`](bpy.types/W/bpy.types.Window.md#bpy.types.Window "bpy.types.Window"), (readonly)

bpy.context.window_manager
    

Type:
    

[`bpy.types.WindowManager`](bpy.types/W/bpy.types.WindowManager.md#bpy.types.WindowManager "bpy.types.WindowManager"), (readonly)

bpy.context.workspace
    

Type:
    

[`bpy.types.WorkSpace`](bpy.types/W/bpy.types.WorkSpace.md#bpy.types.WorkSpace "bpy.types.WorkSpace"), (readonly)

## Buttons Context

bpy.context.texture_slot
    

Type:
    

[`bpy.types.TextureSlot`](bpy.types/T/bpy.types.TextureSlot.md#bpy.types.TextureSlot "bpy.types.TextureSlot")

bpy.context.scene
    

Type:
    

[`bpy.types.Scene`](bpy.types/S/bpy.types.Scene.md#bpy.types.Scene "bpy.types.Scene")

bpy.context.world
    

Type:
    

[`bpy.types.World`](bpy.types/W/bpy.types.World.md#bpy.types.World "bpy.types.World")

bpy.context.object
    

Type:
    

[`bpy.types.Object`](bpy.types/O/bpy.types.Object.md#bpy.types.Object "bpy.types.Object")

bpy.context.mesh
    

Type:
    

[`bpy.types.Mesh`](bpy.types/M/bpy.types.Mesh.md#bpy.types.Mesh "bpy.types.Mesh")

bpy.context.armature
    

Type:
    

[`bpy.types.Armature`](bpy.types/A/bpy.types.Armature.md#bpy.types.Armature "bpy.types.Armature")

bpy.context.lattice
    

Type:
    

[`bpy.types.Lattice`](bpy.types/L/bpy.types.Lattice.md#bpy.types.Lattice "bpy.types.Lattice")

bpy.context.curve
    

Type:
    

[`bpy.types.Curve`](bpy.types/C/bpy.types.Curve.md#bpy.types.Curve "bpy.types.Curve")

bpy.context.meta_ball
    

Type:
    

[`bpy.types.MetaBall`](bpy.types/M/bpy.types.MetaBall.md#bpy.types.MetaBall "bpy.types.MetaBall")

bpy.context.light
    

Type:
    

[`bpy.types.Light`](bpy.types/L/bpy.types.Light.md#bpy.types.Light "bpy.types.Light")

bpy.context.speaker
    

Type:
    

[`bpy.types.Speaker`](bpy.types/S/bpy.types.Speaker.md#bpy.types.Speaker "bpy.types.Speaker")

bpy.context.lightprobe
    

Type:
    

[`bpy.types.LightProbe`](bpy.types/L/bpy.types.LightProbe.md#bpy.types.LightProbe "bpy.types.LightProbe")

bpy.context.camera
    

Type:
    

[`bpy.types.Camera`](bpy.types/C/bpy.types.Camera.md#bpy.types.Camera "bpy.types.Camera")

bpy.context.material
    

Type:
    

[`bpy.types.Material`](bpy.types/M/bpy.types.Material.md#bpy.types.Material "bpy.types.Material")

bpy.context.material_slot
    

Type:
    

[`bpy.types.MaterialSlot`](bpy.types/M/bpy.types.MaterialSlot.md#bpy.types.MaterialSlot "bpy.types.MaterialSlot")

bpy.context.texture
    

Type:
    

[`bpy.types.Texture`](bpy.types/T/bpy.types.Texture.md#bpy.types.Texture "bpy.types.Texture")

bpy.context.texture_user
    

Type:
    

[`bpy.types.ID`](bpy.types/I/bpy.types.ID.md#bpy.types.ID "bpy.types.ID")

bpy.context.texture_user_property
    

Type:
    

[`bpy.types.Property`](bpy.types/P/bpy.types.Property.md#bpy.types.Property "bpy.types.Property")

bpy.context.texture_node
    

Type:
    

[`bpy.types.Node`](bpy.types/N/bpy.types.Node.md#bpy.types.Node "bpy.types.Node")

bpy.context.bone
    

Type:
    

[`bpy.types.Bone`](bpy.types/B/bpy.types.Bone.md#bpy.types.Bone "bpy.types.Bone")

bpy.context.edit_bone
    

Type:
    

[`bpy.types.EditBone`](bpy.types/E/bpy.types.EditBone.md#bpy.types.EditBone "bpy.types.EditBone")

bpy.context.pose_bone
    

Type:
    

[`bpy.types.PoseBone`](bpy.types/P/bpy.types.PoseBone.md#bpy.types.PoseBone "bpy.types.PoseBone")

bpy.context.particle_system
    

Type:
    

[`bpy.types.ParticleSystem`](bpy.types/P/bpy.types.ParticleSystem.md#bpy.types.ParticleSystem "bpy.types.ParticleSystem")

bpy.context.particle_system_editable
    

Type:
    

[`bpy.types.ParticleSystem`](bpy.types/P/bpy.types.ParticleSystem.md#bpy.types.ParticleSystem "bpy.types.ParticleSystem")

bpy.context.particle_settings
    

Type:
    

[`bpy.types.ParticleSettings`](bpy.types/P/bpy.types.ParticleSettings.md#bpy.types.ParticleSettings "bpy.types.ParticleSettings")

bpy.context.cloth
    

Type:
    

[`bpy.types.ClothModifier`](bpy.types/C/bpy.types.ClothModifier.md#bpy.types.ClothModifier "bpy.types.ClothModifier")

bpy.context.soft_body
    

Type:
    

[`bpy.types.SoftBodyModifier`](bpy.types/S/bpy.types.SoftBodyModifier.md#bpy.types.SoftBodyModifier "bpy.types.SoftBodyModifier")

bpy.context.fluid
    

Type:
    

`bpy.types.FluidSimulationModifier`

bpy.context.collision
    

Type:
    

[`bpy.types.CollisionModifier`](bpy.types/C/bpy.types.CollisionModifier.md#bpy.types.CollisionModifier "bpy.types.CollisionModifier")

bpy.context.brush
    

Type:
    

[`bpy.types.Brush`](bpy.types/B/bpy.types.Brush.md#bpy.types.Brush "bpy.types.Brush")

bpy.context.dynamic_paint
    

Type:
    

[`bpy.types.DynamicPaintModifier`](bpy.types/D/bpy.types.DynamicPaintModifier.md#bpy.types.DynamicPaintModifier "bpy.types.DynamicPaintModifier")

bpy.context.line_style
    

Type:
    

[`bpy.types.FreestyleLineStyle`](bpy.types/F/bpy.types.FreestyleLineStyle.md#bpy.types.FreestyleLineStyle "bpy.types.FreestyleLineStyle")

bpy.context.collection
    

Type:
    

[`bpy.types.LayerCollection`](bpy.types/L/bpy.types.LayerCollection.md#bpy.types.LayerCollection "bpy.types.LayerCollection")

bpy.context.gpencil
    

Type:
    

[`bpy.types.GreasePencil`](bpy.types/G/bpy.types.GreasePencil.md#bpy.types.GreasePencil "bpy.types.GreasePencil")

bpy.context.grease_pencil
    

Type:
    

[`bpy.types.GreasePencil`](bpy.types/G/bpy.types.GreasePencil.md#bpy.types.GreasePencil "bpy.types.GreasePencil")

bpy.context.curves
    

Type:
    

Hair Curves

bpy.context.pointcloud
    

Type:
    

[`bpy.types.PointCloud`](bpy.types/P/bpy.types.PointCloud.md#bpy.types.PointCloud "bpy.types.PointCloud")

bpy.context.volume
    

Type:
    

[`bpy.types.Volume`](bpy.types/V/bpy.types.Volume.md#bpy.types.Volume "bpy.types.Volume")

bpy.context.strip
    

Type:
    

[`bpy.types.Strip`](bpy.types/S/bpy.types.Strip.md#bpy.types.Strip "bpy.types.Strip")

bpy.context.strip_modifier
    

Type:
    

[`bpy.types.StripModifier`](bpy.types/S/bpy.types.StripModifier.md#bpy.types.StripModifier "bpy.types.StripModifier")

## Clip Context

bpy.context.edit_movieclip
    

Type:
    

[`bpy.types.MovieClip`](bpy.types/M/bpy.types.MovieClip.md#bpy.types.MovieClip "bpy.types.MovieClip")

bpy.context.edit_mask
    

Type:
    

[`bpy.types.Mask`](bpy.types/M/bpy.types.Mask.md#bpy.types.Mask "bpy.types.Mask")

## File Context

bpy.context.active_file
    

Type:
    

[`bpy.types.FileSelectEntry`](bpy.types/F/bpy.types.FileSelectEntry.md#bpy.types.FileSelectEntry "bpy.types.FileSelectEntry")

bpy.context.selected_files
    

Type:
    

sequence of [`bpy.types.FileSelectEntry`](bpy.types/F/bpy.types.FileSelectEntry.md#bpy.types.FileSelectEntry "bpy.types.FileSelectEntry")

bpy.context.asset_library_reference
    

Type:
    

[`bpy.types.AssetLibraryReference`](bpy.types/A/bpy.types.AssetLibraryReference.md#bpy.types.AssetLibraryReference "bpy.types.AssetLibraryReference")

bpy.context.asset
    

Type:
    

[`bpy.types.AssetRepresentation`](bpy.types/A/bpy.types.AssetRepresentation.md#bpy.types.AssetRepresentation "bpy.types.AssetRepresentation")

bpy.context.selected_assets
    

Type:
    

sequence of [`bpy.types.AssetRepresentation`](bpy.types/A/bpy.types.AssetRepresentation.md#bpy.types.AssetRepresentation "bpy.types.AssetRepresentation")

bpy.context.id
    

Type:
    

[`bpy.types.ID`](bpy.types/I/bpy.types.ID.md#bpy.types.ID "bpy.types.ID")

bpy.context.selected_ids
    

Type:
    

sequence of [`bpy.types.ID`](bpy.types/I/bpy.types.ID.md#bpy.types.ID "bpy.types.ID")

## Image Context

bpy.context.edit_image
    

Type:
    

[`bpy.types.Image`](bpy.types/I/bpy.types.Image.md#bpy.types.Image "bpy.types.Image")

bpy.context.edit_mask
    

Type:
    

[`bpy.types.Mask`](bpy.types/M/bpy.types.Mask.md#bpy.types.Mask "bpy.types.Mask")

## Node Context

bpy.context.selected_nodes
    

Type:
    

sequence of [`bpy.types.Node`](bpy.types/N/bpy.types.Node.md#bpy.types.Node "bpy.types.Node")

bpy.context.active_node
    

Type:
    

[`bpy.types.Node`](bpy.types/N/bpy.types.Node.md#bpy.types.Node "bpy.types.Node")

bpy.context.light
    

Type:
    

[`bpy.types.Light`](bpy.types/L/bpy.types.Light.md#bpy.types.Light "bpy.types.Light")

bpy.context.material
    

Type:
    

[`bpy.types.Material`](bpy.types/M/bpy.types.Material.md#bpy.types.Material "bpy.types.Material")

bpy.context.world
    

Type:
    

[`bpy.types.World`](bpy.types/W/bpy.types.World.md#bpy.types.World "bpy.types.World")

## Screen Context

bpy.context.scene
    

Type:
    

[`bpy.types.Scene`](bpy.types/S/bpy.types.Scene.md#bpy.types.Scene "bpy.types.Scene")

bpy.context.view_layer
    

Type:
    

[`bpy.types.ViewLayer`](bpy.types/V/bpy.types.ViewLayer.md#bpy.types.ViewLayer "bpy.types.ViewLayer")

bpy.context.visible_objects
    

Type:
    

sequence of [`bpy.types.Object`](bpy.types/O/bpy.types.Object.md#bpy.types.Object "bpy.types.Object")

bpy.context.selectable_objects
    

Type:
    

sequence of [`bpy.types.Object`](bpy.types/O/bpy.types.Object.md#bpy.types.Object "bpy.types.Object")

bpy.context.selected_objects
    

Type:
    

sequence of [`bpy.types.Object`](bpy.types/O/bpy.types.Object.md#bpy.types.Object "bpy.types.Object")

bpy.context.editable_objects
    

Type:
    

sequence of [`bpy.types.Object`](bpy.types/O/bpy.types.Object.md#bpy.types.Object "bpy.types.Object")

bpy.context.selected_editable_objects
    

Type:
    

sequence of [`bpy.types.Object`](bpy.types/O/bpy.types.Object.md#bpy.types.Object "bpy.types.Object")

bpy.context.objects_in_mode
    

Type:
    

sequence of [`bpy.types.Object`](bpy.types/O/bpy.types.Object.md#bpy.types.Object "bpy.types.Object")

bpy.context.objects_in_mode_unique_data
    

Type:
    

sequence of [`bpy.types.Object`](bpy.types/O/bpy.types.Object.md#bpy.types.Object "bpy.types.Object")

bpy.context.visible_bones
    

Type:
    

sequence of [`bpy.types.EditBone`](bpy.types/E/bpy.types.EditBone.md#bpy.types.EditBone "bpy.types.EditBone")

bpy.context.editable_bones
    

Type:
    

sequence of [`bpy.types.EditBone`](bpy.types/E/bpy.types.EditBone.md#bpy.types.EditBone "bpy.types.EditBone")

bpy.context.selected_bones
    

Type:
    

sequence of [`bpy.types.EditBone`](bpy.types/E/bpy.types.EditBone.md#bpy.types.EditBone "bpy.types.EditBone")

bpy.context.selected_editable_bones
    

Type:
    

sequence of [`bpy.types.EditBone`](bpy.types/E/bpy.types.EditBone.md#bpy.types.EditBone "bpy.types.EditBone")

bpy.context.visible_pose_bones
    

Type:
    

sequence of [`bpy.types.PoseBone`](bpy.types/P/bpy.types.PoseBone.md#bpy.types.PoseBone "bpy.types.PoseBone")

bpy.context.selected_pose_bones
    

Type:
    

sequence of [`bpy.types.PoseBone`](bpy.types/P/bpy.types.PoseBone.md#bpy.types.PoseBone "bpy.types.PoseBone")

bpy.context.selected_pose_bones_from_active_object
    

Type:
    

sequence of [`bpy.types.PoseBone`](bpy.types/P/bpy.types.PoseBone.md#bpy.types.PoseBone "bpy.types.PoseBone")

bpy.context.active_bone
    

Type:
    

[`bpy.types.EditBone`](bpy.types/E/bpy.types.EditBone.md#bpy.types.EditBone "bpy.types.EditBone") or [`bpy.types.Bone`](bpy.types/B/bpy.types.Bone.md#bpy.types.Bone "bpy.types.Bone")

bpy.context.active_pose_bone
    

Type:
    

[`bpy.types.PoseBone`](bpy.types/P/bpy.types.PoseBone.md#bpy.types.PoseBone "bpy.types.PoseBone")

bpy.context.active_object
    

Type:
    

[`bpy.types.Object`](bpy.types/O/bpy.types.Object.md#bpy.types.Object "bpy.types.Object")

bpy.context.object
    

Type:
    

[`bpy.types.Object`](bpy.types/O/bpy.types.Object.md#bpy.types.Object "bpy.types.Object")

bpy.context.edit_object
    

Type:
    

[`bpy.types.Object`](bpy.types/O/bpy.types.Object.md#bpy.types.Object "bpy.types.Object")

bpy.context.sculpt_object
    

Type:
    

[`bpy.types.Object`](bpy.types/O/bpy.types.Object.md#bpy.types.Object "bpy.types.Object")

bpy.context.vertex_paint_object
    

Type:
    

[`bpy.types.Object`](bpy.types/O/bpy.types.Object.md#bpy.types.Object "bpy.types.Object")

bpy.context.weight_paint_object
    

Type:
    

[`bpy.types.Object`](bpy.types/O/bpy.types.Object.md#bpy.types.Object "bpy.types.Object")

bpy.context.image_paint_object
    

Type:
    

[`bpy.types.Object`](bpy.types/O/bpy.types.Object.md#bpy.types.Object "bpy.types.Object")

bpy.context.particle_edit_object
    

Type:
    

[`bpy.types.Object`](bpy.types/O/bpy.types.Object.md#bpy.types.Object "bpy.types.Object")

bpy.context.pose_object
    

Type:
    

[`bpy.types.Object`](bpy.types/O/bpy.types.Object.md#bpy.types.Object "bpy.types.Object")

bpy.context.active_nla_track
    

Type:
    

[`bpy.types.NlaTrack`](bpy.types/N/bpy.types.NlaTrack.md#bpy.types.NlaTrack "bpy.types.NlaTrack")

bpy.context.active_nla_strip
    

Type:
    

[`bpy.types.NlaStrip`](bpy.types/N/bpy.types.NlaStrip.md#bpy.types.NlaStrip "bpy.types.NlaStrip")

bpy.context.selected_nla_strips
    

Type:
    

sequence of [`bpy.types.NlaStrip`](bpy.types/N/bpy.types.NlaStrip.md#bpy.types.NlaStrip "bpy.types.NlaStrip")

bpy.context.selected_movieclip_tracks
    

Type:
    

sequence of [`bpy.types.MovieTrackingTrack`](bpy.types/M/bpy.types.MovieTrackingTrack.md#bpy.types.MovieTrackingTrack "bpy.types.MovieTrackingTrack")

bpy.context.annotation_data
    

Type:
    

[`bpy.types.GreasePencil`](bpy.types/G/bpy.types.GreasePencil.md#bpy.types.GreasePencil "bpy.types.GreasePencil")

bpy.context.annotation_data_owner
    

Type:
    

[`bpy.types.ID`](bpy.types/I/bpy.types.ID.md#bpy.types.ID "bpy.types.ID")

bpy.context.active_annotation_layer
    

Type:
    

`bpy.types.GPencilLayer`

bpy.context.grease_pencil
    

Type:
    

[`bpy.types.GreasePencil`](bpy.types/G/bpy.types.GreasePencil.md#bpy.types.GreasePencil "bpy.types.GreasePencil")

bpy.context.active_operator
    

Type:
    

[`bpy.types.Operator`](bpy.types/O/bpy.types.Operator.md#bpy.types.Operator "bpy.types.Operator")

bpy.context.active_action
    

Type:
    

[`bpy.types.Action`](bpy.types/A/bpy.types.Action.md#bpy.types.Action "bpy.types.Action")

bpy.context.selected_visible_actions
    

Type:
    

sequence of [`bpy.types.Action`](bpy.types/A/bpy.types.Action.md#bpy.types.Action "bpy.types.Action")

bpy.context.selected_editable_actions
    

Type:
    

sequence of [`bpy.types.Action`](bpy.types/A/bpy.types.Action.md#bpy.types.Action "bpy.types.Action")

bpy.context.visible_fcurves
    

Type:
    

sequence of [`bpy.types.FCurve`](bpy.types/F/bpy.types.FCurve.md#bpy.types.FCurve "bpy.types.FCurve")

bpy.context.editable_fcurves
    

Type:
    

sequence of [`bpy.types.FCurve`](bpy.types/F/bpy.types.FCurve.md#bpy.types.FCurve "bpy.types.FCurve")

bpy.context.selected_visible_fcurves
    

Type:
    

sequence of [`bpy.types.FCurve`](bpy.types/F/bpy.types.FCurve.md#bpy.types.FCurve "bpy.types.FCurve")

bpy.context.selected_editable_fcurves
    

Type:
    

sequence of [`bpy.types.FCurve`](bpy.types/F/bpy.types.FCurve.md#bpy.types.FCurve "bpy.types.FCurve")

bpy.context.active_editable_fcurve
    

Type:
    

[`bpy.types.FCurve`](bpy.types/F/bpy.types.FCurve.md#bpy.types.FCurve "bpy.types.FCurve")

bpy.context.selected_editable_keyframes
    

Type:
    

sequence of [`bpy.types.Keyframe`](bpy.types/K/bpy.types.Keyframe.md#bpy.types.Keyframe "bpy.types.Keyframe")

bpy.context.ui_list
    

Type:
    

[`bpy.types.UIList`](bpy.types/U/bpy.types.UIList.md#bpy.types.UIList "bpy.types.UIList")

bpy.context.property
    

Type:
    

[`bpy.types.AnyType`](bpy.types/A/bpy.types.AnyType.md#bpy.types.AnyType "bpy.types.AnyType") or `str` or `int`

Get the property associated with a hovered button. Returns a tuple of the data-block, data path to the property, and array index.

Note

When the property doesn’t have an associated [`bpy.types.ID`](bpy.types/I/bpy.types.ID.md#bpy.types.ID "bpy.types.ID") non-ID data may be returned. This may occur when accessing windowing data, for example, operator properties.
    
    
    # Example inserting keyframe for the hovered property.
    active_property = bpy.context.property
    if active_property:
        datablock, data_path, index = active_property
        datablock.keyframe_insert(data_path=data_path, index=index, frame=1)
    

bpy.context.asset_library_reference
    

Type:
    

[`bpy.types.AssetLibraryReference`](bpy.types/A/bpy.types.AssetLibraryReference.md#bpy.types.AssetLibraryReference "bpy.types.AssetLibraryReference")

bpy.context.active_strip
    

Type:
    

[`bpy.types.Strip`](bpy.types/S/bpy.types.Strip.md#bpy.types.Strip "bpy.types.Strip")

bpy.context.strips
    

Type:
    

sequence of [`bpy.types.Strip`](bpy.types/S/bpy.types.Strip.md#bpy.types.Strip "bpy.types.Strip")

bpy.context.selected_strips
    

Type:
    

sequence of [`bpy.types.Strip`](bpy.types/S/bpy.types.Strip.md#bpy.types.Strip "bpy.types.Strip")

bpy.context.selected_editable_strips
    

Type:
    

sequence of [`bpy.types.Strip`](bpy.types/S/bpy.types.Strip.md#bpy.types.Strip "bpy.types.Strip")

bpy.context.sequencer_scene
    

Type:
    

[`bpy.types.Scene`](bpy.types/S/bpy.types.Scene.md#bpy.types.Scene "bpy.types.Scene")

## Sequencer Context

bpy.context.edit_mask
    

Type:
    

[`bpy.types.Mask`](bpy.types/M/bpy.types.Mask.md#bpy.types.Mask "bpy.types.Mask")

bpy.context.tool_settings
    

Type:
    

[`bpy.types.ToolSettings`](bpy.types/T/bpy.types.ToolSettings.md#bpy.types.ToolSettings "bpy.types.ToolSettings")

## Text Context

bpy.context.edit_text
    

Type:
    

[`bpy.types.Text`](bpy.types/T/bpy.types.Text.md#bpy.types.Text "bpy.types.Text")

## View3D Context

bpy.context.active_object
    

Type:
    

[`bpy.types.Object`](bpy.types/O/bpy.types.Object.md#bpy.types.Object "bpy.types.Object")

bpy.context.selected_ids
    

Type:
    

sequence of [`bpy.types.ID`](bpy.types/I/bpy.types.ID.md#bpy.types.ID "bpy.types.ID")
