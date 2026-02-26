# LineStyleColorModifier_CreaseAngle(LineStyleColorModifier)

base classes — [[bpy_struct]], [[LineStyleModifier]], [[LineStyleColorModifier]]

_class _bpy.types.LineStyleColorModifier_CreaseAngle(_LineStyleColorModifier_)
    

Change line color based on the underlying crease angle

angle_max
    

Maximum angle to modify thickness

Type:
    

float in [-inf, inf], default 0.0

angle_min
    

Minimum angle to modify thickness

Type:
    

float in [-inf, inf], default 0.0

blend
    

Specify how the modifier value is blended into the base value

Type:
    

enum in [Ramp Blend Items](../../bpy_types_enum_items/ramp_blend_items.md#rna-enum-ramp-blend-items), default `'MIX'`

color_ramp
    

Color ramp used to change line color

Type:
    

[[ColorRamp]], (readonly)

expanded
    

True if the modifier tab is expanded

Type:
    

boolean, default False

influence
    

Influence factor by which the modifier changes the property

Type:
    

float in [0, 1], default 0.0

type
    

Type of the modifier

Type:
    

enum in [Linestyle Color Modifier Type Items](../../bpy_types_enum_items/linestyle_color_modifier_type_items.md#rna-enum-linestyle-color-modifier-type-items), default `'ALONG_STROKE'`, (readonly)

use
    

Enable or disable this modifier during stroke rendering

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

  * [[LineStyleColorModifier.name]]

  
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

| 

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
  * [[LineStyleModifier.bl_rna_get_subclass]]
  * [[LineStyleModifier.bl_rna_get_subclass_py]]
  * [[LineStyleColorModifier.bl_rna_get_subclass]]
  * [[LineStyleColorModifier.bl_rna_get_subclass_py]]

  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
