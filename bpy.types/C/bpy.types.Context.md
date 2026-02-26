# Context(bpy_struct)

base class — [[bpy_struct]]

_class _bpy.types.Context(_bpy_struct_)
    

Current windowmanager and data context

area
    

Type:
    

[[Area]], (readonly)

asset
    

Type:
    

[[AssetRepresentation]], (readonly)

blend_data
    

Type:
    

[[BlendData]], (readonly)

collection
    

Type:
    

[[Collection]], (readonly)

engine
    

Type:
    

string, default “”, (readonly, never None)

gizmo_group
    

Type:
    

[[GizmoGroup]], (readonly)

layer_collection
    

Type:
    

[[LayerCollection]], (readonly)

mode
    

Type:
    

enum in [Context Mode Items](../../bpy_types_enum_items/context_mode_items.md#rna-enum-context-mode-items), default `'EDIT_MESH'`, (readonly)

preferences
    

Type:
    

[[Preferences]], (readonly)

region
    

Type:
    

[[Region]], (readonly)

region_data
    

Type:
    

[[RegionView3D]], (readonly)

region_popup
    

The temporary region for pop-ups (including menus and pop-overs)

Type:
    

[[Region]], (readonly)

scene
    

Type:
    

[[Scene]], (readonly)

screen
    

Type:
    

[[Screen]], (readonly)

space_data
    

The current space, may be None in background-mode, when the cursor is outside the window or when using menu-search

Type:
    

[[Space]], (readonly)

tool_settings
    

Type:
    

[[ToolSettings]], (readonly)

view_layer
    

Type:
    

[[ViewLayer]], (readonly)

window
    

Type:
    

[[Window]], (readonly)

window_manager
    

Type:
    

[[WindowManager]], (readonly)

workspace
    

Type:
    

[[WorkSpace]], (readonly)

evaluated_depsgraph_get()
    

Get the dependency graph for the current scene and view layer, to access to data-blocks with animation and modifiers applied. If any data-blocks have been edited, the dependency graph will be updated. This invalidates all references to evaluated data-blocks from the dependency graph.

Returns:
    

Evaluated dependency graph

Return type:
    

[[Depsgraph]]

copy()
    

Get context members as a dictionary.

Return type:
    

dict[str, Any]

path_resolve(_path_ , _coerce =True_)
    

Returns the property from the path, raise an exception when not found.

Parameters:
    

  * **path** (_str_) – patch which this property resolves.

  * **coerce** (_bool_) – optional argument, when True, the property will be converted into its Python representation.


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

temp_override(_*_ , _window =None_, _screen =None_, _area =None_, _region =None_, _** keywords_)
    

Context manager to temporarily override members in the context.

Parameters:
    

  * **window** ([[bpy.types.Window]]) – Window override or None.

  * **screen** ([[bpy.types.Screen]]) – 

Screen override or None.

Note

Switching to or away from full-screen areas & temporary screens isn’t supported. Passing in these screens will raise an exception, actions that leave the context such screens won’t restore the prior screen.

Note

Changing the screen has wider implications than other arguments as it will also change the works-space and potentially the scene (when pinned).

  * **area** ([[bpy.types.Area]]) – Area override or None.

  * **region** ([[bpy.types.Region]]) – Region override or None.

  * **keywords** – Additional keywords override context members.


Returns:
    

The context manager .

Return type:
    

ContextTempOverride

Overriding the context can be used to temporarily activate another `window` / `area` & `region`, as well as other members such as the `active_object` or `bone`.

Notes:

  * When overriding window, area and regions: the arguments must be consistent, so any region argument that’s passed in must be contained by the current area or the area passed in. The same goes for the area needing to be contained in the current window.

  * Temporary context overrides may be nested, when this is done, members will be added to the existing overrides.

  * Context members are restored outside the scope of the context-manager. The only exception to this is when the data is no longer available.

In the event windowing data was removed (for example), the state of the context is left as-is. While this isn’t likely to happen, explicit window operation such as closing windows or loading a new file remove the windowing data that was set before the temporary context was created.


Overriding the context can be useful to set the context after loading files (which would otherwise be None). For example:
    
    
    import bpy
    from bpy import context
    
    # Reload the current file and select all.
    bpy.ops.wm.open_mainfile(filepath=bpy.data.filepath)
    window = context.window_manager.windows[0]
    with context.temp_override(window=window):
        bpy.ops.mesh.primitive_uv_sphere_add()
        # The context override is needed so it's possible to set edit-mode.
        bpy.ops.object.mode_set(mode='EDIT')
    

This example shows how it’s possible to add an object to the scene in another window.
    
    
    import bpy
    from bpy import context
    
    win_active = context.window
    win_other = None
    for win_iter in context.window_manager.windows:
        if win_iter != win_active:
            win_other = win_iter
            break
    
    # Add cube in the other window.
    with context.temp_override(window=win_other):
        bpy.ops.mesh.primitive_cube_add()
    

**Logging Context Member Access**

Context members can be logged by calling `logging_set(True)` on the “with” target of a temporary override. This will log the members that are being accessed during the operation and may assist in debugging when it is unclear which members need to be overridden.

In the event an operator fails to execute because of a missing context member, logging may help identify which member is required.

This example shows how to log which context members are being accessed. Log statements are printed to your system’s console.

Important

Not all operators rely on Context Members and therefore will not be affected by `bpy.types.Context.temp_override`, use logging to what members if any are accessed.
    
    
    import bpy
    from bpy import context
    
    my_objects = [context.scene.camera]
    
    with context.temp_override(selected_objects=my_objects) as override:
        override.logging_set(True)  # Enable logging.
        bpy.ops.object.delete()
    

## Inherited Properties

  * [[bpy_struct.id_data]]

| 


  
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

| 

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

  
---|---  
  
## References

  * [[AssetShelf.draw_context_menu]]
  * [[AssetShelf.poll]]
  * [[FileHandler.poll_drop]]
  * [[Gizmo.draw]]
  * [[Gizmo.draw_select]]
  * [[Gizmo.exit]]
  * [[Gizmo.invoke]]
  * [[Gizmo.modal]]
  * [[Gizmo.test_select]]
  * [[GizmoGroup.draw_prepare]]
  * [[GizmoGroup.invoke_prepare]]
  * [[GizmoGroup.poll]]
  * [[GizmoGroup.refresh]]
  * [[GizmoGroup.setup]]
  * [[Header.draw]]
  * [[KeyingSetInfo.generate]]
  * [[KeyingSetInfo.iterator]]
  * [[KeyingSetInfo.poll]]
  * [[Macro.draw]]
  * [[Macro.poll]]
  * [[Menu.draw]]
  * [[Menu.poll]]
  * [[Node.draw_buttons]]
  * [[Node.draw_buttons_ext]]
  * [[Node.init]]
  * [[Node.socket_value_update]]
  * [[NodeInternal.draw_buttons]]
  * [[NodeInternal.draw_buttons_ext]]
  * [[NodeSocket.draw]]
  * [[NodeSocket.draw_color]]
  * [[NodeSocketStandard.draw]]
  * [[NodeSocketStandard.draw_color]]
  * [[NodeTree.get_from_context]]
  * [[NodeTree.interface_update]]
  * [[NodeTree.poll]]
  * [[NodeTreeInterfaceSocket.draw]]
  * [[NodeTreeInterfaceSocketBool.draw]]
  * [[NodeTreeInterfaceSocketBundle.draw]]
  * [[NodeTreeInterfaceSocketClosure.draw]]
  * [[NodeTreeInterfaceSocketCollection.draw]]
  * [[NodeTreeInterfaceSocketColor.draw]]
  * [[NodeTreeInterfaceSocketFloat.draw]]
  * [[NodeTreeInterfaceSocketFloatAngle.draw]]
  * [[NodeTreeInterfaceSocketFloatColorTemperature.draw]]
  * [[NodeTreeInterfaceSocketFloatDistance.draw]]
  * [[NodeTreeInterfaceSocketFloatFactor.draw]]
  * [[NodeTreeInterfaceSocketFloatFrequency.draw]]
  * [[NodeTreeInterfaceSocketFloatPercentage.draw]]
  * [[NodeTreeInterfaceSocketFloatTime.draw]]
  * [[NodeTreeInterfaceSocketFloatTimeAbsolute.draw]]
  * [[NodeTreeInterfaceSocketFloatUnsigned.draw]]
  * [[NodeTreeInterfaceSocketFloatWavelength.draw]]
  * [[NodeTreeInterfaceSocketGeometry.draw]]
  * [[NodeTreeInterfaceSocketImage.draw]]
  * [[NodeTreeInterfaceSocketInt.draw]]
  * [[NodeTreeInterfaceSocketIntFactor.draw]]
  * [[NodeTreeInterfaceSocketIntPercentage.draw]]
  * [[NodeTreeInterfaceSocketIntUnsigned.draw]]
  * [[NodeTreeInterfaceSocketMaterial.draw]]
  * [[NodeTreeInterfaceSocketMatrix.draw]]
  * [[NodeTreeInterfaceSocketMenu.draw]]
  * [[NodeTreeInterfaceSocketObject.draw]]
  * [[NodeTreeInterfaceSocketRotation.draw]]

| 

  * [[NodeTreeInterfaceSocketShader.draw]]
  * [[NodeTreeInterfaceSocketString.draw]]
  * [[NodeTreeInterfaceSocketStringFilePath.draw]]
  * [[NodeTreeInterfaceSocketTexture.draw]]
  * [[NodeTreeInterfaceSocketVector.draw]]
  * [[NodeTreeInterfaceSocketVector2D.draw]]
  * [[NodeTreeInterfaceSocketVector4D.draw]]
  * [[NodeTreeInterfaceSocketVectorAcceleration.draw]]
  * [[NodeTreeInterfaceSocketVectorAcceleration2D.draw]]
  * [[NodeTreeInterfaceSocketVectorAcceleration4D.draw]]
  * [[NodeTreeInterfaceSocketVectorDirection.draw]]
  * [[NodeTreeInterfaceSocketVectorDirection2D.draw]]
  * [[NodeTreeInterfaceSocketVectorDirection4D.draw]]
  * [[NodeTreeInterfaceSocketVectorEuler.draw]]
  * [[NodeTreeInterfaceSocketVectorEuler2D.draw]]
  * [[NodeTreeInterfaceSocketVectorEuler4D.draw]]
  * [[NodeTreeInterfaceSocketVectorFactor.draw]]
  * [[NodeTreeInterfaceSocketVectorFactor2D.draw]]
  * [[NodeTreeInterfaceSocketVectorFactor4D.draw]]
  * [[NodeTreeInterfaceSocketVectorPercentage.draw]]
  * [[NodeTreeInterfaceSocketVectorPercentage2D.draw]]
  * [[NodeTreeInterfaceSocketVectorPercentage4D.draw]]
  * [[NodeTreeInterfaceSocketVectorTranslation.draw]]
  * [[NodeTreeInterfaceSocketVectorTranslation2D.draw]]
  * [[NodeTreeInterfaceSocketVectorTranslation4D.draw]]
  * [[NodeTreeInterfaceSocketVectorVelocity.draw]]
  * [[NodeTreeInterfaceSocketVectorVelocity2D.draw]]
  * [[NodeTreeInterfaceSocketVectorVelocity4D.draw]]
  * [[NodeTreeInterfaceSocketVectorXYZ.draw]]
  * [[NodeTreeInterfaceSocketVectorXYZ2D.draw]]
  * [[NodeTreeInterfaceSocketVectorXYZ4D.draw]]
  * [[Operator.cancel]]
  * [[Operator.check]]
  * [[Operator.description]]
  * [[Operator.draw]]
  * [[Operator.execute]]
  * [[Operator.invoke]]
  * [[Operator.modal]]
  * [[Operator.poll]]
  * [[Panel.draw]]
  * [[Panel.draw_header]]
  * [[Panel.draw_header_preset]]
  * [[Panel.poll]]
  * [[RenderEngine.draw]]
  * [[RenderEngine.view_draw]]
  * [[RenderEngine.view_update]]
  * [[UIList.draw_filter]]
  * [[UIList.draw_item]]
  * [[UIList.filter_items]]
  * [[XrSessionState.action_binding_create]]
  * [[XrSessionState.action_create]]
  * [[XrSessionState.action_set_create]]
  * [[XrSessionState.action_state_get]]
  * [[XrSessionState.active_action_set_set]]
  * [[XrSessionState.controller_aim_location_get]]
  * [[XrSessionState.controller_aim_rotation_get]]
  * [[XrSessionState.controller_grip_location_get]]
  * [[XrSessionState.controller_grip_rotation_get]]
  * [[XrSessionState.controller_pose_actions_set]]
  * [[XrSessionState.haptic_action_apply]]
  * [[XrSessionState.haptic_action_stop]]
  * [[XrSessionState.is_running]]
  * [[XrSessionState.reset_to_base_pose]]

  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
  *[*]: Keyword-only parameters separator (PEP 3102)
