# SpreadsheetTableIDGeometry(SpreadsheetTableID)

base classes — [[bpy_struct]], [[SpreadsheetTableID]]

_class _bpy.types.SpreadsheetTableIDGeometry(_SpreadsheetTableID_)
    

attribute_domain
    

Attribute domain to display

Type:
    

enum in [Attribute Domain Items](../../bpy_types_enum_items/attribute_domain_items.md#rna-enum-attribute-domain-items), default `'POINT'`, (readonly)

geometry_component_type
    

Part of the geometry to display data from

Type:
    

enum in [Geometry Component Type Items](../../bpy_types_enum_items/geometry_component_type_items.md#rna-enum-geometry-component-type-items), default `'MESH'`, (readonly)

layer_index
    

Index of the Grease Pencil layer

Type:
    

int in [-inf, inf], default 0, (readonly)

object_eval_state
    

  * `EVALUATED` Evaluated – Use data from fully or partially evaluated object.

  * `ORIGINAL` Original – Use data from original object without any modifiers applied.

  * `VIEWER_NODE` Viewer Node – Use intermediate data from viewer node.


Type:
    

enum in [`'EVALUATED'`, `'ORIGINAL'`, `'VIEWER_NODE'`], default `'EVALUATED'`, (readonly)

viewer_path
    

Path to the data that is displayed

Type:
    

[[ViewerPath]], (readonly)

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

  * [[SpreadsheetTableID.type]]

  
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
  * [[SpreadsheetTableID.bl_rna_get_subclass]]
  * [[SpreadsheetTableID.bl_rna_get_subclass_py]]

  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
