# VertexGroup(bpy_struct)

base class — [[bpy_struct]]

_class _bpy.types.VertexGroup(_bpy_struct_)
    

Group of vertices, used for armature deform and other purposes

index
    

Index number of the vertex group

Type:
    

int in [0, inf], default 0, (readonly)

lock_weight
    

Maintain the relative weights for the group

Type:
    

boolean, default False

name
    

Vertex group name

Type:
    

string, default “”, (never None)

add(_index_ , _weight_ , _type_)
    

Add vertices to the group

Parameters:
    

  * **index** (_int array_ _of_ _1 items in_ _[__-inf_ _,__inf_ _]_) – List of indices

  * **weight** (_float in_ _[__0_ _,__1_ _]_) – Vertex weight

  * **type** (enum in [`'REPLACE'`, `'ADD'`, `'SUBTRACT'`]) – 

Vertex assign mode

    * `REPLACE` Replace – Replace.

    * `ADD` Add – Add.

    * `SUBTRACT` Subtract – Subtract.


remove(_index_)
    

Remove vertices from the group

Parameters:
    

**index** (_int array_ _of_ _1 items in_ _[__-inf_ _,__inf_ _]_) – List of indices

weight(_index_)
    

Get a vertex weight from the group

Parameters:
    

**index** (_int in_ _[__0_ _,__inf_ _]_) – Index, The index of the vertex

Returns:
    

Vertex weight

Return type:
    

float in [0, 1]

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

  * [[Object.vertex_groups]]
  * [[VertexGroups.active]]

| 

  * [[VertexGroups.new]]
  * [[VertexGroups.remove]]

  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
