# MovieClip(ID)

base classes — [[bpy_struct]], [[ID]]

_class _bpy.types.MovieClip(_ID_)
    

MovieClip data-block referencing an external movie file

animation_data
    

Animation data for this data-block

Type:
    

[[AnimData]], (readonly)

annotation
    

Annotation data for this movie clip

Type:
    

[[Annotation]]

colorspace_settings
    

Input color space settings

Type:
    

[[ColorManagedInputColorspaceSettings]], (readonly)

display_aspect
    

Display Aspect for this clip, does not affect rendering

Type:
    

[[mathutils.Vector]] of 2 items in [0.1, inf], default (1.0, 1.0)

filepath
    

Filename of the movie or sequence file

Type:
    

string, default “”, (never None, blend relative `//` prefix supported)

fps
    

Detected frame rate of the movie clip in frames per second

Type:
    

float in [-inf, inf], default 0.0, (readonly)

frame_duration
    

Detected duration of movie clip in frames

Type:
    

int in [-inf, inf], default 0, (readonly)

frame_offset
    

Offset of footage first frame relative to its file name (affects only how footage is loading, does not change data associated with a clip)

Type:
    

int in [-inf, inf], default 0

frame_start
    

Global scene frame number at which this movie starts playing (affects all data associated with a clip)

Type:
    

int in [-inf, inf], default 1

proxy
    

Type:
    

[[MovieClipProxy]], (readonly)

size
    

Width and height in pixels, zero when image data cannot be loaded

Type:
    

int array of 2 items in [-inf, inf], default (0, 0), (readonly)

source
    

Where the clip comes from

  * `SEQUENCE` Image Sequence – Multiple image files, as a sequence.

  * `MOVIE` Movie File – Movie file.


Type:
    

enum in [`'SEQUENCE'`, `'MOVIE'`], default `'SEQUENCE'`, (readonly)

tracking
    

Type:
    

[[MovieTracking]], (readonly)

use_proxy
    

Use a preview proxy and/or timecode index for this clip

Type:
    

boolean, default False

use_proxy_custom_directory
    

Create proxy images in a custom directory (default is movie location)

Type:
    

boolean, default False

metadata()
    

Retrieve metadata of the movie file

Returns:
    

Dict-like object containing the metadata

Return type:
    

[[IDPropertyWrapPtr]]

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

  * [[bpy.context.edit_movieclip]]
  * [[BlendData.movieclips]]
  * [[BlendDataMovieClips.load]]
  * [[BlendDataMovieClips.remove]]
  * [[CameraBackgroundImage.clip]]
  * [[CameraSolverConstraint.clip]]
  * [[CompositorNodeKeyingScreen.clip]]
  * [[CompositorNodeMovieClip.clip]]
  * [[CompositorNodeMovieDistortion.clip]]
  * [[CompositorNodePlaneTrackDeform.clip]]

| 

  * [[CompositorNodeStabilize.clip]]
  * [[CompositorNodeTrackPos.clip]]
  * [[FollowTrackConstraint.clip]]
  * [[MovieClipStrip.clip]]
  * [[ObjectSolverConstraint.clip]]
  * [[Scene.active_clip]]
  * [[SpaceClipEditor.clip]]
  * [[StripsMeta.new_clip]]
  * [[StripsTopLevel.new_clip]]

  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
