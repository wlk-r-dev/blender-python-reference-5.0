# SpaceNodeOverlay(bpy_struct)

base class — [[bpy_struct]]

_class _bpy.types.SpaceNodeOverlay(_bpy_struct_)
    

Settings for display of overlays in the Node Editor

preview_shape
    

Preview shape used by the node previews

  * `FLAT` Flat – Use the default flat previews.

  * `3D` 3D – Use the material preview scene for the node previews.


Type:
    

enum in [`'FLAT'`, `'3D'`], default `'FLAT'`

show_context_path
    

Display breadcrumbs for the editor’s context

Type:
    

boolean, default True

show_named_attributes
    

Show when nodes are using named attributes

Type:
    

boolean, default True

show_overlays
    

Display overlays like colored or dashed wires

Type:
    

boolean, default True

show_previews
    

Display each node’s preview if node is toggled

Type:
    

boolean, default False

show_reroute_auto_labels
    

Label reroute nodes based on the label of connected reroute nodes

Type:
    

boolean, default False

show_timing
    

Display each node’s last execution time

Type:
    

boolean, default False

show_wire_color
    

Color node links based on their connected sockets

Type:
    

boolean, default True

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

  * [[SpaceNodeEditor.overlay]]

| 


  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
