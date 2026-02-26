# AssetShelf(bpy_struct)

base class — [[bpy_struct]]

subclasses — [[IMAGE_AST_brush_paint]], [[NODE_AST_compositor]], [[VIEW3D_AST_brush_gpencil_paint]], [[VIEW3D_AST_brush_gpencil_sculpt]], [[VIEW3D_AST_brush_gpencil_vertex]], [[VIEW3D_AST_brush_gpencil_weight]], [[VIEW3D_AST_brush_sculpt]], [[VIEW3D_AST_brush_sculpt_curves]], [[VIEW3D_AST_brush_texture_paint]], [[VIEW3D_AST_brush_vertex_paint]], [[VIEW3D_AST_brush_weight_paint]], [[VIEW3D_AST_pose_library]]

_class _bpy.types.AssetShelf(_bpy_struct_)
    

Regions for quick access to assets

asset_library_reference
    

Choose the asset library to display assets from

  * `ALL` All Libraries – Show assets from all of the listed asset libraries.

  * `LOCAL` Current File – Show the assets currently available in this Blender session.

  * `ESSENTIALS` Essentials – Show the basic building blocks and utilities coming with Blender.

  * `CUSTOM` Custom – Show assets from the asset libraries configured in the Preferences.


Type:
    

enum in [`'ALL'`, `'LOCAL'`, `'ESSENTIALS'`, `'CUSTOM'`], default `'ALL'`

bl_activate_operator
    

Operator to call when activating an item with asset reference properties

Type:
    

string, default “”, (never None)

bl_default_preview_size
    

Default size of the asset preview thumbnails in pixels

Type:
    

int in [32, 256], default 0

bl_drag_operator
    

Operator to call when dragging an item with asset reference properties

Type:
    

string, default “”, (never None)

bl_idname
    

If this is set, the asset gets a custom ID, otherwise it takes the name of the class used to define the asset (for example, if the class name is “OBJECT_AST_hello”, and bl_idname is not set by the script, then bl_idname = “OBJECT_AST_hello”)

Type:
    

string, default “”, (never None)

bl_options
    

Options for this asset shelf type

  * `NO_ASSET_DRAG` No Asset Dragging – Disable the default asset dragging on drag events. Useful for implementing custom dragging via custom key-map items..

  * `DEFAULT_VISIBLE` Visible by Default – Unhide the asset shelf when it’s available for the first time, otherwise it will be hidden.

  * `STORE_ENABLED_CATALOGS_IN_PREFERENCES` Store Enabled Catalogs in Preferences – Store the shelf’s enabled catalogs in the preferences rather than the local asset shelf settings.

  * `ACTIVATE_FOR_CONTEXT_MENU` When spawning a context menu for an asset, activate the asset and call `bl_activate_operator` if present, rather than just highlighting the asset.


Type:
    

enum set in {`'NO_ASSET_DRAG'`, `'DEFAULT_VISIBLE'`, `'STORE_ENABLED_CATALOGS_IN_PREFERENCES'`, `'ACTIVATE_FOR_CONTEXT_MENU'`}, default set()

bl_space_type
    

The space where the asset shelf will show up in. Ignored for popup asset shelves which can be displayed in any space.

Type:
    

enum in [Space Type Items](../../bpy_types_enum_items/space_type_items.md#rna-enum-space-type-items), default `'EMPTY'`

filter_action
    

Show Action data-blocks

Type:
    

boolean, default False

filter_annotations
    

Show Annotation data-blocks

Type:
    

boolean, default False

filter_armature
    

Show Armature data-blocks

Type:
    

boolean, default False

filter_brush
    

Show Brushes data-blocks

Type:
    

boolean, default False

filter_cachefile
    

Show Cache File data-blocks

Type:
    

boolean, default False

filter_camera
    

Show Camera data-blocks

Type:
    

boolean, default False

filter_curve
    

Show Curve data-blocks

Type:
    

boolean, default False

filter_curves
    

Show/hide Curves data-blocks

Type:
    

boolean, default False

filter_font
    

Show Font data-blocks

Type:
    

boolean, default False

filter_grease_pencil
    

Show Grease Pencil data-blocks

Type:
    

boolean, default False

filter_group
    

Show Collection data-blocks

Type:
    

boolean, default False

filter_image
    

Show Image data-blocks

Type:
    

boolean, default False

filter_lattice
    

Show Lattice data-blocks

Type:
    

boolean, default False

filter_light
    

Show Light data-blocks

Type:
    

boolean, default False

filter_light_probe
    

Show Light Probe data-blocks

Type:
    

boolean, default False

filter_linestyle
    

Show Freestyle’s Line Style data-blocks

Type:
    

boolean, default False

filter_mask
    

Show Mask data-blocks

Type:
    

boolean, default False

filter_material
    

Show Material data-blocks

Type:
    

boolean, default False

filter_mesh
    

Show Mesh data-blocks

Type:
    

boolean, default False

filter_metaball
    

Show Metaball data-blocks

Type:
    

boolean, default False

filter_movie_clip
    

Show Movie Clip data-blocks

Type:
    

boolean, default False

filter_node_tree
    

Show Node Tree data-blocks

Type:
    

boolean, default False

filter_object
    

Show Object data-blocks

Type:
    

boolean, default False

filter_paint_curve
    

Show Paint Curve data-blocks

Type:
    

boolean, default False

filter_palette
    

Show Palette data-blocks

Type:
    

boolean, default False

filter_particle_settings
    

Show Particle Settings data-blocks

Type:
    

boolean, default False

filter_pointcloud
    

Show/hide Point Cloud data-blocks

Type:
    

boolean, default False

filter_scene
    

Show Scene data-blocks

Type:
    

boolean, default False

filter_sound
    

Show Sound data-blocks

Type:
    

boolean, default False

filter_speaker
    

Show Speaker data-blocks

Type:
    

boolean, default False

filter_text
    

Show Text data-blocks

Type:
    

boolean, default False

filter_texture
    

Show Texture data-blocks

Type:
    

boolean, default False

filter_volume
    

Show/hide Volume data-blocks

Type:
    

boolean, default False

filter_work_space
    

Show workspace data-blocks

Type:
    

boolean, default False

filter_world
    

Show World data-blocks

Type:
    

boolean, default False

preview_size
    

Size of the asset preview thumbnails in pixels

Type:
    

int in [32, 256], default 0

search_filter
    

Filter assets by name

Type:
    

string, default “”, (never None)

show_names
    

Show the asset name together with the preview. Otherwise only the preview will be visible.

Type:
    

boolean, default False

_classmethod _poll(_context_)
    

If this method returns a non-null output, the asset shelf will be visible

Return type:
    

boolean

_classmethod _asset_poll(_asset_)
    

Determine if an asset should be visible in the asset shelf. If this method returns a non-null output, the asset will be visible.

Return type:
    

boolean

_classmethod _get_active_asset()
    

Return a reference to the asset that should be highlighted as active in the asset shelf

Returns:
    

The weak reference to the asset to be highlighted as active, or None

Return type:
    

[[AssetWeakReference]]

_classmethod _draw_context_menu(_context_ , _asset_ , _layout_)
    

Draw UI elements into the context menu UI layout displayed on right click

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
  *[/]: Positional-only parameter separator (PEP 570)
