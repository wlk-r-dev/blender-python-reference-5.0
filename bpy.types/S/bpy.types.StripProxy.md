# StripProxy(bpy_struct)

base class — [[bpy_struct]]

_class _bpy.types.StripProxy(_bpy_struct_)
    

Proxy parameters for a sequence strip

build_100
    

Build 100% proxy resolution

Type:
    

boolean, default False

build_25
    

Build 25% proxy resolution

Type:
    

boolean, default False

build_50
    

Build 50% proxy resolution

Type:
    

boolean, default False

build_75
    

Build 75% proxy resolution

Type:
    

boolean, default False

build_record_run
    

Build record run time code index

Type:
    

boolean, default False

directory
    

Location to store the proxy files

Type:
    

string, default “”, (never None, blend relative `//` prefix supported)

filepath
    

Location of custom proxy file

Type:
    

string, default “”, (never None, blend relative `//` prefix supported)

quality
    

Quality of proxies to build

Type:
    

int in [0, 32767], default 0

timecode
    

Method for reading the inputs timecode

  * `NONE` None – Ignore generated timecodes, seek in movie stream based on calculated timestamp.

  * `RECORD_RUN` Record Run – Seek based on timestamps read from movie stream, giving the best match between scene and movie times.

  * `RECORD_RUN_NO_GAPS` Record Run No Gaps – Effectively convert movie to an image sequence, ignoring incomplete or dropped frames, and changes in frame rate.


Type:
    

enum in [`'NONE'`, `'RECORD_RUN'`, `'RECORD_RUN_NO_GAPS'`], default `'NONE'`

use_overwrite
    

Overwrite existing proxy files when building

Type:
    

boolean, default False

use_proxy_custom_directory
    

Use a custom directory to store data

Type:
    

boolean, default False

use_proxy_custom_file
    

Use a custom file to read proxy data from

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

  * [[EffectStrip.proxy]]
  * [[ImageStrip.proxy]]
  * [[MetaStrip.proxy]]

| 

  * [[MovieStrip.proxy]]
  * [[SceneStrip.proxy]]

  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
