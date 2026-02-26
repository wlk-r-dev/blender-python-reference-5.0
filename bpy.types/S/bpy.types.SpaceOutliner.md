# SpaceOutliner(Space)

base classes — [`bpy_struct`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct "bpy.types.bpy_struct"), [`Space`](bpy.types.Space.md#bpy.types.Space "bpy.types.Space")

_class _bpy.types.SpaceOutliner(_Space_)
    

Outliner space data

display_mode
    

Type of information to display

  * `SCENES` Scenes – Display scenes and their view layers, collections and objects.

  * `VIEW_LAYER` View Layer – Display collections and objects in the view layer.

  * `SEQUENCE` Video Sequencer – Display data belonging to the Video Sequencer.

  * `LIBRARIES` Blender File – Display data of current file and linked libraries.

  * `DATA_API` Data API – Display low level Blender data and its properties.

  * `LIBRARY_OVERRIDES` Library Overrides – Display data-blocks with library overrides and list their overridden properties.

  * `ORPHAN_DATA` Unused Data – Display data that is unused and/or will be lost when the file is reloaded.


Type:
    

enum in [`'SCENES'`, `'VIEW_LAYER'`, `'SEQUENCE'`, `'LIBRARIES'`, `'DATA_API'`, `'LIBRARY_OVERRIDES'`, `'ORPHAN_DATA'`], default `'SCENES'`

filter_id_type
    

Data-block type to show

Type:
    

enum in [Id Type Items](../../bpy_types_enum_items/id_type_items.md#rna-enum-id-type-items), default `'ACTION'`

filter_invert
    

Invert the object state filter

Type:
    

boolean, default False

filter_state
    

  * `ALL` All – Show all objects in the view layer.

  * `VISIBLE` Visible – Show visible objects.

  * `SELECTED` Selected – Show selected objects.

  * `ACTIVE` Active – Show only the active object.

  * `SELECTABLE` Selectable – Show only selectable objects.


Type:
    

enum in [`'ALL'`, `'VISIBLE'`, `'SELECTED'`, `'ACTIVE'`, `'SELECTABLE'`], default `'ALL'`

filter_text
    

Live search filtering string

Type:
    

string, default “”, (never None)

lib_override_view_mode
    

Choose different visualizations of library override data

  * `PROPERTIES` Properties – Display all local override data-blocks with their overridden properties and buttons to edit them.

  * `HIERARCHIES` Hierarchies – Display library override relationships.


Type:
    

enum in [`'PROPERTIES'`, `'HIERARCHIES'`], default `'PROPERTIES'`

show_mode_column
    

Show the mode column for mode toggle and activation

Type:
    

boolean, default False

show_restrict_column_enable
    

Exclude from view layer

Type:
    

boolean, default False

show_restrict_column_hide
    

Temporarily hide in viewport

Type:
    

boolean, default False

show_restrict_column_holdout
    

Holdout

Type:
    

boolean, default False

show_restrict_column_indirect_only
    

Indirect only

Type:
    

boolean, default False

show_restrict_column_render
    

Globally disable in renders

Type:
    

boolean, default False

show_restrict_column_select
    

Selectable

Type:
    

boolean, default False

show_restrict_column_viewport
    

Globally disable in viewports

Type:
    

boolean, default False

use_filter_case_sensitive
    

Only use case sensitive matches of search string

Type:
    

boolean, default False

use_filter_children
    

Show children

Type:
    

boolean, default False

use_filter_collection
    

Show collections

Type:
    

boolean, default False

use_filter_complete
    

Only use complete matches of search string

Type:
    

boolean, default False

use_filter_id_type
    

Show only data-blocks of one type

Type:
    

boolean, default False

use_filter_lib_override_system
    

For libraries with overrides created, show the overridden values that are defined/controlled automatically (e.g. to make users of an overridden data-block point to the override data, not the original linked data)

Type:
    

boolean, default False

use_filter_object
    

Show objects

Type:
    

boolean, default False

use_filter_object_armature
    

Show armature objects

Type:
    

boolean, default False

use_filter_object_camera
    

Show camera objects

Type:
    

boolean, default False

use_filter_object_content
    

Show what is inside the objects elements

Type:
    

boolean, default False

use_filter_object_empty
    

Show empty objects

Type:
    

boolean, default False

use_filter_object_grease_pencil
    

Show Grease Pencil objects

Type:
    

boolean, default False

use_filter_object_light
    

Show light objects

Type:
    

boolean, default False

use_filter_object_mesh
    

Show mesh objects

Type:
    

boolean, default False

use_filter_object_others
    

Show curves, lattices, light probes, fonts, …

Type:
    

boolean, default False

use_filter_view_layers
    

Show all the view layers

Type:
    

boolean, default False

use_sort_alpha
    

Type:
    

boolean, default False

use_sync_select
    

Sync outliner selection with other editors

Type:
    

boolean, default False

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

_classmethod _draw_handler_add(_callback_ , _args_ , _region_type_ , _draw_type_)
    

Add a new draw handler to this space type. It will be called every time the specified region in the space type will be drawn. Note: All arguments are positional only for now.

Parameters:
    

  * **callback** (_Callable_ _[__...__,__Any_ _]_) – A function that will be called when the region is drawn. It gets the specified arguments as input, it’s return value is ignored.

  * **args** (_tuple_ _[__Any_ _,__...__]_) – Arguments that will be passed to the callback.

  * **region_type** (_str_) – The region type the callback draws in; usually `WINDOW`. ([`bpy.types.Region.type`](../R/bpy.types.Region.md#bpy.types.Region.type "bpy.types.Region.type"))

  * **draw_type** (_str_) – Usually `POST_PIXEL` for 2D drawing and `POST_VIEW` for 3D drawing. In some cases `PRE_VIEW` can be used. `BACKDROP` can be used for backdrops in the node editor.


Returns:
    

Handler that can be removed later on.

Return type:
    

object

_classmethod _draw_handler_remove(_handler_ , _region_type_)
    

Remove a draw handler that was added previously.

Parameters:
    

  * **handler** (_object_) – The draw handler that should be removed.

  * **region_type** (_str_) – Region type the callback was added to.


## Inherited Properties

  * [`bpy_struct.id_data`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.id_data "bpy.types.bpy_struct.id_data")
  * [`Space.type`](bpy.types.Space.md#bpy.types.Space.type "bpy.types.Space.type")

| 

  * [`Space.show_locked_time`](bpy.types.Space.md#bpy.types.Space.show_locked_time "bpy.types.Space.show_locked_time")
  * [`Space.show_region_header`](bpy.types.Space.md#bpy.types.Space.show_region_header "bpy.types.Space.show_region_header")

  
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
  * [`bpy_struct.keyframe_insert`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.keyframe_insert "bpy.types.bpy_struct.keyframe_insert")

| 

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
  * [`Space.bl_rna_get_subclass`](bpy.types.Space.md#bpy.types.Space.bl_rna_get_subclass "bpy.types.Space.bl_rna_get_subclass")
  * [`Space.bl_rna_get_subclass_py`](bpy.types.Space.md#bpy.types.Space.bl_rna_get_subclass_py "bpy.types.Space.bl_rna_get_subclass_py")
  * [`Space.draw_handler_add`](bpy.types.Space.md#bpy.types.Space.draw_handler_add "bpy.types.Space.draw_handler_add")
  * [`Space.draw_handler_remove`](bpy.types.Space.md#bpy.types.Space.draw_handler_remove "bpy.types.Space.draw_handler_remove")

  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
