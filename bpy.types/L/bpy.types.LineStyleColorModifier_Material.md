# LineStyleColorModifier_Material(LineStyleColorModifier)

base classes — [`bpy_struct`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct "bpy.types.bpy_struct"), [`LineStyleModifier`](bpy.types.LineStyleModifier.md#bpy.types.LineStyleModifier "bpy.types.LineStyleModifier"), [`LineStyleColorModifier`](bpy.types.LineStyleColorModifier.md#bpy.types.LineStyleColorModifier "bpy.types.LineStyleColorModifier")

_class _bpy.types.LineStyleColorModifier_Material(_LineStyleColorModifier_)
    

Change line color based on a material attribute

blend
    

Specify how the modifier value is blended into the base value

Type:
    

enum in [Ramp Blend Items](../../bpy_types_enum_items/ramp_blend_items.md#rna-enum-ramp-blend-items), default `'MIX'`

color_ramp
    

Color ramp used to change line color

Type:
    

[`ColorRamp`](../C/bpy.types.ColorRamp.md#bpy.types.ColorRamp "bpy.types.ColorRamp"), (readonly)

expanded
    

True if the modifier tab is expanded

Type:
    

boolean, default False

influence
    

Influence factor by which the modifier changes the property

Type:
    

float in [0, 1], default 0.0

material_attribute
    

Specify which material attribute is used

Type:
    

enum in [`'LINE'`, `'LINE_R'`, `'LINE_G'`, `'LINE_B'`, `'LINE_A'`, `'DIFF'`, `'DIFF_R'`, `'DIFF_G'`, `'DIFF_B'`, `'SPEC'`, `'SPEC_R'`, `'SPEC_G'`, `'SPEC_B'`, `'SPEC_HARD'`, `'ALPHA'`], default `'LINE'`

type
    

Type of the modifier

Type:
    

enum in [Linestyle Color Modifier Type Items](../../bpy_types_enum_items/linestyle_color_modifier_type_items.md#rna-enum-linestyle-color-modifier-type-items), default `'ALONG_STROKE'`, (readonly)

use
    

Enable or disable this modifier during stroke rendering

Type:
    

boolean, default False

use_ramp
    

Use color ramp to map the BW average into an RGB color

Type:
    

boolean, default False

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

  * [`LineStyleColorModifier.name`](bpy.types.LineStyleColorModifier.md#bpy.types.LineStyleColorModifier.name "bpy.types.LineStyleColorModifier.name")

  
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

| 

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
  * [`LineStyleModifier.bl_rna_get_subclass`](bpy.types.LineStyleModifier.md#bpy.types.LineStyleModifier.bl_rna_get_subclass "bpy.types.LineStyleModifier.bl_rna_get_subclass")
  * [`LineStyleModifier.bl_rna_get_subclass_py`](bpy.types.LineStyleModifier.md#bpy.types.LineStyleModifier.bl_rna_get_subclass_py "bpy.types.LineStyleModifier.bl_rna_get_subclass_py")
  * [`LineStyleColorModifier.bl_rna_get_subclass`](bpy.types.LineStyleColorModifier.md#bpy.types.LineStyleColorModifier.bl_rna_get_subclass "bpy.types.LineStyleColorModifier.bl_rna_get_subclass")
  * [`LineStyleColorModifier.bl_rna_get_subclass_py`](bpy.types.LineStyleColorModifier.md#bpy.types.LineStyleColorModifier.bl_rna_get_subclass_py "bpy.types.LineStyleColorModifier.bl_rna_get_subclass_py")

  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
