# IntProperty(Property)

base classes — [[bpy_struct]], [[Property]]

_class _bpy.types.IntProperty(_Property_)
    

RNA integer number property definition

array_dimensions
    

Length of each dimension of the array

Type:
    

int array of 3 items in [0, inf], default (0, 0, 0), (readonly)

array_length
    

Maximum length of the array, 0 means unlimited

Type:
    

int in [0, inf], default 0, (readonly)

default
    

Default value for this number

Type:
    

int in [-inf, inf], default 0, (readonly)

default_array
    

Default value for this array

Type:
    

int array of 3 items in [-inf, inf], default (0, 0, 0), (readonly)

hard_max
    

Maximum value used by buttons

Type:
    

int in [-inf, inf], default 0, (readonly)

hard_min
    

Minimum value used by buttons

Type:
    

int in [-inf, inf], default 0, (readonly)

is_array
    

Type:
    

boolean, default False, (readonly)

soft_max
    

Maximum value used by buttons

Type:
    

int in [-inf, inf], default 0, (readonly)

soft_min
    

Minimum value used by buttons

Type:
    

int in [-inf, inf], default 0, (readonly)

step
    

Step size used by number buttons, for floats 1/100th of the step size

Type:
    

int in [0, inf], default 0, (readonly)

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
  * [[Property.name]]
  * [[Property.identifier]]
  * [[Property.description]]
  * [[Property.translation_context]]
  * [[Property.type]]
  * [[Property.subtype]]
  * [[Property.srna]]
  * [[Property.unit]]
  * [[Property.icon]]
  * [[Property.is_readonly]]
  * [[Property.is_animatable]]
  * [[Property.is_overridable]]
  * [[Property.is_required]]
  * [[Property.is_argument_optional]]
  * [[Property.is_never_none]]
  * [[Property.is_hidden]]

| 

  * [[Property.is_skip_save]]
  * [[Property.is_skip_preset]]
  * [[Property.is_output]]
  * [[Property.is_registered]]
  * [[Property.is_registered_optional]]
  * [[Property.is_runtime]]
  * [[Property.is_enum_flag]]
  * [[Property.is_library_editable]]
  * [[Property.is_path_output]]
  * [[Property.is_path_supports_blend_relative]]
  * [[Property.is_path_supports_templates]]
  * [[Property.is_deprecated]]
  * [[Property.deprecated_note]]
  * [[Property.deprecated_version]]
  * [[Property.deprecated_removal_version]]
  * [[Property.tags]]

  
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

| 

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
  * [[Property.bl_rna_get_subclass]]
  * [[Property.bl_rna_get_subclass_py]]

  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
