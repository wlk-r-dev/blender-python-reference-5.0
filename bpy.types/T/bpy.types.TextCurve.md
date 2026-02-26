# TextCurve(Curve)

base classes — [[bpy_struct]], [[ID]], [[Curve]]

_class _bpy.types.TextCurve(_Curve_)
    

Curve data-block used for storing text

active_textbox
    

Type:
    

int in [-inf, inf], default 0

align_x
    

Text horizontal alignment from the object or text box center

  * `LEFT` Left – Align text to the left.

  * `CENTER` Center – Center text.

  * `RIGHT` Right – Align text to the right.

  * `JUSTIFY` Justify – Align to the left and the right.

  * `FLUSH` Flush – Align to the left and the right, with equal character spacing.


Type:
    

enum in [`'LEFT'`, `'CENTER'`, `'RIGHT'`, `'JUSTIFY'`, `'FLUSH'`], default `'LEFT'`

align_y
    

Text vertical alignment from the object center

  * `TOP` Top – Align text to the top.

  * `TOP_BASELINE` Top Baseline – Align text to the top line’s baseline.

  * `CENTER` Middle – Align text to the middle.

  * `BOTTOM_BASELINE` Bottom Baseline – Align text to the bottom line’s baseline.

  * `BOTTOM` Bottom – Align text to the bottom.


Type:
    

enum in [`'TOP'`, `'TOP_BASELINE'`, `'CENTER'`, `'BOTTOM_BASELINE'`, `'BOTTOM'`], default `'TOP_BASELINE'`

body
    

Content of this text object

Type:
    

string, default “”, (never None)

body_format
    

Stores the style of each character

Type:
    

[[bpy_prop_collection]] of [[TextCharacterFormat]], (readonly)

edit_format
    

Editing settings character formatting

Type:
    

[[TextCharacterFormat]], (readonly)

family
    

Use objects as font characters (give font objects a common name followed by the character they represent, eg. ‘family-a’, ‘family-b’, etc, set this setting to ‘family-’, and turn on Vertex Instancing)

Type:
    

string, default “”, (never None)

follow_curve
    

Curve deforming text object

Type:
    

[[Object]]

font
    

Type:
    

[[VectorFont]]

font_bold
    

Type:
    

[[VectorFont]]

font_bold_italic
    

Type:
    

[[VectorFont]]

font_italic
    

Type:
    

[[VectorFont]]

has_selection
    

Whether there is any text selected

Type:
    

boolean, default False, (readonly)

is_select_bold
    

Whether the selected text is bold

Type:
    

boolean, default False, (readonly)

is_select_italic
    

Whether the selected text is italics

Type:
    

boolean, default False, (readonly)

is_select_smallcaps
    

Whether the selected text is small caps

Type:
    

boolean, default False, (readonly)

is_select_underline
    

Whether the selected text is underlined

Type:
    

boolean, default False, (readonly)

offset_x
    

Horizontal offset from the object origin

Type:
    

float in [-inf, inf], default 0.0

offset_y
    

Vertical offset from the object origin

Type:
    

float in [-inf, inf], default 0.0

overflow
    

Handle the text behavior when it does not fit in the text boxes

  * `NONE` Overflow – Let the text overflow outside the text boxes.

  * `SCALE` Scale to Fit – Scale down the text to fit inside the text boxes.

  * `TRUNCATE` Truncate – Truncate the text that would go outside the text boxes.


Type:
    

enum in [`'NONE'`, `'SCALE'`, `'TRUNCATE'`], default `'NONE'`

shear
    

Italic angle of the characters

Type:
    

float in [-1, 1], default 0.0

size
    

Type:
    

float in [0.0001, 10000], default 1.0

small_caps_scale
    

Scale of small capitals

Type:
    

float in [-inf, inf], default 0.75

space_character
    

Type:
    

float in [0, 10], default 1.0

space_line
    

Type:
    

