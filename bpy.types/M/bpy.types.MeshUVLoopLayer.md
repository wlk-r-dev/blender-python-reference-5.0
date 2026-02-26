# MeshUVLoopLayer(bpy_struct)

base class — [[bpy_struct]]

_class _bpy.types.MeshUVLoopLayer(_bpy_struct_)
    

active
    

Set the map as active for display and editing

Type:
    

boolean, default False

active_clone
    

Set the map as active for cloning

Type:
    

boolean, default False

active_render
    

Set the UV map as active for rendering

Type:
    

boolean, default False

data
    

Deprecated, use ‘uv’, ‘vertex_select’, ‘edge_select’ or ‘pin’ properties instead

Type:
    

[[bpy_prop_collection]] of [[MeshUVLoop]], (readonly)

name
    

Name of UV map

Type:
    

string, default “”, (never None)

pin
    

UV pinned state in the UV editor

Type:
    

[[bpy_prop_collection]] of [[BoolAttributeValue]], (readonly)

uv
    

UV coordinates on face corners

Type:
    

[[bpy_prop_collection]] of [[Float2AttributeValue]], (readonly)

pin_ensure()
    

pin_ensure

Returns:
    

The boolean attribute

Return type:
    

[[BoolAttribute]]

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

  * [[Mesh.uv_layer_clone]]
  * [[Mesh.uv_layer_stencil]]
  * [[Mesh.uv_layers]]

| 

  * [[UVLoopLayers.active]]
  * [[UVLoopLayers.new]]
  * [[UVLoopLayers.remove]]

  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
