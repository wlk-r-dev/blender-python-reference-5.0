# MeshEdge(bpy_struct)

base class — [[bpy_struct]]

_class _bpy.types.MeshEdge(_bpy_struct_)
    

Edge in a Mesh data-block

hide
    

Type:
    

boolean, default False

index
    

Index of this edge

Type:
    

int in [0, inf], default 0, (readonly)

is_loose
    

Edge is not connected to any faces

Type:
    

boolean, default False, (readonly)

select
    

Type:
    

boolean, default False

use_edge_sharp
    

Sharp edge for shading

Type:
    

boolean, default False

use_seam
    

Seam edge for UV unwrapping

Type:
    

boolean, default False

vertices
    

Vertex indices

Type:
    

int array of 2 items in [0, inf], default (0, 0)

key
    

(readonly)

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

  * [[Mesh.edges]]

| 


  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
