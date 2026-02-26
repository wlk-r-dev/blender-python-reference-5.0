# GreasePencilv3Layers(bpy_struct)

base class — [[bpy_struct]]

_class _bpy.types.GreasePencilv3Layers(_bpy_struct_)
    

Collection of Grease Pencil layers

active
    

Active Grease Pencil layer

Type:
    

[[GreasePencilLayer]]

new(_name_ , _*_ , _set_active =True_, _layer_group =None_)
    

Add a new Grease Pencil layer

Parameters:
    

  * **name** (_string_ _,__(__never None_ _)_) – Name, Name of the layer

  * **set_active** (_boolean_ _,__(__optional_ _)_) – Set Active, Set the newly created layer as the active layer

  * **layer_group** ([[GreasePencilLayerGroup]], (optional)) – The layer group the new layer will be created in (use None for the main stack)


Returns:
    

The newly created layer

Return type:
    

[[GreasePencilLayer]]

remove(_layer_)
    

Remove a Grease Pencil layer

Parameters:
    

**layer** ([[GreasePencilLayer]], (never None)) – The layer to remove

move(_layer_ , _type_)
    

Move a Grease Pencil layer in the layer group or main stack

Parameters:
    

  * **layer** ([[GreasePencilLayer]], (never None)) – The layer to move

  * **type** (enum in [`'DOWN'`, `'UP'`]) – Direction of movement


move_top(_layer_)
    

Move a Grease Pencil layer to the top of the layer group or main stack

Parameters:
    

**layer** ([[GreasePencilLayer]], (never None)) – The layer to move

move_bottom(_layer_)
    

Move a Grease Pencil layer to the bottom of the layer group or main stack

Parameters:
    

**layer** ([[GreasePencilLayer]], (never None)) – The layer to move

move_to_layer_group(_layer_ , _layer_group_)
    

Move a Grease Pencil layer into a layer group

Parameters:
    

  * **layer** ([[GreasePencilLayer]], (never None)) – The layer to move

  * **layer_group** ([[GreasePencilLayerGroup]]) – The layer group the layer will be moved into (use None for the main stack)


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

  * [[GreasePencil.layers]]

| 


  
---|---
  *[*]: Keyword-only parameters separator (PEP 3102)
  *[/]: Positional-only parameter separator (PEP 570)
