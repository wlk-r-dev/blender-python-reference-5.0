# GreasePencilLayer(GreasePencilTreeNode)

base classes — [`bpy_struct`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct "bpy.types.bpy_struct"), [`GreasePencilTreeNode`](bpy.types.GreasePencilTreeNode.md#bpy.types.GreasePencilTreeNode "bpy.types.GreasePencilTreeNode")

_class _bpy.types.GreasePencilLayer(_GreasePencilTreeNode_)
    

Collection of related drawings

blend_mode
    

Blend mode

Type:
    

enum in [`'REGULAR'`, `'HARDLIGHT'`, `'ADD'`, `'SUBTRACT'`, `'MULTIPLY'`, `'DIVIDE'`], default `'REGULAR'`

frames
    

Grease Pencil frames

Type:
    

[`GreasePencilFrames`](bpy.types.GreasePencilFrames.md#bpy.types.GreasePencilFrames "bpy.types.GreasePencilFrames") [`bpy_prop_collection`](../_other/bpy.types.bpy_prop_collection.md#bpy.types.bpy_prop_collection "bpy.types.bpy_prop_collection") of [`GreasePencilFrame`](bpy.types.GreasePencilFrame.md#bpy.types.GreasePencilFrame "bpy.types.GreasePencilFrame"), (readonly)

ignore_locked_materials
    

Allow editing strokes even if they use locked materials

Type:
    

boolean, default False

lock_frame
    

Lock current frame displayed by layer

Type:
    

boolean, default False

mask_layers
    

List of Masking Layers

Type:
    

[`GreasePencilLayerMasks`](bpy.types.GreasePencilLayerMasks.md#bpy.types.GreasePencilLayerMasks "bpy.types.GreasePencilLayerMasks") [`bpy_prop_collection`](../_other/bpy.types.bpy_prop_collection.md#bpy.types.bpy_prop_collection "bpy.types.bpy_prop_collection") of [`GreasePencilLayerMask`](bpy.types.GreasePencilLayerMask.md#bpy.types.GreasePencilLayerMask "bpy.types.GreasePencilLayerMask"), (readonly)

matrix_local
    

Local transformation matrix of the layer

Type:
    

[`mathutils.Matrix`](mathutils.md#mathutils.Matrix "mathutils.Matrix") of 4 * 4 items in [-inf, inf], default ((0.0, 0.0, 0.0, 0.0), (0.0, 0.0, 0.0, 0.0), (0.0, 0.0, 0.0, 0.0), (0.0, 0.0, 0.0, 0.0)), (readonly)

matrix_parent_inverse
    

Inverse of layer’s parent transformation matrix

Type:
    

[`mathutils.Matrix`](mathutils.md#mathutils.Matrix "mathutils.Matrix") of 4 * 4 items in [-inf, inf], default ((0.0, 0.0, 0.0, 0.0), (0.0, 0.0, 0.0, 0.0), (0.0, 0.0, 0.0, 0.0), (0.0, 0.0, 0.0, 0.0)), (readonly)

opacity
    

Layer Opacity

Type:
    

float in [0, 1], default 0.0

parent
    

Parent object

Type:
    

[`Object`](../O/bpy.types.Object.md#bpy.types.Object "bpy.types.Object")

parent_bone
    

Name of parent bone. Only used when the parent object is an armature.

Type:
    

string, default “”, (never None)

pass_index
    

Index number for the “Layer Index” pass

Type:
    

int in [0, inf], default 0

radius_offset
    

Radius change to apply to current strokes

Type:
    

float in [-inf, inf], default 0.0

rotation
    

Euler rotation of the layer

Type:
    

[`mathutils.Euler`](mathutils.md#mathutils.Euler "mathutils.Euler") rotation of 3 items in [-inf, inf], default (0.0, 0.0, 0.0)

scale
    

Scale of the layer

Type:
    

[`mathutils.Vector`](mathutils.md#mathutils.Vector "mathutils.Vector") of 3 items in [-inf, inf], default (1.0, 1.0, 1.0)

tint_color
    

Color for tinting stroke colors

Type:
    

[`mathutils.Color`](mathutils.md#mathutils.Color "mathutils.Color") of 3 items in [0, 1], default (0.0, 0.0, 0.0)

tint_factor
    

Factor of tinting color

Type:
    

float in [0, 1], default 0.0

translation
    

Translation of the layer

Type:
    

[`mathutils.Vector`](mathutils.md#mathutils.Vector "mathutils.Vector") of 3 items in [-inf, inf], default (0.0, 0.0, 0.0)

use_lights
    

Enable the use of lights on stroke and fill materials

Type:
    

boolean, default False

use_viewlayer_masks
    

Include the mask layers when rendering the view-layer

Type:
    

boolean, default False

viewlayer_render
    

Only include Layer in this View Layer render output (leave blank to include always)

Type:
    

string, default “”, (never None)

get_frame_at(_frame_number_)
    

Get the frame at given frame number

Parameters:
    

**frame_number** (_int in_ _[__-1048574_ _,__1048574_ _]_) – Frame Number

Returns:
    

Frame

Return type:
    

[`GreasePencilFrame`](bpy.types.GreasePencilFrame.md#bpy.types.GreasePencilFrame "bpy.types.GreasePencilFrame")

current_frame()
    

The Grease Pencil frame at the current scene time on this layer

Return type:
    

[`GreasePencilFrame`](bpy.types.GreasePencilFrame.md#bpy.types.GreasePencilFrame "bpy.types.GreasePencilFrame")

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

  * [`GreasePencil.layers`](bpy.types.GreasePencil.md#bpy.types.GreasePencil.layers "bpy.types.GreasePencil.layers")
  * [`GreasePencilv3Layers.active`](bpy.types.GreasePencilv3Layers.md#bpy.types.GreasePencilv3Layers.active "bpy.types.GreasePencilv3Layers.active")
  * [`GreasePencilv3Layers.move`](bpy.types.GreasePencilv3Layers.md#bpy.types.GreasePencilv3Layers.move "bpy.types.GreasePencilv3Layers.move")
  * [`GreasePencilv3Layers.move_bottom`](bpy.types.GreasePencilv3Layers.md#bpy.types.GreasePencilv3Layers.move_bottom "bpy.types.GreasePencilv3Layers.move_bottom")

| 

  * [`GreasePencilv3Layers.move_to_layer_group`](bpy.types.GreasePencilv3Layers.md#bpy.types.GreasePencilv3Layers.move_to_layer_group "bpy.types.GreasePencilv3Layers.move_to_layer_group")
  * [`GreasePencilv3Layers.move_top`](bpy.types.GreasePencilv3Layers.md#bpy.types.GreasePencilv3Layers.move_top "bpy.types.GreasePencilv3Layers.move_top")
  * [`GreasePencilv3Layers.new`](bpy.types.GreasePencilv3Layers.md#bpy.types.GreasePencilv3Layers.new "bpy.types.GreasePencilv3Layers.new")
  * [`GreasePencilv3Layers.remove`](bpy.types.GreasePencilv3Layers.md#bpy.types.GreasePencilv3Layers.remove "bpy.types.GreasePencilv3Layers.remove")

  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