float in [0, 10], default 1.0

space_word
    

Type:
    

float in [0, 10], default 1.0

text_boxes
    

Type:
    

[[bpy_prop_collection]] of [[TextBox]], (readonly)

underline_height
    

Type:
    

float in [0, 0.8], default 0.05

underline_position
    

Vertical position of underline

Type:
    

float in [-0.2, 0.8], default 0.0

use_fast_edit
    

Don’t fill polygons while editing

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
  * [[ID.name]]
  * [[ID.name_full]]
  * [[ID.id_type]]
  * [[ID.session_uid]]
  * [[ID.is_evaluated]]
  * [[ID.original]]
  * [[ID.users]]
  * [[ID.use_fake_user]]
  * [[ID.use_extra_user]]
  * [[ID.is_embedded_data]]
  * [[ID.is_linked_packed]]
  * [[ID.is_missing]]
  * [[ID.is_runtime_data]]
  * [[ID.is_editable]]
  * [[ID.tag]]
  * [[ID.is_library_indirect]]
  * [[ID.library]]
  * [[ID.library_weak_reference]]
  * [[ID.asset_data]]
  * [[ID.override_library]]
  * [[ID.preview]]
  * [[Curve.shape_keys]]
  * [[Curve.splines]]
  * [[Curve.path_duration]]
  * [[Curve.use_path]]
  * [[Curve.use_path_follow]]
  * [[Curve.use_path_clamp]]
  * [[Curve.use_stretch]]
  * [[Curve.use_deform_bounds]]
  * [[Curve.use_radius]]

| 

  * [[Curve.bevel_mode]]
  * [[Curve.bevel_profile]]
  * [[Curve.bevel_resolution]]
  * [[Curve.offset]]
  * [[Curve.extrude]]
  * [[Curve.bevel_depth]]
  * [[Curve.resolution_u]]
  * [[Curve.resolution_v]]
  * [[Curve.render_resolution_u]]
  * [[Curve.render_resolution_v]]
  * [[Curve.eval_time]]
  * [[Curve.bevel_object]]
  * [[Curve.taper_object]]
  * [[Curve.dimensions]]
  * [[Curve.fill_mode]]
  * [[Curve.twist_mode]]
  * [[Curve.taper_radius_mode]]
  * [[Curve.bevel_factor_mapping_start]]
  * [[Curve.bevel_factor_mapping_end]]
  * [[Curve.twist_smooth]]
  * [[Curve.use_fill_caps]]
  * [[Curve.use_map_taper]]
  * [[Curve.use_auto_texspace]]
  * [[Curve.texspace_location]]
  * [[Curve.texspace_size]]
  * [[Curve.materials]]
  * [[Curve.bevel_factor_start]]
  * [[Curve.bevel_factor_end]]
  * [[Curve.is_editmode]]
  * [[Curve.animation_data]]
  * [[Curve.cycles]]

  
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

| 

  * [[ID.bl_system_properties_get]]
  * [[ID.rename]]
  * [[ID.evaluated_get]]
  * [[ID.copy]]
  * [[ID.asset_mark]]
  * [[ID.asset_clear]]
  * [[ID.asset_generate_preview]]
  * [[ID.override_create]]
  * [[ID.override_hierarchy_create]]
  * [[ID.user_clear]]
  * [[ID.user_remap]]
  * [[ID.make_local]]
  * [[ID.user_of_id]]
  * [[ID.animation_data_create]]
  * [[ID.animation_data_clear]]
  * [[ID.update_tag]]
  * [[ID.preview_ensure]]
  * [[ID.bl_rna_get_subclass]]
  * [[ID.bl_rna_get_subclass_py]]
  * [[Curve.transform]]
  * [[Curve.validate_material_indices]]
  * [[Curve.update_gpu_tag]]
  * [[Curve.bl_rna_get_subclass]]
  * [[Curve.bl_rna_get_subclass_py]]

  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
