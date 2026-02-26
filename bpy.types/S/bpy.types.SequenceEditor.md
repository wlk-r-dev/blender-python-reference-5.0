# SequenceEditor(bpy_struct)

base class — [[bpy_struct]]

_class _bpy.types.SequenceEditor(_bpy_struct_)
    

Sequence editing data for a Scene data-block

active_strip
    

Sequencer’s active strip

Type:
    

[[Strip]]

cache_final_size
    

Size of final rendered images cache in megabytes

Type:
    

int in [-inf, inf], default 0, (readonly)

cache_raw_size
    

Size of raw source images cache in megabytes

Type:
    

int in [-inf, inf], default 0, (readonly)

channels
    

Type:
    

[[bpy_prop_collection]] of [[SequenceTimelineChannel]], (readonly)

meta_stack
    

Meta strip stack, last is currently edited meta strip

Type:
    

[[bpy_prop_collection]] of [[Strip]], (readonly)

overlay_frame
    

Number of frames to offset

Type:
    

int in [-inf, inf], default 0

proxy_dir
    

Type:
    

string, default “”, (never None, blend relative `//` prefix supported)

proxy_storage
    

How to store proxies for this project

  * `PER_STRIP` Per Strip – Store proxies using per strip settings.

  * `PROJECT` Project – Store proxies using project directory.


Type:
    

enum in [`'PER_STRIP'`, `'PROJECT'`], default `'PER_STRIP'`

selected_retiming_keys
    

Type:
    

boolean, default False, (readonly)

show_missing_media
    

Render missing images/movies with a solid magenta color

Type:
    

boolean, default False

show_overlay_frame
    

Partial overlay on top of the sequencer with a frame offset

Type:
    

boolean, default False

strips
    

Top-level strips only

Type:
    

[[StripsTopLevel]] [[bpy_prop_collection]] of [[Strip]], (readonly)

strips_all
    

All strips, recursively including those inside metastrips

Type:
    

[[bpy_prop_collection]] of [[Strip]], (readonly)

use_cache_final
    

Cache final image for each frame

Type:
    

boolean, default False

use_cache_raw
    

Cache raw images read from disk, for faster tweaking of strip parameters at the cost of memory usage

Type:
    

boolean, default False

use_overlay_frame_lock
    

Type:
    

boolean, default False

use_prefetch
    

Render frames ahead of current frame in the background for faster playback

Type:
    

boolean, default False

display_stack(_meta_sequence_)
    

Display strips stack

Parameters:
    

**meta_sequence** ([[Strip]]) – Meta Strip, Meta to display its stack

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

  * [[Scene.sequence_editor]]

| 

  * [[Scene.sequence_editor_create]]

  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
