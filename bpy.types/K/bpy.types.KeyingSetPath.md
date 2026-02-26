# KeyingSetPath(bpy_struct)

base class — [[bpy_struct]]

_class _bpy.types.KeyingSetPath(_bpy_struct_)
    

Path to a setting for use in a Keying Set

array_index
    

Index to the specific setting if applicable

Type:
    

int in [-inf, inf], default 0

data_path
    

Path to property setting

Type:
    

string, default “”, (never None)

group
    

Name of Action Group to assign setting(s) for this path to

Type:
    

string, default “”, (never None)

group_method
    

Method used to define which Group-name to use

Type:
    

enum in [Keyingset Path Grouping Items](../../bpy_types_enum_items/keyingset_path_grouping_items.md#rna-enum-keyingset-path-grouping-items), default `'NAMED'`

id
    

ID-Block that keyframes for Keying Set should be added to (for Absolute Keying Sets only)

Type:
    

[[ID]]

id_type
    

Type of ID-block that can be used

Type:
    

enum in [Id Type Items](../../bpy_types_enum_items/id_type_items.md#rna-enum-id-type-items), default `'OBJECT'`

use_entire_array
    

When an ‘array/vector’ type is chosen (Location, Rotation, Color, etc.), entire array is to be used

Type:
    

boolean, default False

use_insertkey_needed
    

Only insert keyframes where they’re needed in the relevant F-Curves

Type:
    

boolean, default False

use_insertkey_override_needed
    

Override default setting to only insert keyframes where they’re needed in the relevant F-Curves

Type:
    

boolean, default False

use_insertkey_override_visual
    

Override default setting to insert keyframes based on ‘visual transforms’

Type:
    

boolean, default False

use_insertkey_visual
    

Insert keyframes based on ‘visual transforms’

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

  * [[KeyingSet.paths]]
  * [[KeyingSetPaths.active]]

| 

  * [[KeyingSetPaths.add]]
  * [[KeyingSetPaths.remove]]

  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
