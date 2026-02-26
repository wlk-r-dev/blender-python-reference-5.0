# Context(bpy_struct)

base class — [`bpy_struct`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct "bpy.types.bpy_struct")

_class _bpy.types.Context(_bpy_struct_)
    

Current windowmanager and data context

area
    

Type:
    

[`Area`](../A/bpy.types.Area.md#bpy.types.Area "bpy.types.Area"), (readonly)

asset
    

Type:
    

[`AssetRepresentation`](../A/bpy.types.AssetRepresentation.md#bpy.types.AssetRepresentation "bpy.types.AssetRepresentation"), (readonly)

blend_data
    

Type:
    

[`BlendData`](../B/bpy.types.BlendData.md#bpy.types.BlendData "bpy.types.BlendData"), (readonly)

collection
    

Type:
    

[`Collection`](bpy.types.Collection.md#bpy.types.Collection "bpy.types.Collection"), (readonly)

engine
    

Type:
    

string, default “”, (readonly, never None)

gizmo_group
    

Type:
    

[`GizmoGroup`](../G/bpy.types.GizmoGroup.md#bpy.types.GizmoGroup "bpy.types.GizmoGroup"), (readonly)

layer_collection
    

Type:
    

[`LayerCollection`](../L/bpy.types.LayerCollection.md#bpy.types.LayerCollection "bpy.types.LayerCollection"), (readonly)

mode
    

Type:
    

enum in [Context Mode Items](../../bpy_types_enum_items/context_mode_items.md#rna-enum-context-mode-items), default `'EDIT_MESH'`, (readonly)

preferences
    

Type:
    

[`Preferences`](../P/bpy.types.Preferences.md#bpy.types.Preferences "bpy.types.Preferences"), (readonly)

region
    

Type:
    

[`Region`](../R/bpy.types.Region.md#bpy.types.Region "bpy.types.Region"), (readonly)

region_data
    

Type:
    

[`RegionView3D`](../R/bpy.types.RegionView3D.md#bpy.types.RegionView3D "bpy.types.RegionView3D"), (readonly)

region_popup
    

The temporary region for pop-ups (including menus and pop-overs)

Type:
    

[`Region`](../R/bpy.types.Region.md#bpy.types.Region "bpy.types.Region"), (readonly)

scene
    

Type:
    

[`Scene`](../S/bpy.types.Scene.md#bpy.types.Scene "bpy.types.Scene"), (readonly)

screen
    

Type:
    

[`Screen`](../S/bpy.types.Screen.md#bpy.types.Screen "bpy.types.Screen"), (readonly)

space_data
    

The current space, may be None in background-mode, when the cursor is outside the window or when using menu-search

Type:
    

[`Space`](../S/bpy.types.Space.md#bpy.types.Space "bpy.types.Space"), (readonly)

tool_settings
    

Type:
    

[`ToolSettings`](../T/bpy.types.ToolSettings.md#bpy.types.ToolSettings "bpy.types.ToolSettings"), (readonly)

view_layer
    

Type:
    

[`ViewLayer`](../V/bpy.types.ViewLayer.md#bpy.types.ViewLayer "bpy.types.ViewLayer"), (readonly)

window
    

Type:
    

[`Window`](../W/bpy.types.Window.md#bpy.types.Window "bpy.types.Window"), (readonly)

window_manager
    

Type:
    

[`WindowManager`](../W/bpy.types.WindowManager.md#bpy.types.WindowManager "bpy.types.WindowManager"), (readonly)

workspace
    

Type:
    

[`WorkSpace`](../W/bpy.types.WorkSpace.md#bpy.types.WorkSpace "bpy.types.WorkSpace"), (readonly)

evaluated_depsgraph_get()
    

Get the dependency graph for the current scene and view layer, to access to data-blocks with animation and modifiers applied. If any data-blocks have been edited, the dependency graph will be updated. This invalidates all references to evaluated data-blocks from the dependency graph.

Returns:
    

Evaluated dependency graph

Return type:
    

[`Depsgraph`](../D/bpy.types.Depsgraph.md#bpy.types.Depsgraph "bpy.types.Depsgraph")

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
    

[`bpy.types.Struct`](../S/bpy.types.Struct.md#bpy.types.Struct "bpy.types.Struct") subclass

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
    

  * **window** ([`bpy.types.Window`](../W/bpy.types.Window.md#bpy.types.Window "bpy.types.Window")) – Window override or None.

  * **screen** ([`bpy.types.Screen`](../S/bpy.types.Screen.md#bpy.types.Screen "bpy.types.Screen")) – 

Screen override or None.

Note

Switching to or away from full-screen areas & temporary screens isn’t supported. Passing in these screens will raise an exception, actions that leave the context such screens won’t restore the prior screen.

Note

Changing the screen has wider implications than other arguments as it will also change the works-space and potentially the scene (when pinned).

  * **area** ([`bpy.types.Area`](../A/bpy.types.Area.md#bpy.types.Area "bpy.types.Area")) – Area override or None.

  * **region** ([`bpy.types.Region`](../R/bpy.types.Region.md#bpy.types.Region "bpy.types.Region")) – Region override or None.

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

  * [`bpy_struct.id_data`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.id_data "bpy.types.bpy_struct.id_data")

| 


  
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

| 

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
  * [`bpy_struct.type_recast`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.type_recast "bpy.types.bpy_struct.type_recast")
  * [`bpy_struct.values`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.values "bpy.types.bpy_struct.values")

  
---|---  
  
## References

  * [`AssetShelf.draw_context_menu`](../A/bpy.types.AssetShelf.md#bpy.types.AssetShelf.draw_context_menu "bpy.types.AssetShelf.draw_context_menu")
  * [`AssetShelf.poll`](../A/bpy.types.AssetShelf.md#bpy.types.AssetShelf.poll "bpy.types.AssetShelf.poll")
  * [`FileHandler.poll_drop`](../F/bpy.types.FileHandler.md#bpy.types.FileHandler.poll_drop "bpy.types.FileHandler.poll_drop")
  * [`Gizmo.draw`](../G/bpy.types.Gizmo.md#bpy.types.Gizmo.draw "bpy.types.Gizmo.draw")
  * [`Gizmo.draw_select`](../G/bpy.types.Gizmo.md#bpy.types.Gizmo.draw_select "bpy.types.Gizmo.draw_select")
  * [`Gizmo.exit`](../G/bpy.types.Gizmo.md#bpy.types.Gizmo.exit "bpy.types.Gizmo.exit")
  * [`Gizmo.invoke`](../G/bpy.types.Gizmo.md#bpy.types.Gizmo.invoke "bpy.types.Gizmo.invoke")
  * [`Gizmo.modal`](../G/bpy.types.Gizmo.md#bpy.types.Gizmo.modal "bpy.types.Gizmo.modal")
  * [`Gizmo.test_select`](../G/bpy.types.Gizmo.md#bpy.types.Gizmo.test_select "bpy.types.Gizmo.test_select")
  * [`GizmoGroup.draw_prepare`](../G/bpy.types.GizmoGroup.md#bpy.types.GizmoGroup.draw_prepare "bpy.types.GizmoGroup.draw_prepare")
  * [`GizmoGroup.invoke_prepare`](../G/bpy.types.GizmoGroup.md#bpy.types.GizmoGroup.invoke_prepare "bpy.types.GizmoGroup.invoke_prepare")
  * [`GizmoGroup.poll`](../G/bpy.types.GizmoGroup.md#bpy.types.GizmoGroup.poll "bpy.types.GizmoGroup.poll")
  * [`GizmoGroup.refresh`](../G/bpy.types.GizmoGroup.md#bpy.types.GizmoGroup.refresh "bpy.types.GizmoGroup.refresh")
  * [`GizmoGroup.setup`](../G/bpy.types.GizmoGroup.md#bpy.types.GizmoGroup.setup "bpy.types.GizmoGroup.setup")
  * [`Header.draw`](../H/bpy.types.Header.md#bpy.types.Header.draw "bpy.types.Header.draw")
  * [`KeyingSetInfo.generate`](../K/bpy.types.KeyingSetInfo.md#bpy.types.KeyingSetInfo.generate "bpy.types.KeyingSetInfo.generate")
  * [`KeyingSetInfo.iterator`](../K/bpy.types.KeyingSetInfo.md#bpy.types.KeyingSetInfo.iterator "bpy.types.KeyingSetInfo.iterator")
  * [`KeyingSetInfo.poll`](../K/bpy.types.KeyingSetInfo.md#bpy.types.KeyingSetInfo.poll "bpy.types.KeyingSetInfo.poll")
  * [`Macro.draw`](../M/bpy.types.Macro.md#bpy.types.Macro.draw "bpy.types.Macro.draw")
  * [`Macro.poll`](../M/bpy.types.Macro.md#bpy.types.Macro.poll "bpy.types.Macro.poll")
  * [`Menu.draw`](../M/bpy.types.Menu.md#bpy.types.Menu.draw "bpy.types.Menu.draw")
  * [`Menu.poll`](../M/bpy.types.Menu.md#bpy.types.Menu.poll "bpy.types.Menu.poll")
  * [`Node.draw_buttons`](../N/bpy.types.Node.md#bpy.types.Node.draw_buttons "bpy.types.Node.draw_buttons")
  * [`Node.draw_buttons_ext`](../N/bpy.types.Node.md#bpy.types.Node.draw_buttons_ext "bpy.types.Node.draw_buttons_ext")
  * [`Node.init`](../N/bpy.types.Node.md#bpy.types.Node.init "bpy.types.Node.init")
  * [`Node.socket_value_update`](../N/bpy.types.Node.md#bpy.types.Node.socket_value_update "bpy.types.Node.socket_value_update")
  * [`NodeInternal.draw_buttons`](../N/bpy.types.NodeInternal.md#bpy.types.NodeInternal.draw_buttons "bpy.types.NodeInternal.draw_buttons")
  * [`NodeInternal.draw_buttons_ext`](../N/bpy.types.NodeInternal.md#bpy.types.NodeInternal.draw_buttons_ext "bpy.types.NodeInternal.draw_buttons_ext")
  * [`NodeSocket.draw`](../N/bpy.types.NodeSocket.md#bpy.types.NodeSocket.draw "bpy.types.NodeSocket.draw")
  * [`NodeSocket.draw_color`](../N/bpy.types.NodeSocket.md#bpy.types.NodeSocket.draw_color "bpy.types.NodeSocket.draw_color")
  * [`NodeSocketStandard.draw`](../N/bpy.types.NodeSocketStandard.md#bpy.types.NodeSocketStandard.draw "bpy.types.NodeSocketStandard.draw")
  * [`NodeSocketStandard.draw_color`](../N/bpy.types.NodeSocketStandard.md#bpy.types.NodeSocketStandard.draw_color "bpy.types.NodeSocketStandard.draw_color")
  * [`NodeTree.get_from_context`](../N/bpy.types.NodeTree.md#bpy.types.NodeTree.get_from_context "bpy.types.NodeTree.get_from_context")
  * [`NodeTree.interface_update`](../N/bpy.types.NodeTree.md#bpy.types.NodeTree.interface_update "bpy.types.NodeTree.interface_update")
  * [`NodeTree.poll`](../N/bpy.types.NodeTree.md#bpy.types.NodeTree.poll "bpy.types.NodeTree.poll")
  * [`NodeTreeInterfaceSocket.draw`](../N/bpy.types.NodeTreeInterfaceSocket.md#bpy.types.NodeTreeInterfaceSocket.draw "bpy.types.NodeTreeInterfaceSocket.draw")
  * [`NodeTreeInterfaceSocketBool.draw`](../N/bpy.types.NodeTreeInterfaceSocketBool.md#bpy.types.NodeTreeInterfaceSocketBool.draw "bpy.types.NodeTreeInterfaceSocketBool.draw")
  * [`NodeTreeInterfaceSocketBundle.draw`](../N/bpy.types.NodeTreeInterfaceSocketBundle.md#bpy.types.NodeTreeInterfaceSocketBundle.draw "bpy.types.NodeTreeInterfaceSocketBundle.draw")
  * [`NodeTreeInterfaceSocketClosure.draw`](../N/bpy.types.NodeTreeInterfaceSocketClosure.md#bpy.types.NodeTreeInterfaceSocketClosure.draw "bpy.types.NodeTreeInterfaceSocketClosure.draw")
  * [`NodeTreeInterfaceSocketCollection.draw`](../N/bpy.types.NodeTreeInterfaceSocketCollection.md#bpy.types.NodeTreeInterfaceSocketCollection.draw "bpy.types.NodeTreeInterfaceSocketCollection.draw")
  * [`NodeTreeInterfaceSocketColor.draw`](../N/bpy.types.NodeTreeInterfaceSocketColor.md#bpy.types.NodeTreeInterfaceSocketColor.draw "bpy.types.NodeTreeInterfaceSocketColor.draw")
  * [`NodeTreeInterfaceSocketFloat.draw`](../N/bpy.types.NodeTreeInterfaceSocketFloat.md#bpy.types.NodeTreeInterfaceSocketFloat.draw "bpy.types.NodeTreeInterfaceSocketFloat.draw")
  * [`NodeTreeInterfaceSocketFloatAngle.draw`](../N/bpy.types.NodeTreeInterfaceSocketFloatAngle.md#bpy.types.NodeTreeInterfaceSocketFloatAngle.draw "bpy.types.NodeTreeInterfaceSocketFloatAngle.draw")
  * [`NodeTreeInterfaceSocketFloatColorTemperature.draw`](../N/bpy.types.NodeTreeInterfaceSocketFloatColorTemperature.md#bpy.types.NodeTreeInterfaceSocketFloatColorTemperature.draw "bpy.types.NodeTreeInterfaceSocketFloatColorTemperature.draw")
  * [`NodeTreeInterfaceSocketFloatDistance.draw`](../N/bpy.types.NodeTreeInterfaceSocketFloatDistance.md#bpy.types.NodeTreeInterfaceSocketFloatDistance.draw "bpy.types.NodeTreeInterfaceSocketFloatDistance.draw")
  * [`NodeTreeInterfaceSocketFloatFactor.draw`](../N/bpy.types.NodeTreeInterfaceSocketFloatFactor.md#bpy.types.NodeTreeInterfaceSocketFloatFactor.draw "bpy.types.NodeTreeInterfaceSocketFloatFactor.draw")
  * [`NodeTreeInterfaceSocketFloatFrequency.draw`](../N/bpy.types.NodeTreeInterfaceSocketFloatFrequency.md#bpy.types.NodeTreeInterfaceSocketFloatFrequency.draw "bpy.types.NodeTreeInterfaceSocketFloatFrequency.draw")
  * [`NodeTreeInterfaceSocketFloatPercentage.draw`](../N/bpy.types.NodeTreeInterfaceSocketFloatPercentage.md#bpy.types.NodeTreeInterfaceSocketFloatPercentage.draw "bpy.types.NodeTreeInterfaceSocketFloatPercentage.draw")
  * [`NodeTreeInterfaceSocketFloatTime.draw`](../N/bpy.types.NodeTreeInterfaceSocketFloatTime.md#bpy.types.NodeTreeInterfaceSocketFloatTime.draw "bpy.types.NodeTreeInterfaceSocketFloatTime.draw")
  * [`NodeTreeInterfaceSocketFloatTimeAbsolute.draw`](../N/bpy.types.NodeTreeInterfaceSocketFloatTimeAbsolute.md#bpy.types.NodeTreeInterfaceSocketFloatTimeAbsolute.draw "bpy.types.NodeTreeInterfaceSocketFloatTimeAbsolute.draw")
  * [`NodeTreeInterfaceSocketFloatUnsigned.draw`](../N/bpy.types.NodeTreeInterfaceSocketFloatUnsigned.md#bpy.types.NodeTreeInterfaceSocketFloatUnsigned.draw "bpy.types.NodeTreeInterfaceSocketFloatUnsigned.draw")
  * [`NodeTreeInterfaceSocketFloatWavelength.draw`](../N/bpy.types.NodeTreeInterfaceSocketFloatWavelength.md#bpy.types.NodeTreeInterfaceSocketFloatWavelength.draw "bpy.types.NodeTreeInterfaceSocketFloatWavelength.draw")
  * [`NodeTreeInterfaceSocketGeometry.draw`](../N/bpy.types.NodeTreeInterfaceSocketGeometry.md#bpy.types.NodeTreeInterfaceSocketGeometry.draw "bpy.types.NodeTreeInterfaceSocketGeometry.draw")
  * [`NodeTreeInterfaceSocketImage.draw`](../N/bpy.types.NodeTreeInterfaceSocketImage.md#bpy.types.NodeTreeInterfaceSocketImage.draw "bpy.types.NodeTreeInterfaceSocketImage.draw")
  * [`NodeTreeInterfaceSocketInt.draw`](../N/bpy.types.NodeTreeInterfaceSocketInt.md#bpy.types.NodeTreeInterfaceSocketInt.draw "bpy.types.NodeTreeInterfaceSocketInt.draw")
  * [`NodeTreeInterfaceSocketIntFactor.draw`](../N/bpy.types.NodeTreeInterfaceSocketIntFactor.md#bpy.types.NodeTreeInterfaceSocketIntFactor.draw "bpy.types.NodeTreeInterfaceSocketIntFactor.draw")
  * [`NodeTreeInterfaceSocketIntPercentage.draw`](../N/bpy.types.NodeTreeInterfaceSocketIntPercentage.md#bpy.types.NodeTreeInterfaceSocketIntPercentage.draw "bpy.types.NodeTreeInterfaceSocketIntPercentage.draw")
  * [`NodeTreeInterfaceSocketIntUnsigned.draw`](../N/bpy.types.NodeTreeInterfaceSocketIntUnsigned.md#bpy.types.NodeTreeInterfaceSocketIntUnsigned.draw "bpy.types.NodeTreeInterfaceSocketIntUnsigned.draw")
  * [`NodeTreeInterfaceSocketMaterial.draw`](../N/bpy.types.NodeTreeInterfaceSocketMaterial.md#bpy.types.NodeTreeInterfaceSocketMaterial.draw "bpy.types.NodeTreeInterfaceSocketMaterial.draw")
  * [`NodeTreeInterfaceSocketMatrix.draw`](../N/bpy.types.NodeTreeInterfaceSocketMatrix.md#bpy.types.NodeTreeInterfaceSocketMatrix.draw "bpy.types.NodeTreeInterfaceSocketMatrix.draw")
  * [`NodeTreeInterfaceSocketMenu.draw`](../N/bpy.types.NodeTreeInterfaceSocketMenu.md#bpy.types.NodeTreeInterfaceSocketMenu.draw "bpy.types.NodeTreeInterfaceSocketMenu.draw")
  * [`NodeTreeInterfaceSocketObject.draw`](../N/bpy.types.NodeTreeInterfaceSocketObject.md#bpy.types.NodeTreeInterfaceSocketObject.draw "bpy.types.NodeTreeInterfaceSocketObject.draw")
  * [`NodeTreeInterfaceSocketRotation.draw`](../N/bpy.types.NodeTreeInterfaceSocketRotation.md#bpy.types.NodeTreeInterfaceSocketRotation.draw "bpy.types.NodeTreeInterfaceSocketRotation.draw")

| 

  * [`NodeTreeInterfaceSocketShader.draw`](../N/bpy.types.NodeTreeInterfaceSocketShader.md#bpy.types.NodeTreeInterfaceSocketShader.draw "bpy.types.NodeTreeInterfaceSocketShader.draw")
  * [`NodeTreeInterfaceSocketString.draw`](../N/bpy.types.NodeTreeInterfaceSocketString.md#bpy.types.NodeTreeInterfaceSocketString.draw "bpy.types.NodeTreeInterfaceSocketString.draw")
  * [`NodeTreeInterfaceSocketStringFilePath.draw`](../N/bpy.types.NodeTreeInterfaceSocketStringFilePath.md#bpy.types.NodeTreeInterfaceSocketStringFilePath.draw "bpy.types.NodeTreeInterfaceSocketStringFilePath.draw")
  * [`NodeTreeInterfaceSocketTexture.draw`](../N/bpy.types.NodeTreeInterfaceSocketTexture.md#bpy.types.NodeTreeInterfaceSocketTexture.draw "bpy.types.NodeTreeInterfaceSocketTexture.draw")
  * [`NodeTreeInterfaceSocketVector.draw`](../N/bpy.types.NodeTreeInterfaceSocketVector.md#bpy.types.NodeTreeInterfaceSocketVector.draw "bpy.types.NodeTreeInterfaceSocketVector.draw")
  * [`NodeTreeInterfaceSocketVector2D.draw`](../N/bpy.types.NodeTreeInterfaceSocketVector2D.md#bpy.types.NodeTreeInterfaceSocketVector2D.draw "bpy.types.NodeTreeInterfaceSocketVector2D.draw")
  * [`NodeTreeInterfaceSocketVector4D.draw`](../N/bpy.types.NodeTreeInterfaceSocketVector4D.md#bpy.types.NodeTreeInterfaceSocketVector4D.draw "bpy.types.NodeTreeInterfaceSocketVector4D.draw")
  * [`NodeTreeInterfaceSocketVectorAcceleration.draw`](../N/bpy.types.NodeTreeInterfaceSocketVectorAcceleration.md#bpy.types.NodeTreeInterfaceSocketVectorAcceleration.draw "bpy.types.NodeTreeInterfaceSocketVectorAcceleration.draw")
  * [`NodeTreeInterfaceSocketVectorAcceleration2D.draw`](../N/bpy.types.NodeTreeInterfaceSocketVectorAcceleration2D.md#bpy.types.NodeTreeInterfaceSocketVectorAcceleration2D.draw "bpy.types.NodeTreeInterfaceSocketVectorAcceleration2D.draw")
  * [`NodeTreeInterfaceSocketVectorAcceleration4D.draw`](../N/bpy.types.NodeTreeInterfaceSocketVectorAcceleration4D.md#bpy.types.NodeTreeInterfaceSocketVectorAcceleration4D.draw "bpy.types.NodeTreeInterfaceSocketVectorAcceleration4D.draw")
  * [`NodeTreeInterfaceSocketVectorDirection.draw`](../N/bpy.types.NodeTreeInterfaceSocketVectorDirection.md#bpy.types.NodeTreeInterfaceSocketVectorDirection.draw "bpy.types.NodeTreeInterfaceSocketVectorDirection.draw")
  * [`NodeTreeInterfaceSocketVectorDirection2D.draw`](../N/bpy.types.NodeTreeInterfaceSocketVectorDirection2D.md#bpy.types.NodeTreeInterfaceSocketVectorDirection2D.draw "bpy.types.NodeTreeInterfaceSocketVectorDirection2D.draw")
  * [`NodeTreeInterfaceSocketVectorDirection4D.draw`](../N/bpy.types.NodeTreeInterfaceSocketVectorDirection4D.md#bpy.types.NodeTreeInterfaceSocketVectorDirection4D.draw "bpy.types.NodeTreeInterfaceSocketVectorDirection4D.draw")
  * [`NodeTreeInterfaceSocketVectorEuler.draw`](../N/bpy.types.NodeTreeInterfaceSocketVectorEuler.md#bpy.types.NodeTreeInterfaceSocketVectorEuler.draw "bpy.types.NodeTreeInterfaceSocketVectorEuler.draw")
  * [`NodeTreeInterfaceSocketVectorEuler2D.draw`](../N/bpy.types.NodeTreeInterfaceSocketVectorEuler2D.md#bpy.types.NodeTreeInterfaceSocketVectorEuler2D.draw "bpy.types.NodeTreeInterfaceSocketVectorEuler2D.draw")
  * [`NodeTreeInterfaceSocketVectorEuler4D.draw`](../N/bpy.types.NodeTreeInterfaceSocketVectorEuler4D.md#bpy.types.NodeTreeInterfaceSocketVectorEuler4D.draw "bpy.types.NodeTreeInterfaceSocketVectorEuler4D.draw")
  * [`NodeTreeInterfaceSocketVectorFactor.draw`](../N/bpy.types.NodeTreeInterfaceSocketVectorFactor.md#bpy.types.NodeTreeInterfaceSocketVectorFactor.draw "bpy.types.NodeTreeInterfaceSocketVectorFactor.draw")
  * [`NodeTreeInterfaceSocketVectorFactor2D.draw`](../N/bpy.types.NodeTreeInterfaceSocketVectorFactor2D.md#bpy.types.NodeTreeInterfaceSocketVectorFactor2D.draw "bpy.types.NodeTreeInterfaceSocketVectorFactor2D.draw")
  * [`NodeTreeInterfaceSocketVectorFactor4D.draw`](../N/bpy.types.NodeTreeInterfaceSocketVectorFactor4D.md#bpy.types.NodeTreeInterfaceSocketVectorFactor4D.draw "bpy.types.NodeTreeInterfaceSocketVectorFactor4D.draw")
  * [`NodeTreeInterfaceSocketVectorPercentage.draw`](../N/bpy.types.NodeTreeInterfaceSocketVectorPercentage.md#bpy.types.NodeTreeInterfaceSocketVectorPercentage.draw "bpy.types.NodeTreeInterfaceSocketVectorPercentage.draw")
  * [`NodeTreeInterfaceSocketVectorPercentage2D.draw`](../N/bpy.types.NodeTreeInterfaceSocketVectorPercentage2D.md#bpy.types.NodeTreeInterfaceSocketVectorPercentage2D.draw "bpy.types.NodeTreeInterfaceSocketVectorPercentage2D.draw")
  * [`NodeTreeInterfaceSocketVectorPercentage4D.draw`](../N/bpy.types.NodeTreeInterfaceSocketVectorPercentage4D.md#bpy.types.NodeTreeInterfaceSocketVectorPercentage4D.draw "bpy.types.NodeTreeInterfaceSocketVectorPercentage4D.draw")
  * [`NodeTreeInterfaceSocketVectorTranslation.draw`](../N/bpy.types.NodeTreeInterfaceSocketVectorTranslation.md#bpy.types.NodeTreeInterfaceSocketVectorTranslation.draw "bpy.types.NodeTreeInterfaceSocketVectorTranslation.draw")
  * [`NodeTreeInterfaceSocketVectorTranslation2D.draw`](../N/bpy.types.NodeTreeInterfaceSocketVectorTranslation2D.md#bpy.types.NodeTreeInterfaceSocketVectorTranslation2D.draw "bpy.types.NodeTreeInterfaceSocketVectorTranslation2D.draw")
  * [`NodeTreeInterfaceSocketVectorTranslation4D.draw`](../N/bpy.types.NodeTreeInterfaceSocketVectorTranslation4D.md#bpy.types.NodeTreeInterfaceSocketVectorTranslation4D.draw "bpy.types.NodeTreeInterfaceSocketVectorTranslation4D.draw")
  * [`NodeTreeInterfaceSocketVectorVelocity.draw`](../N/bpy.types.NodeTreeInterfaceSocketVectorVelocity.md#bpy.types.NodeTreeInterfaceSocketVectorVelocity.draw "bpy.types.NodeTreeInterfaceSocketVectorVelocity.draw")
  * [`NodeTreeInterfaceSocketVectorVelocity2D.draw`](../N/bpy.types.NodeTreeInterfaceSocketVectorVelocity2D.md#bpy.types.NodeTreeInterfaceSocketVectorVelocity2D.draw "bpy.types.NodeTreeInterfaceSocketVectorVelocity2D.draw")
  * [`NodeTreeInterfaceSocketVectorVelocity4D.draw`](../N/bpy.types.NodeTreeInterfaceSocketVectorVelocity4D.md#bpy.types.NodeTreeInterfaceSocketVectorVelocity4D.draw "bpy.types.NodeTreeInterfaceSocketVectorVelocity4D.draw")
  * [`NodeTreeInterfaceSocketVectorXYZ.draw`](../N/bpy.types.NodeTreeInterfaceSocketVectorXYZ.md#bpy.types.NodeTreeInterfaceSocketVectorXYZ.draw "bpy.types.NodeTreeInterfaceSocketVectorXYZ.draw")
  * [`NodeTreeInterfaceSocketVectorXYZ2D.draw`](../N/bpy.types.NodeTreeInterfaceSocketVectorXYZ2D.md#bpy.types.NodeTreeInterfaceSocketVectorXYZ2D.draw "bpy.types.NodeTreeInterfaceSocketVectorXYZ2D.draw")
  * [`NodeTreeInterfaceSocketVectorXYZ4D.draw`](../N/bpy.types.NodeTreeInterfaceSocketVectorXYZ4D.md#bpy.types.NodeTreeInterfaceSocketVectorXYZ4D.draw "bpy.types.NodeTreeInterfaceSocketVectorXYZ4D.draw")
  * [`Operator.cancel`](../O/bpy.types.Operator.md#bpy.types.Operator.cancel "bpy.types.Operator.cancel")
  * [`Operator.check`](../O/bpy.types.Operator.md#bpy.types.Operator.check "bpy.types.Operator.check")
  * [`Operator.description`](../O/bpy.types.Operator.md#bpy.types.Operator.description "bpy.types.Operator.description")
  * [`Operator.draw`](../O/bpy.types.Operator.md#bpy.types.Operator.draw "bpy.types.Operator.draw")
  * [`Operator.execute`](../O/bpy.types.Operator.md#bpy.types.Operator.execute "bpy.types.Operator.execute")
  * [`Operator.invoke`](../O/bpy.types.Operator.md#bpy.types.Operator.invoke "bpy.types.Operator.invoke")
  * [`Operator.modal`](../O/bpy.types.Operator.md#bpy.types.Operator.modal "bpy.types.Operator.modal")
  * [`Operator.poll`](../O/bpy.types.Operator.md#bpy.types.Operator.poll "bpy.types.Operator.poll")
  * [`Panel.draw`](../P/bpy.types.Panel.md#bpy.types.Panel.draw "bpy.types.Panel.draw")
  * [`Panel.draw_header`](../P/bpy.types.Panel.md#bpy.types.Panel.draw_header "bpy.types.Panel.draw_header")
  * [`Panel.draw_header_preset`](../P/bpy.types.Panel.md#bpy.types.Panel.draw_header_preset "bpy.types.Panel.draw_header_preset")
  * [`Panel.poll`](../P/bpy.types.Panel.md#bpy.types.Panel.poll "bpy.types.Panel.poll")
  * [`RenderEngine.draw`](../R/bpy.types.RenderEngine.md#bpy.types.RenderEngine.draw "bpy.types.RenderEngine.draw")
  * [`RenderEngine.view_draw`](../R/bpy.types.RenderEngine.md#bpy.types.RenderEngine.view_draw "bpy.types.RenderEngine.view_draw")
  * [`RenderEngine.view_update`](../R/bpy.types.RenderEngine.md#bpy.types.RenderEngine.view_update "bpy.types.RenderEngine.view_update")
  * [`UIList.draw_filter`](../U/bpy.types.UIList.md#bpy.types.UIList.draw_filter "bpy.types.UIList.draw_filter")
  * [`UIList.draw_item`](../U/bpy.types.UIList.md#bpy.types.UIList.draw_item "bpy.types.UIList.draw_item")
  * [`UIList.filter_items`](../U/bpy.types.UIList.md#bpy.types.UIList.filter_items "bpy.types.UIList.filter_items")
  * [`XrSessionState.action_binding_create`](../X/bpy.types.XrSessionState.md#bpy.types.XrSessionState.action_binding_create "bpy.types.XrSessionState.action_binding_create")
  * [`XrSessionState.action_create`](../X/bpy.types.XrSessionState.md#bpy.types.XrSessionState.action_create "bpy.types.XrSessionState.action_create")
  * [`XrSessionState.action_set_create`](../X/bpy.types.XrSessionState.md#bpy.types.XrSessionState.action_set_create "bpy.types.XrSessionState.action_set_create")
  * [`XrSessionState.action_state_get`](../X/bpy.types.XrSessionState.md#bpy.types.XrSessionState.action_state_get "bpy.types.XrSessionState.action_state_get")
  * [`XrSessionState.active_action_set_set`](../X/bpy.types.XrSessionState.md#bpy.types.XrSessionState.active_action_set_set "bpy.types.XrSessionState.active_action_set_set")
  * [`XrSessionState.controller_aim_location_get`](../X/bpy.types.XrSessionState.md#bpy.types.XrSessionState.controller_aim_location_get "bpy.types.XrSessionState.controller_aim_location_get")
  * [`XrSessionState.controller_aim_rotation_get`](../X/bpy.types.XrSessionState.md#bpy.types.XrSessionState.controller_aim_rotation_get "bpy.types.XrSessionState.controller_aim_rotation_get")
  * [`XrSessionState.controller_grip_location_get`](../X/bpy.types.XrSessionState.md#bpy.types.XrSessionState.controller_grip_location_get "bpy.types.XrSessionState.controller_grip_location_get")
  * [`XrSessionState.controller_grip_rotation_get`](../X/bpy.types.XrSessionState.md#bpy.types.XrSessionState.controller_grip_rotation_get "bpy.types.XrSessionState.controller_grip_rotation_get")
  * [`XrSessionState.controller_pose_actions_set`](../X/bpy.types.XrSessionState.md#bpy.types.XrSessionState.controller_pose_actions_set "bpy.types.XrSessionState.controller_pose_actions_set")
  * [`XrSessionState.haptic_action_apply`](../X/bpy.types.XrSessionState.md#bpy.types.XrSessionState.haptic_action_apply "bpy.types.XrSessionState.haptic_action_apply")
  * [`XrSessionState.haptic_action_stop`](../X/bpy.types.XrSessionState.md#bpy.types.XrSessionState.haptic_action_stop "bpy.types.XrSessionState.haptic_action_stop")
  * [`XrSessionState.is_running`](../X/bpy.types.XrSessionState.md#bpy.types.XrSessionState.is_running "bpy.types.XrSessionState.is_running")
  * [`XrSessionState.reset_to_base_pose`](../X/bpy.types.XrSessionState.md#bpy.types.XrSessionState.reset_to_base_pose "bpy.types.XrSessionState.reset_to_base_pose")

  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
  *[*]: Keyword-only parameters separator (PEP 3102)
