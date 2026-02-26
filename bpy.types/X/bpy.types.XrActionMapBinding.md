# XrActionMapBinding(bpy_struct)

base class — [[bpy_struct]]

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
    

[[XrComponentPaths]] [[bpy_prop_collection]] of [[XrComponentPath]], (readonly)

name
    

Name of the action map binding

Type:
    

string, default “”, (never None)

pose_location
    

Type:
    

[[mathutils.Vector]] of 3 items in [-inf, inf], default (0.0, 0.0, 0.0)

pose_rotation
    

Type:
    

[[mathutils.Euler]] rotation of 3 items in [-inf, inf], default (0.0, 0.0, 0.0)

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

| 


  
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

| 

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

  
---|---  
  
## References

  * [[XrActionMapBindings.find]]
  * [[XrActionMapBindings.new]]
  * [[XrActionMapBindings.new_from_binding]]
  * [[XrActionMapBindings.new_from_binding]]

| 

  * [[XrActionMapBindings.remove]]
  * [[XrActionMapItem.bindings]]
  * [[XrSessionState.action_binding_create]]

  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
