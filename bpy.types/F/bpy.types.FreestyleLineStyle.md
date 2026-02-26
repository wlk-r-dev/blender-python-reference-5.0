# FreestyleLineStyle(ID)

base classes — [`bpy_struct`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct "bpy.types.bpy_struct"), [`ID`](../I/bpy.types.ID.md#bpy.types.ID "bpy.types.ID")

_class _bpy.types.FreestyleLineStyle(_ID_)
    

Freestyle line style, reusable by multiple line sets

active_texture
    

Active texture slot being displayed

Type:
    

[`Texture`](../T/bpy.types.Texture.md#bpy.types.Texture "bpy.types.Texture")

active_texture_index
    

Index of active texture slot

Type:
    

int in [0, 17], default 0

alpha
    

Base alpha transparency, possibly modified by alpha transparency modifiers

Type:
    

float in [0, 1], default 1.0

alpha_modifiers
    

List of alpha transparency modifiers

Type:
    

[`LineStyleAlphaModifiers`](../L/bpy.types.LineStyleAlphaModifiers.md#bpy.types.LineStyleAlphaModifiers "bpy.types.LineStyleAlphaModifiers") [`bpy_prop_collection`](../_other/bpy.types.bpy_prop_collection.md#bpy.types.bpy_prop_collection "bpy.types.bpy_prop_collection") of [`LineStyleAlphaModifier`](../L/bpy.types.LineStyleAlphaModifier.md#bpy.types.LineStyleAlphaModifier "bpy.types.LineStyleAlphaModifier"), (readonly)

angle_max
    

Maximum 2D angle for splitting chains

Type:
    

float in [0, 3.14159], default 0.0

angle_min
    

Minimum 2D angle for splitting chains

Type:
    

float in [0, 3.14159], default 0.0

animation_data
    

Animation data for this data-block

Type:
    

[`AnimData`](../A/bpy.types.AnimData.md#bpy.types.AnimData "bpy.types.AnimData"), (readonly)

caps
    

Select the shape of both ends of strokes

  * `BUTT` Butt – Butt cap (flat).

  * `ROUND` Round – Round cap (half-circle).

  * `SQUARE` Square – Square cap (flat and extended).


Type:
    

enum in [`'BUTT'`, `'ROUND'`, `'SQUARE'`], default `'BUTT'`

chain_count
    

Chain count for the selection of first N chains

Type:
    

int in [0, inf], default 10

chaining
    

Select the way how feature edges are jointed to form chains

  * `PLAIN` Plain – Plain chaining.

  * `SKETCHY` Sketchy – Sketchy chaining with a multiple touch.


Type:
    

enum in [`'PLAIN'`, `'SKETCHY'`], default `'PLAIN'`

color
    

Base line color, possibly modified by line color modifiers

Type:
    

[`mathutils.Color`](mathutils.md#mathutils.Color "mathutils.Color") of 3 items in [0, inf], default (0.0, 0.0, 0.0)

color_modifiers
    

List of line color modifiers

Type:
    

[`LineStyleColorModifiers`](../L/bpy.types.LineStyleColorModifiers.md#bpy.types.LineStyleColorModifiers "bpy.types.LineStyleColorModifiers") [`bpy_prop_collection`](../_other/bpy.types.bpy_prop_collection.md#bpy.types.bpy_prop_collection "bpy.types.bpy_prop_collection") of [`LineStyleColorModifier`](../L/bpy.types.LineStyleColorModifier.md#bpy.types.LineStyleColorModifier "bpy.types.LineStyleColorModifier"), (readonly)

dash1
    

Length of the 1st dash for dashed lines

Type:
    

int in [0, 65535], default 0

dash2
    

Length of the 2nd dash for dashed lines

Type:
    

int in [0, 65535], default 0

dash3
    

Length of the 3rd dash for dashed lines

Type:
    

int in [0, 65535], default 0

gap1
    

Length of the 1st gap for dashed lines

Type:
    

int in [0, 65535], default 0

gap2
    

Length of the 2nd gap for dashed lines

Type:
    

int in [0, 65535], default 0

gap3
    

Length of the 3rd gap for dashed lines

Type:
    

int in [0, 65535], default 0

geometry_modifiers
    

List of stroke geometry modifiers

Type:
    

[`LineStyleGeometryModifiers`](../L/bpy.types.LineStyleGeometryModifiers.md#bpy.types.LineStyleGeometryModifiers "bpy.types.LineStyleGeometryModifiers") [`bpy_prop_collection`](../_other/bpy.types.bpy_prop_collection.md#bpy.types.bpy_prop_collection "bpy.types.bpy_prop_collection") of [`LineStyleGeometryModifier`](../L/bpy.types.LineStyleGeometryModifier.md#bpy.types.LineStyleGeometryModifier "bpy.types.LineStyleGeometryModifier"), (readonly)

integration_type
    

Select the way how the sort key is computed for each chain

  * `MEAN` Mean – The value computed for the chain is the mean of the values obtained for chain vertices.

  * `MIN` Min – The value computed for the chain is the minimum of the values obtained for chain vertices.

  * `MAX` Max – The value computed for the chain is the maximum of the values obtained for chain vertices.

  * `FIRST` First – The value computed for the chain is the value obtained for the first chain vertex.

  * `LAST` Last – The value computed for the chain is the value obtained for the last chain vertex.


Type:
    

enum in [`'MEAN'`, `'MIN'`, `'MAX'`, `'FIRST'`, `'LAST'`], default `'MEAN'`

length_max
    

Maximum curvilinear 2D length for the selection of chains

Type:
    

float in [0, 10000], default 10000.0

length_min
    

Minimum curvilinear 2D length for the selection of chains

Type:
    

float in [0, 10000], default 0.0

material_boundary
    

If true, chains of feature edges are split at material boundaries

Type:
    

boolean, default False

node_tree
    

Node tree for node-based shaders

Type:
    

[`NodeTree`](../N/bpy.types.NodeTree.md#bpy.types.NodeTree "bpy.types.NodeTree"), (readonly)

panel
    

Select the property panel to be shown

  * `STROKES` Strokes – Show the panel for stroke construction.

  * `COLOR` Color – Show the panel for line color options.

  * `ALPHA` Alpha – Show the panel for alpha transparency options.

  * `THICKNESS` Thickness – Show the panel for line thickness options.

  * `GEOMETRY` Geometry – Show the panel for stroke geometry options.

  * `TEXTURE` Texture – Show the panel for stroke texture options.


Type:
    

enum in [`'STROKES'`, `'COLOR'`, `'ALPHA'`, `'THICKNESS'`, `'GEOMETRY'`, `'TEXTURE'`], default `'STROKES'`

rounds
    

Number of rounds in a sketchy multiple touch

Type:
    

int in [1, 1000], default 3

sort_key
    

Select the sort key to determine the stacking order of chains

  * `DISTANCE_FROM_CAMERA` Distance from Camera – Sort by distance from camera (closer lines lie on top of further lines).

  * `2D_LENGTH` 2D Length – Sort by curvilinear 2D length (longer lines lie on top of shorter lines).

  * `PROJECTED_X` Projected X – Sort by the projected X value in the image coordinate system.

  * `PROJECTED_Y` Projected Y – Sort by the projected Y value in the image coordinate system.


Type:
    

enum in [`'DISTANCE_FROM_CAMERA'`, `'2D_LENGTH'`, `'PROJECTED_X'`, `'PROJECTED_Y'`], default `'DISTANCE_FROM_CAMERA'`

sort_order
    

Select the sort order

  * `DEFAULT` Default – Default order of the sort key.

  * `REVERSE` Reverse – Reverse order.


Type:
    

enum in [`'DEFAULT'`, `'REVERSE'`], default `'DEFAULT'`

split_dash1
    

Length of the 1st dash for splitting

Type:
    

int in [0, 65535], default 0

split_dash2
    

Length of the 2nd dash for splitting

Type:
    

int in [0, 65535], default 0

split_dash3
    

Length of the 3rd dash for splitting

Type:
    

int in [0, 65535], default 0

split_gap1
    

Length of the 1st gap for splitting

Type:
    

int in [0, 65535], default 0

split_gap2
    

Length of the 2nd gap for splitting

Type:
    

int in [0, 65535], default 0

split_gap3
    

Length of the 3rd gap for splitting

Type:
    

int in [0, 65535], default 0

split_length
    

Curvilinear 2D length for chain splitting

Type:
    

float in [0, 10000], default 100.0

texture_slots
    

Texture slots defining the mapping and influence of textures

Type:
    

[`LineStyleTextureSlots`](../L/bpy.types.LineStyleTextureSlots.md#bpy.types.LineStyleTextureSlots "bpy.types.LineStyleTextureSlots") [`bpy_prop_collection`](../_other/bpy.types.bpy_prop_collection.md#bpy.types.bpy_prop_collection "bpy.types.bpy_prop_collection") of [`LineStyleTextureSlot`](../L/bpy.types.LineStyleTextureSlot.md#bpy.types.LineStyleTextureSlot "bpy.types.LineStyleTextureSlot"), (readonly)

texture_spacing
    

Spacing for textures along stroke length

Type:
    

float in [0.01, 100], default 1.0

thickness
    

Base line thickness, possibly modified by line thickness modifiers

Type:
    

float in [0, 10000], default 3.0

thickness_modifiers
    

List of line thickness modifiers

Type:
    

[`LineStyleThicknessModifiers`](../L/bpy.types.LineStyleThicknessModifiers.md#bpy.types.LineStyleThicknessModifiers "bpy.types.LineStyleThicknessModifiers") [`bpy_prop_collection`](../_other/bpy.types.bpy_prop_collection.md#bpy.types.bpy_prop_collection "bpy.types.bpy_prop_collection") of [`LineStyleThicknessModifier`](../L/bpy.types.LineStyleThicknessModifier.md#bpy.types.LineStyleThicknessModifier "bpy.types.LineStyleThicknessModifier"), (readonly)

thickness_position
    

Thickness position of silhouettes and border edges (applicable when plain chaining is used with the Same Object option)

  * `CENTER` Center – Silhouettes and border edges are centered along stroke geometry.

  * `INSIDE` Inside – Silhouettes and border edges are drawn inside of stroke geometry.

  * `OUTSIDE` Outside – Silhouettes and border edges are drawn outside of stroke geometry.

  * `RELATIVE` Relative – Silhouettes and border edges are shifted by a user-defined ratio.


Type:
    

enum in [`'CENTER'`, `'INSIDE'`, `'OUTSIDE'`, `'RELATIVE'`], default `'CENTER'`

thickness_ratio
    

A number between 0 (inside) and 1 (outside) specifying the relative position of stroke thickness

Type:
    

float in [0, 1], default 0.5

use_angle_max
    

Split chains at points with angles larger than the maximum 2D angle

Type:
    

boolean, default False

use_angle_min
    

Split chains at points with angles smaller than the minimum 2D angle

Type:
    

boolean, default False

use_chain_count
    

Enable the selection of first N chains

Type:
    

boolean, default False

use_chaining
    

Enable chaining of feature edges

Type:
    

boolean, default True

use_dashed_line
    

Enable or disable dashed line

Type:
    

boolean, default False

use_length_max
    

Enable the selection of chains by a maximum 2D length

Type:
    

boolean, default False

use_length_min
    

Enable the selection of chains by a minimum 2D length

Type:
    

boolean, default False

use_nodes
    

Use shader nodes for the line style

Type:
    

boolean, default False

use_same_object
    

If true, only feature edges of the same object are joined

Type:
    

boolean, default True

use_sorting
    

Arrange the stacking order of strokes

Type:
    

boolean, default False

use_split_length
    

Enable chain splitting by curvilinear 2D length

Type:
    

boolean, default False

use_split_pattern
    

Enable chain splitting by dashed line patterns

Type:
    

boolean, default False

use_texture
    

Enable or disable textured strokes

Type:
    

boolean, default True

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
  * [`ID.name`](../I/bpy.types.ID.md#bpy.types.ID.name "bpy.types.ID.name")
  * [`ID.name_full`](../I/bpy.types.ID.md#bpy.types.ID.name_full "bpy.types.ID.name_full")
  * [`ID.id_type`](../I/bpy.types.ID.md#bpy.types.ID.id_type "bpy.types.ID.id_type")
  * [`ID.session_uid`](../I/bpy.types.ID.md#bpy.types.ID.session_uid "bpy.types.ID.session_uid")
  * [`ID.is_evaluated`](../I/bpy.types.ID.md#bpy.types.ID.is_evaluated "bpy.types.ID.is_evaluated")
  * [`ID.original`](../I/bpy.types.ID.md#bpy.types.ID.original "bpy.types.ID.original")
  * [`ID.users`](../I/bpy.types.ID.md#bpy.types.ID.users "bpy.types.ID.users")
  * [`ID.use_fake_user`](../I/bpy.types.ID.md#bpy.types.ID.use_fake_user "bpy.types.ID.use_fake_user")
  * [`ID.use_extra_user`](../I/bpy.types.ID.md#bpy.types.ID.use_extra_user "bpy.types.ID.use_extra_user")
  * [`ID.is_embedded_data`](../I/bpy.types.ID.md#bpy.types.ID.is_embedded_data "bpy.types.ID.is_embedded_data")

| 

  * [`ID.is_linked_packed`](../I/bpy.types.ID.md#bpy.types.ID.is_linked_packed "bpy.types.ID.is_linked_packed")
  * [`ID.is_missing`](../I/bpy.types.ID.md#bpy.types.ID.is_missing "bpy.types.ID.is_missing")
  * [`ID.is_runtime_data`](../I/bpy.types.ID.md#bpy.types.ID.is_runtime_data "bpy.types.ID.is_runtime_data")
  * [`ID.is_editable`](../I/bpy.types.ID.md#bpy.types.ID.is_editable "bpy.types.ID.is_editable")
  * [`ID.tag`](../I/bpy.types.ID.md#bpy.types.ID.tag "bpy.types.ID.tag")
  * [`ID.is_library_indirect`](../I/bpy.types.ID.md#bpy.types.ID.is_library_indirect "bpy.types.ID.is_library_indirect")
  * [`ID.library`](../I/bpy.types.ID.md#bpy.types.ID.library "bpy.types.ID.library")
  * [`ID.library_weak_reference`](../I/bpy.types.ID.md#bpy.types.ID.library_weak_reference "bpy.types.ID.library_weak_reference")
  * [`ID.asset_data`](../I/bpy.types.ID.md#bpy.types.ID.asset_data "bpy.types.ID.asset_data")
  * [`ID.override_library`](../I/bpy.types.ID.md#bpy.types.ID.override_library "bpy.types.ID.override_library")
  * [`ID.preview`](../I/bpy.types.ID.md#bpy.types.ID.preview "bpy.types.ID.preview")

  
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
  * [`bpy_struct.keyframe_insert`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.keyframe_insert "bpy.types.bpy_struct.keyframe_insert")
  * [`bpy_struct.keys`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.keys "bpy.types.bpy_struct.keys")
  * [`bpy_struct.path_from_id`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.path_from_id "bpy.types.bpy_struct.path_from_id")
  * [`bpy_struct.path_from_module`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.path_from_module "bpy.types.bpy_struct.path_from_module")
  * [`bpy_struct.path_resolve`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.path_resolve "bpy.types.bpy_struct.path_resolve")
  * [`bpy_struct.pop`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.pop "bpy.types.bpy_struct.pop")
  * [`bpy_struct.property_overridable_library_set`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.property_overridable_library_set "bpy.types.bpy_struct.property_overridable_library_set")
  * [`bpy_struct.property_unset`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.property_unset "bpy.types.bpy_struct.property_unset")
  * [`bpy_struct.rna_ancestors`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.rna_ancestors "bpy.types.bpy_struct.rna_ancestors")

| 

  * [`bpy_struct.type_recast`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.type_recast "bpy.types.bpy_struct.type_recast")
  * [`bpy_struct.values`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.values "bpy.types.bpy_struct.values")
  * [`ID.bl_system_properties_get`](../I/bpy.types.ID.md#bpy.types.ID.bl_system_properties_get "bpy.types.ID.bl_system_properties_get")
  * [`ID.rename`](../I/bpy.types.ID.md#bpy.types.ID.rename "bpy.types.ID.rename")
  * [`ID.evaluated_get`](../I/bpy.types.ID.md#bpy.types.ID.evaluated_get "bpy.types.ID.evaluated_get")
  * [`ID.copy`](../I/bpy.types.ID.md#bpy.types.ID.copy "bpy.types.ID.copy")
  * [`ID.asset_mark`](../I/bpy.types.ID.md#bpy.types.ID.asset_mark "bpy.types.ID.asset_mark")
  * [`ID.asset_clear`](../I/bpy.types.ID.md#bpy.types.ID.asset_clear "bpy.types.ID.asset_clear")
  * [`ID.asset_generate_preview`](../I/bpy.types.ID.md#bpy.types.ID.asset_generate_preview "bpy.types.ID.asset_generate_preview")
  * [`ID.override_create`](../I/bpy.types.ID.md#bpy.types.ID.override_create "bpy.types.ID.override_create")
  * [`ID.override_hierarchy_create`](../I/bpy.types.ID.md#bpy.types.ID.override_hierarchy_create "bpy.types.ID.override_hierarchy_create")
  * [`ID.user_clear`](../I/bpy.types.ID.md#bpy.types.ID.user_clear "bpy.types.ID.user_clear")
  * [`ID.user_remap`](../I/bpy.types.ID.md#bpy.types.ID.user_remap "bpy.types.ID.user_remap")
  * [`ID.make_local`](../I/bpy.types.ID.md#bpy.types.ID.make_local "bpy.types.ID.make_local")
  * [`ID.user_of_id`](../I/bpy.types.ID.md#bpy.types.ID.user_of_id "bpy.types.ID.user_of_id")
  * [`ID.animation_data_create`](../I/bpy.types.ID.md#bpy.types.ID.animation_data_create "bpy.types.ID.animation_data_create")
  * [`ID.animation_data_clear`](../I/bpy.types.ID.md#bpy.types.ID.animation_data_clear "bpy.types.ID.animation_data_clear")
  * [`ID.update_tag`](../I/bpy.types.ID.md#bpy.types.ID.update_tag "bpy.types.ID.update_tag")
  * [`ID.preview_ensure`](../I/bpy.types.ID.md#bpy.types.ID.preview_ensure "bpy.types.ID.preview_ensure")
  * [`ID.bl_rna_get_subclass`](../I/bpy.types.ID.md#bpy.types.ID.bl_rna_get_subclass "bpy.types.ID.bl_rna_get_subclass")
  * [`ID.bl_rna_get_subclass_py`](../I/bpy.types.ID.md#bpy.types.ID.bl_rna_get_subclass_py "bpy.types.ID.bl_rna_get_subclass_py")

  
---|---  
  
## References

  * [`bpy.context.line_style`](../../bpy.context.md#bpy.context.line_style "bpy.context.line_style")
  * [`BlendData.linestyles`](../B/bpy.types.BlendData.md#bpy.types.BlendData.linestyles "bpy.types.BlendData.linestyles")
  * [`BlendDataLineStyles.new`](../B/bpy.types.BlendDataLineStyles.md#bpy.types.BlendDataLineStyles.new "bpy.types.BlendDataLineStyles.new")

| 

  * [`BlendDataLineStyles.remove`](../B/bpy.types.BlendDataLineStyles.md#bpy.types.BlendDataLineStyles.remove "bpy.types.BlendDataLineStyles.remove")
  * [`FreestyleLineSet.linestyle`](bpy.types.FreestyleLineSet.md#bpy.types.FreestyleLineSet.linestyle "bpy.types.FreestyleLineSet.linestyle")

  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
