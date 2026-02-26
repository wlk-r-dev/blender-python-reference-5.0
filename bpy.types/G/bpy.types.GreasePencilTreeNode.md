# GreasePencilTreeNode(bpy_struct)

base class — [[bpy_struct]]

subclasses — [[GreasePencilLayer]], [[GreasePencilLayerGroup]]

_class _bpy.types.GreasePencilTreeNode(_bpy_struct_)
    

Grease Pencil node in the layer tree. Either a layer or a group

channel_color
    

Color of the channel in the dope sheet

Type:
    

[[mathutils.Color]] of 3 items in [0, inf], default (0.0, 0.0, 0.0)

hide
    

Set tree node visibility

Type:
    

boolean, default False

lock
    

Protect tree node from editing

Type:
    

boolean, default False

name
    

The name of the tree node

Type:
    

string, default “”, (never None)

next_node
    

The layer tree node after (i.e. above) this one

Type:
    

`GreasePencilTreeNode`, (readonly)

parent_group
    

The parent group of this layer tree node

Type:
    

[[GreasePencilLayerGroup]], (readonly)

prev_node
    

The layer tree node before (i.e. below) this one

Type:
    

`GreasePencilTreeNode`, (readonly)

select
    

Tree node is selected

Type:
    

boolean, default False

use_masks
    

The visibility of drawings in this tree node is affected by the layers in the masks list

Type:
    

boolean, default False

use_onion_skinning
    

Display onion skins before and after the current frame

Type:
    

boolean, default False

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

  * `GreasePencilTreeNode.next_node`

| 

  * `GreasePencilTreeNode.prev_node`

  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
