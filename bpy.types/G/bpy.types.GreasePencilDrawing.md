# GreasePencilDrawing(bpy_struct)

base class — [`bpy_struct`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct "bpy.types.bpy_struct")

_class _bpy.types.GreasePencilDrawing(_bpy_struct_)
    

A Grease Pencil drawing

attributes
    

Geometry attributes

Type:
    

[`AttributeGroupGreasePencilDrawing`](../A/bpy.types.AttributeGroupGreasePencilDrawing.md#bpy.types.AttributeGroupGreasePencilDrawing "bpy.types.AttributeGroupGreasePencilDrawing") [`bpy_prop_collection`](../_other/bpy.types.bpy_prop_collection.md#bpy.types.bpy_prop_collection "bpy.types.bpy_prop_collection") of [`Attribute`](../A/bpy.types.Attribute.md#bpy.types.Attribute "bpy.types.Attribute"), (readonly)

color_attributes
    

Geometry color attributes

Type:
    

[`AttributeGroupGreasePencilDrawing`](../A/bpy.types.AttributeGroupGreasePencilDrawing.md#bpy.types.AttributeGroupGreasePencilDrawing "bpy.types.AttributeGroupGreasePencilDrawing") [`bpy_prop_collection`](../_other/bpy.types.bpy_prop_collection.md#bpy.types.bpy_prop_collection "bpy.types.bpy_prop_collection") of [`Attribute`](../A/bpy.types.Attribute.md#bpy.types.Attribute "bpy.types.Attribute"), (readonly)

curve_offsets
    

Offset indices of the first point of each curve

Type:
    

[`bpy_prop_collection`](../_other/bpy.types.bpy_prop_collection.md#bpy.types.bpy_prop_collection "bpy.types.bpy_prop_collection") of [`IntAttributeValue`](../I/bpy.types.IntAttributeValue.md#bpy.types.IntAttributeValue "bpy.types.IntAttributeValue"), (readonly)

type
    

Drawing type

Type:
    

enum in [`'DRAWING'`, `'REFERENCE'`], default `'DRAWING'`, (readonly)

user_count
    

The number of keyframes this drawing is used by

Type:
    

int in [-inf, inf], default 0, (readonly)

strokes
    

Return a collection of all the Grease Pencil strokes in this drawing.

Note

This API should _not_ be used for performance critical operations. Use the `GreasePencilDrawing.attributes` API instead.

Note

When point/curves count of a drawing is changed, the slice returned by this call prior to the change is no longer valid. You need to get the new stroke slice via `drawing.strokes[n]`.

(readonly)

add_strokes(_sizes_)
    

Add new strokes with provided sizes at the end

Parameters:
    

**sizes** (_int array_ _of_ _1 items in_ _[__1_ _,__inf_ _]_) – Sizes, The number of points in each stroke

remove_strokes(_*_ , _indices =(0,)_)
    

Remove all strokes. If indices are provided, remove only the strokes with the given indices.

Parameters:
    

**indices** (_int array_ _of_ _1 items in_ _[__0_ _,__inf_ _]__,__(__optional_ _)_) – Indices, The indices of the strokes to remove

resize_strokes(_sizes_ , _*_ , _indices =(0,)_)
    

Resize all existing strokes. If indices are provided, resize only the strokes with the given indices. If the new size for a stroke is smaller, the stroke is trimmed. If the new size for a stroke is larger, the new end values are default initialized.

Parameters:
    

  * **sizes** (_int array_ _of_ _1 items in_ _[__1_ _,__inf_ _]_) – Sizes, The number of points in each stroke

  * **indices** (_int array_ _of_ _1 items in_ _[__0_ _,__inf_ _]__,__(__optional_ _)_) – Indices, The indices of the stroke to resize


reorder_strokes(_new_indices_)
    

Reorder the strokes by the new indices.

Parameters:
    

**new_indices** (_int array_ _of_ _1 items in_ _[__0_ _,__inf_ _]_) – New indices, The new index for each of the strokes

set_types(_*_ , _type ='CATMULL_ROM'_, _indices =(0,)_)
    

Set the curve type. If indices are provided, set only the types with the given curve indices.

Parameters:
    

  * **type** (enum in [Curves Type Items](../../bpy_types_enum_items/curves_type_items.md#rna-enum-curves-type-items), (optional)) – Type

  * **indices** (_int array_ _of_ _1 items in_ _[__0_ _,__inf_ _]__,__(__optional_ _)_) – Indices, The indices of the curves to resize


tag_positions_changed()
    

Indicate that the positions of points in the drawing have changed

vertex_group_assign(_vgroup_name_ , _indices_ptr_ , _weight_)
    

Assign points to vertex group

Parameters:
    

  * **vgroup_name** (_string_ _,__(__never None_ _)_) – Vertex Group Name, Name of the vertex group

  * **indices_ptr** (_int array_ _of_ _1 items in_ _[__-inf_ _,__inf_ _]_) – Indices, The point indices to assign the weight to

  * **weight** (_float in_ _[__0_ _,__1_ _]_) – Vertex weight


vertex_group_remove(_vgroup_name_ , _indices_ptr_)
    

Remove points from vertex group

Parameters:
    

  * **vgroup_name** (_string_ _,__(__never None_ _)_) – Vertex Group Name, Name of the vertex group

  * **indices_ptr** (_int array_ _of_ _1 items in_ _[__-inf_ _,__inf_ _]_) – Indices, The point indices to remove from the vertex group


set_vertex_weights(_vertex_group_name_ , _indices_ , _weights_ , _*_ , _assign_mode ='REPLACE'_)
    

Set the weights of vertices in a grease pencil drawing

Parameters:
    

  * **vertex_group_name** (_string_ _,__(__never None_ _)_) – Vertex Group Name, Name of the vertex group

  * **indices** (_int array_ _of_ _1 items in_ _[__-inf_ _,__inf_ _]_) – Indices, The point indices in the vertex group to modify

  * **weights** (_float array_ _of_ _1 items in_ _[__0_ _,__1_ _]_) – Weights, The weight for each corresponding index in the indices array

  * **assign_mode** (enum in [`'REPLACE'`, `'ADD'`, `'SUBTRACT'`], (optional)) – 
    * `REPLACE` Replace – Replace.

    * `ADD` Add – Add.

    * `SUBTRACT` Subtract – Subtract.


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

  * [`GreasePencilFrame.drawing`](bpy.types.GreasePencilFrame.md#bpy.types.GreasePencilFrame.drawing "bpy.types.GreasePencilFrame.drawing")

| 


  
---|---
  *[*]: Keyword-only parameters separator (PEP 3102)
  *[/]: Positional-only parameter separator (PEP 570)
