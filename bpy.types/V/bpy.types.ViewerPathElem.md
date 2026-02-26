# ViewerPathElem(bpy_struct)

base class — [[bpy_struct]]

subclasses — [[EvaluateClosureNodeViewerPathElem]], [[ForeachGeometryElementZoneViewerPathElem]], [[GroupNodeViewerPathElem]], [[IDViewerPathElem]], [[ModifierViewerPathElem]], [[RepeatZoneViewerPathElem]], [[SimulationZoneViewerPathElem]], [[ViewerNodeViewerPathElem]]

_class _bpy.types.ViewerPathElem(_bpy_struct_)
    

Element of a viewer path

type
    

Type of the path element

Type:
    

enum in [`'ID'`, `'MODIFIER'`, `'GROUP_NODE'`, `'SIMULATION_ZONE'`, `'VIEWER_NODE'`, `'REPEAT_ZONE'`, `'FOREACH_GEOMETRY_ELEMENT_ZONE'`, `'EVALUATE_CLOSURE'`], default `'ID'`, (readonly)

ui_name
    

Name that can be displayed in the UI for this element

Type:
    

string, default “”, (readonly, never None)

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

  * [[ViewerPath.path]]

| 


  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
