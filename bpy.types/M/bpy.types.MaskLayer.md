# MaskLayer(bpy_struct)

base class — [[bpy_struct]]

_class _bpy.types.MaskLayer(_bpy_struct_)
    

Single layer used for masking pixels

alpha
    

Render Opacity

Type:
    

float in [-inf, inf], default 0.0

blend
    

Method of blending mask layers

Type:
    

enum in [`'MERGE_ADD'`, `'MERGE_SUBTRACT'`, `'ADD'`, `'SUBTRACT'`, `'LIGHTEN'`, `'DARKEN'`, `'MUL'`, `'REPLACE'`, `'DIFFERENCE'`], default `'ADD'`

falloff
    

Falloff type of the feather

Type:
    

enum in [Proportional Falloff Curve Only Items](../../bpy_types_enum_items/proportional_falloff_curve_only_items.md#rna-enum-proportional-falloff-curve-only-items), default `'SMOOTH'`

hide
    

Restrict visibility in the viewport

Type:
    

boolean, default False

hide_render
    

Restrict renderability

Type:
    

boolean, default False

hide_select
    

Restrict selection in the viewport

Type:
    

boolean, default False

invert
    

Invert the mask black/white

Type:
    

boolean, default False

name
    

Unique name of layer

Type:
    

string, default “”, (never None)

select
    

Layer is selected for editing in the Dope Sheet

Type:
    

boolean, default False

splines
    

Collection of splines which defines this layer

Type:
    

[[MaskSplines]] [[bpy_prop_collection]] of [[MaskSpline]], (readonly)

use_fill_holes
    

Calculate holes when filling overlapping curves

Type:
    

boolean, default False

use_fill_overlap
    

Calculate self intersections and overlap before filling

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

  * [[Mask.layers]]
  * [[MaskLayers.active]]

| 

  * [[MaskLayers.new]]
  * [[MaskLayers.remove]]

  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
