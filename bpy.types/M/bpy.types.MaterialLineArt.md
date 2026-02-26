# MaterialLineArt(bpy_struct)

base class — [[bpy_struct]]

_class _bpy.types.MaterialLineArt(_bpy_struct_)
    

intersection_priority
    

The intersection line will be included into the object with the higher intersection priority value

Type:
    

int in [0, 255], default 0

mat_occlusion
    

Faces with this material will behave as if it has set number of layers in occlusion

Type:
    

int in [0, 255], default 1

use_intersection_priority_override
    

Override object and collection intersection priority value

Type:
    

boolean, default False

use_material_mask
    

Use material masks to filter out occluded strokes

Type:
    

boolean, default False

use_material_mask_bits
    

Type:
    

boolean array of 8 items, default (False, False, False, False, False, False, False, False)

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

  * [[Material.lineart]]

| 


  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
