# PointCacheItem(bpy_struct)

base class — [[bpy_struct]]

_class _bpy.types.PointCacheItem(_bpy_struct_)
    

Point cache for physics simulations

filepath
    

Cache file path

Type:
    

string, default “”, (never None, blend relative `//` prefix supported)

frame_end
    

Frame on which the simulation stops

Type:
    

int in [1, 1048574], default 0

frame_start
    

Frame on which the simulation starts

Type:
    

int in [-1048574, 1048574], default 0

frame_step
    

Number of frames between cached frames

Type:
    

int in [1, 20], default 0

index
    

Index number of cache files

Type:
    

int in [-1, 100], default 0

info
    

Info on current cache status

Type:
    

string, default “”, (readonly, never None)

is_baked
    

The cache is baked

Type:
    

boolean, default False, (readonly)

is_baking
    

The cache is being baked

Type:
    

boolean, default False, (readonly)

is_frame_skip
    

Some frames were skipped while baking/saving that cache

Type:
    

boolean, default False, (readonly)

is_outdated
    

Type:
    

boolean, default False, (readonly)

name
    

Cache name

Type:
    

string, default “”, (never None)

use_disk_cache
    

Save cache files to disk (.blend file must be saved first)

Type:
    

boolean, default False

use_external
    

Read cache from an external location

Type:
    

boolean, default False

use_library_path
    

Use this file’s path for the disk cache when library linked into another file (for local bakes per scene file, disable this option)

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

  * [[PointCache.point_caches]]

| 


  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
