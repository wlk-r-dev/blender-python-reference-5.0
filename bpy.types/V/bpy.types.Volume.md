# Volume(ID)

base classes — [[bpy_struct]], [[ID]]

_class _bpy.types.Volume(_ID_)
    

Volume data-block for 3D volume grids

animation_data
    

Animation data for this data-block

Type:
    

[[AnimData]], (readonly)

display
    

Volume display settings for 3D viewport

Type:
    

[[VolumeDisplay]], (readonly)

filepath
    

Volume file used by this Volume data-block

Type:
    

string, default “”, (never None, blend relative `//` prefix supported)

frame_duration
    

Number of frames of the sequence to use

Type:
    

int in [0, 1048574], default 0

frame_offset
    

Offset the number of the frame to use in the animation

Type:
    

int in [-inf, inf], default 0

frame_start
    

Global starting frame of the sequence, assuming first has a #1

Type:
    

int in [-1048574, 1048574], default 1

grids
    

3D volume grids

Type:
    

[[VolumeGrids]] [[bpy_prop_collection]] of [[VolumeGrid]], (readonly)

is_sequence
    

Whether the cache is separated in a series of files

Type:
    

boolean, default False

materials
    

Type:
    

[[IDMaterials]] [[bpy_prop_collection]] of [[Material]], (readonly)

packed_file
    

Type:
    

[[PackedFile]], (readonly)

render
    

Volume render settings for 3D viewport

Type:
    

[[VolumeRender]], (readonly)

sequence_mode
    

Sequence playback mode

  * `CLIP` Clip – Hide frames outside the specified frame range.

  * `EXTEND` Extend – Repeat the start frame before, and the end frame after the frame range.

  * `REPEAT` Repeat – Cycle the frames in the sequence.

  * `PING_PONG` Ping-Pong – Repeat the frames, reversing the playback direction every other cycle.


Type:
    

enum in [`'CLIP'`, `'EXTEND'`, `'REPEAT'`, `'PING_PONG'`], default `'CLIP'`

velocity_grid
    

Name of the velocity field, or the base name if the velocity is split into multiple grids

Type:
    

string, default “”, (never None)

velocity_scale
    

Factor to control the amount of motion blur

Type:
    

float in [0, inf], default 1.0

velocity_unit
    

Define how the velocity vectors are interpreted with regard to time, ‘frame’ means the delta time is 1 frame, ‘second’ means the delta time is 1 / FPS

Type:
    

enum in [Velocity Unit Items](../../bpy_types_enum_items/velocity_unit_items.md#rna-enum-velocity-unit-items), default `'FRAME'`

velocity_x_grid
    

Name of the grid for the X axis component of the velocity field if it was split into multiple grids

Type:
    

string, default “”, (readonly, never None)

velocity_y_grid
    

Name of the grid for the Y axis component of the velocity field if it was split into multiple grids

Type:
    

string, default “”, (readonly, never None)

velocity_z_grid
    

Name of the grid for the Z axis component of the velocity field if it was split into multiple grids

Type:
    

string, default “”, (readonly, never None)

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

  * [[bpy.context.volume]]
  * [[BlendData.volumes]]

| 

  * [[BlendDataVolumes.new]]
  * [[BlendDataVolumes.remove]]

  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
