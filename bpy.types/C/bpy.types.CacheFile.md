# CacheFile(ID)

base classes — [[bpy_struct]], [[ID]]

_class _bpy.types.CacheFile(_ID_)
    

active_index
    

Type:
    

int in [0, inf], default 0

animation_data
    

Animation data for this data-block

Type:
    

[[AnimData]], (readonly)

filepath
    

Path to external displacements file

Type:
    

string, default “”, (never None, blend relative `//` prefix supported)

forward_axis
    

Type:
    

enum in [Object Axis Items](../../bpy_types_enum_items/object_axis_items.md#rna-enum-object-axis-items), default `'POS_X'`

frame
    

The time to use for looking up the data in the cache file, or to determine which file to use in a file sequence

Type:
    

float in [-1.04857e+06, 1.04857e+06], default 0.0

frame_offset
    

Subtracted from the current frame to use for looking up the data in the cache file, or to determine which file to use in a file sequence

Type:
    

float in [-1.04857e+06, 1.04857e+06], default 0.0

is_sequence
    

Whether the cache is separated in a series of files

Type:
    

boolean, default False

layers
    

Layers of the cache

Type:
    

[[CacheFileLayers]] [[bpy_prop_collection]] of [[CacheFileLayer]], (readonly)

object_paths
    

Paths of the objects inside the Alembic archive

Type:
    

[[CacheObjectPaths]] [[bpy_prop_collection]] of [[CacheObjectPath]], (readonly)

override_frame
    

Whether to use a custom frame for looking up data in the cache file, instead of using the current scene frame

Type:
    

boolean, default False

scale
    

Value by which to enlarge or shrink the object with respect to the world’s origin (only applicable through a Transform Cache constraint)

Type:
    

float in [0.0001, 1000], default 1.0

up_axis
    

Type:
    

enum in [Object Axis Items](../../bpy_types_enum_items/object_axis_items.md#rna-enum-object-axis-items), default `'POS_X'`

velocity_name
    

Name of the Alembic attribute used for generating motion blur data

Type:
    

string, default “”, (never None)

velocity_unit
    

Define how the velocity vectors are interpreted with regard to time, ‘frame’ means the delta time is 1 frame, ‘second’ means the delta time is 1 / FPS

Type:
    

enum in [Velocity Unit Items](../../bpy_types_enum_items/velocity_unit_items.md#rna-enum-velocity-unit-items), default `'FRAME'`

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
  * [[ID.name]]
  * [[ID.name_full]]
  * [[ID.id_type]]
  * [[ID.session_uid]]
  * [[ID.is_evaluated]]
  * [[ID.original]]
  * [[ID.users]]
  * [[ID.use_fake_user]]
  * [[ID.use_extra_user]]
  * [[ID.is_embedded_data]]

| 

  * [[ID.is_linked_packed]]
  * [[ID.is_missing]]
  * [[ID.is_runtime_data]]
  * [[ID.is_editable]]
  * [[ID.tag]]
  * [[ID.is_library_indirect]]
  * [[ID.library]]
  * [[ID.library_weak_reference]]
  * [[ID.asset_data]]
  * [[ID.override_library]]
  * [[ID.preview]]

  
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
  * [[bpy_struct.keys]]
  * [[bpy_struct.path_from_id]]
  * [[bpy_struct.path_from_module]]
  * [[bpy_struct.path_resolve]]
  * [[bpy_struct.pop]]
  * [[bpy_struct.property_overridable_library_set]]
  * [[bpy_struct.property_unset]]
  * [[bpy_struct.rna_ancestors]]

| 

  * [[bpy_struct.type_recast]]
  * [[bpy_struct.values]]
  * [[ID.bl_system_properties_get]]
  * [[ID.rename]]
  * [[ID.evaluated_get]]
  * [[ID.copy]]
  * [[ID.asset_mark]]
  * [[ID.asset_clear]]
  * [[ID.asset_generate_preview]]
  * [[ID.override_create]]
  * [[ID.override_hierarchy_create]]
  * [[ID.user_clear]]
  * [[ID.user_remap]]
  * [[ID.make_local]]
  * [[ID.user_of_id]]
  * [[ID.animation_data_create]]
  * [[ID.animation_data_clear]]
  * [[ID.update_tag]]
  * [[ID.preview_ensure]]
  * [[ID.bl_rna_get_subclass]]
  * [[ID.bl_rna_get_subclass_py]]

  
---|---  
  
## References

  * [[BlendData.cache_files]]
  * [[MeshSequenceCacheModifier.cache_file]]

| 

  * [[TransformCacheConstraint.cache_file]]

  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
