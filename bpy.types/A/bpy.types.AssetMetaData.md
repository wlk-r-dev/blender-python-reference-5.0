# AssetMetaData(bpy_struct)

base class — [[bpy_struct]]

_class _bpy.types.AssetMetaData(_bpy_struct_)
    

Additional data stored for an asset data-block

active_tag
    

Index of the tag set for editing

Type:
    

int in [-32768, 32767], default 0

author
    

Name of the creator of the asset

Type:
    

string, default “”, (never None)

catalog_id
    

Identifier for the asset’s catalog, used by Blender to look up the asset’s catalog path. Must be a UUID according to RFC4122.

Type:
    

string, default “”, (never None)

catalog_simple_name
    

Simple name of the asset’s catalog, for debugging and data recovery purposes

Type:
    

string, default “”, (readonly, never None)

copyright
    

Copyright notice for this asset. An empty copyright notice does not necessarily indicate that this is copyright-free. Contact the author if any clarification is needed.

Type:
    

string, default “”, (never None)

description
    

A description of the asset to be displayed for the user

Type:
    

string, default “”, (never None)

license
    

The type of license this asset is distributed under. An empty license name does not necessarily indicate that this is free of licensing terms. Contact the author if any clarification is needed.

Type:
    

string, default “”, (never None)

tags
    

Custom tags (name tokens) for the asset, used for filtering and general asset management

Type:
    

[[AssetTags]] [[bpy_prop_collection]] of [[AssetTag]], (readonly)

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

  * [[AssetRepresentation.metadata]]
  * [[FileSelectEntry.asset_data]]

| 

  * [[ID.asset_data]]

  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
