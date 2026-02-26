# GeometryNodeStringToCurves(GeometryNode)

base classes — [[bpy_struct]], [[Node]], [[NodeInternal]], [[GeometryNode]]

_class _bpy.types.GeometryNodeStringToCurves(_GeometryNode_)
    

Generate a paragraph of text with a specific font, using a curve instance to store each character

align_x
    

Text horizontal alignment from the object or text box center

  * `LEFT` Left – Align text to the left.

  * `CENTER` Center – Align text to the center.

  * `RIGHT` Right – Align text to the right.

  * `JUSTIFY` Justify – Align text to the left and the right.

  * `FLUSH` Flush – Align text to the left and the right, with equal character spacing.


Type:
    

enum in [`'LEFT'`, `'CENTER'`, `'RIGHT'`, `'JUSTIFY'`, `'FLUSH'`], default `'LEFT'`

align_y
    

Text vertical alignment from the object center

  * `TOP` Top – Align text to the top.

  * `TOP_BASELINE` Top Baseline – Align text to the top line’s baseline.

  * `MIDDLE` Middle – Align text to the middle.

  * `BOTTOM_BASELINE` Bottom Baseline – Align text to the bottom line’s baseline.

  * `BOTTOM` Bottom – Align text to the bottom.


Type:
    

enum in [`'TOP'`, `'TOP_BASELINE'`, `'MIDDLE'`, `'BOTTOM_BASELINE'`, `'BOTTOM'`], default `'TOP_BASELINE'`

font
    

Font of the text. Falls back to the UI font by default.

Type:
    

[[VectorFont]]

overflow
    

Handle the text behavior when it does not fit in the text boxes

  * `OVERFLOW` Overflow – Let the text use more space than the specified height.

  * `SCALE_TO_FIT` Scale To Fit – Scale the text size to fit inside the width and height.

  * `TRUNCATE` Truncate – Only output curves that fit within the width and height. Output the remainder to the “Remainder” output..


Type:
    

enum in [`'OVERFLOW'`, `'SCALE_TO_FIT'`, `'TRUNCATE'`], default `'OVERFLOW'`

pivot_mode
    

Pivot point position relative to character

  * `MIDPOINT` Midpoint – Midpoint.

  * `TOP_LEFT` Top Left – Top Left.

  * `TOP_CENTER` Top Center – Top Center.

  * `TOP_RIGHT` Top Right – Top Right.

  * `BOTTOM_LEFT` Bottom Left – Bottom Left.

  * `BOTTOM_CENTER` Bottom Center – Bottom Center.

  * `BOTTOM_RIGHT` Bottom Right – Bottom Right.


Type:
    

enum in [`'MIDPOINT'`, `'TOP_LEFT'`, `'TOP_CENTER'`, `'TOP_RIGHT'`, `'BOTTOM_LEFT'`, `'BOTTOM_CENTER'`, `'BOTTOM_RIGHT'`], default `'BOTTOM_LEFT'`

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
  * `GeometryNode.poll`
  * [[GeometryNode.bl_rna_get_subclass]]
  * [[GeometryNode.bl_rna_get_subclass_py]]

  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
