# DisplaceModifier(Modifier)

base classes — [[bpy_struct]], [[Modifier]]

_class _bpy.types.DisplaceModifier(_Modifier_)
    

Displacement modifier

direction
    

  * `X` X – Use the texture’s intensity value to displace in the X direction.

  * `Y` Y – Use the texture’s intensity value to displace in the Y direction.

  * `Z` Z – Use the texture’s intensity value to displace in the Z direction.

  * `NORMAL` Normal – Use the texture’s intensity value to displace along the vertex normal.

  * `CUSTOM_NORMAL` Custom Normal – Use the texture’s intensity value to displace along the (averaged) custom normal (falls back to vertex).

  * `RGB_TO_XYZ` RGB to XYZ – Use the texture’s RGB values to displace the mesh in the XYZ direction.


Type:
    

enum in [`'X'`, `'Y'`, `'Z'`, `'NORMAL'`, `'CUSTOM_NORMAL'`, `'RGB_TO_XYZ'`], default `'NORMAL'`

invert_vertex_group
    

Invert vertex group influence

Type:
    

boolean, default False

mid_level
    

Material value that gives no displacement

Type:
    

float in [-inf, inf], default 0.5

space
    

  * `LOCAL` Local – Direction is defined in local coordinates.

  * `GLOBAL` Global – Direction is defined in global coordinates.


Type:
    

enum in [`'LOCAL'`, `'GLOBAL'`], default `'LOCAL'`

strength
    

Amount to displace geometry

Type:
    

float in [-inf, inf], default 1.0

texture
    

Type:
    

[[Texture]]

texture_coords
    

  * `LOCAL` Local – Use the local coordinate system for the texture coordinates.

  * `GLOBAL` Global – Use the global coordinate system for the texture coordinates.

  * `OBJECT` Object – Use the linked object’s local coordinate system for the texture coordinates.

  * `UV` UV – Use UV coordinates for the texture coordinates.


Type:
    

enum in [`'LOCAL'`, `'GLOBAL'`, `'OBJECT'`, `'UV'`], default `'LOCAL'`

texture_coords_bone
    

Bone to set the texture coordinates

Type:
    

string, default “”, (never None)

texture_coords_object
    

Object to set the texture coordinates

Type:
    

[[Object]]

uv_layer
    

UV map name

Type:
    

string, default “”, (never None)

vertex_group
    

Name of Vertex Group which determines influence of modifier per point

Type:
    

string, default “”, (never None)

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
  * [[Modifier.name]]
  * [[Modifier.type]]
  * [[Modifier.show_viewport]]
  * [[Modifier.show_render]]
  * [[Modifier.show_in_editmode]]
  * [[Modifier.show_on_cage]]

| 

  * [[Modifier.show_expanded]]
  * [[Modifier.is_active]]
  * [[Modifier.use_pin_to_last]]
  * [[Modifier.is_override_data]]
  * [[Modifier.use_apply_on_spline]]
  * [[Modifier.execution_time]]
  * [[Modifier.persistent_uid]]

  
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
  * [[Modifier.bl_rna_get_subclass]]
  * [[Modifier.bl_rna_get_subclass_py]]

  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
