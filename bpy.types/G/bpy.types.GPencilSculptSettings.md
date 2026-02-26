# GPencilSculptSettings(bpy_struct)

base class — [[bpy_struct]]

_class _bpy.types.GPencilSculptSettings(_bpy_struct_)
    

General properties for Grease Pencil stroke sculpting tools

guide
    

Type:
    

[[GPencilSculptGuide]], (readonly)

intersection_threshold
    

Threshold for stroke intersections

Type:
    

float in [0, 10], default 0.1

lock_axis
    

  * `VIEW` View – Align strokes to current view plane.

  * `AXIS_Y` Front (X-Z) – Project strokes to plane locked to Y.

  * `AXIS_X` Side (Y-Z) – Project strokes to plane locked to X.

  * `AXIS_Z` Top (X-Y) – Project strokes to plane locked to Z.

  * `CURSOR` Cursor – Align strokes to current 3D cursor orientation.


Type:
    

enum in [`'VIEW'`, `'AXIS_Y'`, `'AXIS_X'`, `'AXIS_Z'`, `'CURSOR'`], default `'VIEW'`

multiframe_falloff_curve
    

Custom curve to control falloff of brush effect by Grease Pencil frames

Type:
    

[[CurveMapping]], (readonly)

thickness_primitive_curve
    

Custom curve to control primitive thickness

Type:
    

[[CurveMapping]], (readonly)

use_automasking_layer_active
    

Affect only the Active Layer

Type:
    

boolean, default False

use_automasking_layer_stroke
    

Affect only strokes below the cursor

Type:
    

boolean, default False

use_automasking_material_active
    

Affect only the Active Material

Type:
    

boolean, default False

use_automasking_material_stroke
    

Affect only strokes below the cursor

Type:
    

boolean, default False

use_automasking_stroke
    

Affect only strokes below the cursor

Type:
    

boolean, default False

use_multiframe_falloff
    

Use falloff effect when edit in multiframe mode to compute brush effect by frame

Type:
    

boolean, default False

use_scale_thickness
    

Scale the stroke thickness when transforming strokes

Type:
    

boolean, default False

use_thickness_curve
    

Use curve to define primitive stroke thickness

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

  * [[ToolSettings.gpencil_sculpt]]

| 


  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
