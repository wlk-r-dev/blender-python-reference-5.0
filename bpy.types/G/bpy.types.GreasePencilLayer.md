# GreasePencilLayer(GreasePencilTreeNode)

base classes — [[bpy_struct]], [[GreasePencilTreeNode]]

_class _bpy.types.GreasePencilLayer(_GreasePencilTreeNode_)
    

Collection of related drawings

blend_mode
    

Blend mode

Type:
    

enum in [`'REGULAR'`, `'HARDLIGHT'`, `'ADD'`, `'SUBTRACT'`, `'MULTIPLY'`, `'DIVIDE'`], default `'REGULAR'`

frames
    

Grease Pencil frames

Type:
    

[[GreasePencilFrames]] [[bpy_prop_collection]] of [[GreasePencilFrame]], (readonly)

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
    

[[GreasePencilLayerMasks]] [[bpy_prop_collection]] of [[GreasePencilLayerMask]], (readonly)

matrix_local
    

Local transformation matrix of the layer

Type:
    

[[mathutils.Matrix]] of 4 * 4 items in [-inf, inf], default ((0.0, 0.0, 0.0, 0.0), (0.0, 0.0, 0.0, 0.0), (0.0, 0.0, 0.0, 0.0), (0.0, 0.0, 0.0, 0.0)), (readonly)

matrix_parent_inverse
    

Inverse of layer’s parent transformation matrix

Type:
    

[[mathutils.Matrix]] of 4 * 4 items in [-inf, inf], default ((0.0, 0.0, 0.0, 0.0), (0.0, 0.0, 0.0, 0.0), (0.0, 0.0, 0.0, 0.0), (0.0, 0.0, 0.0, 0.0)), (readonly)

opacity
    

Layer Opacity

Type:
    

float in [0, 1], default 0.0

parent
    

Parent object

Type:
    

[[Object]]

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
    

[[mathutils.Euler]] rotation of 3 items in [-inf, inf], default (0.0, 0.0, 0.0)

scale
    

Scale of the layer

Type:
    

[[mathutils.Vector]] of 3 items in [-inf, inf], default (1.0, 1.0, 1.0)

tint_color
    

Color for tinting stroke colors

Type:
    

[[mathutils.Color]] of 3 items in [0, 1], default (0.0, 0.0, 0.0)

tint_factor
    

Factor of tinting color

Type:
    

float in [0, 1], default 0.0

translation
    

Translation of the layer

Type:
    

[[mathutils.Vector]] of 3 items in [-inf, inf], default (0.0, 0.0, 0.0)

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
    

[[GreasePencilFrame]]

current_frame()
    

The Grease Pencil frame at the current scene time on this layer

Return type:
    

[[GreasePencilFrame]]

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

  * [[GreasePencil.layers]]
  * [[GreasePencilv3Layers.active]]
  * [[GreasePencilv3Layers.move]]
  * [[GreasePencilv3Layers.move_bottom]]

| 

  * [[GreasePencilv3Layers.move_to_layer_group]]
  * [[GreasePencilv3Layers.move_top]]
  * [[GreasePencilv3Layers.new]]
  * [[GreasePencilv3Layers.remove]]

  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
