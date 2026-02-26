# Object(ID)

## Basic Object Operations Example

This script demonstrates basic operations on object like creating new object, placing it into a view layer, selecting it and making it active.
    
    
    import bpy
    
    view_layer = bpy.context.view_layer
    
    # Create new light data-block.
    light_data = bpy.data.lights.new(name="New Light", type='POINT')
    
    # Create new object with our light data-block.
    light_object = bpy.data.objects.new(name="New Light", object_data=light_data)
    
    # Link light object to the active collection of current view layer,
    # so that it'll appear in the current scene.
    view_layer.active_layer_collection.collection.objects.link(light_object)
    
    # Place light to a specified location.
    light_object.location = (5.0, 5.0, 5.0)
    
    # And finally select it and make it active.
    light_object.select_set(True)
    view_layer.objects.active = light_object
    

base classes — [`bpy_struct`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct "bpy.types.bpy_struct"), [`ID`](../I/bpy.types.ID.md#bpy.types.ID "bpy.types.ID")

_class _bpy.types.Object(_ID_)
    

Object data-block defining an object in a scene

active_material
    

Active material being displayed

Type:
    

[`Material`](../M/bpy.types.Material.md#bpy.types.Material "bpy.types.Material")

active_material_index
    

Index of active material slot

Type:
    

int in [0, inf], default 0

active_selection_set
    

Index of the currently active selection set

Type:
    

int in [-inf, inf], default 0

active_shape_key
    

Current shape key

Type:
    

[`ShapeKey`](../S/bpy.types.ShapeKey.md#bpy.types.ShapeKey "bpy.types.ShapeKey"), (readonly)

active_shape_key_index
    

Current shape key index

Type:
    

int in [-32768, 32767], default 0

add_rest_position_attribute
    

Add a “rest_position” attribute that is a copy of the position attribute before shape keys and modifiers are evaluated

Type:
    

boolean, default False

animation_data
    

Animation data for this data-block

Type:
    

[`AnimData`](../A/bpy.types.AnimData.md#bpy.types.AnimData "bpy.types.AnimData"), (readonly)

animation_visualization
    

Animation data for this data-block

Type:
    

[`AnimViz`](../A/bpy.types.AnimViz.md#bpy.types.AnimViz "bpy.types.AnimViz"), (readonly, never None)

bound_box
    

Object’s bounding box in object-space coordinates, all values are -1.0 when not available

Type:
    

float multi-dimensional array of 8 * 3 items in [-inf, inf], default ((0.0, 0.0, 0.0), (0.0, 0.0, 0.0), (0.0, 0.0, 0.0), (0.0, 0.0, 0.0), (0.0, 0.0, 0.0), (0.0, 0.0, 0.0), (0.0, 0.0, 0.0), (0.0, 0.0, 0.0)), (readonly)

collision
    

Settings for using the object as a collider in physics simulation

Type:
    

[`CollisionSettings`](../C/bpy.types.CollisionSettings.md#bpy.types.CollisionSettings "bpy.types.CollisionSettings"), (readonly)

color
    

Object color and alpha, used when the Object Color mode is enabled

Type:
    

float array of 4 items in [0, inf], default (1.0, 1.0, 1.0, 1.0)

constraints
    

Constraints affecting the transformation of the object

Type:
    

[`ObjectConstraints`](bpy.types.ObjectConstraints.md#bpy.types.ObjectConstraints "bpy.types.ObjectConstraints") [`bpy_prop_collection`](../_other/bpy.types.bpy_prop_collection.md#bpy.types.bpy_prop_collection "bpy.types.bpy_prop_collection") of [`Constraint`](../C/bpy.types.Constraint.md#bpy.types.Constraint "bpy.types.Constraint"), (readonly)

cycles
    

Cycles object settings

Type:
    

`CyclesObjectSettings`, (readonly)

data
    

Object data

Type:
    

[`ID`](../I/bpy.types.ID.md#bpy.types.ID "bpy.types.ID")

delta_location
    

Extra translation added to the location of the object

Type:
    

[`mathutils.Vector`](mathutils.md#mathutils.Vector "mathutils.Vector") of 3 items in [-inf, inf], default (0.0, 0.0, 0.0)

delta_rotation_euler
    

Extra rotation added to the rotation of the object (when using Euler rotations)

Type:
    

[`mathutils.Euler`](mathutils.md#mathutils.Euler "mathutils.Euler") rotation of 3 items in [-inf, inf], default (0.0, 0.0, 0.0)

delta_rotation_quaternion
    

Extra rotation added to the rotation of the object (when using Quaternion rotations)

Type:
    

[`mathutils.Quaternion`](mathutils.md#mathutils.Quaternion "mathutils.Quaternion") rotation of 4 items in [-inf, inf], default (1.0, 0.0, 0.0, 0.0)

delta_scale
    

Extra scaling added to the scale of the object

Type:
    

[`mathutils.Vector`](mathutils.md#mathutils.Vector "mathutils.Vector") of 3 items in [-inf, inf], default (1.0, 1.0, 1.0)

dimensions
    

Absolute bounding box dimensions of the object. Warning: Assigning to it or its members multiple consecutive times will not work correctly, as this needs up-to-date evaluated data

Type:
    

[`mathutils.Vector`](mathutils.md#mathutils.Vector "mathutils.Vector") of 3 items in [-inf, inf], default (0.0, 0.0, 0.0)

display
    

Object display settings for 3D viewport

Type:
    

[`ObjectDisplay`](bpy.types.ObjectDisplay.md#bpy.types.ObjectDisplay "bpy.types.ObjectDisplay"), (readonly, never None)

display_bounds_type
    

Object boundary display type

  * `BOX` Box – Display bounds as box.

  * `SPHERE` Sphere – Display bounds as sphere.

  * `CYLINDER` Cylinder – Display bounds as cylinder.

  * `CONE` Cone – Display bounds as cone.

  * `CAPSULE` Capsule – Display bounds as capsule.


Type:
    

enum in [`'BOX'`, `'SPHERE'`, `'CYLINDER'`, `'CONE'`, `'CAPSULE'`], default `'BOX'`

display_type
    

How to display object in viewport

  * `BOUNDS` Bounds – Display the bounds of the object.

  * `WIRE` Wire – Display the object as a wireframe.

  * `SOLID` Solid – Display the object as a solid (if solid drawing is enabled in the viewport).

  * `TEXTURED` Textured – Display the object with textures (if textures are enabled in the viewport).


Type:
    

enum in [`'BOUNDS'`, `'WIRE'`, `'SOLID'`, `'TEXTURED'`], default `'TEXTURED'`

empty_display_size
    

Size of display for empties in the viewport

Type:
    

float in [0.0001, 1000], default 1.0

empty_display_type
    

Viewport display style for empties

Type:
    

enum in [Object Empty Drawtype Items](../../bpy_types_enum_items/object_empty_drawtype_items.md#rna-enum-object-empty-drawtype-items), default `'PLAIN_AXES'`

empty_image_depth
    

Determine which other objects will occlude the image

Type:
    

enum in [`'DEFAULT'`, `'FRONT'`, `'BACK'`], default `'DEFAULT'`

empty_image_offset
    

Origin offset distance

Type:
    

float array of 2 items in [-inf, inf], default (-0.5, -0.5)

empty_image_side
    

Show front/back side

Type:
    

enum in [`'DOUBLE_SIDED'`, `'FRONT'`, `'BACK'`], default `'DOUBLE_SIDED'`

field
    

Settings for using the object as a field in physics simulation

Type:
    

[`FieldSettings`](../F/bpy.types.FieldSettings.md#bpy.types.FieldSettings "bpy.types.FieldSettings"), (readonly)

hide_probe_plane
    

Globally disable in planar light probes

Type:
    

boolean, default False

hide_probe_sphere
    

Globally disable in spherical light probes

Type:
    

boolean, default False

hide_probe_volume
    

Globally disable in volume probes

Type:
    

boolean, default False

hide_render
    

Globally disable in renders

Type:
    

boolean, default False

hide_select
    

Disable selection in viewport

Type:
    

boolean, default False

hide_surface_pick
    

Disable surface influence during selection, snapping and depth-picking operators. Usually used to avoid semi-transparent objects to affect scene navigation

Type:
    

boolean, default False

hide_viewport
    

Globally disable in viewports

Type:
    

boolean, default False

image_user
    

Parameters defining which layer, pass and frame of the image is displayed

Type:
    

[`ImageUser`](../I/bpy.types.ImageUser.md#bpy.types.ImageUser "bpy.types.ImageUser"), (readonly, never None)

instance_collection
    

Instance an existing collection

Type:
    

[`Collection`](../C/bpy.types.Collection.md#bpy.types.Collection "bpy.types.Collection")

instance_faces_scale
    

Scale the face instance objects

Type:
    

float in [0.001, 10000], default 1.0

instance_type
    

If not None, object instancing method to use

  * `NONE` None.

  * `VERTS` Vertices – Instantiate child objects on all vertices.

  * `FACES` Faces – Instantiate child objects on all faces.

  * `COLLECTION` Collection – Enable collection instancing.


Type:
    

enum in [`'NONE'`, `'VERTS'`, `'FACES'`, `'COLLECTION'`], default `'NONE'`

is_from_instancer
    

Object comes from a instancer

Type:
    

boolean, default False, (readonly)

is_from_set
    

Object comes from a background set

Type:
    

boolean, default False, (readonly)

is_holdout
    

Render objects as a holdout or matte, creating a hole in the image with zero alpha, to fill out in compositing with real footage or another render

Type:
    

boolean, default False

is_instancer
    

Type:
    

boolean, default False, (readonly)

is_shadow_catcher
    

Only render shadows and reflections on this object, for compositing renders into real footage. Objects with this setting are considered to already exist in the footage, objects without it are synthetic objects being composited into it.

Type:
    

boolean, default False

light_linking
    

Light linking settings

Type:
    

[`ObjectLightLinking`](bpy.types.ObjectLightLinking.md#bpy.types.ObjectLightLinking "bpy.types.ObjectLightLinking"), (readonly, never None)

lightgroup
    

Lightgroup that the object belongs to

Type:
    

string, default “”, (never None)

lineart
    

Line Art settings for the object

Type:
    

[`ObjectLineArt`](bpy.types.ObjectLineArt.md#bpy.types.ObjectLineArt "bpy.types.ObjectLineArt"), (readonly)

location
    

Location of the object

Type:
    

[`mathutils.Vector`](mathutils.md#mathutils.Vector "mathutils.Vector") of 3 items in [-inf, inf], default (0.0, 0.0, 0.0)

lock_location
    

Lock editing of location when transforming

Type:
    

boolean array of 3 items, default (False, False, False)

lock_rotation
    

Lock editing of rotation when transforming

Type:
    

boolean array of 3 items, default (False, False, False)

lock_rotation_w
    

Lock editing of ‘angle’ component of four-component rotations when transforming

Type:
    

boolean, default False

lock_rotations_4d
    

Lock editing of four component rotations by components (instead of as Eulers)

Type:
    

boolean, default True

lock_scale
    

Lock editing of scale when transforming

Type:
    

boolean array of 3 items, default (False, False, False)

material_slots
    

Material slots in the object

Type:
    

[`bpy_prop_collection`](../_other/bpy.types.bpy_prop_collection.md#bpy.types.bpy_prop_collection "bpy.types.bpy_prop_collection") of [`MaterialSlot`](../M/bpy.types.MaterialSlot.md#bpy.types.MaterialSlot "bpy.types.MaterialSlot"), (readonly)

matrix_basis
    

Matrix access to location, rotation and scale (including deltas), before constraints and parenting are applied

Type:
    

[`mathutils.Matrix`](mathutils.md#mathutils.Matrix "mathutils.Matrix") of 4 * 4 items in [-inf, inf], default ((0.0, 0.0, 0.0, 0.0), (0.0, 0.0, 0.0, 0.0), (0.0, 0.0, 0.0, 0.0), (0.0, 0.0, 0.0, 0.0))

matrix_local
    

Parent relative transformation matrix. Warning: Only takes into account object parenting, so e.g. in case of bone parenting you get a matrix relative to the Armature object, not to the actual parent bone

Type:
    

[`mathutils.Matrix`](mathutils.md#mathutils.Matrix "mathutils.Matrix") of 4 * 4 items in [-inf, inf], default ((0.0, 0.0, 0.0, 0.0), (0.0, 0.0, 0.0, 0.0), (0.0, 0.0, 0.0, 0.0), (0.0, 0.0, 0.0, 0.0))

matrix_parent_inverse
    

Inverse of object’s parent matrix at time of parenting

Type:
    

[`mathutils.Matrix`](mathutils.md#mathutils.Matrix "mathutils.Matrix") of 4 * 4 items in [-inf, inf], default ((1.0, 0.0, 0.0, 0.0), (0.0, 1.0, 0.0, 0.0), (0.0, 0.0, 1.0, 0.0), (0.0, 0.0, 0.0, 1.0))

matrix_world
    

Worldspace transformation matrix

Type:
    

[`mathutils.Matrix`](mathutils.md#mathutils.Matrix "mathutils.Matrix") of 4 * 4 items in [-inf, inf], default ((0.0, 0.0, 0.0, 0.0), (0.0, 0.0, 0.0, 0.0), (0.0, 0.0, 0.0, 0.0), (0.0, 0.0, 0.0, 0.0))

mode
    

Object interaction mode

Type:
    

enum in [Object Mode Items](../../bpy_types_enum_items/object_mode_items.md#rna-enum-object-mode-items), default `'OBJECT'`, (readonly)

modifiers
    

Modifiers affecting the geometric data of the object

Type:
    

[`ObjectModifiers`](bpy.types.ObjectModifiers.md#bpy.types.ObjectModifiers "bpy.types.ObjectModifiers") [`bpy_prop_collection`](../_other/bpy.types.bpy_prop_collection.md#bpy.types.bpy_prop_collection "bpy.types.bpy_prop_collection") of [`Modifier`](../M/bpy.types.Modifier.md#bpy.types.Modifier "bpy.types.Modifier"), (readonly)

motion_path
    

Motion Path for this element

Type:
    

[`MotionPath`](../M/bpy.types.MotionPath.md#bpy.types.MotionPath "bpy.types.MotionPath"), (readonly)

parent
    

Parent object

Type:
    

`Object`

parent_bone
    

Name of parent bone in case of a bone parenting relation

Type:
    

string, default “”, (never None)

parent_type
    

Type of parent relation

  * `OBJECT` Object – The object is parented to an object.

  * `ARMATURE` Armature.

  * `LATTICE` Lattice – The object is parented to a lattice.

  * `VERTEX` Vertex – The object is parented to a vertex.

  * `VERTEX_3` 3 Vertices.

  * `BONE` Bone – The object is parented to a bone.


Type:
    

enum in [`'OBJECT'`, `'ARMATURE'`, `'LATTICE'`, `'VERTEX'`, `'VERTEX_3'`, `'BONE'`], default `'OBJECT'`

parent_vertices
    

Indices of vertices in case of a vertex parenting relation

Type:
    

int array of 3 items in [0, inf], default (0, 0, 0)

particle_systems
    

Particle systems emitted from the object

Type:
    

[`ParticleSystems`](../P/bpy.types.ParticleSystems.md#bpy.types.ParticleSystems "bpy.types.ParticleSystems") [`bpy_prop_collection`](../_other/bpy.types.bpy_prop_collection.md#bpy.types.bpy_prop_collection "bpy.types.bpy_prop_collection") of [`ParticleSystem`](../P/bpy.types.ParticleSystem.md#bpy.types.ParticleSystem "bpy.types.ParticleSystem"), (readonly)

pass_index
    

Index number for the “Object Index” render pass

Type:
    

int in [0, 32767], default 0

pose
    

Current pose for armatures

Type:
    

[`Pose`](../P/bpy.types.Pose.md#bpy.types.Pose "bpy.types.Pose"), (readonly)

rigid_body
    

Settings for rigid body simulation

Type:
    

[`RigidBodyObject`](../R/bpy.types.RigidBodyObject.md#bpy.types.RigidBodyObject "bpy.types.RigidBodyObject"), (readonly)

rigid_body_constraint
    

Constraint constraining rigid bodies

Type:
    

[`RigidBodyConstraint`](../R/bpy.types.RigidBodyConstraint.md#bpy.types.RigidBodyConstraint "bpy.types.RigidBodyConstraint"), (readonly)

rotation_axis_angle
    

Angle of Rotation for Axis-Angle rotation representation

Type:
    

float array of 4 items in [-inf, inf], default (0.0, 0.0, 1.0, 0.0)

rotation_euler
    

Rotation in Eulers

Type:
    

[`mathutils.Euler`](mathutils.md#mathutils.Euler "mathutils.Euler") rotation of 3 items in [-inf, inf], default (0.0, 0.0, 0.0)

rotation_mode
    

The kind of rotation to apply, values from other rotation modes are not used

Type:
    

enum in [Object Rotation Mode Items](../../bpy_types_enum_items/object_rotation_mode_items.md#rna-enum-object-rotation-mode-items), default `'XYZ'`

rotation_quaternion
    

Rotation in Quaternions

Type:
    

[`mathutils.Quaternion`](mathutils.md#mathutils.Quaternion "mathutils.Quaternion") rotation of 4 items in [-inf, inf], default (1.0, 0.0, 0.0, 0.0)

scale
    

Scaling of the object

Type:
    

[`mathutils.Vector`](mathutils.md#mathutils.Vector "mathutils.Vector") of 3 items in [-inf, inf], default (1.0, 1.0, 1.0)

selection_sets
    

List of groups of bones for easy selection

Type:
    

[`bpy_prop_collection`](../_other/bpy.types.bpy_prop_collection.md#bpy.types.bpy_prop_collection "bpy.types.bpy_prop_collection") of `SelectionSet`, (readonly)

shader_effects
    

Effects affecting display of object

Type:
    

[`ObjectShaderFx`](bpy.types.ObjectShaderFx.md#bpy.types.ObjectShaderFx "bpy.types.ObjectShaderFx") [`bpy_prop_collection`](../_other/bpy.types.bpy_prop_collection.md#bpy.types.bpy_prop_collection "bpy.types.bpy_prop_collection") of [`ShaderFx`](../S/bpy.types.ShaderFx.md#bpy.types.ShaderFx "bpy.types.ShaderFx"), (readonly)

shadow_terminator_geometry_offset
    

Offset rays from the surface to reduce shadow terminator artifact on low poly geometry. Only affects triangles at grazing angles to light

Type:
    

float in [0, inf], default 0.1

shadow_terminator_normal_offset
    

Offset rays from the surface to reduce shadow terminator artifact on low poly geometry. Only affect triangles that are affected by the geometry offset

Type:
    

float in [0, inf], default 0.0

shadow_terminator_shading_offset
    

Push the shadow terminator towards the light to hide artifacts on low poly geometry

Type:
    

float in [0, inf], default 0.0

show_all_edges
    

Display all edges for mesh objects

Type:
    

boolean, default False

show_axis
    

Display the object’s origin and axes

Type:
    

boolean, default False

show_bounds
    

Display the object’s bounds

Type:
    

boolean, default False

show_empty_image_only_axis_aligned
    

Only display the image when it is aligned with the view axis

Type:
    

boolean, default False

show_empty_image_orthographic
    

Display image in orthographic mode

Type:
    

boolean, default True

show_empty_image_perspective
    

Display image in perspective mode

Type:
    

boolean, default True

show_in_front
    

Make the object display in front of others

Type:
    

boolean, default False

show_instancer_for_render
    

Make instancer visible when rendering

Type:
    

boolean, default True

show_instancer_for_viewport
    

Make instancer visible in the viewport

Type:
    

boolean, default True

show_name
    

Display the object’s name

Type:
    

boolean, default False

show_only_shape_key
    

Only show the active shape key at full value

Type:
    

boolean, default False

show_texture_space
    

Display the object’s texture space

Type:
    

boolean, default False

show_transparent
    

Display material transparency in the object

Type:
    

boolean, default False

show_wire
    

Display the object’s wireframe over solid shading

Type:
    

boolean, default False

soft_body
    

Settings for soft body simulation

Type:
    

[`SoftBodySettings`](../S/bpy.types.SoftBodySettings.md#bpy.types.SoftBodySettings "bpy.types.SoftBodySettings"), (readonly)

track_axis
    

Axis that points in the ‘forward’ direction (applies to Instance Vertices when Align to Vertex Normal is enabled)

Type:
    

enum in [Object Axis Items](../../bpy_types_enum_items/object_axis_items.md#rna-enum-object-axis-items), default `'POS_X'`

type
    

Type of object

Type:
    

enum in [Object Type Items](../../bpy_types_enum_items/object_type_items.md#rna-enum-object-type-items), default `'EMPTY'`, (readonly)

up_axis
    

Axis that points in the upward direction (applies to Instance Vertices when Align to Vertex Normal is enabled)

Type:
    

enum in [`'X'`, `'Y'`, `'Z'`], default `'X'`

use_camera_lock_parent
    

View Lock 3D viewport camera transformation affects the object’s parent instead

Type:
    

boolean, default False

use_dynamic_topology_sculpting
    

Type:
    

boolean, default False, (readonly)

use_empty_image_alpha
    

Use alpha blending instead of alpha test (can produce sorting artifacts)

Type:
    

boolean, default False

use_grease_pencil_lights
    

Lights affect Grease Pencil object

Type:
    

boolean, default True

use_instance_faces_scale
    

Scale instance based on face size

Type:
    

boolean, default False

use_instance_vertices_rotation
    

Rotate instance according to vertex normal

Type:
    

boolean, default False

use_mesh_mirror_x
    

Enable mesh symmetry in the X axis

Type:
    

boolean, default False

use_mesh_mirror_y
    

Enable mesh symmetry in the Y axis

Type:
    

boolean, default False

use_mesh_mirror_z
    

Enable mesh symmetry in the Z axis

Type:
    

boolean, default False

use_parent_final_indices
    

Use the final evaluated indices rather than the original mesh indices

Type:
    

boolean, default False

use_shape_key_edit_mode
    

Display shape keys in edit mode (for meshes only)

Type:
    

boolean, default False

use_simulation_cache
    

Cache frames during simulation nodes playback

Type:
    

boolean, default True

vertex_groups
    

Vertex groups of the object

Type:
    

[`VertexGroups`](../V/bpy.types.VertexGroups.md#bpy.types.VertexGroups "bpy.types.VertexGroups") [`bpy_prop_collection`](../_other/bpy.types.bpy_prop_collection.md#bpy.types.bpy_prop_collection "bpy.types.bpy_prop_collection") of [`VertexGroup`](../V/bpy.types.VertexGroup.md#bpy.types.VertexGroup "bpy.types.VertexGroup"), (readonly)

visible_camera
    

Object visibility to camera rays

Type:
    

boolean, default True

visible_diffuse
    

Object visibility to diffuse rays

Type:
    

boolean, default True

visible_glossy
    

Object visibility to glossy rays

Type:
    

boolean, default True

visible_shadow
    

Object visibility to shadow rays

Type:
    

boolean, default True

visible_transmission
    

Object visibility to transmission rays

Type:
    

boolean, default True

visible_volume_scatter
    

Object visibility to volume scattering rays

Type:
    

boolean, default True

children
    

All the children of this object.

Type:
    

tuple of `Object`

Note

Takes `O(len(bpy.data.objects))` time.

(readonly)

children_recursive
    

A list of all children from this object.

Type:
    

list of `Object`

Note

Takes `O(len(bpy.data.objects))` time.

(readonly)

users_collection
    

The collections this object is in.

Type:
    

tuple of [`Collection`](../C/bpy.types.Collection.md#bpy.types.Collection "bpy.types.Collection")

Note

Takes `O(len(bpy.data.collections) + len(bpy.data.scenes))` time.

(readonly)

users_scene
    

The scenes this object is in.

Type:
    

tuple of [`Scene`](../S/bpy.types.Scene.md#bpy.types.Scene "bpy.types.Scene")

Note

Takes `O(len(bpy.data.scenes) * len(bpy.data.objects))` time.

(readonly)

select_get(_*_ , _view_layer =None_)
    

Test if the object is selected. The selection state is per view layer.

Parameters:
    

**view_layer** ([`ViewLayer`](../V/bpy.types.ViewLayer.md#bpy.types.ViewLayer "bpy.types.ViewLayer"), (optional)) – Use this instead of the active view layer

Returns:
    

Object selected

Return type:
    

boolean

select_set(_state_ , _*_ , _view_layer =None_)
    

Select or deselect the object. The selection state is per view layer.

Parameters:
    

  * **state** (_boolean_) – Selection state to define

  * **view_layer** ([`ViewLayer`](../V/bpy.types.ViewLayer.md#bpy.types.ViewLayer "bpy.types.ViewLayer"), (optional)) – Use this instead of the active view layer


hide_get(_*_ , _view_layer =None_)
    

Test if the object is hidden for viewport editing. This hiding state is per view layer.

Parameters:
    

**view_layer** ([`ViewLayer`](../V/bpy.types.ViewLayer.md#bpy.types.ViewLayer "bpy.types.ViewLayer"), (optional)) – Use this instead of the active view layer

Returns:
    

Object hidden

Return type:
    

boolean

hide_set(_state_ , _*_ , _view_layer =None_)
    

Hide the object for viewport editing. This hiding state is per view layer.

Parameters:
    

  * **state** (_boolean_) – Hide state to define

  * **view_layer** ([`ViewLayer`](../V/bpy.types.ViewLayer.md#bpy.types.ViewLayer "bpy.types.ViewLayer"), (optional)) – Use this instead of the active view layer


visible_get(_*_ , _view_layer =None_, _viewport =None_)
    

Test if the object is visible in the 3D viewport, taking into account all visibility settings

Parameters:
    

  * **view_layer** ([`ViewLayer`](../V/bpy.types.ViewLayer.md#bpy.types.ViewLayer "bpy.types.ViewLayer"), (optional)) – Use this instead of the active view layer

  * **viewport** ([`SpaceView3D`](../S/bpy.types.SpaceView3D.md#bpy.types.SpaceView3D "bpy.types.SpaceView3D"), (optional)) – Use this instead of the active 3D viewport


Returns:
    

Object visible

Return type:
    

boolean

holdout_get(_*_ , _view_layer =None_)
    

Test if object is masked in the view layer

Parameters:
    

**view_layer** ([`ViewLayer`](../V/bpy.types.ViewLayer.md#bpy.types.ViewLayer "bpy.types.ViewLayer"), (optional)) – Use this instead of the active view layer

Returns:
    

Object holdout

Return type:
    

boolean

indirect_only_get(_*_ , _view_layer =None_)
    

Test if object is set to contribute only indirectly (through shadows and reflections) in the view layer

Parameters:
    

**view_layer** ([`ViewLayer`](../V/bpy.types.ViewLayer.md#bpy.types.ViewLayer "bpy.types.ViewLayer"), (optional)) – Use this instead of the active view layer

Returns:
    

Object indirect only

Return type:
    

boolean

local_view_get(_viewport_)
    

Get the local view state for this object

Parameters:
    

**viewport** ([`SpaceView3D`](../S/bpy.types.SpaceView3D.md#bpy.types.SpaceView3D "bpy.types.SpaceView3D"), (never None)) – Viewport in local view

Returns:
    

Object local view state

Return type:
    

boolean

local_view_set(_viewport_ , _state_)
    

Set the local view state for this object

Parameters:
    

  * **viewport** ([`SpaceView3D`](../S/bpy.types.SpaceView3D.md#bpy.types.SpaceView3D "bpy.types.SpaceView3D"), (never None)) – Viewport in local view

  * **state** (_boolean_) – Local view state to define


visible_in_viewport_get(_viewport_)
    

Check for local view and local collections for this viewport and object

Parameters:
    

**viewport** ([`SpaceView3D`](../S/bpy.types.SpaceView3D.md#bpy.types.SpaceView3D "bpy.types.SpaceView3D"), (never None)) – Viewport in local collections

Returns:
    

Object viewport visibility

Return type:
    

boolean

convert_space(_*_ , _pose_bone =None_, _matrix =((0.0, 0.0, 0.0, 0.0), (0.0, 0.0, 0.0, 0.0), (0.0, 0.0, 0.0, 0.0), (0.0, 0.0, 0.0, 0.0))_, _from_space ='WORLD'_, _to_space ='WORLD'_)
    

Convert (transform) the given matrix from one space to another

Parameters:
    

  * **pose_bone** ([`PoseBone`](../P/bpy.types.PoseBone.md#bpy.types.PoseBone "bpy.types.PoseBone"), (optional)) – Bone to use to define spaces (may be None, in which case only the two ‘WORLD’ and ‘LOCAL’ spaces are usable)

  * **matrix** ([`mathutils.Matrix`](mathutils.md#mathutils.Matrix "mathutils.Matrix") of 4 * 4 items in [-inf, inf], (optional)) – The matrix to transform

  * **from_space** (enum in [`'WORLD'`, `'POSE'`, `'LOCAL_WITH_PARENT'`, `'LOCAL'`], (optional)) – 

The space in which ‘matrix’ is currently

    * `WORLD` World Space – The most global space in Blender.

    * `POSE` Pose Space – The pose space of a bone (its armature’s object space).

    * `LOCAL_WITH_PARENT` Local With Parent – The rest pose local space of a bone (this matrix includes parent transforms).

    * `LOCAL` Local Space – The local space of an object/bone.

  * **to_space** (enum in [`'WORLD'`, `'POSE'`, `'LOCAL_WITH_PARENT'`, `'LOCAL'`], (optional)) – 

The space to which you want to transform ‘matrix’

    * `WORLD` World Space – The most global space in Blender.

    * `POSE` Pose Space – The pose space of a bone (its armature’s object space).

    * `LOCAL_WITH_PARENT` Local With Parent – The rest pose local space of a bone (this matrix includes parent transforms).

    * `LOCAL` Local Space – The local space of an object/bone.


Returns:
    

The transformed matrix

Return type:
    

[`mathutils.Matrix`](mathutils.md#mathutils.Matrix "mathutils.Matrix") of 4 * 4 items in [-inf, inf]

calc_matrix_camera(_depsgraph_ , _*_ , _x =1_, _y =1_, _scale_x =1.0_, _scale_y =1.0_)
    

Generate the camera projection matrix of this object (mostly useful for Camera and Light types)

Parameters:
    

  * **depsgraph** ([`Depsgraph`](../D/bpy.types.Depsgraph.md#bpy.types.Depsgraph "bpy.types.Depsgraph")) – Depsgraph to get evaluated data from

  * **x** (_int in_ _[__0_ _,__inf_ _]__,__(__optional_ _)_) – Width of the render area

  * **y** (_int in_ _[__0_ _,__inf_ _]__,__(__optional_ _)_) – Height of the render area

  * **scale_x** (_float in_ _[__1e-06_ _,__inf_ _]__,__(__optional_ _)_) – Width scaling factor

  * **scale_y** (_float in_ _[__1e-06_ _,__inf_ _]__,__(__optional_ _)_) – Height scaling factor


Returns:
    

The camera projection matrix

Return type:
    

[`mathutils.Matrix`](mathutils.md#mathutils.Matrix "mathutils.Matrix") of 4 * 4 items in [-inf, inf]

camera_fit_coords(_depsgraph_ , _coordinates_)
    

Compute the coordinate (and scale for ortho cameras) given object should be to ‘see’ all given coordinates

Parameters:
    

  * **depsgraph** ([`Depsgraph`](../D/bpy.types.Depsgraph.md#bpy.types.Depsgraph "bpy.types.Depsgraph")) – Depsgraph to get evaluated data from

  * **coordinates** (_float array_ _of_ _1 items in_ _[__-inf_ _,__inf_ _]__,__(__never None_ _)_) – Coordinates to fit in


Returns:
    

`co_return`, The location to aim to be able to see all given points, [`mathutils.Vector`](mathutils.md#mathutils.Vector "mathutils.Vector") of 3 items in [-inf, inf]

`scale_return`, The ortho scale to aim to be able to see all given points (if relevant), float in [-inf, inf]

Return type:
    

([`mathutils.Vector`](mathutils.md#mathutils.Vector "mathutils.Vector") of 3 items in [-inf, inf], float in [-inf, inf])

crazyspace_eval(_depsgraph_ , _scene_)
    

Compute orientation mapping between vertices of an original object and object with shape keys and deforming modifiers applied.The evaluation is to be freed with the crazyspace_eval_free function

Parameters:
    

  * **depsgraph** ([`Depsgraph`](../D/bpy.types.Depsgraph.md#bpy.types.Depsgraph "bpy.types.Depsgraph")) – Dependency Graph, Evaluated dependency graph

  * **scene** ([`Scene`](../S/bpy.types.Scene.md#bpy.types.Scene "bpy.types.Scene")) – Scene, Scene of the object


crazyspace_displacement_to_deformed(_*_ , _vertex_index =0_, _displacement =(0.0, 0.0, 0.0)_)
    

Convert displacement vector from non-deformed object space to deformed object space

Parameters:
    

  * **vertex_index** (_int in_ _[__-inf_ _,__inf_ _]__,__(__optional_ _)_) – vertex_index

  * **displacement** ([`mathutils.Vector`](mathutils.md#mathutils.Vector "mathutils.Vector") of 3 items in [-inf, inf], (optional)) – displacement


Returns:
    

displacement_deformed

Return type:
    

[`mathutils.Vector`](mathutils.md#mathutils.Vector "mathutils.Vector") of 3 items in [-inf, inf]

crazyspace_displacement_to_original(_*_ , _vertex_index =0_, _displacement =(0.0, 0.0, 0.0)_)
    

Free evaluated state of crazyspace

Parameters:
    

  * **vertex_index** (_int in_ _[__-inf_ _,__inf_ _]__,__(__optional_ _)_) – vertex_index

  * **displacement** ([`mathutils.Vector`](mathutils.md#mathutils.Vector "mathutils.Vector") of 3 items in [-inf, inf], (optional)) – displacement


Returns:
    

displacement_original

Return type:
    

[`mathutils.Vector`](mathutils.md#mathutils.Vector "mathutils.Vector") of 3 items in [-inf, inf]

crazyspace_eval_clear()
    

crazyspace_eval_clear

to_mesh(_*_ , _preserve_all_data_layers =False_, _depsgraph =None_)
    

Create a Mesh data-block from the current state of the object. The object owns the data-block. To force free it use to_mesh_clear(). The result is temporary and cannot be used by objects from the main database.

Parameters:
    

  * **preserve_all_data_layers** (_boolean_ _,__(__optional_ _)_) – Preserve all data layers in the mesh, like UV maps and vertex groups. By default Blender only computes the subset of data layers needed for viewport display and rendering, for better performance.

  * **depsgraph** ([`Depsgraph`](../D/bpy.types.Depsgraph.md#bpy.types.Depsgraph "bpy.types.Depsgraph"), (optional)) – Dependency Graph, Evaluated dependency graph which is required when preserve_all_data_layers is true


Returns:
    

Mesh created from object

Return type:
    

[`Mesh`](../M/bpy.types.Mesh.md#bpy.types.Mesh "bpy.types.Mesh")

to_mesh_clear()
    

Clears mesh data-block created by to_mesh()

to_curve(_depsgraph_ , _*_ , _apply_modifiers =False_)
    

Create a Curve data-block from the current state of the object. This only works for curve and text objects. The object owns the data-block. To force free it, use to_curve_clear(). The result is temporary and cannot be used by objects from the main database.

Parameters:
    

  * **depsgraph** ([`Depsgraph`](../D/bpy.types.Depsgraph.md#bpy.types.Depsgraph "bpy.types.Depsgraph")) – Dependency Graph, Evaluated dependency graph

  * **apply_modifiers** (_boolean_ _,__(__optional_ _)_) – Apply the deform modifiers on the control points of the curve. This is only supported for curve objects.


Returns:
    

Curve created from object

Return type:
    

[`Curve`](../C/bpy.types.Curve.md#bpy.types.Curve "bpy.types.Curve")

to_curve_clear()
    

Clears curve data-block created by to_curve()

find_armature()
    

Find armature influencing this object as a parent or via a modifier

Returns:
    

Armature object influencing this object or nullptr

Return type:
    

`Object`

shape_key_add(_*_ , _name ='Key'_, _from_mix =True_)
    

Add shape key to this object

Parameters:
    

  * **name** (_string_ _,__(__optional_ _,__never None_ _)_) – Unique name for the new key-block

  * **from_mix** (_boolean_ _,__(__optional_ _)_) – Create new shape from existing mix of shapes


Returns:
    

New shape key-block

Return type:
    

[`ShapeKey`](../S/bpy.types.ShapeKey.md#bpy.types.ShapeKey "bpy.types.ShapeKey")

shape_key_remove(_key_)
    

Remove a Shape Key from this object

Parameters:
    

**key** ([`ShapeKey`](../S/bpy.types.ShapeKey.md#bpy.types.ShapeKey "bpy.types.ShapeKey"), (never None)) – Key-block to be removed

shape_key_clear()
    

Remove all Shape Keys from this object

ray_cast(_origin_ , _direction_ , _*_ , _distance =1.70141e+38_, _depsgraph =None_)
    

Cast a ray onto evaluated geometry, in object space (using context’s or provided depsgraph to get evaluated mesh if needed)

Parameters:
    

  * **origin** ([`mathutils.Vector`](mathutils.md#mathutils.Vector "mathutils.Vector") of 3 items in [-inf, inf]) – Origin of the ray, in object space

  * **direction** ([`mathutils.Vector`](mathutils.md#mathutils.Vector "mathutils.Vector") of 3 items in [-inf, inf]) – Direction of the ray, in object space

  * **distance** (_float in_ _[__0_ _,__inf_ _]__,__(__optional_ _)_) – Maximum distance

  * **depsgraph** ([`Depsgraph`](../D/bpy.types.Depsgraph.md#bpy.types.Depsgraph "bpy.types.Depsgraph"), (optional)) – Depsgraph to use to get evaluated data, when called from original object (only needed if current Context’s depsgraph is not suitable)


Returns:
    

`result`, Whether the ray successfully hit the geometry, boolean

`location`, The hit location of this ray cast, [`mathutils.Vector`](mathutils.md#mathutils.Vector "mathutils.Vector") of 3 items in [-inf, inf]

`normal`, The face normal at the ray cast hit location, [`mathutils.Vector`](mathutils.md#mathutils.Vector "mathutils.Vector") of 3 items in [-inf, inf]

`index`, The face index, -1 when original data isn’t available, int in [-inf, inf]

Return type:
    

(boolean, [`mathutils.Vector`](mathutils.md#mathutils.Vector "mathutils.Vector") of 3 items in [-inf, inf], [`mathutils.Vector`](mathutils.md#mathutils.Vector "mathutils.Vector") of 3 items in [-inf, inf], int in [-inf, inf])

closest_point_on_mesh(_origin_ , _*_ , _distance =1.84467e+19_, _depsgraph =None_)
    

Find the nearest point on evaluated geometry, in object space (using context’s or provided depsgraph to get evaluated mesh if needed)

Parameters:
    

  * **origin** ([`mathutils.Vector`](mathutils.md#mathutils.Vector "mathutils.Vector") of 3 items in [-inf, inf]) – Point to find closest geometry from (in object space)

  * **distance** (_float in_ _[__0_ _,__inf_ _]__,__(__optional_ _)_) – Maximum distance

  * **depsgraph** ([`Depsgraph`](../D/bpy.types.Depsgraph.md#bpy.types.Depsgraph "bpy.types.Depsgraph"), (optional)) – Depsgraph to use to get evaluated data, when called from original object (only needed if current Context’s depsgraph is not suitable)


Returns:
    

`result`, Whether closest point on geometry was found, boolean

`location`, The location on the object closest to the point, [`mathutils.Vector`](mathutils.md#mathutils.Vector "mathutils.Vector") of 3 items in [-inf, inf]

`normal`, The face normal at the closest point, [`mathutils.Vector`](mathutils.md#mathutils.Vector "mathutils.Vector") of 3 items in [-inf, inf]

`index`, The face index, -1 when original data isn’t available, int in [-inf, inf]

Return type:
    

(boolean, [`mathutils.Vector`](mathutils.md#mathutils.Vector "mathutils.Vector") of 3 items in [-inf, inf], [`mathutils.Vector`](mathutils.md#mathutils.Vector "mathutils.Vector") of 3 items in [-inf, inf], int in [-inf, inf])

is_modified(_scene_ , _settings_)
    

Determine if this object is modified from the base mesh data

Parameters:
    

  * **scene** ([`Scene`](../S/bpy.types.Scene.md#bpy.types.Scene "bpy.types.Scene"), (never None)) – Scene in which to check the object

  * **settings** (enum in [`'PREVIEW'`, `'RENDER'`]) – 

Modifier settings to apply

    * `PREVIEW` Preview – Apply modifier preview settings.

    * `RENDER` Render – Apply modifier render settings.


Returns:
    

Whether the object is modified

Return type:
    

boolean

is_deform_modified(_scene_ , _settings_)
    

Determine if this object is modified by a deformation from the base mesh data

Parameters:
    

  * **scene** ([`Scene`](../S/bpy.types.Scene.md#bpy.types.Scene "bpy.types.Scene"), (never None)) – Scene in which to check the object

  * **settings** (enum in [`'PREVIEW'`, `'RENDER'`]) – 

Modifier settings to apply

    * `PREVIEW` Preview – Apply modifier preview settings.

    * `RENDER` Render – Apply modifier render settings.


Returns:
    

Whether the object is deform-modified

Return type:
    

boolean

update_from_editmode()
    

Load the objects edit-mode data into the object data

Returns:
    

Success

Return type:
    

boolean

cache_release()
    

Release memory used by caches associated with this object. Intended to be used by render engines only.

evaluated_geometry()
    

Get the evaluated geometry set of this evaluated object. This only works for objects that contain geometry data like meshes and curves but not e.g. cameras.

Returns:
    

The evaluated geometry.

Return type:
    

[`bpy.types.GeometrySet`](../G/bpy.types.GeometrySet.md#bpy.types.GeometrySet "bpy.types.GeometrySet")

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

### Inherited Properties

  * [`bpy_struct.id_data`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.id_data "bpy.types.bpy_struct.id_data")
  * [`ID.name`](../I/bpy.types.ID.md#bpy.types.ID.name "bpy.types.ID.name")
  * [`ID.name_full`](../I/bpy.types.ID.md#bpy.types.ID.name_full "bpy.types.ID.name_full")
  * [`ID.id_type`](../I/bpy.types.ID.md#bpy.types.ID.id_type "bpy.types.ID.id_type")
  * [`ID.session_uid`](../I/bpy.types.ID.md#bpy.types.ID.session_uid "bpy.types.ID.session_uid")
  * [`ID.is_evaluated`](../I/bpy.types.ID.md#bpy.types.ID.is_evaluated "bpy.types.ID.is_evaluated")
  * [`ID.original`](../I/bpy.types.ID.md#bpy.types.ID.original "bpy.types.ID.original")
  * [`ID.users`](../I/bpy.types.ID.md#bpy.types.ID.users "bpy.types.ID.users")
  * [`ID.use_fake_user`](../I/bpy.types.ID.md#bpy.types.ID.use_fake_user "bpy.types.ID.use_fake_user")
  * [`ID.use_extra_user`](../I/bpy.types.ID.md#bpy.types.ID.use_extra_user "bpy.types.ID.use_extra_user")
  * [`ID.is_embedded_data`](../I/bpy.types.ID.md#bpy.types.ID.is_embedded_data "bpy.types.ID.is_embedded_data")

| 

  * [`ID.is_linked_packed`](../I/bpy.types.ID.md#bpy.types.ID.is_linked_packed "bpy.types.ID.is_linked_packed")
  * [`ID.is_missing`](../I/bpy.types.ID.md#bpy.types.ID.is_missing "bpy.types.ID.is_missing")
  * [`ID.is_runtime_data`](../I/bpy.types.ID.md#bpy.types.ID.is_runtime_data "bpy.types.ID.is_runtime_data")
  * [`ID.is_editable`](../I/bpy.types.ID.md#bpy.types.ID.is_editable "bpy.types.ID.is_editable")
  * [`ID.tag`](../I/bpy.types.ID.md#bpy.types.ID.tag "bpy.types.ID.tag")
  * [`ID.is_library_indirect`](../I/bpy.types.ID.md#bpy.types.ID.is_library_indirect "bpy.types.ID.is_library_indirect")
  * [`ID.library`](../I/bpy.types.ID.md#bpy.types.ID.library "bpy.types.ID.library")
  * [`ID.library_weak_reference`](../I/bpy.types.ID.md#bpy.types.ID.library_weak_reference "bpy.types.ID.library_weak_reference")
  * [`ID.asset_data`](../I/bpy.types.ID.md#bpy.types.ID.asset_data "bpy.types.ID.asset_data")
  * [`ID.override_library`](../I/bpy.types.ID.md#bpy.types.ID.override_library "bpy.types.ID.override_library")
  * [`ID.preview`](../I/bpy.types.ID.md#bpy.types.ID.preview "bpy.types.ID.preview")

  
---|---  
  
### Inherited Functions

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
  * [`bpy_struct.keys`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.keys "bpy.types.bpy_struct.keys")
  * [`bpy_struct.path_from_id`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.path_from_id "bpy.types.bpy_struct.path_from_id")
  * [`bpy_struct.path_from_module`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.path_from_module "bpy.types.bpy_struct.path_from_module")
  * [`bpy_struct.path_resolve`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.path_resolve "bpy.types.bpy_struct.path_resolve")
  * [`bpy_struct.pop`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.pop "bpy.types.bpy_struct.pop")
  * [`bpy_struct.property_overridable_library_set`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.property_overridable_library_set "bpy.types.bpy_struct.property_overridable_library_set")
  * [`bpy_struct.property_unset`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.property_unset "bpy.types.bpy_struct.property_unset")
  * [`bpy_struct.rna_ancestors`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.rna_ancestors "bpy.types.bpy_struct.rna_ancestors")

| 

  * [`bpy_struct.type_recast`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.type_recast "bpy.types.bpy_struct.type_recast")
  * [`bpy_struct.values`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.values "bpy.types.bpy_struct.values")
  * [`ID.bl_system_properties_get`](../I/bpy.types.ID.md#bpy.types.ID.bl_system_properties_get "bpy.types.ID.bl_system_properties_get")
  * [`ID.rename`](../I/bpy.types.ID.md#bpy.types.ID.rename "bpy.types.ID.rename")
  * [`ID.evaluated_get`](../I/bpy.types.ID.md#bpy.types.ID.evaluated_get "bpy.types.ID.evaluated_get")
  * [`ID.copy`](../I/bpy.types.ID.md#bpy.types.ID.copy "bpy.types.ID.copy")
  * [`ID.asset_mark`](../I/bpy.types.ID.md#bpy.types.ID.asset_mark "bpy.types.ID.asset_mark")
  * [`ID.asset_clear`](../I/bpy.types.ID.md#bpy.types.ID.asset_clear "bpy.types.ID.asset_clear")
  * [`ID.asset_generate_preview`](../I/bpy.types.ID.md#bpy.types.ID.asset_generate_preview "bpy.types.ID.asset_generate_preview")
  * [`ID.override_create`](../I/bpy.types.ID.md#bpy.types.ID.override_create "bpy.types.ID.override_create")
  * [`ID.override_hierarchy_create`](../I/bpy.types.ID.md#bpy.types.ID.override_hierarchy_create "bpy.types.ID.override_hierarchy_create")
  * [`ID.user_clear`](../I/bpy.types.ID.md#bpy.types.ID.user_clear "bpy.types.ID.user_clear")
  * [`ID.user_remap`](../I/bpy.types.ID.md#bpy.types.ID.user_remap "bpy.types.ID.user_remap")
  * [`ID.make_local`](../I/bpy.types.ID.md#bpy.types.ID.make_local "bpy.types.ID.make_local")
  * [`ID.user_of_id`](../I/bpy.types.ID.md#bpy.types.ID.user_of_id "bpy.types.ID.user_of_id")
  * [`ID.animation_data_create`](../I/bpy.types.ID.md#bpy.types.ID.animation_data_create "bpy.types.ID.animation_data_create")
  * [`ID.animation_data_clear`](../I/bpy.types.ID.md#bpy.types.ID.animation_data_clear "bpy.types.ID.animation_data_clear")
  * [`ID.update_tag`](../I/bpy.types.ID.md#bpy.types.ID.update_tag "bpy.types.ID.update_tag")
  * [`ID.preview_ensure`](../I/bpy.types.ID.md#bpy.types.ID.preview_ensure "bpy.types.ID.preview_ensure")
  * [`ID.bl_rna_get_subclass`](../I/bpy.types.ID.md#bpy.types.ID.bl_rna_get_subclass "bpy.types.ID.bl_rna_get_subclass")
  * [`ID.bl_rna_get_subclass_py`](../I/bpy.types.ID.md#bpy.types.ID.bl_rna_get_subclass_py "bpy.types.ID.bl_rna_get_subclass_py")

  
---|---  
  
### References

  * [`bpy.context.active_object`](../../bpy.context.md#bpy.context.active_object "bpy.context.active_object")
  * [`bpy.context.edit_object`](../../bpy.context.md#bpy.context.edit_object "bpy.context.edit_object")
  * [`bpy.context.editable_objects`](../../bpy.context.md#bpy.context.editable_objects "bpy.context.editable_objects")
  * [`bpy.context.image_paint_object`](../../bpy.context.md#bpy.context.image_paint_object "bpy.context.image_paint_object")
  * [`bpy.context.object`](../../bpy.context.md#bpy.context.object "bpy.context.object")
  * [`bpy.context.objects_in_mode`](../../bpy.context.md#bpy.context.objects_in_mode "bpy.context.objects_in_mode")
  * [`bpy.context.objects_in_mode_unique_data`](../../bpy.context.md#bpy.context.objects_in_mode_unique_data "bpy.context.objects_in_mode_unique_data")
  * [`bpy.context.particle_edit_object`](../../bpy.context.md#bpy.context.particle_edit_object "bpy.context.particle_edit_object")
  * [`bpy.context.pose_object`](../../bpy.context.md#bpy.context.pose_object "bpy.context.pose_object")
  * [`bpy.context.sculpt_object`](../../bpy.context.md#bpy.context.sculpt_object "bpy.context.sculpt_object")
  * [`bpy.context.selectable_objects`](../../bpy.context.md#bpy.context.selectable_objects "bpy.context.selectable_objects")
  * [`bpy.context.selected_editable_objects`](../../bpy.context.md#bpy.context.selected_editable_objects "bpy.context.selected_editable_objects")
  * [`bpy.context.selected_objects`](../../bpy.context.md#bpy.context.selected_objects "bpy.context.selected_objects")
  * [`bpy.context.vertex_paint_object`](../../bpy.context.md#bpy.context.vertex_paint_object "bpy.context.vertex_paint_object")
  * [`bpy.context.visible_objects`](../../bpy.context.md#bpy.context.visible_objects "bpy.context.visible_objects")
  * [`bpy.context.weight_paint_object`](../../bpy.context.md#bpy.context.weight_paint_object "bpy.context.weight_paint_object")
  * [`Action.flip_with_pose`](../A/bpy.types.Action.md#bpy.types.Action.flip_with_pose "bpy.types.Action.flip_with_pose")
  * [`ActionConstraint.target`](../A/bpy.types.ActionConstraint.md#bpy.types.ActionConstraint.target "bpy.types.ActionConstraint.target")
  * [`ArmatureModifier.object`](../A/bpy.types.ArmatureModifier.md#bpy.types.ArmatureModifier.object "bpy.types.ArmatureModifier.object")
  * [`ArrayModifier.curve`](../A/bpy.types.ArrayModifier.md#bpy.types.ArrayModifier.curve "bpy.types.ArrayModifier.curve")
  * [`ArrayModifier.end_cap`](../A/bpy.types.ArrayModifier.md#bpy.types.ArrayModifier.end_cap "bpy.types.ArrayModifier.end_cap")
  * [`ArrayModifier.offset_object`](../A/bpy.types.ArrayModifier.md#bpy.types.ArrayModifier.offset_object "bpy.types.ArrayModifier.offset_object")
  * [`ArrayModifier.start_cap`](../A/bpy.types.ArrayModifier.md#bpy.types.ArrayModifier.start_cap "bpy.types.ArrayModifier.start_cap")
  * [`BlendData.objects`](../B/bpy.types.BlendData.md#bpy.types.BlendData.objects "bpy.types.BlendData.objects")
  * [`BlendDataMeshes.new_from_object`](../B/bpy.types.BlendDataMeshes.md#bpy.types.BlendDataMeshes.new_from_object "bpy.types.BlendDataMeshes.new_from_object")
  * [`BlendDataObjects.new`](../B/bpy.types.BlendDataObjects.md#bpy.types.BlendDataObjects.new "bpy.types.BlendDataObjects.new")
  * [`BlendDataObjects.remove`](../B/bpy.types.BlendDataObjects.md#bpy.types.BlendDataObjects.remove "bpy.types.BlendDataObjects.remove")
  * [`BoidRuleAvoid.object`](../B/bpy.types.BoidRuleAvoid.md#bpy.types.BoidRuleAvoid.object "bpy.types.BoidRuleAvoid.object")
  * [`BoidRuleFollowLeader.object`](../B/bpy.types.BoidRuleFollowLeader.md#bpy.types.BoidRuleFollowLeader.object "bpy.types.BoidRuleFollowLeader.object")
  * [`BoidRuleGoal.object`](../B/bpy.types.BoidRuleGoal.md#bpy.types.BoidRuleGoal.object "bpy.types.BoidRuleGoal.object")
  * [`BooleanModifier.object`](../B/bpy.types.BooleanModifier.md#bpy.types.BooleanModifier.object "bpy.types.BooleanModifier.object")
  * [`CameraDOFSettings.focus_object`](../C/bpy.types.CameraDOFSettings.md#bpy.types.CameraDOFSettings.focus_object "bpy.types.CameraDOFSettings.focus_object")
  * [`CastModifier.object`](../C/bpy.types.CastModifier.md#bpy.types.CastModifier.object "bpy.types.CastModifier.object")
  * [`ChildOfConstraint.target`](../C/bpy.types.ChildOfConstraint.md#bpy.types.ChildOfConstraint.target "bpy.types.ChildOfConstraint.target")
  * [`ClampToConstraint.target`](../C/bpy.types.ClampToConstraint.md#bpy.types.ClampToConstraint.target "bpy.types.ClampToConstraint.target")
  * [`Collection.all_objects`](../C/bpy.types.Collection.md#bpy.types.Collection.all_objects "bpy.types.Collection.all_objects")
  * [`Collection.objects`](../C/bpy.types.Collection.md#bpy.types.Collection.objects "bpy.types.Collection.objects")
  * [`CollectionObjects.link`](../C/bpy.types.CollectionObjects.md#bpy.types.CollectionObjects.link "bpy.types.CollectionObjects.link")
  * [`CollectionObjects.unlink`](../C/bpy.types.CollectionObjects.md#bpy.types.CollectionObjects.unlink "bpy.types.CollectionObjects.unlink")
  * [`Constraint.space_object`](../C/bpy.types.Constraint.md#bpy.types.Constraint.space_object "bpy.types.Constraint.space_object")
  * [`ConstraintTarget.target`](../C/bpy.types.ConstraintTarget.md#bpy.types.ConstraintTarget.target "bpy.types.ConstraintTarget.target")
  * [`ConstraintTargetBone.target`](../C/bpy.types.ConstraintTargetBone.md#bpy.types.ConstraintTargetBone.target "bpy.types.ConstraintTargetBone.target")
  * [`CopyLocationConstraint.target`](../C/bpy.types.CopyLocationConstraint.md#bpy.types.CopyLocationConstraint.target "bpy.types.CopyLocationConstraint.target")
  * [`CopyRotationConstraint.target`](../C/bpy.types.CopyRotationConstraint.md#bpy.types.CopyRotationConstraint.target "bpy.types.CopyRotationConstraint.target")
  * [`CopyScaleConstraint.target`](../C/bpy.types.CopyScaleConstraint.md#bpy.types.CopyScaleConstraint.target "bpy.types.CopyScaleConstraint.target")
  * [`CopyTransformsConstraint.target`](../C/bpy.types.CopyTransformsConstraint.md#bpy.types.CopyTransformsConstraint.target "bpy.types.CopyTransformsConstraint.target")
  * [`Curve.bevel_object`](../C/bpy.types.Curve.md#bpy.types.Curve.bevel_object "bpy.types.Curve.bevel_object")
  * [`Curve.taper_object`](../C/bpy.types.Curve.md#bpy.types.Curve.taper_object "bpy.types.Curve.taper_object")
  * [`CurveModifier.object`](../C/bpy.types.CurveModifier.md#bpy.types.CurveModifier.object "bpy.types.CurveModifier.object")
  * [`Curves.surface`](../C/bpy.types.Curves.md#bpy.types.Curves.surface "bpy.types.Curves.surface")
  * `CyclesRenderSettings.dicing_camera`
  * [`DampedTrackConstraint.target`](../D/bpy.types.DampedTrackConstraint.md#bpy.types.DampedTrackConstraint.target "bpy.types.DampedTrackConstraint.target")
  * [`DataTransferModifier.object`](../D/bpy.types.DataTransferModifier.md#bpy.types.DataTransferModifier.object "bpy.types.DataTransferModifier.object")
  * [`Depsgraph.objects`](../D/bpy.types.Depsgraph.md#bpy.types.Depsgraph.objects "bpy.types.Depsgraph.objects")
  * [`DepsgraphObjectInstance.instance_object`](../D/bpy.types.DepsgraphObjectInstance.md#bpy.types.DepsgraphObjectInstance.instance_object "bpy.types.DepsgraphObjectInstance.instance_object")
  * [`DepsgraphObjectInstance.object`](../D/bpy.types.DepsgraphObjectInstance.md#bpy.types.DepsgraphObjectInstance.object "bpy.types.DepsgraphObjectInstance.object")
  * [`DepsgraphObjectInstance.parent`](../D/bpy.types.DepsgraphObjectInstance.md#bpy.types.DepsgraphObjectInstance.parent "bpy.types.DepsgraphObjectInstance.parent")
  * [`DisplaceModifier.texture_coords_object`](../D/bpy.types.DisplaceModifier.md#bpy.types.DisplaceModifier.texture_coords_object "bpy.types.DisplaceModifier.texture_coords_object")
  * [`DynamicPaintSurface.output_exists`](../D/bpy.types.DynamicPaintSurface.md#bpy.types.DynamicPaintSurface.output_exists "bpy.types.DynamicPaintSurface.output_exists")
  * [`FieldSettings.source_object`](../F/bpy.types.FieldSettings.md#bpy.types.FieldSettings.source_object "bpy.types.FieldSettings.source_object")
  * [`FloorConstraint.target`](../F/bpy.types.FloorConstraint.md#bpy.types.FloorConstraint.target "bpy.types.FloorConstraint.target")
  * [`FluidDomainSettings.guide_parent`](../F/bpy.types.FluidDomainSettings.md#bpy.types.FluidDomainSettings.guide_parent "bpy.types.FluidDomainSettings.guide_parent")
  * [`FollowPathConstraint.target`](../F/bpy.types.FollowPathConstraint.md#bpy.types.FollowPathConstraint.target "bpy.types.FollowPathConstraint.target")
  * [`FollowTrackConstraint.camera`](../F/bpy.types.FollowTrackConstraint.md#bpy.types.FollowTrackConstraint.camera "bpy.types.FollowTrackConstraint.camera")
  * [`FollowTrackConstraint.depth_object`](../F/bpy.types.FollowTrackConstraint.md#bpy.types.FollowTrackConstraint.depth_object "bpy.types.FollowTrackConstraint.depth_object")
  * [`GPencilSculptGuide.reference_object`](../G/bpy.types.GPencilSculptGuide.md#bpy.types.GPencilSculptGuide.reference_object "bpy.types.GPencilSculptGuide.reference_object")
  * [`GeometryAttributeConstraint.target`](../G/bpy.types.GeometryAttributeConstraint.md#bpy.types.GeometryAttributeConstraint.target "bpy.types.GeometryAttributeConstraint.target")
  * [`GeometryNodeInputObject.object`](../G/bpy.types.GeometryNodeInputObject.md#bpy.types.GeometryNodeInputObject.object "bpy.types.GeometryNodeInputObject.object")
  * [`GreasePencilArmatureModifier.object`](../G/bpy.types.GreasePencilArmatureModifier.md#bpy.types.GreasePencilArmatureModifier.object "bpy.types.GreasePencilArmatureModifier.object")
  * [`GreasePencilArrayModifier.offset_object`](../G/bpy.types.GreasePencilArrayModifier.md#bpy.types.GreasePencilArrayModifier.offset_object "bpy.types.GreasePencilArrayModifier.offset_object")
  * [`GreasePencilBuildModifier.object`](../G/bpy.types.GreasePencilBuildModifier.md#bpy.types.GreasePencilBuildModifier.object "bpy.types.GreasePencilBuildModifier.object")
  * [`GreasePencilHookModifier.object`](../G/bpy.types.GreasePencilHookModifier.md#bpy.types.GreasePencilHookModifier.object "bpy.types.GreasePencilHookModifier.object")
  * [`GreasePencilLatticeModifier.object`](../G/bpy.types.GreasePencilLatticeModifier.md#bpy.types.GreasePencilLatticeModifier.object "bpy.types.GreasePencilLatticeModifier.object")
  * [`GreasePencilLayer.parent`](../G/bpy.types.GreasePencilLayer.md#bpy.types.GreasePencilLayer.parent "bpy.types.GreasePencilLayer.parent")
  * [`GreasePencilLineartModifier.light_contour_object`](../G/bpy.types.GreasePencilLineartModifier.md#bpy.types.GreasePencilLineartModifier.light_contour_object "bpy.types.GreasePencilLineartModifier.light_contour_object")
  * [`GreasePencilLineartModifier.source_camera`](../G/bpy.types.GreasePencilLineartModifier.md#bpy.types.GreasePencilLineartModifier.source_camera "bpy.types.GreasePencilLineartModifier.source_camera")
  * [`GreasePencilLineartModifier.source_object`](../G/bpy.types.GreasePencilLineartModifier.md#bpy.types.GreasePencilLineartModifier.source_object "bpy.types.GreasePencilLineartModifier.source_object")
  * [`GreasePencilMirrorModifier.object`](../G/bpy.types.GreasePencilMirrorModifier.md#bpy.types.GreasePencilMirrorModifier.object "bpy.types.GreasePencilMirrorModifier.object")
  * [`GreasePencilOutlineModifier.object`](../G/bpy.types.GreasePencilOutlineModifier.md#bpy.types.GreasePencilOutlineModifier.object "bpy.types.GreasePencilOutlineModifier.object")
  * [`GreasePencilShrinkwrapModifier.auxiliary_target`](../G/bpy.types.GreasePencilShrinkwrapModifier.md#bpy.types.GreasePencilShrinkwrapModifier.auxiliary_target "bpy.types.GreasePencilShrinkwrapModifier.auxiliary_target")
  * [`GreasePencilShrinkwrapModifier.target`](../G/bpy.types.GreasePencilShrinkwrapModifier.md#bpy.types.GreasePencilShrinkwrapModifier.target "bpy.types.GreasePencilShrinkwrapModifier.target")
  * [`GreasePencilTintModifier.object`](../G/bpy.types.GreasePencilTintModifier.md#bpy.types.GreasePencilTintModifier.object "bpy.types.GreasePencilTintModifier.object")
  * [`GreasePencilWeightProximityModifier.object`](../G/bpy.types.GreasePencilWeightProximityModifier.md#bpy.types.GreasePencilWeightProximityModifier.object "bpy.types.GreasePencilWeightProximityModifier.object")
  * [`HookModifier.object`](../H/bpy.types.HookModifier.md#bpy.types.HookModifier.object "bpy.types.HookModifier.object")

| 

  * [`KinematicConstraint.pole_target`](../K/bpy.types.KinematicConstraint.md#bpy.types.KinematicConstraint.pole_target "bpy.types.KinematicConstraint.pole_target")
  * [`KinematicConstraint.target`](../K/bpy.types.KinematicConstraint.md#bpy.types.KinematicConstraint.target "bpy.types.KinematicConstraint.target")
  * [`LatticeModifier.object`](../L/bpy.types.LatticeModifier.md#bpy.types.LatticeModifier.object "bpy.types.LatticeModifier.object")
  * [`LayerObjects.active`](../L/bpy.types.LayerObjects.md#bpy.types.LayerObjects.active "bpy.types.LayerObjects.active")
  * [`LayerObjects.selected`](../L/bpy.types.LayerObjects.md#bpy.types.LayerObjects.selected "bpy.types.LayerObjects.selected")
  * [`LimitDistanceConstraint.target`](../L/bpy.types.LimitDistanceConstraint.md#bpy.types.LimitDistanceConstraint.target "bpy.types.LimitDistanceConstraint.target")
  * [`LineStyleAlphaModifier_DistanceFromObject.target`](../L/bpy.types.LineStyleAlphaModifier_DistanceFromObject.md#bpy.types.LineStyleAlphaModifier_DistanceFromObject.target "bpy.types.LineStyleAlphaModifier_DistanceFromObject.target")
  * [`LineStyleColorModifier_DistanceFromObject.target`](../L/bpy.types.LineStyleColorModifier_DistanceFromObject.md#bpy.types.LineStyleColorModifier_DistanceFromObject.target "bpy.types.LineStyleColorModifier_DistanceFromObject.target")
  * [`LineStyleThicknessModifier_DistanceFromObject.target`](../L/bpy.types.LineStyleThicknessModifier_DistanceFromObject.md#bpy.types.LineStyleThicknessModifier_DistanceFromObject.target "bpy.types.LineStyleThicknessModifier_DistanceFromObject.target")
  * [`LockedTrackConstraint.target`](../L/bpy.types.LockedTrackConstraint.md#bpy.types.LockedTrackConstraint.target "bpy.types.LockedTrackConstraint.target")
  * [`MaskModifier.armature`](../M/bpy.types.MaskModifier.md#bpy.types.MaskModifier.armature "bpy.types.MaskModifier.armature")
  * [`MeshDeformModifier.object`](../M/bpy.types.MeshDeformModifier.md#bpy.types.MeshDeformModifier.object "bpy.types.MeshDeformModifier.object")
  * [`MeshToVolumeModifier.object`](../M/bpy.types.MeshToVolumeModifier.md#bpy.types.MeshToVolumeModifier.object "bpy.types.MeshToVolumeModifier.object")
  * [`MirrorModifier.mirror_object`](../M/bpy.types.MirrorModifier.md#bpy.types.MirrorModifier.mirror_object "bpy.types.MirrorModifier.mirror_object")
  * [`NodeSocketObject.default_value`](../N/bpy.types.NodeSocketObject.md#bpy.types.NodeSocketObject.default_value "bpy.types.NodeSocketObject.default_value")
  * [`NodeTreeInterfaceSocketObject.default_value`](../N/bpy.types.NodeTreeInterfaceSocketObject.md#bpy.types.NodeTreeInterfaceSocketObject.default_value "bpy.types.NodeTreeInterfaceSocketObject.default_value")
  * [`NormalEditModifier.target`](../N/bpy.types.NormalEditModifier.md#bpy.types.NormalEditModifier.target "bpy.types.NormalEditModifier.target")
  * `Object.find_armature`
  * `Object.parent`
  * [`ObjectBase.object`](bpy.types.ObjectBase.md#bpy.types.ObjectBase.object "bpy.types.ObjectBase.object")
  * [`ObjectSolverConstraint.camera`](bpy.types.ObjectSolverConstraint.md#bpy.types.ObjectSolverConstraint.camera "bpy.types.ObjectSolverConstraint.camera")
  * [`ParticleEdit.object`](../P/bpy.types.ParticleEdit.md#bpy.types.ParticleEdit.object "bpy.types.ParticleEdit.object")
  * [`ParticleEdit.shape_object`](../P/bpy.types.ParticleEdit.md#bpy.types.ParticleEdit.shape_object "bpy.types.ParticleEdit.shape_object")
  * [`ParticleHairKey.co_object`](../P/bpy.types.ParticleHairKey.md#bpy.types.ParticleHairKey.co_object "bpy.types.ParticleHairKey.co_object")
  * [`ParticleHairKey.co_object_set`](../P/bpy.types.ParticleHairKey.md#bpy.types.ParticleHairKey.co_object_set "bpy.types.ParticleHairKey.co_object_set")
  * [`ParticleInstanceModifier.object`](../P/bpy.types.ParticleInstanceModifier.md#bpy.types.ParticleInstanceModifier.object "bpy.types.ParticleInstanceModifier.object")
  * [`ParticleSettings.instance_object`](../P/bpy.types.ParticleSettings.md#bpy.types.ParticleSettings.instance_object "bpy.types.ParticleSettings.instance_object")
  * [`ParticleSettingsTextureSlot.object`](../P/bpy.types.ParticleSettingsTextureSlot.md#bpy.types.ParticleSettingsTextureSlot.object "bpy.types.ParticleSettingsTextureSlot.object")
  * [`ParticleSystem.co_hair`](../P/bpy.types.ParticleSystem.md#bpy.types.ParticleSystem.co_hair "bpy.types.ParticleSystem.co_hair")
  * [`ParticleSystem.parent`](../P/bpy.types.ParticleSystem.md#bpy.types.ParticleSystem.parent "bpy.types.ParticleSystem.parent")
  * [`ParticleSystem.reactor_target_object`](../P/bpy.types.ParticleSystem.md#bpy.types.ParticleSystem.reactor_target_object "bpy.types.ParticleSystem.reactor_target_object")
  * [`ParticleTarget.object`](../P/bpy.types.ParticleTarget.md#bpy.types.ParticleTarget.object "bpy.types.ParticleTarget.object")
  * [`PivotConstraint.target`](../P/bpy.types.PivotConstraint.md#bpy.types.PivotConstraint.target "bpy.types.PivotConstraint.target")
  * [`PoseBone.custom_shape`](../P/bpy.types.PoseBone.md#bpy.types.PoseBone.custom_shape "bpy.types.PoseBone.custom_shape")
  * [`RenderEngine.bake`](../R/bpy.types.RenderEngine.md#bpy.types.RenderEngine.bake "bpy.types.RenderEngine.bake")
  * [`RenderEngine.camera_model_matrix`](../R/bpy.types.RenderEngine.md#bpy.types.RenderEngine.camera_model_matrix "bpy.types.RenderEngine.camera_model_matrix")
  * [`RenderEngine.camera_override`](../R/bpy.types.RenderEngine.md#bpy.types.RenderEngine.camera_override "bpy.types.RenderEngine.camera_override")
  * [`RenderEngine.camera_shift_x`](../R/bpy.types.RenderEngine.md#bpy.types.RenderEngine.camera_shift_x "bpy.types.RenderEngine.camera_shift_x")
  * [`RenderEngine.use_spherical_stereo`](../R/bpy.types.RenderEngine.md#bpy.types.RenderEngine.use_spherical_stereo "bpy.types.RenderEngine.use_spherical_stereo")
  * [`RigidBodyConstraint.object1`](../R/bpy.types.RigidBodyConstraint.md#bpy.types.RigidBodyConstraint.object1 "bpy.types.RigidBodyConstraint.object1")
  * [`RigidBodyConstraint.object2`](../R/bpy.types.RigidBodyConstraint.md#bpy.types.RigidBodyConstraint.object2 "bpy.types.RigidBodyConstraint.object2")
  * [`RigidBodyWorld.convex_sweep_test`](../R/bpy.types.RigidBodyWorld.md#bpy.types.RigidBodyWorld.convex_sweep_test "bpy.types.RigidBodyWorld.convex_sweep_test")
  * [`BakeSettings.cage_object`](../B/bpy.types.BakeSettings.md#bpy.types.BakeSettings.cage_object "bpy.types.BakeSettings.cage_object")
  * [`Scene.camera`](../S/bpy.types.Scene.md#bpy.types.Scene.camera "bpy.types.Scene.camera")
  * [`Scene.objects`](../S/bpy.types.Scene.md#bpy.types.Scene.objects "bpy.types.Scene.objects")
  * [`Scene.ray_cast`](../S/bpy.types.Scene.md#bpy.types.Scene.ray_cast "bpy.types.Scene.ray_cast")
  * [`Scene.uvedit_aspect`](../S/bpy.types.Scene.md#bpy.types.Scene.uvedit_aspect "bpy.types.Scene.uvedit_aspect")
  * [`SceneStrip.scene_camera`](../S/bpy.types.SceneStrip.md#bpy.types.SceneStrip.scene_camera "bpy.types.SceneStrip.scene_camera")
  * [`ScrewModifier.object`](../S/bpy.types.ScrewModifier.md#bpy.types.ScrewModifier.object "bpy.types.ScrewModifier.object")
  * [`Sculpt.gravity_object`](../S/bpy.types.Sculpt.md#bpy.types.Sculpt.gravity_object "bpy.types.Sculpt.gravity_object")
  * [`ShaderFxShadow.object`](../S/bpy.types.ShaderFxShadow.md#bpy.types.ShaderFxShadow.object "bpy.types.ShaderFxShadow.object")
  * [`ShaderFxSwirl.object`](../S/bpy.types.ShaderFxSwirl.md#bpy.types.ShaderFxSwirl.object "bpy.types.ShaderFxSwirl.object")
  * [`ShaderNodeTexCoord.object`](../S/bpy.types.ShaderNodeTexCoord.md#bpy.types.ShaderNodeTexCoord.object "bpy.types.ShaderNodeTexCoord.object")
  * [`ShrinkwrapConstraint.target`](../S/bpy.types.ShrinkwrapConstraint.md#bpy.types.ShrinkwrapConstraint.target "bpy.types.ShrinkwrapConstraint.target")
  * [`ShrinkwrapModifier.auxiliary_target`](../S/bpy.types.ShrinkwrapModifier.md#bpy.types.ShrinkwrapModifier.auxiliary_target "bpy.types.ShrinkwrapModifier.auxiliary_target")
  * [`ShrinkwrapModifier.target`](../S/bpy.types.ShrinkwrapModifier.md#bpy.types.ShrinkwrapModifier.target "bpy.types.ShrinkwrapModifier.target")
  * [`SimpleDeformModifier.origin`](../S/bpy.types.SimpleDeformModifier.md#bpy.types.SimpleDeformModifier.origin "bpy.types.SimpleDeformModifier.origin")
  * [`SpaceView3D.camera`](../S/bpy.types.SpaceView3D.md#bpy.types.SpaceView3D.camera "bpy.types.SpaceView3D.camera")
  * [`SpaceView3D.lock_object`](../S/bpy.types.SpaceView3D.md#bpy.types.SpaceView3D.lock_object "bpy.types.SpaceView3D.lock_object")
  * [`SplineIKConstraint.target`](../S/bpy.types.SplineIKConstraint.md#bpy.types.SplineIKConstraint.target "bpy.types.SplineIKConstraint.target")
  * [`StretchToConstraint.target`](../S/bpy.types.StretchToConstraint.md#bpy.types.StretchToConstraint.target "bpy.types.StretchToConstraint.target")
  * [`SurfaceDeformModifier.target`](../S/bpy.types.SurfaceDeformModifier.md#bpy.types.SurfaceDeformModifier.target "bpy.types.SurfaceDeformModifier.target")
  * [`TextCurve.follow_curve`](../T/bpy.types.TextCurve.md#bpy.types.TextCurve.follow_curve "bpy.types.TextCurve.follow_curve")
  * [`TimelineMarker.camera`](../T/bpy.types.TimelineMarker.md#bpy.types.TimelineMarker.camera "bpy.types.TimelineMarker.camera")
  * [`ToolSettings.anim_mirror_object`](../T/bpy.types.ToolSettings.md#bpy.types.ToolSettings.anim_mirror_object "bpy.types.ToolSettings.anim_mirror_object")
  * [`ToolSettings.anim_relative_object`](../T/bpy.types.ToolSettings.md#bpy.types.ToolSettings.anim_relative_object "bpy.types.ToolSettings.anim_relative_object")
  * [`TrackToConstraint.target`](../T/bpy.types.TrackToConstraint.md#bpy.types.TrackToConstraint.target "bpy.types.TrackToConstraint.target")
  * [`TransformConstraint.target`](../T/bpy.types.TransformConstraint.md#bpy.types.TransformConstraint.target "bpy.types.TransformConstraint.target")
  * [`UVProjector.object`](../U/bpy.types.UVProjector.md#bpy.types.UVProjector.object "bpy.types.UVProjector.object")
  * [`UVWarpModifier.object_from`](../U/bpy.types.UVWarpModifier.md#bpy.types.UVWarpModifier.object_from "bpy.types.UVWarpModifier.object_from")
  * [`UVWarpModifier.object_to`](../U/bpy.types.UVWarpModifier.md#bpy.types.UVWarpModifier.object_to "bpy.types.UVWarpModifier.object_to")
  * [`VertexWeightEditModifier.mask_tex_map_object`](../V/bpy.types.VertexWeightEditModifier.md#bpy.types.VertexWeightEditModifier.mask_tex_map_object "bpy.types.VertexWeightEditModifier.mask_tex_map_object")
  * [`VertexWeightMixModifier.mask_tex_map_object`](../V/bpy.types.VertexWeightMixModifier.md#bpy.types.VertexWeightMixModifier.mask_tex_map_object "bpy.types.VertexWeightMixModifier.mask_tex_map_object")
  * [`VertexWeightProximityModifier.mask_tex_map_object`](../V/bpy.types.VertexWeightProximityModifier.md#bpy.types.VertexWeightProximityModifier.mask_tex_map_object "bpy.types.VertexWeightProximityModifier.mask_tex_map_object")
  * [`VertexWeightProximityModifier.target`](../V/bpy.types.VertexWeightProximityModifier.md#bpy.types.VertexWeightProximityModifier.target "bpy.types.VertexWeightProximityModifier.target")
  * [`ViewLayer.objects`](../V/bpy.types.ViewLayer.md#bpy.types.ViewLayer.objects "bpy.types.ViewLayer.objects")
  * [`VolumeDisplaceModifier.texture_map_object`](../V/bpy.types.VolumeDisplaceModifier.md#bpy.types.VolumeDisplaceModifier.texture_map_object "bpy.types.VolumeDisplaceModifier.texture_map_object")
  * [`VolumeToMeshModifier.object`](../V/bpy.types.VolumeToMeshModifier.md#bpy.types.VolumeToMeshModifier.object "bpy.types.VolumeToMeshModifier.object")
  * [`WarpModifier.object_from`](../W/bpy.types.WarpModifier.md#bpy.types.WarpModifier.object_from "bpy.types.WarpModifier.object_from")
  * [`WarpModifier.object_to`](../W/bpy.types.WarpModifier.md#bpy.types.WarpModifier.object_to "bpy.types.WarpModifier.object_to")
  * [`WarpModifier.texture_coords_object`](../W/bpy.types.WarpModifier.md#bpy.types.WarpModifier.texture_coords_object "bpy.types.WarpModifier.texture_coords_object")
  * [`WaveModifier.start_position_object`](../W/bpy.types.WaveModifier.md#bpy.types.WaveModifier.start_position_object "bpy.types.WaveModifier.start_position_object")
  * [`WaveModifier.texture_coords_object`](../W/bpy.types.WaveModifier.md#bpy.types.WaveModifier.texture_coords_object "bpy.types.WaveModifier.texture_coords_object")
  * [`XrSessionSettings.base_pose_object`](../X/bpy.types.XrSessionSettings.md#bpy.types.XrSessionSettings.base_pose_object "bpy.types.XrSessionSettings.base_pose_object")

  
---|---
  *[*]: Keyword-only parameters separator (PEP 3102)
  *[/]: Positional-only parameter separator (PEP 570)
