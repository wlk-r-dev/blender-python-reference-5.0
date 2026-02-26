# RenderLayer(bpy_struct)

base class — [[bpy_struct]]

_class _bpy.types.RenderLayer(_bpy_struct_)
    

name
    

View layer name

Type:
    

string, default “”, (readonly, never None)

passes
    

Type:
    

[[RenderPasses]] [[bpy_prop_collection]] of [[RenderPass]], (readonly)

use_ao
    

Render Ambient Occlusion in this Layer

Type:
    

boolean, default False, (readonly)

use_grease_pencil
    

Render Grease Pencil on this layer

Type:
    

boolean, default False, (readonly)

use_motion_blur
    

Render motion blur in this Layer, if enabled in the scene

Type:
    

boolean, default False, (readonly)

use_pass_ambient_occlusion
    

Deliver Ambient Occlusion pass

Type:
    

boolean, default False, (readonly)

use_pass_combined
    

Deliver full combined RGBA buffer

Type:
    

boolean, default False, (readonly)

use_pass_diffuse_color
    

Deliver diffuse color pass

Type:
    

boolean, default False, (readonly)

use_pass_diffuse_direct
    

Deliver diffuse direct pass

Type:
    

boolean, default False, (readonly)

use_pass_diffuse_indirect
    

Deliver diffuse indirect pass

Type:
    

boolean, default False, (readonly)

use_pass_emit
    

Deliver emission pass

Type:
    

boolean, default False, (readonly)

use_pass_environment
    

Deliver environment lighting pass

Type:
    

boolean, default False, (readonly)

use_pass_glossy_color
    

Deliver glossy color pass

Type:
    

boolean, default False, (readonly)

use_pass_glossy_direct
    

Deliver glossy direct pass

Type:
    

boolean, default False, (readonly)

use_pass_glossy_indirect
    

Deliver glossy indirect pass

Type:
    

boolean, default False, (readonly)

use_pass_material_index
    

Deliver material index pass

Type:
    

boolean, default False, (readonly)

use_pass_mist
    

Deliver mist factor pass (0.0 to 1.0)

Type:
    

boolean, default False, (readonly)

use_pass_normal
    

Deliver normal pass

Type:
    

boolean, default False, (readonly)

use_pass_object_index
    

Deliver object index pass

Type:
    

boolean, default False, (readonly)

use_pass_position
    

Deliver position pass

Type:
    

boolean, default False, (readonly)

use_pass_shadow
    

Deliver shadow pass

Type:
    

boolean, default False, (readonly)

use_pass_subsurface_color
    

Deliver subsurface color pass

Type:
    

boolean, default False, (readonly)

use_pass_subsurface_direct
    

Deliver subsurface direct pass

Type:
    

boolean, default False, (readonly)

use_pass_subsurface_indirect
    

Deliver subsurface indirect pass

Type:
    

boolean, default False, (readonly)

use_pass_transmission_color
    

Deliver transmission color pass

Type:
    

boolean, default False, (readonly)

use_pass_transmission_direct
    

Deliver transmission direct pass

Type:
    

boolean, default False, (readonly)

use_pass_transmission_indirect
    

Deliver transmission indirect pass

Type:
    

boolean, default False, (readonly)

use_pass_uv
    

Deliver texture UV pass

Type:
    

boolean, default False, (readonly)

use_pass_vector
    

Deliver speed vector pass

Type:
    

boolean, default False, (readonly)

use_pass_z
    

Deliver depth values pass

Type:
    

boolean, default False, (readonly)

use_sky
    

Render Sky in this Layer

Type:
    

boolean, default False, (readonly)

use_solid
    

Render Solid faces in this Layer

Type:
    

boolean, default False, (readonly)

use_strand
    

Render Strands in this Layer

Type:
    

boolean, default False, (readonly)

use_volumes
    

Render volumes in this Layer

Type:
    

boolean, default False, (readonly)

load_from_file(_filepath_ , _*_ , _x =0_, _y =0_)
    

Copies the pixels of this renderlayer from an image file

Parameters:
    

  * **filepath** (_string_ _,__(__never None_ _)_) – File Path, File path to load into this render tile, must be no smaller than the renderlayer

  * **x** (_int in_ _[__0_ _,__inf_ _]__,__(__optional_ _)_) – Offset X, Offset the position to copy from if the image is larger than the render layer

  * **y** (_int in_ _[__0_ _,__inf_ _]__,__(__optional_ _)_) – Offset Y, Offset the position to copy from if the image is larger than the render layer


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

  * [[RenderResult.layers]]

| 


  
---|---
  *[*]: Keyword-only parameters separator (PEP 3102)
  *[/]: Positional-only parameter separator (PEP 570)
