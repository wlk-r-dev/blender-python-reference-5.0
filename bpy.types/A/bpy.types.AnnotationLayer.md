# AnnotationLayer(bpy_struct)

base class — [[bpy_struct]]

_class _bpy.types.AnnotationLayer(_bpy_struct_)
    

Collection of related sketches

active_frame
    

Frame currently being displayed for this layer

Type:
    

[[AnnotationFrame]], (readonly)

annotation_hide
    

Set annotation Visibility

Type:
    

boolean, default False

annotation_onion_after_color
    

Base color for ghosts after the active frame

Type:
    

[[mathutils.Color]] of 3 items in [0, 1], default (0.25, 0.1, 1.0)

annotation_onion_after_range
    

Maximum number of frames to show after current frame

Type:
    

int in [-1, 120], default 0

annotation_onion_before_color
    

Base color for ghosts before the active frame

Type:
    

[[mathutils.Color]] of 3 items in [0, 1], default (0.302, 0.851, 0.302)

annotation_onion_before_range
    

Maximum number of frames to show before current frame

Type:
    

int in [-1, 120], default 0

annotation_onion_use_custom_color
    

Use custom colors for onion skinning instead of the theme

Type:
    

boolean, default False

annotation_opacity
    

Annotation Layer Opacity

Type:
    

float in [0, 1], default 0.0

color
    

Color for all strokes in this layer

Type:
    

[[mathutils.Color]] of 3 items in [0, 1], default (0.0, 0.0, 0.0)

frames
    

Sketches for this layer on different frames

Type:
    

[[AnnotationFrames]] [[bpy_prop_collection]] of [[AnnotationFrame]], (readonly)

info
    

Layer name

Type:
    

string, default “”, (never None)

is_ruler
    

This is a special ruler layer

Type:
    

boolean, default False, (readonly)

lock
    

Protect layer from further editing and/or frame changes

Type:
    

boolean, default False

lock_frame
    

Lock current frame displayed by layer

Type:
    

boolean, default False

select
    

Layer is selected for editing in the Dope Sheet

Type:
    

boolean, default False

show_in_front
    

Make the layer display in front of objects

Type:
    

boolean, default False

thickness
    

Thickness of annotation strokes

Type:
    

int in [1, 10], default 0

use_annotation_onion_skinning
    

Display annotation onion skins before and after the current frame

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

  * [[Annotation.layers]]
  * [[AnnotationLayers.new]]

| 

  * [[AnnotationLayers.remove]]

  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
