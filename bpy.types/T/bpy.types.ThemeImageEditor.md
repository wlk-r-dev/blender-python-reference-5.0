# ThemeImageEditor(bpy_struct)

base class — [[bpy_struct]]

_class _bpy.types.ThemeImageEditor(_bpy_struct_)
    

Theme settings for the Image Editor

edge_select
    

Type:
    

[[mathutils.Color]] of 3 items in [0, 1], default (0.0, 0.0, 0.0)

edge_width
    

Type:
    

int in [1, 32], default 0

editmesh_active
    

Type:
    

float array of 4 items in [0, 1], default (0.0, 0.0, 0.0, 0.0)

face
    

Type:
    

float array of 4 items in [0, 1], default (0.0, 0.0, 0.0, 0.0)

face_mode_select
    

Type:
    

float array of 4 items in [0, 1], default (0.0, 0.0, 0.0, 0.0)

face_select
    

Type:
    

float array of 4 items in [0, 1], default (0.0, 0.0, 0.0, 0.0)

facedot_size
    

Type:
    

int in [1, 10], default 0

grid
    

Type:
    

float array of 4 items in [0, 1], default (0.0, 0.0, 0.0, 0.0)

metadatabg
    

Type:
    

[[mathutils.Color]] of 3 items in [0, 1], default (0.0, 0.0, 0.0)

metadatatext
    

Type:
    

[[mathutils.Color]] of 3 items in [0, 1], default (0.0, 0.0, 0.0)

preview_stitch_active
    

Type:
    

float array of 4 items in [0, 1], default (0.0, 0.0, 0.0, 0.0)

preview_stitch_edge
    

Type:
    

float array of 4 items in [0, 1], default (0.0, 0.0, 0.0, 0.0)

preview_stitch_face
    

Type:
    

float array of 4 items in [0, 1], default (0.0, 0.0, 0.0, 0.0)

preview_stitch_stitchable
    

Type:
    

float array of 4 items in [0, 1], default (0.0, 0.0, 0.0, 0.0)

preview_stitch_unstitchable
    

Type:
    

float array of 4 items in [0, 1], default (0.0, 0.0, 0.0, 0.0)

preview_stitch_vert
    

Type:
    

float array of 4 items in [0, 1], default (0.0, 0.0, 0.0, 0.0)

scope_back
    

Type:
    

float array of 4 items in [0, 1], default (0.0, 0.0, 0.0, 0.0)

space
    

Settings for space

Type:
    

[[ThemeSpaceGeneric]], (readonly, never None)

uv_shadow
    

Type:
    

float array of 4 items in [0, 1], default (0.0, 0.0, 0.0, 0.0)

vertex
    

Type:
    

[[mathutils.Color]] of 3 items in [0, 1], default (0.0, 0.0, 0.0)

vertex_select
    

Type:
    

[[mathutils.Color]] of 3 items in [0, 1], default (0.0, 0.0, 0.0)

vertex_size
    

Type:
    

int in [1, 32], default 0

wire_edit
    

Type:
    

[[mathutils.Color]] of 3 items in [0, 1], default (0.0, 0.0, 0.0)

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

  * [[Theme.image_editor]]

| 


  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
