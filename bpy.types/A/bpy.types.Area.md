# Area(bpy_struct)

base class — [[bpy_struct]]

_class _bpy.types.Area(_bpy_struct_)
    

Area in a subdivided screen, containing an editor

height
    

Area height

Type:
    

int in [0, 32767], default 0, (readonly)

regions
    

Regions this area is subdivided in

Type:
    

[[bpy_prop_collection]] of [[Region]], (readonly)

show_menus
    

Show menus in the header

Type:
    

boolean, default False

spaces
    

Spaces contained in this area, the first being the active space (NOTE: Useful for example to restore a previously used 3D view space in a certain area to get the old view orientation)

Type:
    

[[AreaSpaces]] [[bpy_prop_collection]] of [[Space]], (readonly)

type
    

Current editor type for this area

Type:
    

enum in [Space Type Items](../../bpy_types_enum_items/space_type_items.md#rna-enum-space-type-items), default `'VIEW_3D'`

ui_type
    

Current editor type for this area

Type:
    

enum in []

width
    

Area width

Type:
    

int in [0, 32767], default 0, (readonly)

x
    

The window relative vertical location of the area

Type:
    

int in [-inf, inf], default 0, (readonly)

y
    

The window relative horizontal location of the area

Type:
    

int in [-inf, inf], default 0, (readonly)

tag_redraw()
    

tag_redraw

header_text_set(_text_)
    

Set the header status text

Parameters:
    

**text** (_string_) – Text, New string for the header, None clears the text

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

  * [[Context.area]]

| 

  * [[Screen.areas]]

  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
