# Property(bpy_struct)

base class — [[bpy_struct]]

subclasses — [[BoolProperty]], [[CollectionProperty]], [[EnumProperty]], [[FloatProperty]], [[IntProperty]], [[PointerProperty]], [[StringProperty]]

_class _bpy.types.Property(_bpy_struct_)
    

RNA property definition

deprecated_note
    

A note regarding deprecation

Type:
    

string, default “”, (readonly, never None)

deprecated_removal_version
    

The Blender version this is expected to be removed

Type:
    

int array of 3 items in [-inf, inf], default (0, 0, 0), (readonly)

deprecated_version
    

The Blender version this was deprecated

Type:
    

int array of 3 items in [-inf, inf], default (0, 0, 0), (readonly)

description
    

Description of the property for tooltips

Type:
    

string, default “”, (readonly, never None)

icon
    

Icon of the item

Type:
    

enum in [Icon Items](../../bpy_types_enum_items/icon_items.md#rna-enum-icon-items), default `'NONE'`, (readonly)

identifier
    

Unique name used in the code and scripting

Type:
    

string, default “”, (readonly, never None)

is_animatable
    

Property is animatable through RNA

Type:
    

boolean, default False, (readonly)

is_argument_optional
    

True when the property is optional in a Python function implementing an RNA function

Type:
    

boolean, default False, (readonly)

is_deprecated
    

The property is deprecated

Type:
    

boolean, default False, (readonly)

is_enum_flag
    

True when multiple enums

Type:
    

boolean, default False, (readonly)

is_hidden
    

True when the property is hidden

Type:
    

boolean, default False, (readonly)

is_library_editable
    

Property is editable from linked instances (changes not saved)

Type:
    

boolean, default False, (readonly)

is_never_none
    

True when this value cannot be set to None

Type:
    

boolean, default False, (readonly)

is_output
    

True when this property is an output value from an RNA function

Type:
    

boolean, default False, (readonly)

is_overridable
    

Property is overridable through RNA

Type:
    

boolean, default False, (readonly)

is_path_output
    

Property is a filename, filepath or directory output

Type:
    

boolean, default False, (readonly)

is_path_supports_blend_relative
    

Property is a path which supports the “//” prefix, signifying the location as relative to the “.blend” file’s directory

Type:
    

boolean, default False, (readonly)

is_path_supports_templates
    

Property is a path which supports the “{variable_name}” variable expression syntax, which substitutes the value of the referenced variable in place of the expression

Type:
    

boolean, default False, (readonly)

is_readonly
    

Property is editable through RNA

Type:
    

boolean, default False, (readonly)

is_registered
    

Property is registered as part of type registration

Type:
    

boolean, default False, (readonly)

is_registered_optional
    

Property is optionally registered as part of type registration

Type:
    

boolean, default False, (readonly)

is_required
    

False when this property is an optional argument in an RNA function

Type:
    

boolean, default False, (readonly)

is_runtime
    

Property has been dynamically created at runtime

Type:
    

boolean, default False, (readonly)

is_skip_preset
    

True when the property is not saved in presets

Type:
    

boolean, default False, (readonly)

is_skip_save
    

True when the property uses ghost values

Type:
    

boolean, default False, (readonly)

name
    

Human readable name

Type:
    

string, default “”, (readonly, never None)

srna
    

Struct definition used for properties assigned to this item

Type:
    

[[Struct]], (readonly)

subtype
    

Semantic interpretation of the property

Type:
    

enum in [Property Subtype Items](../../bpy_types_enum_items/property_subtype_items.md#rna-enum-property-subtype-items), default `'NONE'`, (readonly)

tags
    

Subset of tags (defined in parent struct) that are set for this property

Type:
    

enum set in {}, default set(), (readonly)

translation_context
    

Translation context of the property’s name

Type:
    

string, default “”, (readonly, never None)

type
    

Data type of the property

Type:
    

enum in [Property Type Items](../../bpy_types_enum_items/property_type_items.md#rna-enum-property-type-items), default `'BOOLEAN'`, (readonly)

unit
    

Type of units for this property

Type:
    

enum in [Property Unit Items](../../bpy_types_enum_items/property_unit_items.md#rna-enum-property-unit-items), default `'NONE'`, (readonly)

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

  * [[bpy.context.texture_user_property]]
  * [[Function.parameters]]

| 

  * [[Struct.properties]]

  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
