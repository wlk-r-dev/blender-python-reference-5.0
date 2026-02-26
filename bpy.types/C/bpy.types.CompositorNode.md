# CompositorNode(NodeInternal)

base classes — [[bpy_struct]], [[Node]], [[NodeInternal]]

subclasses — [[CompositorNodeAlphaOver]], [[CompositorNodeAntiAliasing]], [[CompositorNodeBilateralblur]], [[CompositorNodeBlur]], [[CompositorNodeBokehBlur]], [[CompositorNodeBokehImage]], [[CompositorNodeBoxMask]], [[CompositorNodeBrightContrast]], [[CompositorNodeChannelMatte]], [[CompositorNodeChromaMatte]], [[CompositorNodeColorBalance]], [[CompositorNodeColorCorrection]], [[CompositorNodeColorMatte]], [[CompositorNodeColorSpill]], [[CompositorNodeCombineColor]], [[CompositorNodeConvertColorSpace]], [[CompositorNodeConvertToDisplay]], [[CompositorNodeConvolve]], [[CompositorNodeCornerPin]], [[CompositorNodeCrop]], [[CompositorNodeCryptomatte]], [[CompositorNodeCryptomatteV2]], [[CompositorNodeCurveRGB]], [[CompositorNodeCustomGroup]], [[CompositorNodeDBlur]], [[CompositorNodeDefocus]], [[CompositorNodeDenoise]], [[CompositorNodeDespeckle]], [[CompositorNodeDiffMatte]], [[CompositorNodeDilateErode]], [[CompositorNodeDisplace]], [[CompositorNodeDistanceMatte]], [[CompositorNodeDoubleEdgeMask]], [[CompositorNodeEllipseMask]], [[CompositorNodeExposure]], [[CompositorNodeFilter]], [[CompositorNodeFlip]], [[CompositorNodeGamma]], [[CompositorNodeGlare]], [[CompositorNodeGroup]], [[CompositorNodeHueCorrect]], [[CompositorNodeHueSat]], [[CompositorNodeIDMask]], [[CompositorNodeImage]], [[CompositorNodeImageCoordinates]], [[CompositorNodeImageInfo]], [[CompositorNodeInpaint]], [[CompositorNodeInvert]], [[CompositorNodeKeying]], [[CompositorNodeKeyingScreen]], [[CompositorNodeKuwahara]], [[CompositorNodeLensdist]], [[CompositorNodeLevels]], [[CompositorNodeLumaMatte]], [[CompositorNodeMapUV]], [[CompositorNodeMask]], [[CompositorNodeMovieClip]], [[CompositorNodeMovieDistortion]], [[CompositorNodeNormal]], [[CompositorNodeNormalize]], [[CompositorNodeOutputFile]], [[CompositorNodePixelate]], [[CompositorNodePlaneTrackDeform]], [[CompositorNodePosterize]], [[CompositorNodePremulKey]], [[CompositorNodeRGB]], [[CompositorNodeRGBToBW]], [[CompositorNodeRLayers]], [[CompositorNodeRelativeToPixel]], [[CompositorNodeRotate]], [[CompositorNodeScale]], [[CompositorNodeSceneTime]], [[CompositorNodeSeparateColor]], [[CompositorNodeSetAlpha]], [[CompositorNodeSplit]], [[CompositorNodeStabilize]], [[CompositorNodeSwitch]], [[CompositorNodeSwitchView]], [[CompositorNodeTime]], [[CompositorNodeTonemap]], [[CompositorNodeTrackPos]], [[CompositorNodeTransform]], [[CompositorNodeTranslate]], [[CompositorNodeVecBlur]], [[CompositorNodeViewer]], [[CompositorNodeZcombine]]

_class _bpy.types.CompositorNode(_NodeInternal_)
    

tag_need_exec()
    

Tag the node for compositor update

update()
    

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
  * [[Node.type]]
  * [[Node.location]]
  * [[Node.location_absolute]]
  * [[Node.width]]
  * [[Node.height]]
  * [[Node.dimensions]]
  * [[Node.name]]
  * [[Node.label]]
  * [[Node.inputs]]
  * [[Node.outputs]]
  * [[Node.internal_links]]
  * [[Node.parent]]
  * [[Node.warning_propagation]]
  * [[Node.use_custom_color]]
  * [[Node.color]]
  * [[Node.color_tag]]

| 

  * [[Node.select]]
  * [[Node.show_options]]
  * [[Node.show_preview]]
  * [[Node.hide]]
  * [[Node.mute]]
  * [[Node.show_texture]]
  * [[Node.bl_idname]]
  * [[Node.bl_label]]
  * [[Node.bl_description]]
  * [[Node.bl_icon]]
  * [[Node.bl_static_type]]
  * [[Node.bl_width_default]]
  * [[Node.bl_width_min]]
  * [[Node.bl_width_max]]
  * [[Node.bl_height_default]]
  * [[Node.bl_height_min]]
  * [[Node.bl_height_max]]

  
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
  * [[bpy_struct.type_recast]]
  * [[bpy_struct.values]]
  * [[Node.bl_system_properties_get]]

| 

  * [[Node.socket_value_update]]
  * [[Node.is_registered_node_type]]
  * [[Node.poll]]
  * [[Node.poll_instance]]
  * [[Node.update]]
  * [[Node.insert_link]]
  * [[Node.init]]
  * [[Node.copy]]
  * [[Node.free]]
  * [[Node.draw_buttons]]
  * [[Node.draw_buttons_ext]]
  * [[Node.draw_label]]
  * [[Node.debug_zone_body_lazy_function_graph]]
  * [[Node.debug_zone_lazy_function_graph]]
  * [[Node.poll]]
  * [[Node.bl_rna_get_subclass]]
  * [[Node.bl_rna_get_subclass_py]]
  * [[NodeInternal.poll]]
  * [[NodeInternal.poll_instance]]
  * [[NodeInternal.update]]
  * [[NodeInternal.draw_buttons]]
  * [[NodeInternal.draw_buttons_ext]]
  * [[NodeInternal.bl_rna_get_subclass]]
  * [[NodeInternal.bl_rna_get_subclass_py]]

  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
