# PointerProperty(Property)

base classes — [`bpy_struct`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct "bpy.types.bpy_struct"), [`Property`](bpy.types.Property.md#bpy.types.Property "bpy.types.Property")

_class _bpy.types.PointerProperty(_Property_)
    

RNA pointer property to point to another RNA struct

fixed_type
    

Fixed pointer type, empty if variable type

Type:
    

[`Struct`](../S/bpy.types.Struct.md#bpy.types.Struct "bpy.types.Struct"), (readonly)

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
  * [`Property.name`](bpy.types.Property.md#bpy.types.Property.name "bpy.types.Property.name")
  * [`Property.identifier`](bpy.types.Property.md#bpy.types.Property.identifier "bpy.types.Property.identifier")
  * [`Property.description`](bpy.types.Property.md#bpy.types.Property.description "bpy.types.Property.description")
  * [`Property.translation_context`](bpy.types.Property.md#bpy.types.Property.translation_context "bpy.types.Property.translation_context")
  * [`Property.type`](bpy.types.Property.md#bpy.types.Property.type "bpy.types.Property.type")
  * [`Property.subtype`](bpy.types.Property.md#bpy.types.Property.subtype "bpy.types.Property.subtype")
  * [`Property.srna`](bpy.types.Property.md#bpy.types.Property.srna "bpy.types.Property.srna")
  * [`Property.unit`](bpy.types.Property.md#bpy.types.Property.unit "bpy.types.Property.unit")
  * [`Property.icon`](bpy.types.Property.md#bpy.types.Property.icon "bpy.types.Property.icon")
  * [`Property.is_readonly`](bpy.types.Property.md#bpy.types.Property.is_readonly "bpy.types.Property.is_readonly")
  * [`Property.is_animatable`](bpy.types.Property.md#bpy.types.Property.is_animatable "bpy.types.Property.is_animatable")
  * [`Property.is_overridable`](bpy.types.Property.md#bpy.types.Property.is_overridable "bpy.types.Property.is_overridable")
  * [`Property.is_required`](bpy.types.Property.md#bpy.types.Property.is_required "bpy.types.Property.is_required")
  * [`Property.is_argument_optional`](bpy.types.Property.md#bpy.types.Property.is_argument_optional "bpy.types.Property.is_argument_optional")
  * [`Property.is_never_none`](bpy.types.Property.md#bpy.types.Property.is_never_none "bpy.types.Property.is_never_none")
  * [`Property.is_hidden`](bpy.types.Property.md#bpy.types.Property.is_hidden "bpy.types.Property.is_hidden")

| 

  * [`Property.is_skip_save`](bpy.types.Property.md#bpy.types.Property.is_skip_save "bpy.types.Property.is_skip_save")
  * [`Property.is_skip_preset`](bpy.types.Property.md#bpy.types.Property.is_skip_preset "bpy.types.Property.is_skip_preset")
  * [`Property.is_output`](bpy.types.Property.md#bpy.types.Property.is_output "bpy.types.Property.is_output")
  * [`Property.is_registered`](bpy.types.Property.md#bpy.types.Property.is_registered "bpy.types.Property.is_registered")
  * [`Property.is_registered_optional`](bpy.types.Property.md#bpy.types.Property.is_registered_optional "bpy.types.Property.is_registered_optional")
  * [`Property.is_runtime`](bpy.types.Property.md#bpy.types.Property.is_runtime "bpy.types.Property.is_runtime")
  * [`Property.is_enum_flag`](bpy.types.Property.md#bpy.types.Property.is_enum_flag "bpy.types.Property.is_enum_flag")
  * [`Property.is_library_editable`](bpy.types.Property.md#bpy.types.Property.is_library_editable "bpy.types.Property.is_library_editable")
  * [`Property.is_path_output`](bpy.types.Property.md#bpy.types.Property.is_path_output "bpy.types.Property.is_path_output")
  * [`Property.is_path_supports_blend_relative`](bpy.types.Property.md#bpy.types.Property.is_path_supports_blend_relative "bpy.types.Property.is_path_supports_blend_relative")
  * [`Property.is_path_supports_templates`](bpy.types.Property.md#bpy.types.Property.is_path_supports_templates "bpy.types.Property.is_path_supports_templates")
  * [`Property.is_deprecated`](bpy.types.Property.md#bpy.types.Property.is_deprecated "bpy.types.Property.is_deprecated")
  * [`Property.deprecated_note`](bpy.types.Property.md#bpy.types.Property.deprecated_note "bpy.types.Property.deprecated_note")
  * [`Property.deprecated_version`](bpy.types.Property.md#bpy.types.Property.deprecated_version "bpy.types.Property.deprecated_version")
  * [`Property.deprecated_removal_version`](bpy.types.Property.md#bpy.types.Property.deprecated_removal_version "bpy.types.Property.deprecated_removal_version")
  * [`Property.tags`](bpy.types.Property.md#bpy.types.Property.tags "bpy.types.Property.tags")

  
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

| 

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
  * [`Property.bl_rna_get_subclass`](bpy.types.Property.md#bpy.types.Property.bl_rna_get_subclass "bpy.types.Property.bl_rna_get_subclass")
  * [`Property.bl_rna_get_subclass_py`](bpy.types.Property.md#bpy.types.Property.bl_rna_get_subclass_py "bpy.types.Property.bl_rna_get_subclass_py")

  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
