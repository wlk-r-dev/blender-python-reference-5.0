# MirrorModifier(Modifier)

base classes — [`bpy_struct`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct "bpy.types.bpy_struct"), [`Modifier`](bpy.types.Modifier.md#bpy.types.Modifier "bpy.types.Modifier")

_class _bpy.types.MirrorModifier(_Modifier_)
    

Mirroring modifier

bisect_threshold
    

Distance from the bisect plane within which vertices are removed

Type:
    

float in [0, inf], default 0.001

merge_threshold
    

Distance within which mirrored vertices are merged

Type:
    

float in [0, inf], default 0.001

mirror_object
    

Object to use as mirror

Type:
    

[`Object`](../O/bpy.types.Object.md#bpy.types.Object "bpy.types.Object")

mirror_offset_u
    

Amount to offset mirrored UVs flipping point from the 0.5 on the U axis

Type:
    

float in [-1, 1], default 0.0

mirror_offset_v
    

Amount to offset mirrored UVs flipping point from the 0.5 point on the V axis

Type:
    

float in [-1, 1], default 0.0

offset_u
    

Mirrored UV offset on the U axis

Type:
    

float in [-10000, 10000], default 0.0

offset_v
    

Mirrored UV offset on the V axis

Type:
    

float in [-10000, 10000], default 0.0

use_axis
    

Enable axis mirror

Type:
    

boolean array of 3 items, default (False, False, False)

use_bisect_axis
    

Cuts the mesh across the mirror plane

Type:
    

boolean array of 3 items, default (False, False, False)

use_bisect_flip_axis
    

Flips the direction of the slice

Type:
    

boolean array of 3 items, default (False, False, False)

use_clip
    

Prevent vertices from going through the mirror during transform

Type:
    

boolean, default False

use_mirror_merge
    

Merge vertices within the merge threshold

Type:
    

boolean, default True

use_mirror_u
    

Mirror the U texture coordinate around the flip offset point

Type:
    

boolean, default False

use_mirror_udim
    

Mirror the texture coordinate around each tile center

Type:
    

boolean, default False

use_mirror_v
    

Mirror the V texture coordinate around the flip offset point

Type:
    

boolean, default False

use_mirror_vertex_groups
    

Mirror vertex groups (e.g. .R->.L)

Type:
    

boolean, default True

_classmethod _bl_rna_get_subclass(_id_ , _default =None_, _/_)
    

Parameters:
    

**id** (_str_) – The RNA type identifier.

Returns:
    

The RNA type or default when not found.

Return type:
    

[`bpy.types.Struct`](../S/bpy.types.Struct.md#bpy.types.Struct "bpy.types.Struct") subclass

_classmethod _bl_rna_get_subclass_py(_id_ , _default =None_, _/_)
    

Parameters:
    

**id** (_str_) – The RNA type identifier.

Returns:
    

The class or default when not found.

Return type:
    

type

## Inherited Properties

  * [`bpy_struct.id_data`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.id_data "bpy.types.bpy_struct.id_data")
  * [`Modifier.name`](bpy.types.Modifier.md#bpy.types.Modifier.name "bpy.types.Modifier.name")
  * [`Modifier.type`](bpy.types.Modifier.md#bpy.types.Modifier.type "bpy.types.Modifier.type")
  * [`Modifier.show_viewport`](bpy.types.Modifier.md#bpy.types.Modifier.show_viewport "bpy.types.Modifier.show_viewport")
  * [`Modifier.show_render`](bpy.types.Modifier.md#bpy.types.Modifier.show_render "bpy.types.Modifier.show_render")
  * [`Modifier.show_in_editmode`](bpy.types.Modifier.md#bpy.types.Modifier.show_in_editmode "bpy.types.Modifier.show_in_editmode")
  * [`Modifier.show_on_cage`](bpy.types.Modifier.md#bpy.types.Modifier.show_on_cage "bpy.types.Modifier.show_on_cage")

| 

  * [`Modifier.show_expanded`](bpy.types.Modifier.md#bpy.types.Modifier.show_expanded "bpy.types.Modifier.show_expanded")
  * [`Modifier.is_active`](bpy.types.Modifier.md#bpy.types.Modifier.is_active "bpy.types.Modifier.is_active")
  * [`Modifier.use_pin_to_last`](bpy.types.Modifier.md#bpy.types.Modifier.use_pin_to_last "bpy.types.Modifier.use_pin_to_last")
  * [`Modifier.is_override_data`](bpy.types.Modifier.md#bpy.types.Modifier.is_override_data "bpy.types.Modifier.is_override_data")
  * [`Modifier.use_apply_on_spline`](bpy.types.Modifier.md#bpy.types.Modifier.use_apply_on_spline "bpy.types.Modifier.use_apply_on_spline")
  * [`Modifier.execution_time`](bpy.types.Modifier.md#bpy.types.Modifier.execution_time "bpy.types.Modifier.execution_time")
  * [`Modifier.persistent_uid`](bpy.types.Modifier.md#bpy.types.Modifier.persistent_uid "bpy.types.Modifier.persistent_uid")

  
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
  * [`bpy_struct.keyframe_delete`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.keyframe_delete "bpy.types.bpy_struct.keyframe_delete")

| 

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
  * [`Modifier.bl_rna_get_subclass`](bpy.types.Modifier.md#bpy.types.Modifier.bl_rna_get_subclass "bpy.types.Modifier.bl_rna_get_subclass")
  * [`Modifier.bl_rna_get_subclass_py`](bpy.types.Modifier.md#bpy.types.Modifier.bl_rna_get_subclass_py "bpy.types.Modifier.bl_rna_get_subclass_py")

  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
