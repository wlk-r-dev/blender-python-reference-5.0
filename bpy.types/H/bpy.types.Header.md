# Header(bpy_struct)

base class — [[bpy_struct]]

_class _bpy.types.Header(_bpy_struct_)
    

Editor header containing UI elements

bl_idname
    

If this is set, the header gets a custom ID, otherwise it takes the name of the class used to define the header; for example, if the class name is “OBJECT_HT_hello”, and bl_idname is not set by the script, then bl_idname = “OBJECT_HT_hello”

Type:
    

string, default “”, (never None)

bl_region_type
    

The region where the header is going to be used in (defaults to header region)

Type:
    

enum in [Region Type Items](../../bpy_types_enum_items/region_type_items.md#rna-enum-region-type-items), default `'HEADER'`

bl_space_type
    

The space where the header is going to be used in

Type:
    

enum in [Space Type Items](../../bpy_types_enum_items/space_type_items.md#rna-enum-space-type-items), default `'EMPTY'`

layout
    

Structure of the header in the UI

Type:
    

[[UILayout]], (readonly)

draw(_context_)
    

Draw UI elements into the header UI layout

_classmethod _append(_draw_func_)
    

Append a draw function to this menu, takes the same arguments as the menus draw function

_classmethod _is_extended()
    

_classmethod _prepend(_draw_func_)
    

Prepend a draw function to this menu, takes the same arguments as the menus draw function

_classmethod _remove(_draw_func_)
    

Remove a draw function that has been added to this menu.

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
  *[/]: Positional-only parameter separator (PEP 570)
