# ShaderNodeTexImage(ShaderNode)

base classes — [[bpy_struct]], [[Node]], [[NodeInternal]], [[ShaderNode]]

_class _bpy.types.ShaderNodeTexImage(_ShaderNode_)
    

Sample an image file as a texture

color_mapping
    

Color mapping settings

Type:
    

[[ColorMapping]], (readonly, never None)

extension
    

How the image is extrapolated past its original bounds

  * `REPEAT` Repeat – Cause the image to repeat horizontally and vertically.

  * `EXTEND` Extend – Extend by repeating edge pixels of the image.

  * `CLIP` Clip – Clip to image size and set exterior pixels as transparent.

  * `MIRROR` Mirror – Repeatedly flip the image horizontally and vertically.


Type:
    

enum in [`'REPEAT'`, `'EXTEND'`, `'CLIP'`, `'MIRROR'`], default `'REPEAT'`

image
    

Type:
    

[[Image]]

image_user
    

Parameters defining which layer, pass and frame of the image is displayed

Type:
    

[[ImageUser]], (readonly, never None)

interpolation
    

Texture interpolation

  * `Linear` Linear – Linear interpolation.

  * `Closest` Closest – No interpolation (sample closest texel).

  * `Cubic` Cubic – Cubic interpolation.

  * `Smart` Smart – Bicubic when magnifying, else bilinear (OSL only).


Type:
    

enum in [`'Linear'`, `'Closest'`, `'Cubic'`, `'Smart'`], default `'Linear'`

projection
    

Method to project 2D image on object with a 3D texture vector

  * `FLAT` Flat – Image is projected flat using the X and Y coordinates of the texture vector.

  * `BOX` Box – Image is projected using different components for each side of the object space bounding box.

  * `SPHERE` Sphere – Image is projected spherically using the Z axis as central.

  * `TUBE` Tube – Image is projected from the tube using the Z axis as central.


Type:
    

enum in [`'FLAT'`, `'BOX'`, `'SPHERE'`, `'TUBE'`], default `'FLAT'`

projection_blend
    

For box projection, amount of blend to use between sides

Type:
    

float in [0, 1], default 0.0

texture_mapping
    

Texture coordinate mapping settings

Type:
    

[[TexMapping]], (readonly, never None)

_classmethod _is_registered_node_type()
    

True if a registered node type

Returns:
    

Result

Return type:
    

boolean

_classmethod _input_template(_index_)
    

Input socket template

Parameters:
    

**index** (_int in_ _[__0_ _,__inf_ _]_) – Index

Returns:
    

result

Return type:
    

[[NodeInternalSocketTemplate]]

_classmethod _output_template(_index_)
    

Output socket template

Parameters:
    

**index** (_int in_ _[__0_ _,__inf_ _]_) – Index

Returns:
    

result

Return type:
    

[[NodeInternalSocketTemplate]]

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
  * [[Node.type]]
  * [[Node.location]]
  * [[Node.location_absolute]]
  * [[Node.width]]
  * [[Node.height]]
  * [[Node.dimensions]]
  * [[Node.name]]
  * [[Node.label]]
  * [[Node.inputs]]
  * [[Node.outputs]]
  * [[Node.internal_links]]
  * [[Node.parent]]
  * [[Node.warning_propagation]]
  * [[Node.use_custom_color]]
  * [[Node.color]]
  * [[Node.color_tag]]

| 

  * [[Node.select]]
  * [[Node.show_options]]
  * [[Node.show_preview]]
  * [[Node.hide]]
  * [[Node.mute]]
  * [[Node.show_texture]]
  * [[Node.bl_idname]]
  * [[Node.bl_label]]
  * [[Node.bl_description]]
  * [[Node.bl_icon]]
  * [[Node.bl_static_type]]
  * [[Node.bl_width_default]]
  * [[Node.bl_width_min]]
  * [[Node.bl_width_max]]
  * [[Node.bl_height_default]]
  * [[Node.bl_height_min]]
  * [[Node.bl_height_max]]

  
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
  * [[Node.bl_system_properties_get]]
  * [[Node.socket_value_update]]

| 

  * [[Node.is_registered_node_type]]
  * [[Node.poll]]
  * [[Node.poll_instance]]
  * [[Node.update]]
  * [[Node.insert_link]]
  * [[Node.init]]
  * [[Node.copy]]
  * [[Node.free]]
  * [[Node.draw_buttons]]
  * [[Node.draw_buttons_ext]]
  * [[Node.draw_label]]
  * [[Node.debug_zone_body_lazy_function_graph]]
  * [[Node.debug_zone_lazy_function_graph]]
  * [[Node.poll]]
  * [[Node.bl_rna_get_subclass]]
  * [[Node.bl_rna_get_subclass_py]]
  * [[NodeInternal.poll]]
  * [[NodeInternal.poll_instance]]
  * [[NodeInternal.update]]
  * [[NodeInternal.draw_buttons]]
  * [[NodeInternal.draw_buttons_ext]]
  * [[NodeInternal.bl_rna_get_subclass]]
  * [[NodeInternal.bl_rna_get_subclass_py]]
  * `ShaderNode.poll`
  * [[ShaderNode.bl_rna_get_subclass]]
  * [[ShaderNode.bl_rna_get_subclass_py]]

  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
