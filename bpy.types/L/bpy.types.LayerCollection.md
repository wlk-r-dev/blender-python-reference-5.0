# LayerCollection(bpy_struct)

base class — [[bpy_struct]]

_class _bpy.types.LayerCollection(_bpy_struct_)
    

Layer collection

children
    

Layer collection children

Type:
    

[[bpy_prop_collection]] of `LayerCollection`, (readonly)

collection
    

Collection this layer collection is wrapping

Type:
    

[[Collection]], (readonly, never None)

exclude
    

Exclude from view layer

Type:
    

boolean, default False

hide_viewport
    

Temporarily hide in viewport

Type:
    

boolean, default False

holdout
    

Mask out objects in collection from view layer

Type:
    

boolean, default False

indirect_only
    

Objects in collection only contribute indirectly (through shadows and reflections) in the view layer

Type:
    

boolean, default False

is_visible
    

Whether this collection is visible for the view layer, take into account the collection parent

Type:
    

boolean, default False, (readonly)

name
    

Name of this layer collection (same as its collection one)

Type:
    

string, default “”, (readonly, never None)

visible_get()
    

Whether this collection is visible, take into account the collection parent and the viewport

Return type:
    

boolean

has_objects()
    

Return type:
    

boolean

has_selected_objects(_view_layer_)
    

Parameters:
    

**view_layer** ([[ViewLayer]]) – View layer the layer collection belongs to

Return type:
    

boolean

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

  * [[bpy.context.collection]]
  * [[Context.layer_collection]]
  * `LayerCollection.children`

| 

  * [[ViewLayer.active_layer_collection]]
  * [[ViewLayer.layer_collection]]

  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
