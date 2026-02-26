# WorkSpaceTool(bpy_struct)

base class — [[bpy_struct]]

_class _bpy.types.WorkSpaceTool(_bpy_struct_)
    

brush_type
    

If the tool uses brushes and is limited to a specific brush type, the identifier of the brush type

Type:
    

enum in [`'DEFAULT'`], default `'DEFAULT'`, (readonly)

has_datablock
    

Type:
    

boolean, default False, (readonly)

idname
    

Type:
    

string, default “”, (never None)

idname_fallback
    

Type:
    

string, default “”, (never None)

index
    

Type:
    

int in [-inf, inf], default 0, (readonly)

mode
    

Type:
    

enum in [`'DEFAULT'`], default `'DEFAULT'`, (readonly)

space_type
    

Type:
    

enum in [Space Type Items](../../bpy_types_enum_items/space_type_items.md#rna-enum-space-type-items), default `'EMPTY'`, (readonly)

use_brushes
    

Type:
    

boolean, default False, (readonly)

use_paint_canvas
    

Does this tool use a painting canvas

Type:
    

boolean, default False, (readonly)

widget
    

Type:
    

string, default “”, (readonly, never None)

setup(_idname_ , _*_ , _cursor ='DEFAULT'_, _keymap =''_, _gizmo_group =''_, _brush_type =''_, _data_block =''_, _operator =''_, _index =0_, _options ={}_, _idname_fallback =''_, _keymap_fallback =''_)
    

Set the tool settings

Parameters:
    

  * **idname** (_string_ _,__(__never None_ _)_) – Identifier

  * **cursor** (enum in [Window Cursor Items](../../bpy_types_enum_items/window_cursor_items.md#rna-enum-window-cursor-items), (optional)) – cursor

  * **keymap** (_string_ _,__(__optional_ _,__never None_ _)_) – Key Map

  * **gizmo_group** (_string_ _,__(__optional_ _,__never None_ _)_) – Gizmo Group

  * **brush_type** (_enum in_ _[__]__,__(__optional_ _)_) – Brush Type, Limit this tool to a specific type of brush

  * **data_block** (_string_ _,__(__optional_ _,__never None_ _)_) – Data Block

  * **operator** (_string_ _,__(__optional_ _,__never None_ _)_) – Operator

  * **index** (_int in_ _[__-inf_ _,__inf_ _]__,__(__optional_ _)_) – Index

  * **options** (enum set in {`'KEYMAP_FALLBACK'`, `'USE_BRUSHES'`}, (optional)) – 

Tool Options

    * `KEYMAP_FALLBACK` Fallback.

    * `USE_BRUSHES` Uses Brushes – Allow this tool to use brushes via the asset system.

  * **idname_fallback** (_string_ _,__(__optional_ _,__never None_ _)_) – Fallback Identifier

  * **keymap_fallback** (_string_ _,__(__optional_ _,__never None_ _)_) – Fallback Key Map


operator_properties(_operator_)
    

operator_properties

Return type:
    

[[OperatorProperties]], (never None)

gizmo_group_properties(_group_)
    

gizmo_group_properties

Return type:
    

[[GizmoGroupProperties]], (never None)

refresh_from_context()
    

refresh_from_context

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

  * [[WorkSpace.tools]]
  * [[wmTools.from_space_image_mode]]
  * [[wmTools.from_space_node]]

| 

  * [[wmTools.from_space_sequencer]]
  * [[wmTools.from_space_view3d_mode]]

  
---|---
  *[*]: Keyword-only parameters separator (PEP 3102)
  *[/]: Positional-only parameter separator (PEP 570)
