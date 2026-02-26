# SpaceUVEditor(bpy_struct)

base class — [`bpy_struct`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct "bpy.types.bpy_struct")

_class _bpy.types.SpaceUVEditor(_bpy_struct_)
    

UV editor data for the image editor space

custom_grid_subdivisions
    

Number of grid units in UV space that make one UV Unit

Type:
    

int array of 2 items in [1, 5000], default (10, 10)

display_stretch_type
    

Type of stretch to display

  * `ANGLE` Angle – Angular distortion between UV and 3D angles.

  * `AREA` Area – Area distortion between UV and 3D faces.


Type:
    

enum in [`'ANGLE'`, `'AREA'`], default `'ANGLE'`

edge_display_type
    

Display style for UV edges

  * `OUTLINE` Outline – Display white edges with black outline.

  * `DASH` Dash – Display dashed black-white edges.

  * `BLACK` Black – Display black edges.

  * `WHITE` White – Display white edges.


Type:
    

enum in [`'OUTLINE'`, `'DASH'`, `'BLACK'`, `'WHITE'`], default `'OUTLINE'`

grid_shape_source
    

Specify source for the grid shape

  * `DYNAMIC` Dynamic – Dynamic grid.

  * `FIXED` Fixed – Manually set grid divisions.

  * `PIXEL` Pixel – Grid aligns with pixels from image.


Type:
    

enum in [`'DYNAMIC'`, `'FIXED'`, `'PIXEL'`], default `'DYNAMIC'`

lock_bounds
    

Constraint to stay within the image bounds while editing

Type:
    

boolean, default False

pixel_round_mode
    

Round UVs to pixels while editing

  * `DISABLED` Disabled – Don’t round to pixels.

  * `CORNER` Corner – Round to pixel corners.

  * `CENTER` Center – Round to pixel centers.


Type:
    

enum in [`'DISABLED'`, `'CORNER'`, `'CENTER'`], default `'DISABLED'`

show_faces
    

Display faces over the image

Type:
    

boolean, default False

show_grid_over_image
    

Show the grid over the image

Type:
    

boolean, default True

show_metadata
    

Display metadata properties of the image

Type:
    

boolean, default False

show_modified_edges
    

Display edges after modifiers are applied

Type:
    

boolean, default False

show_pixel_coords
    

Display UV coordinates in pixels rather than from 0.0 to 1.0

Type:
    

boolean, default False

show_stretch
    

Display faces colored according to the difference in shape between UVs and their 3D coordinates (blue for low distortion, red for high distortion)

Type:
    

boolean, default False

show_uv
    

Display overlay of UV layer

Type:
    

boolean, default False

stretch_opacity
    

Opacity of the UV Stretch overlay

Type:
    

float in [0, 1], default 0.0

tile_grid_shape
    

How many tiles will be shown in the background

Type:
    

int array of 2 items in [1, 100], default (1, 1)

use_live_unwrap
    

Continuously unwrap the selected UV island while transforming pinned vertices

Type:
    

boolean, default False

uv_face_opacity
    

Opacity of faces in UV overlays

Type:
    

float in [0, 1], default 0.0

uv_opacity
    

Opacity of UV overlays

Type:
    

float in [0, 1], default 0.0

_classmethod _bl_rna_get_subclass(_id_ , _default =None_, _/_)
    

Parameters:
    

**id** (_str_) – The RNA type identifier.

Returns:
    

The RNA type or default when not found.

Return type:
    

[`bpy.types.Struct`](bpy.types.Struct.md#bpy.types.Struct "bpy.types.Struct") subclass

_classmethod _bl_rna_get_subclass_py(_id_ , _default =None_, _/_)
    

Parameters:
    

**id** (_str_) – The RNA type identifier.

Returns:
    

The class or default when not found.

Return type:
    

type

## Inherited Properties

  * [`bpy_struct.id_data`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.id_data "bpy.types.bpy_struct.id_data")

| 


  
---|---  
  
## Inherited Functions

  * [`bpy_struct.as_pointer`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.as_pointer "bpy.types.bpy_struct.as_pointer")
  * [`bpy_struct.driver_add`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.driver_add "bpy.types.bpy_struct.driver_add")
  * [`bpy_struct.driver_remove`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.driver_remove "bpy.types.bpy_struct.driver_remove")
  * [`bpy_struct.get`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.get "bpy.types.bpy_struct.get")
  * [`bpy_struct.id_properties_clear`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.id_properties_clear "bpy.types.bpy_struct.id_properties_clear")
  * [`bpy_struct.id_properties_ensure`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.id_properties_ensure "bpy.types.bpy_struct.id_properties_ensure")
  * [`bpy_struct.id_properties_ui`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.id_properties_ui "bpy.types.bpy_struct.id_properties_ui")
  * [`bpy_struct.is_property_hidden`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.is_property_hidden "bpy.types.bpy_struct.is_property_hidden")
  * [`bpy_struct.is_property_overridable_library`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.is_property_overridable_library "bpy.types.bpy_struct.is_property_overridable_library")
  * [`bpy_struct.is_property_readonly`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.is_property_readonly "bpy.types.bpy_struct.is_property_readonly")
  * [`bpy_struct.is_property_set`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.is_property_set "bpy.types.bpy_struct.is_property_set")
  * [`bpy_struct.items`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.items "bpy.types.bpy_struct.items")

| 

  * [`bpy_struct.keyframe_delete`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.keyframe_delete "bpy.types.bpy_struct.keyframe_delete")
  * [`bpy_struct.keyframe_insert`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.keyframe_insert "bpy.types.bpy_struct.keyframe_insert")
  * [`bpy_struct.keys`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.keys "bpy.types.bpy_struct.keys")
  * [`bpy_struct.path_from_id`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.path_from_id "bpy.types.bpy_struct.path_from_id")
  * [`bpy_struct.path_from_module`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.path_from_module "bpy.types.bpy_struct.path_from_module")
  * [`bpy_struct.path_resolve`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.path_resolve "bpy.types.bpy_struct.path_resolve")
  * [`bpy_struct.pop`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.pop "bpy.types.bpy_struct.pop")
  * [`bpy_struct.property_overridable_library_set`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.property_overridable_library_set "bpy.types.bpy_struct.property_overridable_library_set")
  * [`bpy_struct.property_unset`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.property_unset "bpy.types.bpy_struct.property_unset")
  * [`bpy_struct.rna_ancestors`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.rna_ancestors "bpy.types.bpy_struct.rna_ancestors")
  * [`bpy_struct.type_recast`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.type_recast "bpy.types.bpy_struct.type_recast")
  * [`bpy_struct.values`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.values "bpy.types.bpy_struct.values")

  
---|---  
  
## References

  * [`SpaceImageEditor.uv_editor`](bpy.types.SpaceImageEditor.md#bpy.types.SpaceImageEditor.uv_editor "bpy.types.SpaceImageEditor.uv_editor")

| 


  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
