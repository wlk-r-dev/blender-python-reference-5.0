# Gizmo(bpy_struct)

base class — [`bpy_struct`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct "bpy.types.bpy_struct")

_class _bpy.types.Gizmo(_bpy_struct_)
    

Collection of gizmos

alpha
    

Type:
    

float in [0, 1], default 0.0

alpha_highlight
    

Type:
    

float in [0, 1], default 0.0

bl_idname
    

Type:
    

string, default “”, (never None)

color
    

Type:
    

[`mathutils.Color`](mathutils.md#mathutils.Color "mathutils.Color") of 3 items in [0, inf], default (0.0, 0.0, 0.0)

color_highlight
    

Type:
    

[`mathutils.Color`](mathutils.md#mathutils.Color "mathutils.Color") of 3 items in [0, inf], default (0.0, 0.0, 0.0)

group
    

Gizmo group this gizmo is a member of

Type:
    

[`GizmoGroup`](bpy.types.GizmoGroup.md#bpy.types.GizmoGroup "bpy.types.GizmoGroup"), (readonly)

hide
    

Type:
    

boolean, default False

hide_keymap
    

Ignore the key-map for this gizmo

Type:
    

boolean, default False

hide_select
    

Type:
    

boolean, default False

is_highlight
    

Type:
    

boolean, default False, (readonly)

is_modal
    

Type:
    

boolean, default False, (readonly)

line_width
    

Type:
    

float in [0, inf], default 0.0

matrix_basis
    

Type:
    

[`mathutils.Matrix`](mathutils.md#mathutils.Matrix "mathutils.Matrix") of 4 * 4 items in [-inf, inf], default ((0.0, 0.0, 0.0, 0.0), (0.0, 0.0, 0.0, 0.0), (0.0, 0.0, 0.0, 0.0), (0.0, 0.0, 0.0, 0.0))

matrix_offset
    

Type:
    

[`mathutils.Matrix`](mathutils.md#mathutils.Matrix "mathutils.Matrix") of 4 * 4 items in [-inf, inf], default ((0.0, 0.0, 0.0, 0.0), (0.0, 0.0, 0.0, 0.0), (0.0, 0.0, 0.0, 0.0), (0.0, 0.0, 0.0, 0.0))

matrix_space
    

Type:
    

[`mathutils.Matrix`](mathutils.md#mathutils.Matrix "mathutils.Matrix") of 4 * 4 items in [-inf, inf], default ((0.0, 0.0, 0.0, 0.0), (0.0, 0.0, 0.0, 0.0), (0.0, 0.0, 0.0, 0.0), (0.0, 0.0, 0.0, 0.0))

matrix_world
    

Type:
    

[`mathutils.Matrix`](mathutils.md#mathutils.Matrix "mathutils.Matrix") of 4 * 4 items in [-inf, inf], default ((0.0, 0.0, 0.0, 0.0), (0.0, 0.0, 0.0, 0.0), (0.0, 0.0, 0.0, 0.0), (0.0, 0.0, 0.0, 0.0)), (readonly)

properties
    

Type:
    

[`GizmoProperties`](bpy.types.GizmoProperties.md#bpy.types.GizmoProperties "bpy.types.GizmoProperties"), (readonly, never None)

scale_basis
    

Type:
    

float in [0, inf], default 0.0

select
    

Type:
    

boolean, default False

select_bias
    

Depth bias used for selection

Type:
    

float in [-inf, inf], default 0.0

use_draw_hover
    

Type:
    

boolean, default False

use_draw_modal
    

Show while dragging

Type:
    

boolean, default False

use_draw_offset_scale
    

Scale the offset matrix (use to apply screen-space offset)

Type:
    

boolean, default False

use_draw_scale
    

Use scale when calculating the matrix

Type:
    

boolean, default True

use_draw_value
    

Show an indicator for the current value while dragging

Type:
    

boolean, default False

use_event_handle_all
    

When highlighted, do not pass events through to be handled by other keymaps

Type:
    

boolean, default False

use_grab_cursor
    

Type:
    

boolean, default False

use_operator_tool_properties
    

Merge active tool properties on activation (does not overwrite existing)

Type:
    

boolean, default False

use_select_background
    

Don’t write into the depth buffer

Type:
    

boolean, default False

use_tooltip
    

Use tooltips when hovering over this gizmo

Type:
    

boolean, default True

draw(_context_)
    

draw_select(_context_ , _*_ , _select_id =0_)
    

test_select(_context_ , _location_)
    

Parameters:
    

**location** (_int array_ _of_ _2 items in_ _[__-inf_ _,__inf_ _]__,__(__never None_ _)_) – Location, Region coordinates

Returns:
    

Use -1 to skip this gizmo

Return type:
    

int in [-1, inf]

modal(_context_ , _event_ , _tweak_)
    

Parameters:
    

**tweak** (enum set in {`'PRECISE'`, `'SNAP'`}) – Tweak

Returns:
    

result

Return type:
    

enum set in [Operator Return Items](../../bpy_types_enum_items/operator_return_items.md#rna-enum-operator-return-items)

setup()
    

invoke(_context_ , _event_)
    

Returns:
    

result

Return type:
    

enum set in [Operator Return Items](../../bpy_types_enum_items/operator_return_items.md#rna-enum-operator-return-items)

exit(_context_ , _cancel_)
    

Parameters:
    

**cancel** (_boolean_) – Cancel, otherwise confirm

select_refresh()
    

draw_preset_box(_matrix_ , _*_ , _select_id =-1_)
    

Draw a box

Parameters:
    

  * **matrix** ([`mathutils.Matrix`](mathutils.md#mathutils.Matrix "mathutils.Matrix") of 4 * 4 items in [-inf, inf]) – The matrix to transform

  * **select_id** (_int in_ _[__-1_ _,__inf_ _]__,__(__optional_ _)_) – ID to use when gizmo is selectable. Use -1 when not selecting.


draw_preset_arrow(_matrix_ , _*_ , _axis ='POS_Z'_, _select_id =-1_)
    

Draw a box

Parameters:
    

  * **matrix** ([`mathutils.Matrix`](mathutils.md#mathutils.Matrix "mathutils.Matrix") of 4 * 4 items in [-inf, inf]) – The matrix to transform

  * **axis** (enum in [Object Axis Items](../../bpy_types_enum_items/object_axis_items.md#rna-enum-object-axis-items), (optional)) – Arrow Orientation

  * **select_id** (_int in_ _[__-1_ _,__inf_ _]__,__(__optional_ _)_) – ID to use when gizmo is selectable. Use -1 when not selecting.


draw_preset_circle(_matrix_ , _*_ , _axis ='POS_Z'_, _select_id =-1_)
    

Draw a box

Parameters:
    

  * **matrix** ([`mathutils.Matrix`](mathutils.md#mathutils.Matrix "mathutils.Matrix") of 4 * 4 items in [-inf, inf]) – The matrix to transform

  * **axis** (enum in [Object Axis Items](../../bpy_types_enum_items/object_axis_items.md#rna-enum-object-axis-items), (optional)) – Arrow Orientation

  * **select_id** (_int in_ _[__-1_ _,__inf_ _]__,__(__optional_ _)_) – ID to use when gizmo is selectable. Use -1 when not selecting.


target_set_prop(_target_ , _data_ , _property_ , _*_ , _index =-1_)
    

Parameters:
    

  * **target** (_string_ _,__(__never None_ _)_) – Target property

  * **data** ([`AnyType`](../A/bpy.types.AnyType.md#bpy.types.AnyType "bpy.types.AnyType"), (never None)) – Data from which to take property

  * **property** (_string_ _,__(__never None_ _)_) – Identifier of property in data


target_set_operator(_operator_ , _*_ , _index =0_)
    

Operator to run when activating the gizmo (overrides property targets)

Parameters:
    

  * **operator** (_string_ _,__(__never None_ _)_) – Target operator

  * **index** (_int in_ _[__0_ _,__255_ _]__,__(__optional_ _)_) – Part index


Returns:
    

Operator properties to fill in

Return type:
    

[`OperatorProperties`](../O/bpy.types.OperatorProperties.md#bpy.types.OperatorProperties "bpy.types.OperatorProperties")

target_is_valid(_property_)
    

Parameters:
    

**property** (_string_ _,__(__never None_ _)_) – Property identifier

Return type:
    

boolean

draw_custom_shape(_shape_ , _*_ , _matrix =None_, _select_id =None_)
    

Draw a shape created form `Gizmo.draw_custom_shape`.

Parameters:
    

  * **shape** (_Any_) – The cached shape to draw.

  * **matrix** ([`mathutils.Matrix`](mathutils.md#mathutils.Matrix "mathutils.Matrix")) – 4x4 matrix, when not given `Gizmo.matrix_world` is used.

  * **select_id** (_int_) – The selection id. Only use when drawing within `Gizmo.draw_select`.


_static _new_custom_shape(_type_ , _verts_)
    

Create a new shape that can be passed to `Gizmo.draw_custom_shape`.

Parameters:
    

  * **type** (_str_) – The type of shape to create in (POINTS, LINES, TRIS, LINE_STRIP).

  * **verts** (_Sequence_ _[__Sequence_ _[__float_ _]__]_) – Sequence of 2D or 3D coordinates.


Returns:
    

The newly created shape (the return type make change).

Return type:
    

Any

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

target_get_range(target):
    

Get the range for this target property.

Parameters:
    

**target** – Target property name.

Returns:
    

The range of this property (min, max).

Return type:
    

tuple[float, float]

target_get_value(target):
    

Get the value of this target property.

Parameters:
    

**target** (_str_) – Target property name.

Returns:
    

The value of the target property as a value or array based on the target type.

Return type:
    

float | tuple[float, …]

target_set_handler(target, get, set, range=None):
    

Assigns callbacks to a gizmos property.

Parameters:
    

  * **target** (_str_) – Target property name.

  * **get** (_Callable_ _[__[__]__,__float_ _|__Sequence_ _[__float_ _]__]_) – Function that returns the value for this property (single value or sequence).

  * **set** (_Callable_ _[__[__tuple_ _[__float_ _,__...__]__]__,__Any_ _]_) – Function that takes a single value argument and applies it.

  * **range** (_callable_) – Function that returns a (min, max) tuple for gizmos that use a range. The returned value is not used.


target_set_value(target):
    

Set the value of this target property.

Parameters:
    

**target** (_str_) – Target property name.

## Inherited Properties

  * [`bpy_struct.id_data`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.id_data "bpy.types.bpy_struct.id_data")

| 


  
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

| 

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
  * [`bpy_struct.type_recast`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.type_recast "bpy.types.bpy_struct.type_recast")
  * [`bpy_struct.values`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.values "bpy.types.bpy_struct.values")

  
---|---  
  
## References

  * [`GizmoGroup.gizmos`](bpy.types.GizmoGroup.md#bpy.types.GizmoGroup.gizmos "bpy.types.GizmoGroup.gizmos")
  * [`GizmoGroup.invoke_prepare`](bpy.types.GizmoGroup.md#bpy.types.GizmoGroup.invoke_prepare "bpy.types.GizmoGroup.invoke_prepare")

| 

  * [`Gizmos.new`](bpy.types.Gizmos.md#bpy.types.Gizmos.new "bpy.types.Gizmos.new")
  * [`Gizmos.remove`](bpy.types.Gizmos.md#bpy.types.Gizmos.remove "bpy.types.Gizmos.remove")

  
---|---
  *[*]: Keyword-only parameters separator (PEP 3102)
  *[/]: Positional-only parameter separator (PEP 570)
