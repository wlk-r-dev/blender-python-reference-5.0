# GreasePencilLayerGroup(GreasePencilTreeNode)

base classes — [[bpy_struct]], [[GreasePencilTreeNode]]

_class _bpy.types.GreasePencilLayerGroup(_GreasePencilTreeNode_)
    

Group of Grease Pencil layers

color_tag
    

Type:
    

enum in [`'NONE'`, `'COLOR1'`, `'COLOR2'`, `'COLOR3'`, `'COLOR4'`, `'COLOR5'`, `'COLOR6'`, `'COLOR7'`, `'COLOR8'`], default `'COLOR1'`

is_expanded
    

The layer group is expanded in the UI

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
  * [[GreasePencilTreeNode.name]]
  * [[GreasePencilTreeNode.hide]]
  * [[GreasePencilTreeNode.lock]]
  * [[GreasePencilTreeNode.select]]
  * [[GreasePencilTreeNode.use_onion_skinning]]

| 

  * [[GreasePencilTreeNode.use_masks]]
  * [[GreasePencilTreeNode.channel_color]]
  * [[GreasePencilTreeNode.next_node]]
  * [[GreasePencilTreeNode.prev_node]]
  * [[GreasePencilTreeNode.parent_group]]

  
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
  * [[bpy_struct.keyframe_delete]]

| 

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
  * [[GreasePencilTreeNode.bl_rna_get_subclass]]
  * [[GreasePencilTreeNode.bl_rna_get_subclass_py]]

  
---|---  
  
## References

  * [[GreasePencil.layer_groups]]
  * [[GreasePencilTreeNode.parent_group]]
  * [[GreasePencilv3LayerGroup.active]]
  * [[GreasePencilv3LayerGroup.move]]
  * [[GreasePencilv3LayerGroup.move_bottom]]
  * [[GreasePencilv3LayerGroup.move_to_layer_group]]
  * [[GreasePencilv3LayerGroup.move_to_layer_group]]

| 

  * [[GreasePencilv3LayerGroup.move_top]]
  * [[GreasePencilv3LayerGroup.new]]
  * [[GreasePencilv3LayerGroup.new]]
  * [[GreasePencilv3LayerGroup.remove]]
  * [[GreasePencilv3Layers.move_to_layer_group]]
  * [[GreasePencilv3Layers.new]]

  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
