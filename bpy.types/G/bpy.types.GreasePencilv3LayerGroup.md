# GreasePencilv3LayerGroup(bpy_struct)

base class — [[bpy_struct]]

_class _bpy.types.GreasePencilv3LayerGroup(_bpy_struct_)
    

Collection of Grease Pencil layers

active
    

Active Grease Pencil layer group

Type:
    

[[GreasePencilLayerGroup]]

new(_name_ , _*_ , _parent_group =None_)
    

Add a new Grease Pencil layer group

Parameters:
    

  * **name** (_string_ _,__(__never None_ _)_) – Name, Name of the layer group

  * **parent_group** ([[GreasePencilLayerGroup]], (optional)) – The parent layer group the new group will be created in (use None for the main stack)


Returns:
    

The newly created layer group

Return type:
    

[[GreasePencilLayerGroup]]

remove(_layer_group_ , _*_ , _keep_children =False_)
    

Remove a new Grease Pencil layer group

Parameters:
    

  * **layer_group** ([[GreasePencilLayerGroup]], (never None)) – The layer group to remove

  * **keep_children** (_boolean_ _,__(__optional_ _)_) – Keep the children nodes of the group and only delete the group itself


move(_layer_group_ , _type_)
    

Move a layer group in the parent layer group or main stack

Parameters:
    

  * **layer_group** ([[GreasePencilLayerGroup]], (never None)) – The layer group to move

  * **type** (enum in [`'DOWN'`, `'UP'`]) – Direction of movement


move_top(_layer_group_)
    

Move a layer group to the top of the parent layer group or main stack

Parameters:
    

**layer_group** ([[GreasePencilLayerGroup]], (never None)) – The layer group to move

move_bottom(_layer_group_)
    

Move a layer group to the bottom of the parent layer group or main stack

Parameters:
    

**layer_group** ([[GreasePencilLayerGroup]], (never None)) – The layer group to move

move_to_layer_group(_layer_group_ , _parent_group_)
    

Move a layer group into a parent layer group

Parameters:
    

  * **layer_group** ([[GreasePencilLayerGroup]], (never None)) – The layer group to move

  * **parent_group** ([[GreasePencilLayerGroup]]) – The parent layer group the layer group will be moved into (use None for the main stack)


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

  * [[GreasePencil.layer_groups]]

| 


  
---|---
  *[*]: Keyword-only parameters separator (PEP 3102)
  *[/]: Positional-only parameter separator (PEP 570)
