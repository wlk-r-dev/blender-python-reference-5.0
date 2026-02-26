# MeshLoop(bpy_struct)

base class — [[bpy_struct]]

_class _bpy.types.MeshLoop(_bpy_struct_)
    

Loop in a Mesh data-block

bitangent
    

Bitangent vector of this vertex for this face (must be computed beforehand using calc_tangents, use it only if really needed, slower access than bitangent_sign)

Type:
    

[[mathutils.Vector]] of 3 items in [-1, 1], default (0.0, 0.0, 0.0), (readonly)

bitangent_sign
    

Sign of the bitangent vector of this vertex for this face (must be computed beforehand using calc_tangents, bitangent = bitangent_sign * cross(normal, tangent))

Type:
    

float in [-1, 1], default 0.0, (readonly)

edge_index
    

Edge index

Type:
    

int in [0, inf], default 0

index
    

Index of this loop

Type:
    

int in [0, inf], default 0, (readonly)

normal
    

The normal direction of the face corner, taking into account sharp faces, sharp edges, and custom normal data

Type:
    

[[mathutils.Vector]] of 3 items in [-1, 1], default (0.0, 0.0, 0.0), (readonly)

tangent
    

Local space unit length tangent vector of this vertex for this face (must be computed beforehand using calc_tangents)

Type:
    

[[mathutils.Vector]] of 3 items in [-1, 1], default (0.0, 0.0, 0.0), (readonly)

vertex_index
    

Vertex index

Type:
    

int in [0, inf], default 0

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

  * [[Mesh.loops]]

| 


  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
