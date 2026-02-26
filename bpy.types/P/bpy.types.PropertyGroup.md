# PropertyGroup(bpy_struct)

## Custom Properties

PropertyGroups are the base class for dynamically defined sets of properties.

They can be used to extend existing Blender data with your own types which can be animated, accessed from the user interface and from Python.

Note

The values assigned to Blender data are saved to disk but the class definitions are not, this means whenever you load Blender the class needs to be registered too.

This is best done by creating an add-on which loads on startup and registers your properties.

Note

PropertyGroups must be registered before assigning them to Blender data.

See also

Property types used in class declarations are all in [`bpy.props`](../../bpy.props.md#module-bpy.props "bpy.props")
    
    
    import bpy
    
    
    class MyPropertyGroup(bpy.types.PropertyGroup):
        custom_1: bpy.props.FloatProperty(name="My Float")
        custom_2: bpy.props.IntProperty(name="My Int")
    
    
    bpy.utils.register_class(MyPropertyGroup)
    
    bpy.types.Object.my_prop_grp = bpy.props.PointerProperty(type=MyPropertyGroup)
    
    
    # Test this worked.
    bpy.data.objects[0].my_prop_grp.custom_1 = 22.0
    

base class — [`bpy_struct`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct "bpy.types.bpy_struct")

subclasses — [`OperatorFileListElement`](../O/bpy.types.OperatorFileListElement.md#bpy.types.OperatorFileListElement "bpy.types.OperatorFileListElement"), [`OperatorMousePath`](../O/bpy.types.OperatorMousePath.md#bpy.types.OperatorMousePath "bpy.types.OperatorMousePath"), [`OperatorStrokeElement`](../O/bpy.types.OperatorStrokeElement.md#bpy.types.OperatorStrokeElement "bpy.types.OperatorStrokeElement"), [`SelectedUvElement`](../S/bpy.types.SelectedUvElement.md#bpy.types.SelectedUvElement "bpy.types.SelectedUvElement")

_class _bpy.types.PropertyGroup(_bpy_struct_)
    

Group of ID properties

name
    

Unique name used in the code and scripting

Type:
    

string, default “”, (never None)

bl_system_properties_get(_*_ , _do_create =False_)
    

DEBUG ONLY. Internal access to runtime-defined RNA data storage, intended solely for testing and debugging purposes. Do not access it in regular scripting work, and in particular, do not assume that it contains writable data

Parameters:
    

**do_create** (_boolean_ _,__(__optional_ _)_) – Ensure that system properties are created if they do not exist yet

Returns:
    

The system properties root container, or None if there are no system properties stored in this data yet, and its creation was not requested

Return type:
    

`PropertyGroup`

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

### Inherited Properties

  * [`bpy_struct.id_data`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.id_data "bpy.types.bpy_struct.id_data")

| 


  
---|---  
  
### Inherited Functions

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
  
### References

  * [`AddonPreferences.bl_system_properties_get`](../A/bpy.types.AddonPreferences.md#bpy.types.AddonPreferences.bl_system_properties_get "bpy.types.AddonPreferences.bl_system_properties_get")
  * [`Bone.bl_system_properties_get`](../B/bpy.types.Bone.md#bpy.types.Bone.bl_system_properties_get "bpy.types.Bone.bl_system_properties_get")
  * [`BoneCollection.bl_system_properties_get`](../B/bpy.types.BoneCollection.md#bpy.types.BoneCollection.bl_system_properties_get "bpy.types.BoneCollection.bl_system_properties_get")
  * [`CollectionExport.export_properties`](../C/bpy.types.CollectionExport.md#bpy.types.CollectionExport.export_properties "bpy.types.CollectionExport.export_properties")
  * [`EditBone.bl_system_properties_get`](../E/bpy.types.EditBone.md#bpy.types.EditBone.bl_system_properties_get "bpy.types.EditBone.bl_system_properties_get")
  * [`GizmoGroupProperties.bl_system_properties_get`](../G/bpy.types.GizmoGroupProperties.md#bpy.types.GizmoGroupProperties.bl_system_properties_get "bpy.types.GizmoGroupProperties.bl_system_properties_get")
  * [`GizmoProperties.bl_system_properties_get`](../G/bpy.types.GizmoProperties.md#bpy.types.GizmoProperties.bl_system_properties_get "bpy.types.GizmoProperties.bl_system_properties_get")
  * [`ID.bl_system_properties_get`](../I/bpy.types.ID.md#bpy.types.ID.bl_system_properties_get "bpy.types.ID.bl_system_properties_get")
  * [`IDPropertyWrapPtr.bl_system_properties_get`](../I/bpy.types.IDPropertyWrapPtr.md#bpy.types.IDPropertyWrapPtr.bl_system_properties_get "bpy.types.IDPropertyWrapPtr.bl_system_properties_get")
  * [`KeyConfigPreferences.bl_system_properties_get`](../K/bpy.types.KeyConfigPreferences.md#bpy.types.KeyConfigPreferences.bl_system_properties_get "bpy.types.KeyConfigPreferences.bl_system_properties_get")
  * [`Node.bl_system_properties_get`](../N/bpy.types.Node.md#bpy.types.Node.bl_system_properties_get "bpy.types.Node.bl_system_properties_get")
  * [`NodeSocket.bl_system_properties_get`](../N/bpy.types.NodeSocket.md#bpy.types.NodeSocket.bl_system_properties_get "bpy.types.NodeSocket.bl_system_properties_get")
  * [`NodeTreeInterfaceSocket.bl_system_properties_get`](../N/bpy.types.NodeTreeInterfaceSocket.md#bpy.types.NodeTreeInterfaceSocket.bl_system_properties_get "bpy.types.NodeTreeInterfaceSocket.bl_system_properties_get")

| 

  * [`NodesModifier.bl_system_properties_get`](../N/bpy.types.NodesModifier.md#bpy.types.NodesModifier.bl_system_properties_get "bpy.types.NodesModifier.bl_system_properties_get")
  * [`OperatorProperties.bl_system_properties_get`](../O/bpy.types.OperatorProperties.md#bpy.types.OperatorProperties.bl_system_properties_get "bpy.types.OperatorProperties.bl_system_properties_get")
  * [`PoseBone.bl_system_properties_get`](bpy.types.PoseBone.md#bpy.types.PoseBone.bl_system_properties_get "bpy.types.PoseBone.bl_system_properties_get")
  * `PropertyGroup.bl_system_properties_get`
  * [`PropertyGroupItem.collection`](bpy.types.PropertyGroupItem.md#bpy.types.PropertyGroupItem.collection "bpy.types.PropertyGroupItem.collection")
  * [`PropertyGroupItem.group`](bpy.types.PropertyGroupItem.md#bpy.types.PropertyGroupItem.group "bpy.types.PropertyGroupItem.group")
  * [`PropertyGroupItem.idp_array`](bpy.types.PropertyGroupItem.md#bpy.types.PropertyGroupItem.idp_array "bpy.types.PropertyGroupItem.idp_array")
  * [`Strip.bl_system_properties_get`](../S/bpy.types.Strip.md#bpy.types.Strip.bl_system_properties_get "bpy.types.Strip.bl_system_properties_get")
  * [`TimelineMarker.bl_system_properties_get`](../T/bpy.types.TimelineMarker.md#bpy.types.TimelineMarker.bl_system_properties_get "bpy.types.TimelineMarker.bl_system_properties_get")
  * [`UIList.bl_system_properties_get`](../U/bpy.types.UIList.md#bpy.types.UIList.bl_system_properties_get "bpy.types.UIList.bl_system_properties_get")
  * [`View3DShading.bl_system_properties_get`](../V/bpy.types.View3DShading.md#bpy.types.View3DShading.bl_system_properties_get "bpy.types.View3DShading.bl_system_properties_get")
  * [`ViewLayer.bl_system_properties_get`](../V/bpy.types.ViewLayer.md#bpy.types.ViewLayer.bl_system_properties_get "bpy.types.ViewLayer.bl_system_properties_get")

  
---|---
  *[*]: Keyword-only parameters separator (PEP 3102)
  *[/]: Positional-only parameter separator (PEP 570)
