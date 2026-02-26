# XrActionMapBinding(bpy_struct)

base class — [`bpy_struct`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct "bpy.types.bpy_struct")

_class _bpy.types.XrActionMapBinding(_bpy_struct_)
    

Binding in an XR action map item

axis0_region
    

Action execution region for the first input axis

  * `ANY` Any – Use any axis region for operator execution.

  * `POSITIVE` Positive – Use positive axis region only for operator execution.

  * `NEGATIVE` Negative – Use negative axis region only for operator execution.


Type:
    

enum in [`'ANY'`, `'POSITIVE'`, `'NEGATIVE'`], default `'ANY'`

axis1_region
    

Action execution region for the second input axis

  * `ANY` Any – Use any axis region for operator execution.

  * `POSITIVE` Positive – Use positive axis region only for operator execution.

  * `NEGATIVE` Negative – Use negative axis region only for operator execution.


Type:
    

enum in [`'ANY'`, `'POSITIVE'`, `'NEGATIVE'`], default `'ANY'`

component_paths
    

OpenXR component paths

Type:
    

[`XrComponentPaths`](bpy.types.XrComponentPaths.md#bpy.types.XrComponentPaths "bpy.types.XrComponentPaths") [`bpy_prop_collection`](../_other/bpy.types.bpy_prop_collection.md#bpy.types.bpy_prop_collection "bpy.types.bpy_prop_collection") of [`XrComponentPath`](bpy.types.XrComponentPath.md#bpy.types.XrComponentPath "bpy.types.XrComponentPath"), (readonly)

name
    

Name of the action map binding

Type:
    

string, default “”, (never None)

pose_location
    

Type:
    

[`mathutils.Vector`](mathutils.md#mathutils.Vector "mathutils.Vector") of 3 items in [-inf, inf], default (0.0, 0.0, 0.0)

pose_rotation
    

Type:
    

[`mathutils.Euler`](mathutils.md#mathutils.Euler "mathutils.Euler") rotation of 3 items in [-inf, inf], default (0.0, 0.0, 0.0)

profile
    

OpenXR interaction profile path

Type:
    

string, default “”, (never None)

threshold
    

Input threshold for button/axis actions

Type:
    

float in [0, 1], default 0.0

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

  * [`XrActionMapBindings.find`](bpy.types.XrActionMapBindings.md#bpy.types.XrActionMapBindings.find "bpy.types.XrActionMapBindings.find")
  * [`XrActionMapBindings.new`](bpy.types.XrActionMapBindings.md#bpy.types.XrActionMapBindings.new "bpy.types.XrActionMapBindings.new")
  * [`XrActionMapBindings.new_from_binding`](bpy.types.XrActionMapBindings.md#bpy.types.XrActionMapBindings.new_from_binding "bpy.types.XrActionMapBindings.new_from_binding")
  * [`XrActionMapBindings.new_from_binding`](bpy.types.XrActionMapBindings.md#bpy.types.XrActionMapBindings.new_from_binding "bpy.types.XrActionMapBindings.new_from_binding")

| 

  * [`XrActionMapBindings.remove`](bpy.types.XrActionMapBindings.md#bpy.types.XrActionMapBindings.remove "bpy.types.XrActionMapBindings.remove")
  * [`XrActionMapItem.bindings`](bpy.types.XrActionMapItem.md#bpy.types.XrActionMapItem.bindings "bpy.types.XrActionMapItem.bindings")
  * [`XrSessionState.action_binding_create`](bpy.types.XrSessionState.md#bpy.types.XrSessionState.action_binding_create "bpy.types.XrSessionState.action_binding_create")

  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
