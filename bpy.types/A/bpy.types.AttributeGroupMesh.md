# AttributeGroupMesh(bpy_struct)

base class — [[bpy_struct]]

_class _bpy.types.AttributeGroupMesh(_bpy_struct_)
    

Group of geometry attributes

active
    

Active attribute

Type:
    

[[Attribute]]

active_color
    

Active color attribute for display and editing

Type:
    

[[Attribute]]

active_color_index
    

Active color attribute index

Type:
    

int in [-inf, inf], default 0

active_color_name
    

The name of the active color attribute for display and editing

Type:
    

string, default “”, (never None)

active_index
    

Active attribute index or -1 when none are active

Type:
    

int in [-1, inf], default 0

default_color_name
    

The name of the default color attribute used as a fallback for rendering

Type:
    

string, default “”, (never None)

render_color_index
    

The index of the color attribute used as a fallback for rendering

Type:
    

int in [-inf, inf], default 0

new(_name_ , _type_ , _domain_)
    

Add attribute to geometry

Parameters:
    

  * **name** (_string_ _,__(__never None_ _)_) – Name, Name of geometry attribute

  * **type** (enum in [Attribute Type Items](../../bpy_types_enum_items/attribute_type_items.md#rna-enum-attribute-type-items)) – Type, Attribute type

  * **domain** (enum in [Attribute Domain Items](../../bpy_types_enum_items/attribute_domain_items.md#rna-enum-attribute-domain-items)) – Domain, Type of element that attribute is stored on


Returns:
    

New geometry attribute

Return type:
    

[[Attribute]]

remove(_attribute_)
    

Remove attribute from geometry

Parameters:
    

**attribute** ([[Attribute]], (never None)) – Geometry Attribute

domain_size(_domain_)
    

Get the size of a given domain

Parameters:
    

**domain** (enum in [Attribute Domain Items](../../bpy_types_enum_items/attribute_domain_items.md#rna-enum-attribute-domain-items)) – Domain, Type of element that attribute is stored on

Returns:
    

Size, Size of the domain

Return type:
    

int in [0, inf]

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

  * [[Mesh.attributes]]

| 

  * [[Mesh.color_attributes]]

  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
