# GreasePencilLayerGroup(GreasePencilTreeNode)

base classes — [`bpy_struct`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct "bpy.types.bpy_struct"), [`GreasePencilTreeNode`](bpy.types.GreasePencilTreeNode.md#bpy.types.GreasePencilTreeNode "bpy.types.GreasePencilTreeNode")

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
  * [`GreasePencilTreeNode.name`](bpy.types.GreasePencilTreeNode.md#bpy.types.GreasePencilTreeNode.name "bpy.types.GreasePencilTreeNode.name")
  * [`GreasePencilTreeNode.hide`](bpy.types.GreasePencilTreeNode.md#bpy.types.GreasePencilTreeNode.hide "bpy.types.GreasePencilTreeNode.hide")
  * [`GreasePencilTreeNode.lock`](bpy.types.GreasePencilTreeNode.md#bpy.types.GreasePencilTreeNode.lock "bpy.types.GreasePencilTreeNode.lock")
  * [`GreasePencilTreeNode.select`](bpy.types.GreasePencilTreeNode.md#bpy.types.GreasePencilTreeNode.select "bpy.types.GreasePencilTreeNode.select")
  * [`GreasePencilTreeNode.use_onion_skinning`](bpy.types.GreasePencilTreeNode.md#bpy.types.GreasePencilTreeNode.use_onion_skinning "bpy.types.GreasePencilTreeNode.use_onion_skinning")

| 

  * [`GreasePencilTreeNode.use_masks`](bpy.types.GreasePencilTreeNode.md#bpy.types.GreasePencilTreeNode.use_masks "bpy.types.GreasePencilTreeNode.use_masks")
  * [`GreasePencilTreeNode.channel_color`](bpy.types.GreasePencilTreeNode.md#bpy.types.GreasePencilTreeNode.channel_color "bpy.types.GreasePencilTreeNode.channel_color")
  * [`GreasePencilTreeNode.next_node`](bpy.types.GreasePencilTreeNode.md#bpy.types.GreasePencilTreeNode.next_node "bpy.types.GreasePencilTreeNode.next_node")
  * [`GreasePencilTreeNode.prev_node`](bpy.types.GreasePencilTreeNode.md#bpy.types.GreasePencilTreeNode.prev_node "bpy.types.GreasePencilTreeNode.prev_node")
  * [`GreasePencilTreeNode.parent_group`](bpy.types.GreasePencilTreeNode.md#bpy.types.GreasePencilTreeNode.parent_group "bpy.types.GreasePencilTreeNode.parent_group")

  
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
  * [`bpy_struct.keyframe_delete`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.keyframe_delete "bpy.types.bpy_struct.keyframe_delete")

| 

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
  * [`GreasePencilTreeNode.bl_rna_get_subclass`](bpy.types.GreasePencilTreeNode.md#bpy.types.GreasePencilTreeNode.bl_rna_get_subclass "bpy.types.GreasePencilTreeNode.bl_rna_get_subclass")
  * [`GreasePencilTreeNode.bl_rna_get_subclass_py`](bpy.types.GreasePencilTreeNode.md#bpy.types.GreasePencilTreeNode.bl_rna_get_subclass_py "bpy.types.GreasePencilTreeNode.bl_rna_get_subclass_py")

  
---|---  
  
## References

  * [`GreasePencil.layer_groups`](bpy.types.GreasePencil.md#bpy.types.GreasePencil.layer_groups "bpy.types.GreasePencil.layer_groups")
  * [`GreasePencilTreeNode.parent_group`](bpy.types.GreasePencilTreeNode.md#bpy.types.GreasePencilTreeNode.parent_group "bpy.types.GreasePencilTreeNode.parent_group")
  * [`GreasePencilv3LayerGroup.active`](bpy.types.GreasePencilv3LayerGroup.md#bpy.types.GreasePencilv3LayerGroup.active "bpy.types.GreasePencilv3LayerGroup.active")
  * [`GreasePencilv3LayerGroup.move`](bpy.types.GreasePencilv3LayerGroup.md#bpy.types.GreasePencilv3LayerGroup.move "bpy.types.GreasePencilv3LayerGroup.move")
  * [`GreasePencilv3LayerGroup.move_bottom`](bpy.types.GreasePencilv3LayerGroup.md#bpy.types.GreasePencilv3LayerGroup.move_bottom "bpy.types.GreasePencilv3LayerGroup.move_bottom")
  * [`GreasePencilv3LayerGroup.move_to_layer_group`](bpy.types.GreasePencilv3LayerGroup.md#bpy.types.GreasePencilv3LayerGroup.move_to_layer_group "bpy.types.GreasePencilv3LayerGroup.move_to_layer_group")
  * [`GreasePencilv3LayerGroup.move_to_layer_group`](bpy.types.GreasePencilv3LayerGroup.md#bpy.types.GreasePencilv3LayerGroup.move_to_layer_group "bpy.types.GreasePencilv3LayerGroup.move_to_layer_group")

| 

  * [`GreasePencilv3LayerGroup.move_top`](bpy.types.GreasePencilv3LayerGroup.md#bpy.types.GreasePencilv3LayerGroup.move_top "bpy.types.GreasePencilv3LayerGroup.move_top")
  * [`GreasePencilv3LayerGroup.new`](bpy.types.GreasePencilv3LayerGroup.md#bpy.types.GreasePencilv3LayerGroup.new "bpy.types.GreasePencilv3LayerGroup.new")
  * [`GreasePencilv3LayerGroup.new`](bpy.types.GreasePencilv3LayerGroup.md#bpy.types.GreasePencilv3LayerGroup.new "bpy.types.GreasePencilv3LayerGroup.new")
  * [`GreasePencilv3LayerGroup.remove`](bpy.types.GreasePencilv3LayerGroup.md#bpy.types.GreasePencilv3LayerGroup.remove "bpy.types.GreasePencilv3LayerGroup.remove")
  * [`GreasePencilv3Layers.move_to_layer_group`](bpy.types.GreasePencilv3Layers.md#bpy.types.GreasePencilv3Layers.move_to_layer_group "bpy.types.GreasePencilv3Layers.move_to_layer_group")
  * [`GreasePencilv3Layers.new`](bpy.types.GreasePencilv3Layers.md#bpy.types.GreasePencilv3Layers.new "bpy.types.GreasePencilv3Layers.new")

  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
