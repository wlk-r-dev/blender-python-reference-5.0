# SpaceNodeEditor(Space)

base classes — [[bpy_struct]], [[Space]]

_class _bpy.types.SpaceNodeEditor(_Space_)
    

Node editor space data

backdrop_channels
    

Channels of the image to draw

  * `COLOR_ALPHA` Color & Alpha – Display image with RGB colors and alpha transparency.

  * `COLOR` Color – Display image with RGB colors.

  * `ALPHA` Alpha – Display alpha transparency channel.

  * `RED` Red.

  * `GREEN` Green.

  * `BLUE` Blue.


Type:
    

enum in [`'COLOR_ALPHA'`, `'COLOR'`, `'ALPHA'`, `'RED'`, `'GREEN'`, `'BLUE'`], default `'COLOR'`

backdrop_offset
    

Backdrop offset

Type:
    

float array of 2 items in [-inf, inf], default (0.0, 0.0)

backdrop_zoom
    

Backdrop zoom factor

Type:
    

float in [0.01, inf], default 1.0

cursor_location
    

Location for adding new nodes

Type:
    

[[mathutils.Vector]] of 2 items in [-inf, inf], default (0.0, 0.0)

edit_tree
    

Node tree being displayed and edited

Type:
    

[[NodeTree]], (readonly)

id
    

Data-block whose nodes are being edited

Type:
    

[[ID]], (readonly)

id_from
    

Data-block from which the edited data-block is linked

Type:
    

[[ID]], (readonly)

insert_offset_direction
    

Direction to offset nodes on insertion

Type:
    

enum in [`'RIGHT'`, `'LEFT'`], default `'RIGHT'`

node_tree
    

Base node tree from context

Type:
    

[[NodeTree]]

node_tree_sub_type
    

Type:
    

enum in []

overlay
    

Settings for display of overlays in the Node Editor

Type:
    

[[SpaceNodeOverlay]], (readonly, never None)

path
    

Path from the data-block to the currently edited node tree

Type:
    

[[SpaceNodeEditorPath]] [[bpy_prop_collection]] of [[NodeTreePath]], (readonly)

pin
    

Use the pinned node tree

Type:
    

boolean, default False

selected_node_group
    

Node group to edit

Type:
    

[[NodeTree]]

shader_type
    

Type of data to take shader from

  * `OBJECT` Object – Edit shader nodes from Object.

  * `WORLD` World – Edit shader nodes from World.

  * `LINESTYLE` Line Style – Edit shader nodes from Line Style.


Type:
    

enum in [`'OBJECT'`, `'WORLD'`, `'LINESTYLE'`], default `'OBJECT'`

show_annotation
    

Show annotations for this view

Type:
    

boolean, default False

show_backdrop
    

Use active Viewer Node output as backdrop for compositing nodes

Type:
    

boolean, default False

show_gizmo
    

Show gizmos of all types

Type:
    

boolean, default False

show_gizmo_active_node
    

Context sensitive gizmo for the active node

Type:
    

boolean, default True

show_region_asset_shelf
    

Display a region with assets that may currently be relevant (such as brushes in paint modes, or poses in Pose Mode)

Type:
    

boolean, default False

show_region_toolbar
    

Type:
    

boolean, default False

show_region_ui
    

Type:
    

boolean, default False

supports_previews
    

Whether the node editor’s type supports displaying node previews

Type:
    

boolean, default False, (readonly)

texture_type
    

Type of data to take texture from

  * `WORLD` World – Edit texture nodes from World.

  * `BRUSH` Brush – Edit texture nodes from Brush.

  * `LINESTYLE` Line Style – Edit texture nodes from Line Style.


Type:
    

enum in [`'WORLD'`, `'BRUSH'`, `'LINESTYLE'`], default `'WORLD'`

tree_type
    

Node tree type to display and edit

  * `GeometryNodeTree` Geometry Node Editor – Advanced geometry editing and tools creation using nodes.

  * `CompositorNodeTree` Compositor – Create effects and post-process renders, images, and the 3D Viewport.

  * `ShaderNodeTree` Shader Editor – Edit materials, lights, and world shading using nodes.

  * `TextureNodeTree` Texture Node Editor – Edit textures using nodes.


Type:
    

enum in [`'GeometryNodeTree'`, `'CompositorNodeTree'`, `'ShaderNodeTree'`, `'TextureNodeTree'`], default `'DEFAULT'`

cursor_location_from_region(_x_ , _y_)
    

Set the cursor location using region coordinates

Parameters:
    

  * **x** (_int in_ _[__-inf_ _,__inf_ _]_) – x, Region x coordinate

  * **y** (_int in_ _[__-inf_ _,__inf_ _]_) – y, Region y coordinate


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

_classmethod _draw_handler_add(_callback_ , _args_ , _region_type_ , _draw_type_)
    

Add a new draw handler to this space type. It will be called every time the specified region in the space type will be drawn. Note: All arguments are positional only for now.

Parameters:
    

  * **callback** (_Callable_ _[__...__,__Any_ _]_) – A function that will be called when the region is drawn. It gets the specified arguments as input, it’s return value is ignored.

  * **args** (_tuple_ _[__Any_ _,__...__]_) – Arguments that will be passed to the callback.

  * **region_type** (_str_) – The region type the callback draws in; usually `WINDOW`. ([[bpy.types.Region.type]])

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

  * [[bpy_struct.id_data]]
  * [[Space.type]]

| 

  * [[Space.show_locked_time]]
  * [[Space.show_region_header]]

  
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
  * [[bpy_struct.keyframe_insert]]

| 

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
  * [[Space.bl_rna_get_subclass]]
  * [[Space.bl_rna_get_subclass_py]]
  * [[Space.draw_handler_add]]
  * [[Space.draw_handler_remove]]

  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
