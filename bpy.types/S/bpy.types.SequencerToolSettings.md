# SequencerToolSettings(bpy_struct)

base class — [[bpy_struct]]

_class _bpy.types.SequencerToolSettings(_bpy_struct_)
    

fit_method
    

Scale fit method

Type:
    

enum in [Strip Scale Method Items](../../bpy_types_enum_items/strip_scale_method_items.md#rna-enum-strip-scale-method-items), default `'FIT'`

overlap_mode
    

How to resolve overlap after transformation

  * `EXPAND` Expand – Move strips so transformed strips fit.

  * `OVERWRITE` Overwrite – Trim or split strips to resolve overlap.

  * `SHUFFLE` Shuffle – Move transformed strips to nearest free space to resolve overlap.


Type:
    

enum in [`'EXPAND'`, `'OVERWRITE'`, `'SHUFFLE'`], default `'EXPAND'`

pivot_point
    

Rotation or scaling pivot point

  * `CENTER` Bounding Box Center.

  * `MEDIAN` Median Point.

  * `CURSOR` 2D Cursor – Pivot around the 2D cursor.

  * `INDIVIDUAL_ORIGINS` Individual Origins – Pivot around each selected island’s own median point.


Type:
    

enum in [`'CENTER'`, `'MEDIAN'`, `'CURSOR'`, `'INDIVIDUAL_ORIGINS'`], default `'CENTER'`

snap_distance
    

Maximum distance for snapping in pixels

Type:
    

int in [-inf, inf], default 15

snap_ignore_muted
    

Don’t snap to hidden strips

Type:
    

boolean, default False

snap_ignore_sound
    

Don’t snap to sound strips

Type:
    

boolean, default False

snap_to_borders
    

Snap to preview borders

Type:
    

boolean, default False

snap_to_center
    

Snap to preview center

Type:
    

boolean, default False

snap_to_current_frame
    

Snap to current frame

Type:
    

boolean, default False

snap_to_frame_range
    

Snap to preview or scene start and end frame

Type:
    

boolean, default False

snap_to_hold_offset
    

Snap to strip hold offsets

Type:
    

boolean, default False

snap_to_markers
    

Snap to markers

Type:
    

boolean, default False

snap_to_retiming_keys
    

Snap to retiming keys

Type:
    

boolean, default False

snap_to_strips_preview
    

Snap to borders and origins of deselected, visible strips

Type:
    

boolean, default False

use_snap_current_frame_to_strips
    

Snap current frame to strip start or end

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

  * [[ToolSettings.sequencer_tool_settings]]

| 


  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
