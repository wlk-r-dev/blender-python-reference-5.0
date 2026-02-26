# FreestyleSettings(bpy_struct)

base class — [[bpy_struct]]

_class _bpy.types.FreestyleSettings(_bpy_struct_)
    

Freestyle settings for a ViewLayer data-block

as_render_pass
    

Renders Freestyle output to a separate pass instead of overlaying it on the Combined pass

Type:
    

boolean, default False

crease_angle
    

Angular threshold for detecting crease edges

Type:
    

float in [0, 3.14159], default 0.0

kr_derivative_epsilon
    

Kr derivative epsilon for computing suggestive contours

Type:
    

float in [-1000, 1000], default 0.0

linesets
    

Type:
    

[[Linesets]] [[bpy_prop_collection]] of [[FreestyleLineSet]], (readonly)

mode
    

Select the Freestyle control mode

  * `SCRIPT` Python Scripting – Advanced mode for using style modules written in Python.

  * `EDITOR` Parameter Editor – Basic mode for interactive style parameter editing.


Type:
    

enum in [`'SCRIPT'`, `'EDITOR'`], default `'SCRIPT'`

modules
    

A list of style modules (to be applied from top to bottom)

Type:
    

[[FreestyleModules]] [[bpy_prop_collection]] of [[FreestyleModuleSettings]], (readonly)

sphere_radius
    

Sphere radius for computing curvatures

Type:
    

float in [0, 1000], default 1.0

use_culling
    

If enabled, out-of-view edges are ignored

Type:
    

boolean, default False

use_material_boundaries
    

Enable material boundaries

Type:
    

boolean, default False

use_ridges_and_valleys
    

Enable ridges and valleys

Type:
    

boolean, default False

use_smoothness
    

Take face smoothness into account in view map calculation

Type:
    

boolean, default False

use_suggestive_contours
    

Enable suggestive contours

Type:
    

boolean, default False

use_view_map_cache
    

Keep the computed view map and avoid recalculating it if mesh geometry is unchanged

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

  * [[ViewLayer.freestyle_settings]]

| 


  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
