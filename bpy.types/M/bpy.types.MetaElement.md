# MetaElement(bpy_struct)

base class — [[bpy_struct]]

_class _bpy.types.MetaElement(_bpy_struct_)
    

Blobby element in a metaball data-block

co
    

Type:
    

[[mathutils.Vector]] of 3 items in [-inf, inf], default (0.0, 0.0, 0.0)

hide
    

Hide element

Type:
    

boolean, default False

radius
    

Type:
    

float in [0, inf], default 0.0

rotation
    

Normalized quaternion rotation

Type:
    

[[mathutils.Quaternion]] rotation of 4 items in [-inf, inf], default (0.0, 0.0, 0.0, 0.0)

select
    

Select element

Type:
    

boolean, default False

size_x
    

Size of element, use of components depends on element type

Type:
    

float in [0, 20], default 0.0

size_y
    

Size of element, use of components depends on element type

Type:
    

float in [0, 20], default 0.0

size_z
    

Size of element, use of components depends on element type

Type:
    

float in [0, 20], default 0.0

stiffness
    

Stiffness defines how much of the element to fill

Type:
    

float in [0, 10], default 0.0

type
    

Metaball type

Type:
    

enum in [Metaelem Type Items](../../bpy_types_enum_items/metaelem_type_items.md#rna-enum-metaelem-type-items), default `'BALL'`

use_negative
    

Set metaball as negative one

Type:
    

boolean, default False

use_scale_stiffness
    

Scale stiffness instead of radius

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

  * [[MetaBall.elements]]
  * [[MetaBallElements.active]]

| 

  * [[MetaBallElements.new]]
  * [[MetaBallElements.remove]]

  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
