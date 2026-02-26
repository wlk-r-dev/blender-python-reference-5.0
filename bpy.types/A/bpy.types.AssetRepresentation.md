# AssetRepresentation(bpy_struct)

base class — [[bpy_struct]]

_class _bpy.types.AssetRepresentation(_bpy_struct_)
    

Information about an entity that makes it possible for the asset system to deal with the entity as asset

full_library_path
    

Absolute path to the .blend file containing this asset

Type:
    

string, default “”, (readonly, never None)

full_path
    

Absolute path to the .blend file containing this asset extended with the path of the asset inside the file

Type:
    

string, default “”, (readonly, never None)

id_type
    

The type of the data-block, if the asset represents one (‘NONE’ otherwise)

Type:
    

enum in [Id Type Items](../../bpy_types_enum_items/id_type_items.md#rna-enum-id-type-items), default `'ACTION'`, (readonly)

local_id
    

The local data-block this asset represents; only valid if that is a data-block in this file

Type:
    

[[ID]], (readonly)

metadata
    

Additional information about the asset

Type:
    

[[AssetMetaData]], (readonly)

name
    

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

  * [[bpy.context.asset]]
  * [[bpy.context.selected_assets]]
  * [[AssetShelf.asset_poll]]

| 

  * [[AssetShelf.draw_context_menu]]
  * [[Context.asset]]

  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
