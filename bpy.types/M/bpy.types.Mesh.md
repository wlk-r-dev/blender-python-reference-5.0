# Mesh(ID)

## Mesh Data

The mesh data is accessed in object mode and intended for compact storage, for more flexible mesh editing from Python see [`bmesh`](bmesh.md#module-bmesh "bmesh").

Blender stores 4 main arrays to define mesh geometry.

  * `Mesh.vertices` (3 points in space)

  * `Mesh.edges` (reference 2 vertices)

  * `Mesh.loops` (reference a single vertex and edge)

  * `Mesh.polygons`: (reference a range of loops)


Each polygon references a slice in the loop array, this way, polygons do not store vertices or corner data such as UVs directly, only a reference to loops that the polygon uses.

`Mesh.loops`, `Mesh.uv_layers` `Mesh.vertex_colors` are all aligned so the same polygon loop indices can be used to find the UVs and vertex colors as with as the vertices.

To compare mesh API options see: [NGons and Tessellation Faces](../../info/info_gotchas_meshes.md#info-gotcha-mesh-faces)

This example script prints the vertices and UVs for each polygon, assumes the active object is a mesh with UVs.
    
    
    import bpy
    
    me = bpy.context.object.data
    uv_layer = me.uv_layers.active.data
    
    for poly in me.polygons:
        print("Polygon index: {:d}, length: {:d}".format(poly.index, poly.loop_total))
    
        # Range is used here to show how the polygons reference loops,
        # for convenience 'poly.loop_indices' can be used instead.
        for loop_index in range(poly.loop_start, poly.loop_start + poly.loop_total):
            print("    Vertex: {:d}".format(me.loops[loop_index].vertex_index))
            print("    UV: {!r}".format(uv_layer[loop_index].uv))
    

base classes — [`bpy_struct`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct "bpy.types.bpy_struct"), [`ID`](../I/bpy.types.ID.md#bpy.types.ID "bpy.types.ID")

_class _bpy.types.Mesh(_ID_)
    

Mesh data-block defining geometric surfaces

animation_data
    

Animation data for this data-block

Type:
    

[`AnimData`](../A/bpy.types.AnimData.md#bpy.types.AnimData "bpy.types.AnimData"), (readonly)

attributes
    

Geometry attributes

Type:
    

[`AttributeGroupMesh`](../A/bpy.types.AttributeGroupMesh.md#bpy.types.AttributeGroupMesh "bpy.types.AttributeGroupMesh") [`bpy_prop_collection`](../_other/bpy.types.bpy_prop_collection.md#bpy.types.bpy_prop_collection "bpy.types.bpy_prop_collection") of [`Attribute`](../A/bpy.types.Attribute.md#bpy.types.Attribute "bpy.types.Attribute"), (readonly)

auto_texspace
    

Adjust active object’s texture space automatically when transforming object

Type:
    

boolean, default True

color_attributes
    

Geometry color attributes

Type:
    

[`AttributeGroupMesh`](../A/bpy.types.AttributeGroupMesh.md#bpy.types.AttributeGroupMesh "bpy.types.AttributeGroupMesh") [`bpy_prop_collection`](../_other/bpy.types.bpy_prop_collection.md#bpy.types.bpy_prop_collection "bpy.types.bpy_prop_collection") of [`Attribute`](../A/bpy.types.Attribute.md#bpy.types.Attribute "bpy.types.Attribute"), (readonly)

corner_normals
    

The “slit” normal direction of each face corner, influenced by vertex normals, sharp faces, sharp edges, and custom normals. May be empty.

Type:
    

[`bpy_prop_collection`](../_other/bpy.types.bpy_prop_collection.md#bpy.types.bpy_prop_collection "bpy.types.bpy_prop_collection") of [`MeshNormalValue`](bpy.types.MeshNormalValue.md#bpy.types.MeshNormalValue "bpy.types.MeshNormalValue"), (readonly)

cycles
    

Cycles mesh settings

Type:
    

`CyclesMeshSettings`, (readonly)

edges
    

Edges of the mesh

Type:
    

[`MeshEdges`](bpy.types.MeshEdges.md#bpy.types.MeshEdges "bpy.types.MeshEdges") [`bpy_prop_collection`](../_other/bpy.types.bpy_prop_collection.md#bpy.types.bpy_prop_collection "bpy.types.bpy_prop_collection") of [`MeshEdge`](bpy.types.MeshEdge.md#bpy.types.MeshEdge "bpy.types.MeshEdge"), (readonly)

has_custom_normals
    

True if there is custom normal data for this mesh

Type:
    

boolean, default False, (readonly)

is_editmode
    

True when used in editmode

Type:
    

boolean, default False, (readonly)

loop_triangle_polygons
    

The face index for each loop triangle

Type:
    

[`bpy_prop_collection`](../_other/bpy.types.bpy_prop_collection.md#bpy.types.bpy_prop_collection "bpy.types.bpy_prop_collection") of [`ReadOnlyInteger`](../R/bpy.types.ReadOnlyInteger.md#bpy.types.ReadOnlyInteger "bpy.types.ReadOnlyInteger"), (readonly)

loop_triangles
    

Tessellation of mesh polygons into triangles

Type:
    

[`MeshLoopTriangles`](bpy.types.MeshLoopTriangles.md#bpy.types.MeshLoopTriangles "bpy.types.MeshLoopTriangles") [`bpy_prop_collection`](../_other/bpy.types.bpy_prop_collection.md#bpy.types.bpy_prop_collection "bpy.types.bpy_prop_collection") of [`MeshLoopTriangle`](bpy.types.MeshLoopTriangle.md#bpy.types.MeshLoopTriangle "bpy.types.MeshLoopTriangle"), (readonly)

loops
    

Loops of the mesh (face corners)

Type:
    

[`MeshLoops`](bpy.types.MeshLoops.md#bpy.types.MeshLoops "bpy.types.MeshLoops") [`bpy_prop_collection`](../_other/bpy.types.bpy_prop_collection.md#bpy.types.bpy_prop_collection "bpy.types.bpy_prop_collection") of [`MeshLoop`](bpy.types.MeshLoop.md#bpy.types.MeshLoop "bpy.types.MeshLoop"), (readonly)

materials
    

Type:
    

[`IDMaterials`](../I/bpy.types.IDMaterials.md#bpy.types.IDMaterials "bpy.types.IDMaterials") [`bpy_prop_collection`](../_other/bpy.types.bpy_prop_collection.md#bpy.types.bpy_prop_collection "bpy.types.bpy_prop_collection") of [`Material`](bpy.types.Material.md#bpy.types.Material "bpy.types.Material"), (readonly)

normals_domain
    

The attribute domain that gives enough information to represent the mesh’s normals

Type:
    

enum in [`'POINT'`, `'FACE'`, `'CORNER'`], default `'FACE'`, (readonly)

polygon_normals
    

The normal direction of each face, defined by the winding order and position of its vertices

Type:
    

[`bpy_prop_collection`](../_other/bpy.types.bpy_prop_collection.md#bpy.types.bpy_prop_collection "bpy.types.bpy_prop_collection") of [`MeshNormalValue`](bpy.types.MeshNormalValue.md#bpy.types.MeshNormalValue "bpy.types.MeshNormalValue"), (readonly)

polygons
    

Polygons of the mesh

Type:
    

[`MeshPolygons`](bpy.types.MeshPolygons.md#bpy.types.MeshPolygons "bpy.types.MeshPolygons") [`bpy_prop_collection`](../_other/bpy.types.bpy_prop_collection.md#bpy.types.bpy_prop_collection "bpy.types.bpy_prop_collection") of [`MeshPolygon`](bpy.types.MeshPolygon.md#bpy.types.MeshPolygon "bpy.types.MeshPolygon"), (readonly)

radial_symmetry
    

Number of mirrored regions around a central axis

Type:
    

int array of 3 items in [1, 64], default (1, 1, 1)

remesh_mode
    

  * `VOXEL` Voxel – Use the voxel remesher.

  * `QUAD` Quad – Use the quad remesher.


Type:
    

enum in [`'VOXEL'`, `'QUAD'`], default `'VOXEL'`

remesh_voxel_adaptivity
    

Reduces the final face count by simplifying geometry where detail is not needed, generating triangles. A value greater than 0 disables Fix Poles.

Type:
    

float in [0, 1], default 0.0

remesh_voxel_size
    

Size of the voxel in object space used for volume evaluation. Lower values preserve finer details.

Type:
    

float in [0, inf], default 0.1

shape_keys
    

Type:
    

[`Key`](../K/bpy.types.Key.md#bpy.types.Key "bpy.types.Key"), (readonly)

skin_vertices
    

All skin vertices

Type:
    

[`bpy_prop_collection`](../_other/bpy.types.bpy_prop_collection.md#bpy.types.bpy_prop_collection "bpy.types.bpy_prop_collection") of [`MeshSkinVertexLayer`](bpy.types.MeshSkinVertexLayer.md#bpy.types.MeshSkinVertexLayer "bpy.types.MeshSkinVertexLayer"), (readonly)

texco_mesh
    

Derive texture coordinates from another mesh

Type:
    

`Mesh`

texspace_location
    

Texture space location

Type:
    

[`mathutils.Vector`](mathutils.md#mathutils.Vector "mathutils.Vector") of 3 items in [-inf, inf], default (0.0, 0.0, 0.0)

texspace_size
    

Texture space size

Type:
    

[`mathutils.Vector`](mathutils.md#mathutils.Vector "mathutils.Vector") of 3 items in [-inf, inf], default (1.0, 1.0, 1.0)

texture_mesh
    

Use another mesh for texture indices (vertex indices must be aligned)

Type:
    

`Mesh`

total_edge_sel
    

Selected edge count in editmode

Type:
    

int in [0, inf], default 0, (readonly)

total_face_sel
    

Selected face count in editmode

Type:
    

int in [0, inf], default 0, (readonly)

total_vert_sel
    

Selected vertex count in editmode

Type:
    

int in [0, inf], default 0, (readonly)

use_auto_texspace
    

Adjust active object’s texture space automatically when transforming object

Type:
    

boolean, default True

use_mirror_topology
    

Use topology based mirroring (for when both sides of mesh have matching, unique topology)

Type:
    

boolean, default False

use_mirror_vertex_groups
    

Mirror the left/right vertex groups when painting. The symmetry axis is determined by the symmetry settings.

Type:
    

boolean, default True

use_mirror_x
    

Enable symmetry in the X axis

Type:
    

boolean, default False

use_mirror_y
    

Enable symmetry in the Y axis

Type:
    

boolean, default False

use_mirror_z
    

Enable symmetry in the Z axis

Type:
    

boolean, default False

use_paint_bone_selection
    

Bone selection during painting

Type:
    

boolean, default True

use_paint_mask
    

Face selection masking for painting

Type:
    

boolean, default False

use_paint_mask_vertex
    

Vertex selection masking for painting

Type:
    

boolean, default False

use_remesh_fix_poles
    

Produces fewer poles and a better topology flow

Type:
    

boolean, default False

use_remesh_preserve_attributes
    

Transfer all attributes to the new mesh

Type:
    

boolean, default False

use_remesh_preserve_volume
    

Projects the mesh to preserve the volume and details of the original mesh

Type:
    

boolean, default False

uv_layer_clone
    

UV loop layer to be used as cloning source

Type:
    

[`MeshUVLoopLayer`](bpy.types.MeshUVLoopLayer.md#bpy.types.MeshUVLoopLayer "bpy.types.MeshUVLoopLayer")

uv_layer_clone_index
    

Clone UV loop layer index

Type:
    

int in [0, inf], default 0

uv_layer_stencil
    

UV loop layer to mask the painted area

Type:
    

[`MeshUVLoopLayer`](bpy.types.MeshUVLoopLayer.md#bpy.types.MeshUVLoopLayer "bpy.types.MeshUVLoopLayer")

uv_layer_stencil_index
    

Mask UV loop layer index

Type:
    

int in [0, inf], default 0

uv_layers
    

All UV loop layers

Type:
    

[`UVLoopLayers`](../U/bpy.types.UVLoopLayers.md#bpy.types.UVLoopLayers "bpy.types.UVLoopLayers") [`bpy_prop_collection`](../_other/bpy.types.bpy_prop_collection.md#bpy.types.bpy_prop_collection "bpy.types.bpy_prop_collection") of [`MeshUVLoopLayer`](bpy.types.MeshUVLoopLayer.md#bpy.types.MeshUVLoopLayer "bpy.types.MeshUVLoopLayer"), (readonly)

vertex_colors
    

Legacy vertex color layers. Deprecated, use color attributes instead.

Type:
    

[`LoopColors`](../L/bpy.types.LoopColors.md#bpy.types.LoopColors "bpy.types.LoopColors") [`bpy_prop_collection`](../_other/bpy.types.bpy_prop_collection.md#bpy.types.bpy_prop_collection "bpy.types.bpy_prop_collection") of [`MeshLoopColorLayer`](bpy.types.MeshLoopColorLayer.md#bpy.types.MeshLoopColorLayer "bpy.types.MeshLoopColorLayer"), (readonly)

vertex_normals
    

The normal direction of each vertex, defined as the average of the surrounding face normals

Type:
    

[`bpy_prop_collection`](../_other/bpy.types.bpy_prop_collection.md#bpy.types.bpy_prop_collection "bpy.types.bpy_prop_collection") of [`MeshNormalValue`](bpy.types.MeshNormalValue.md#bpy.types.MeshNormalValue "bpy.types.MeshNormalValue"), (readonly)

vertices
    

Vertices of the mesh

Type:
    

[`MeshVertices`](bpy.types.MeshVertices.md#bpy.types.MeshVertices "bpy.types.MeshVertices") [`bpy_prop_collection`](../_other/bpy.types.bpy_prop_collection.md#bpy.types.bpy_prop_collection "bpy.types.bpy_prop_collection") of [`MeshVertex`](bpy.types.MeshVertex.md#bpy.types.MeshVertex "bpy.types.MeshVertex"), (readonly)

edge_creases
    

Edge crease values for subdivision surface, corresponding to the “crease_edge” attribute.

(readonly)

edge_keys
    

(readonly)

vertex_creases
    

Vertex crease values for subdivision surface, corresponding to the “crease_vert” attribute.

(readonly)

vertex_paint_mask
    

Mask values for sculpting and painting, corresponding to the “.sculpt_mask” attribute.

(readonly)

transform(_matrix_ , _*_ , _shape_keys =False_)
    

Transform mesh vertices by a matrix (Warning: inverts normals if matrix is negative)

Parameters:
    

  * **matrix** ([`mathutils.Matrix`](mathutils.md#mathutils.Matrix "mathutils.Matrix") of 4 * 4 items in [-inf, inf]) – Matrix

  * **shape_keys** (_boolean_ _,__(__optional_ _)_) – Transform Shape Keys


flip_normals()
    

Invert winding of all polygons (clears tessellation, does not handle custom normals)

set_sharp_from_angle(_*_ , _angle =3.14159_)
    

Reset and fill the “sharp_edge” attribute based on the angle of faces neighboring manifold edges

Parameters:
    

**angle** (_float in_ _[__0_ _,__3.14159_ _]__,__(__optional_ _)_) – Angle, Angle between faces beyond which edges are marked sharp

split_faces()
    

Split faces based on the edge angle

calc_tangents(_*_ , _uvmap =''_)
    

Compute tangents and bitangent signs, to be used together with the custom normals to get a complete tangent space for normal mapping (custom normals are also computed if not yet present)

Parameters:
    

**uvmap** (_string_ _,__(__optional_ _,__never None_ _)_) – Name of the UV map to use for tangent space computation

free_tangents()
    

Free tangents

calc_loop_triangles()
    

Calculate loop triangle tessellation (supports editmode too)

calc_smooth_groups(_*_ , _use_bitflags =False_, _use_boundary_vertices_for_bitflags =False_)
    

Calculate smooth groups from sharp edges

Parameters:
    

  * **use_bitflags** (_boolean_ _,__(__optional_ _)_) – Produce bitflags groups instead of simple numeric values

  * **use_boundary_vertices_for_bitflags** (_boolean_ _,__(__optional_ _)_) – Also consider different smoothgroups sharing only vertices (but without any common edge) as neighbors, preventing them from sharing the same bitflag value. Only effective when `use_bitflags` is set. WARNING: Will overflow (run out of available bits) easily with some types of topology, e.g. large fans of sharp edges


Returns:
    

`poly_groups`, Smooth Groups, int array of 1 items in [-inf, inf]

`groups`, Total number of groups, int in [0, inf]

Return type:
    

(int array of 1 items in [-inf, inf], int in [0, inf])

normals_split_custom_set(_normals_)
    

Define custom normals of this mesh (use zero-vectors to keep auto ones)

Parameters:
    

**normals** (_float multi-dimensional array_ _of_ _1 * 3 items in_ _[__-1_ _,__1_ _]_) – Normals

normals_split_custom_set_from_vertices(_normals_)
    

Define custom normals of this mesh, from vertices’ normals (use zero-vectors to keep auto ones)

Parameters:
    

**normals** (_float multi-dimensional array_ _of_ _1 * 3 items in_ _[__-1_ _,__1_ _]_) – Normals

update(_*_ , _calc_edges =False_, _calc_edges_loose =False_)
    

update

Parameters:
    

  * **calc_edges** (_boolean_ _,__(__optional_ _)_) – Calculate Edges, Force recalculation of edges

  * **calc_edges_loose** (_boolean_ _,__(__optional_ _)_) – Calculate Loose Edges, Calculate the loose state of each edge


update_gpu_tag()
    

update_gpu_tag

unit_test_compare(_*_ , _mesh =None_, _threshold =7.1526e-06_)
    

unit_test_compare

Parameters:
    

  * **mesh** (`Mesh`, (optional)) – Mesh to compare to

  * **threshold** (_float in_ _[__0_ _,__inf_ _]__,__(__optional_ _)_) – Threshold, Comparison tolerance threshold


Returns:
    

Return value, String description of result of comparison

Return type:
    

string, (never None)

clear_geometry()
    

Remove all geometry from the mesh. Note that this does not free shape keys or materials.

validate(_*_ , _verbose =False_, _clean_customdata =True_)
    

Validate geometry, return True when the mesh has had invalid geometry corrected/removed

Parameters:
    

  * **verbose** (_boolean_ _,__(__optional_ _)_) – Verbose, Output information about the errors found

  * **clean_customdata** (_boolean_ _,__(__optional_ _)_) – Clean Custom Data, Remove temp/cached custom-data layers, like e.g. normals…


Returns:
    

Result

Return type:
    

boolean

validate_material_indices()
    

Validate material indices of polygons, return True when the mesh has had invalid indices corrected (to default 0)

Returns:
    

Result

Return type:
    

boolean

count_selected_items()
    

Return the number of selected items (vert, edge, face)

Returns:
    

Result

Return type:
    

int array of 3 items in [0, inf]

edge_creases_ensure()
    

edge_creases_remove()
    

from_pydata(_vertices_ , _edges_ , _faces_ , _shade_flat =True_)
    

Make a mesh from a list of vertices/edges/faces Until we have a nicer way to make geometry, use this.

Parameters:
    

  * **vertices** (_Iterable_ _[__Sequence_ _[__float_ _]__]_) – float triplets each representing (X, Y, Z) eg: [(0.0, 1.0, 0.5), …].

  * **edges** (_Iterable_ _[__Sequence_ _[__int_ _]__]_) – 

int pairs, each pair contains two indices to the _vertices_ argument. eg: [(1, 2), …]

When an empty iterable is passed in, the edges are inferred from the polygons.

  * **faces** (_Iterable_ _[__Sequence_ _[__int_ _]__]_) – iterator of faces, each faces contains three or more indices to the _vertices_ argument. eg: [(5, 6, 8, 9), (1, 2, 3), …]


Warning

Invalid mesh data _(out of range indices, edges with matching indices, 2 sided faces… etc)_ are **not** prevented. If the data used for mesh creation isn’t known to be valid, run `Mesh.validate` after this function.

shade_flat()
    

Render and display faces uniform, using face normals, setting the “sharp_face” attribute true for every face

shade_smooth()
    

Render and display faces smooth, using interpolated vertex normals, removing the “sharp_face” attribute

vertex_creases_ensure()
    

vertex_creases_remove()
    

vertex_paint_mask_ensure()
    

vertex_paint_mask_remove()
    

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

  * [`bpy.context.mesh`](../../bpy.context.md#bpy.context.mesh "bpy.context.mesh")
  * [`BlendData.meshes`](../B/bpy.types.BlendData.md#bpy.types.BlendData.meshes "bpy.types.BlendData.meshes")
  * [`BlendDataMeshes.new`](../B/bpy.types.BlendDataMeshes.md#bpy.types.BlendDataMeshes.new "bpy.types.BlendDataMeshes.new")
  * [`BlendDataMeshes.new_from_object`](../B/bpy.types.BlendDataMeshes.md#bpy.types.BlendDataMeshes.new_from_object "bpy.types.BlendDataMeshes.new_from_object")
  * [`BlendDataMeshes.remove`](../B/bpy.types.BlendDataMeshes.md#bpy.types.BlendDataMeshes.remove "bpy.types.BlendDataMeshes.remove")

| 

  * `Mesh.texco_mesh`
  * `Mesh.texture_mesh`
  * `Mesh.unit_test_compare`
  * [`Object.to_mesh`](../O/bpy.types.Object.md#bpy.types.Object.to_mesh "bpy.types.Object.to_mesh")

  
---|---
  *[*]: Keyword-only parameters separator (PEP 3102)
  *[/]: Positional-only parameter separator (PEP 570)
