# Keyframe(bpy_struct)

base class — [`bpy_struct`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct "bpy.types.bpy_struct")

_class _bpy.types.Keyframe(_bpy_struct_)
    

Bézier curve point with two handles defining a Keyframe on an F-Curve

amplitude
    

Amount to boost elastic bounces for ‘elastic’ easing

Type:
    

float in [0, inf], default 0.0

back
    

Amount of overshoot for ‘back’ easing

Type:
    

float in [-inf, inf], default 0.0

co
    

Coordinates of the control point

Type:
    

[`mathutils.Vector`](mathutils.md#mathutils.Vector "mathutils.Vector") of 2 items in [-inf, inf], default (0.0, 0.0)

co_ui
    

Coordinates of the control point. Note: Changing this value also updates the handles similar to using the graph editor transform operator

Type:
    

[`mathutils.Vector`](mathutils.md#mathutils.Vector "mathutils.Vector") of 2 items in [-inf, inf], default (0.0, 0.0)

easing
    

Which ends of the segment between this and the next keyframe easing interpolation is applied to

Type:
    

enum in [Beztriple Interpolation Easing Items](../../bpy_types_enum_items/beztriple_interpolation_easing_items.md#rna-enum-beztriple-interpolation-easing-items), default `'AUTO'`

handle_left
    

Coordinates of the left handle (before the control point)

Type:
    

[`mathutils.Vector`](mathutils.md#mathutils.Vector "mathutils.Vector") of 2 items in [-inf, inf], default (0.0, 0.0)

handle_left_type
    

Handle types

Type:
    

enum in [Keyframe Handle Type Items](../../bpy_types_enum_items/keyframe_handle_type_items.md#rna-enum-keyframe-handle-type-items), default `'FREE'`

handle_right
    

Coordinates of the right handle (after the control point)

Type:
    

[`mathutils.Vector`](mathutils.md#mathutils.Vector "mathutils.Vector") of 2 items in [-inf, inf], default (0.0, 0.0)

handle_right_type
    

Handle types

Type:
    

enum in [Keyframe Handle Type Items](../../bpy_types_enum_items/keyframe_handle_type_items.md#rna-enum-keyframe-handle-type-items), default `'FREE'`

interpolation
    

Interpolation method to use for segment of the F-Curve from this Keyframe until the next Keyframe

Type:
    

enum in [Beztriple Interpolation Mode Items](../../bpy_types_enum_items/beztriple_interpolation_mode_items.md#rna-enum-beztriple-interpolation-mode-items), default `'CONSTANT'`

period
    

Time between bounces for elastic easing

Type:
    

float in [-inf, inf], default 0.0

select_control_point
    

Control point selection status

Type:
    

boolean, default False

select_left_handle
    

Left handle selection status

Type:
    

boolean, default False

select_right_handle
    

Right handle selection status

Type:
    

boolean, default False

type
    

Type of keyframe (for visual purposes only)

Type:
    

enum in [Beztriple Keyframe Type Items](../../bpy_types_enum_items/beztriple_keyframe_type_items.md#rna-enum-beztriple-keyframe-type-items), default `'KEYFRAME'`

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

  * [`bpy.context.selected_editable_keyframes`](../../bpy.context.md#bpy.context.selected_editable_keyframes "bpy.context.selected_editable_keyframes")
  * [`FCurve.keyframe_points`](../F/bpy.types.FCurve.md#bpy.types.FCurve.keyframe_points "bpy.types.FCurve.keyframe_points")

| 

  * [`FCurveKeyframePoints.insert`](../F/bpy.types.FCurveKeyframePoints.md#bpy.types.FCurveKeyframePoints.insert "bpy.types.FCurveKeyframePoints.insert")
  * [`FCurveKeyframePoints.remove`](../F/bpy.types.FCurveKeyframePoints.md#bpy.types.FCurveKeyframePoints.remove "bpy.types.FCurveKeyframePoints.remove")

  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
