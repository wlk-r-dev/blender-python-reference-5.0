# BMesh Types (bmesh.types)

## Base Mesh Type

_class _bmesh.types.BMesh
    

The BMesh data structure

calc_loop_triangles()
    

Calculate triangle tessellation from quads/ngons.

Returns:
    

The triangulated faces.

Return type:
    

list[tuple[`bmesh.types.BMLoop`, `bmesh.types.BMLoop`, `bmesh.types.BMLoop`]]

calc_volume(_*_ , _signed =False_)
    

Calculate mesh volume based on face normals.

Parameters:
    

**signed** (_bool_) – when signed is true, negative values may be returned.

Returns:
    

The volume of the mesh.

Return type:
    

float

clear()
    

Clear all mesh data.

copy()
    

Returns:
    

A copy of this BMesh.

Return type:
    

`bmesh.types.BMesh`

free()
    

Explicitly free the BMesh data from memory, causing exceptions on further access.

Note

The BMesh is freed automatically, typically when the script finishes executing. However in some cases its hard to predict when this will be and its useful to explicitly free the data.

from_mesh(_mesh_ , _*_ , _face_normals =True_, _vertex_normals =True_, _use_shape_key =False_, _shape_key_index =0_)
    

Initialize this bmesh from existing mesh data-block.

Parameters:
    

  * **mesh** ([`bpy.types.Mesh`](../bpy.types/M/bpy.types.Mesh.md#bpy.types.Mesh "bpy.types.Mesh")) – The mesh data to load.

  * **use_shape_key** (_bool_) – Use the locations from a shape key.

  * **shape_key_index** (_int_) – The shape key index to use.


Note

Multiple calls can be used to join multiple meshes.

Custom-data layers are only copied from `mesh` on initialization. Further calls will copy custom-data to matching layers, layers missing on the target mesh won’t be added.

from_object(_object_ , _depsgraph_ , _*_ , _cage =False_, _face_normals =True_, _vertex_normals =True_)
    

Initialize this bmesh from existing object data-block (only meshes are currently supported).

Parameters:
    

  * **object** ([`bpy.types.Object`](../bpy.types/O/bpy.types.Object.md#bpy.types.Object "bpy.types.Object")) – The object data to load.

  * **cage** (_bool_) – Get the mesh as a deformed cage.

  * **face_normals** (_bool_) – Calculate face normals.

  * **vertex_normals** (_bool_) – Calculate vertex normals.


normal_update()
    

Update normals of mesh faces and verts.

Note

The normal of any vertex where `is_wire` is True will be a zero vector.

select_flush(_select_)
    

Flush selection from vertices, independent of the current selection mode.

Parameters:
    

**select** (_bool_) – flush selection or de-selected elements.

select_flush_mode(_*_ , _flush_down =False_)
    

Flush selection based on the current mode current `bmesh.types.BMesh.select_mode`.

Parameters:
    

**flush_down** (_bool_) – Flush selection down from faces to edges & verts or from edges to verts. This option is ignored when vertex selection mode is enabled.

to_mesh(_mesh_)
    

Writes this BMesh data into an existing Mesh data-block.

Parameters:
    

**mesh** ([`bpy.types.Mesh`](../bpy.types/M/bpy.types.Mesh.md#bpy.types.Mesh "bpy.types.Mesh")) – The mesh data to write into.

transform(_matrix_ , _*_ , _filter =None_)
    

Transform the mesh (optionally filtering flagged data only).

Parameters:
    

  * **matrix** ([`mathutils.Matrix`](mathutils.md#mathutils.Matrix "mathutils.Matrix")) – 4x4x transform matrix.

  * **filter** (_set_ _[__Literal_ _[__'SELECT'__,__'HIDE'__,__'SEAM'__,__'SMOOTH'__,__'TAG'__]__]_) – Flag to filter vertices..


uv_select_flush(_select_)
    

Flush selection from UV vertices to edges & faces independent of the selection mode.

Parameters:
    

**select** (_bool_) – Flush selection or de-selected elements.

Note

  * This function doesn’t flush the selection to the mesh, typically `bmesh.types.BMesh.uv_select_sync_to_mesh` should be called afterwards.


uv_select_flush_mode(_*_ , _flush_down =False_)
    

Flush selection based on the current mode current `BMesh.select_mode`.

Parameters:
    

**flush_down** (_bool_) – Flush selection down from faces to edges & verts or from edges to verts. This option is ignored when vertex selection mode is enabled.

uv_select_flush_shared(_select_)
    

Flush selection from UV vertices to contiguous UV’s independent of the selection mode.

Parameters:
    

**select** (_bool_) – Flush selection or de-selected elements.

Note

  * This function doesn’t flush the selection to the mesh, typically `bmesh.types.BMesh.uv_select_sync_to_mesh` should be called afterwards.


uv_select_foreach_set(_select_ , _/_ , _*_ , _loop_verts =()_, _loop_edges =()_, _faces =()_, _sticky_select_mode ='SHARED_LOCATION'_)
    

Set the UV selection state for loop-vertices, loop-edges & faces.

This is a close equivalent to selecting in the UV editor.

Parameters:
    

  * **select** (_bool_) – The selection state to set.

  * **loop_verts** (Iterable[`bmesh.types.BMLoop`]) – Loop verts to operate on.

  * **loop_edges** (Iterable[`bmesh.types.BMLoop`]) – Loop edges to operate on.

  * **faces** (Iterable[`bmesh.types.BMFace`]) – Faces to operate on.

  * **sticky_select_mode** (Literal[‘SHARED_LOCATION’, ‘DISABLED’, ‘SHARED_VERTEX’]) – See ([`bpy.types.ToolSettings.uv_sticky_select_mode`](../bpy.types/T/bpy.types.ToolSettings.md#bpy.types.ToolSettings.uv_sticky_select_mode "bpy.types.ToolSettings.uv_sticky_select_mode") which may be passed in directly)..


Note

  * This function selection-mode independent, typically `bmesh.types.BMesh.uv_select_flush_mode` should be called afterwards.

  * This function doesn’t flush the selection to the mesh, typically `bmesh.types.BMesh.uv_select_sync_to_mesh` should be called afterwards.


uv_select_foreach_set_from_mesh(_select_ , _/_ , _*_ , _verts =()_, _edges =()_, _faces =()_, _sticky_select_mode ='SHARED_LOCATION'_)
    

Select or de-select mesh elements, updating the UV selection.

An equivalent to selecting from the 3D viewport for selection operations that support maintaining a synchronized UV selection.

Parameters:
    

  * **select** (_bool_) – The selection state to set.

  * **verts** (Iterable[`bmesh.types.BMVert`]) – Verts to operate on.

  * **edges** (Iterable[`bmesh.types.BMEdge`]) – Edges to operate on.

  * **faces** (Iterable[`bmesh.types.BMFace`]) – Faces to operate on.

  * **sticky_select_mode** (Literal[‘SHARED_LOCATION’, ‘DISABLED’, ‘SHARED_VERTEX’]) – See ([`bpy.types.ToolSettings.uv_sticky_select_mode`](../bpy.types/T/bpy.types.ToolSettings.md#bpy.types.ToolSettings.uv_sticky_select_mode "bpy.types.ToolSettings.uv_sticky_select_mode") which may be passed in directly)..


uv_select_sync_from_mesh(_*_ , _sticky_select_mode ='SHARED_LOCATION'_)
    

Sync selection from mesh to UVs.

Parameters:
    

**sticky_select_mode** (Literal[‘SHARED_LOCATION’, ‘DISABLED’, ‘SHARED_VERTEX’]) – Behavior when flushing from the mesh to UV selection ([`bpy.types.ToolSettings.uv_sticky_select_mode`](../bpy.types/T/bpy.types.ToolSettings.md#bpy.types.ToolSettings.uv_sticky_select_mode "bpy.types.ToolSettings.uv_sticky_select_mode") which may be passed in directly).. This should only be used when preparing to create a UV selection.

Note

  * This function doesn’t flush the selection to the mesh, typically `bmesh.types.BMesh.uv_select_sync_to_mesh` should be called afterwards.


uv_select_sync_to_mesh()
    

Sync selection from UVs to the mesh.

edges
    

This meshes edge sequence (read-only).

Type:
    

`bmesh.types.BMEdgeSeq`

faces
    

This meshes face sequence (read-only).

Type:
    

`bmesh.types.BMFaceSeq`

is_valid
    

True when this element is valid (hasn’t been removed).

Type:
    

bool

is_wrapped
    

True when this mesh is owned by blender (typically the editmode BMesh).

Type:
    

bool

loops
    

This meshes loops (read-only).

Type:
    

`bmesh.types.BMLoopSeq`

Note

Loops must be accessed via faces, this is only exposed for layer access.

select_history
    

Sequence of selected items (the last is displayed as active).

Type:
    

`bmesh.types.BMEditSelSeq`

select_mode
    

The selection mode, cannot be assigned an empty set.

Type:
    

set[Literal[‘VERT’, ‘EDGE’, ‘FACE’]]

uv_select_sync_valid
    

When true, the UV selection has been synchronized. Setting to False means the UV selection will be ignored. While setting to true is supported it is up to the script author to ensure a correct selection state before doing so. :type: bool

verts
    

This meshes vert sequence (read-only).

Type:
    

`bmesh.types.BMVertSeq`

## Mesh Elements

_class _bmesh.types.BMVert
    

The BMesh vertex type

calc_edge_angle(_fallback =None_)
    

Return the angle between this vert’s two connected edges.

Parameters:
    

**fallback** (_Any_) – return this when the vert doesn’t have 2 edges (instead of raising a `ValueError`).

Returns:
    

Angle between edges in radians.

Return type:
    

float

calc_shell_factor()
    

Return a multiplier calculated based on the sharpness of the vertex. Where a flat surface gives 1.0, and higher values sharper edges. This is used to maintain shell thickness when offsetting verts along their normals.

Returns:
    

offset multiplier

Return type:
    

float

copy_from(_other_)
    

Copy values from another element of matching type.

copy_from_face_interp(_face_)
    

Interpolate the customdata from a face onto this loop (the loops vert should overlap the face).

Parameters:
    

**face** (`bmesh.types.BMFace`) – The face to interpolate data from.

copy_from_vert_interp(_vert_pair_ , _fac_)
    

Interpolate the customdata from a vert between 2 other verts.

Parameters:
    

**vert_pair** (Sequence[`bmesh.types.BMVert`]) – The verts between which to interpolate data from.

hide_set(_hide_)
    

Set the hide state. This is different from the _hide_ attribute because it updates the selection and hide state of associated geometry.

Parameters:
    

**hide** (_bool_) – Hidden or visible.

normal_update()
    

Update vertex normal. This does not update the normals of adjoining faces.

Note

The vertex normal will be a zero vector if vertex `is_wire` is True.

select_set(_select_)
    

Set the selection. This is different from the _select_ attribute because it updates the selection state of associated geometry.

Parameters:
    

**select** (_bool_) – Select or de-select.

Note

This only flushes down, so selecting a face will select all its vertices but de-selecting a vertex won’t de-select all the faces that use it, before finishing with a mesh typically flushing is still needed.

co
    

The coordinates for this vertex as a 3D, wrapped vector.

Type:
    

[`mathutils.Vector`](mathutils.md#mathutils.Vector "mathutils.Vector")

hide
    

Hidden state of this element.

Type:
    

bool

index
    

Index of this element.

Type:
    

int

Note

This value is not necessarily valid, while editing the mesh it can become _dirty_.

It’s also possible to assign any number to this attribute for a scripts internal logic.

To ensure the value is up to date - see `bmesh.types.BMElemSeq.index_update`.

is_boundary
    

True when this vertex is connected to boundary edges (read-only).

Type:
    

bool

is_manifold
    

True when this vertex is manifold (read-only).

Type:
    

bool

is_valid
    

True when this element is valid (hasn’t been removed).

Type:
    

bool

is_wire
    

True when this vertex is not connected to any faces (read-only).

Type:
    

bool

link_edges
    

Edges connected to this vertex (read-only).

Type:
    

`bmesh.types.BMElemSeq` of `bmesh.types.BMEdge`

link_faces
    

Faces connected to this vertex (read-only).

Type:
    

`bmesh.types.BMElemSeq` of `bmesh.types.BMFace`

link_loops
    

Loops that use this vertex (read-only).

Type:
    

`bmesh.types.BMElemSeq` of `bmesh.types.BMLoop`

normal
    

The normal for this vertex as a 3D, wrapped vector.

Type:
    

[`mathutils.Vector`](mathutils.md#mathutils.Vector "mathutils.Vector")

select
    

Selected state of this element.

Type:
    

bool

tag
    

Generic attribute scripts can use for own logic

Type:
    

bool

_class _bmesh.types.BMEdge
    

The BMesh edge connecting 2 verts

calc_face_angle(_fallback =None_)
    

Parameters:
    

**fallback** (_Any_) – return this when the edge doesn’t have 2 faces (instead of raising a `ValueError`).

Returns:
    

The angle between 2 connected faces in radians.

Return type:
    

float

calc_face_angle_signed(_fallback =None_)
    

Parameters:
    

**fallback** (_Any_) – return this when the edge doesn’t have 2 faces (instead of raising a `ValueError`).

Returns:
    

The angle between 2 connected faces in radians (negative for concave join).

Return type:
    

float

calc_length()
    

Returns:
    

The length between both verts.

Return type:
    

float

calc_tangent(_loop_)
    

Return the tangent at this edge relative to a face (pointing inward into the face). This uses the face normal for calculation.

Parameters:
    

**loop** (`bmesh.types.BMLoop`) – The loop used for tangent calculation.

Returns:
    

a normalized vector.

Return type:
    

[`mathutils.Vector`](mathutils.md#mathutils.Vector "mathutils.Vector")

copy_from(_other_)
    

Copy values from another element of matching type.

hide_set(_hide_)
    

Set the hide state. This is different from the _hide_ attribute because it updates the selection and hide state of associated geometry.

Parameters:
    

**hide** (_bool_) – Hidden or visible.

normal_update()
    

Update normals of all connected faces and the edge verts.

Note

The normal of edge vertex will be a zero vector if vertex `is_wire` is True.

other_vert(_vert_)
    

Return the other vertex on this edge or None if the vertex is not used by this edge.

Parameters:
    

**vert** (`bmesh.types.BMVert`) – a vert in this edge.

Returns:
    

The edges other vert.

Return type:
    

`bmesh.types.BMVert` | None

select_set(_select_)
    

Set the selection. This is different from the _select_ attribute because it updates the selection state of associated geometry.

Parameters:
    

**select** (_bool_) – Select or de-select.

Note

This only flushes down, so selecting a face will select all its vertices but de-selecting a vertex won’t de-select all the faces that use it, before finishing with a mesh typically flushing is still needed.

hide
    

Hidden state of this element.

Type:
    

bool

index
    

Index of this element.

Type:
    

int

Note

This value is not necessarily valid, while editing the mesh it can become _dirty_.

It’s also possible to assign any number to this attribute for a scripts internal logic.

To ensure the value is up to date - see `bmesh.types.BMElemSeq.index_update`.

is_boundary
    

True when this edge is at the boundary of a face (read-only).

Type:
    

bool

is_contiguous
    

True when this edge is manifold, between two faces with the same winding (read-only).

Type:
    

bool

is_convex
    

True when this edge joins two convex faces, depends on a valid face normal (read-only).

Type:
    

bool

is_manifold
    

True when this edge is manifold (read-only).

Type:
    

bool

is_valid
    

True when this element is valid (hasn’t been removed).

Type:
    

bool

is_wire
    

True when this edge is not connected to any faces (read-only).

Type:
    

bool

link_faces
    

Faces connected to this edge, (read-only).

Type:
    

`bmesh.types.BMElemSeq` of `bmesh.types.BMFace`

link_loops
    

Loops connected to this edge, (read-only).

Type:
    

`bmesh.types.BMElemSeq` of `bmesh.types.BMLoop`

seam
    

Seam for UV unwrapping.

Type:
    

bool

select
    

Selected state of this element.

Type:
    

bool

smooth
    

Smooth state of this element.

Type:
    

bool

tag
    

Generic attribute scripts can use for own logic

Type:
    

bool

verts
    

Verts this edge uses (always 2), (read-only).

Type:
    

`bmesh.types.BMElemSeq` of `bmesh.types.BMVert`

_class _bmesh.types.BMFace
    

The BMesh face with 3 or more sides

calc_area()
    

Return the area of the face.

Returns:
    

Return the area of the face.

Return type:
    

float

calc_center_bounds()
    

Return bounds center of the face.

Returns:
    

a 3D vector.

Return type:
    

[`mathutils.Vector`](mathutils.md#mathutils.Vector "mathutils.Vector")

calc_center_median()
    

Return median center of the face.

Returns:
    

a 3D vector.

Return type:
    

[`mathutils.Vector`](mathutils.md#mathutils.Vector "mathutils.Vector")

calc_center_median_weighted()
    

Return median center of the face weighted by edge lengths.

Returns:
    

a 3D vector.

Return type:
    

[`mathutils.Vector`](mathutils.md#mathutils.Vector "mathutils.Vector")

calc_perimeter()
    

Return the perimeter of the face.

Returns:
    

Return the perimeter of the face.

Return type:
    

float

calc_tangent_edge()
    

Return face tangent based on longest edge.

Returns:
    

a normalized vector.

Return type:
    

[`mathutils.Vector`](mathutils.md#mathutils.Vector "mathutils.Vector")

calc_tangent_edge_diagonal()
    

Return face tangent based on the edge farthest from any vertex.

Returns:
    

a normalized vector.

Return type:
    

[`mathutils.Vector`](mathutils.md#mathutils.Vector "mathutils.Vector")

calc_tangent_edge_pair()
    

Return face tangent based on the two longest disconnected edges.

  * Tris: Use the edge pair with the most similar lengths.

  * Quads: Use the longest edge pair.

  * NGons: Use the two longest disconnected edges.


Returns:
    

a normalized vector.

Return type:
    

[`mathutils.Vector`](mathutils.md#mathutils.Vector "mathutils.Vector")

calc_tangent_vert_diagonal()
    

Return face tangent based on the two most distant vertices.

Returns:
    

a normalized vector.

Return type:
    

[`mathutils.Vector`](mathutils.md#mathutils.Vector "mathutils.Vector")

copy(_*_ , _verts =True_, _edges =True_)
    

Make a copy of this face.

Parameters:
    

  * **verts** (_bool_) – When set, the faces verts will be duplicated too.

  * **edges** (_bool_) – When set, the faces edges will be duplicated too.


Returns:
    

The newly created face.

Return type:
    

`bmesh.types.BMFace`

copy_from(_other_)
    

Copy values from another element of matching type.

copy_from_face_interp(_face_ , _vert =True_)
    

Interpolate the customdata from another face onto this one (faces should overlap).

Parameters:
    

  * **face** (`bmesh.types.BMFace`) – The face to interpolate data from.

  * **vert** (_bool_) – When True, also copy vertex data.


hide_set(_hide_)
    

Set the hide state. This is different from the _hide_ attribute because it updates the selection and hide state of associated geometry.

Parameters:
    

**hide** (_bool_) – Hidden or visible.

normal_flip()
    

Reverses winding of a face, which flips its normal.

normal_update()
    

Update face normal based on the positions of the face verts. This does not update the normals of face verts.

select_set(_select_)
    

Set the selection. This is different from the _select_ attribute because it updates the selection state of associated geometry.

Parameters:
    

**select** (_bool_) – Select or de-select.

Note

This only flushes down, so selecting a face will select all its vertices but de-selecting a vertex won’t de-select all the faces that use it, before finishing with a mesh typically flushing is still needed.

uv_select_set(_select_)
    

Select the face.

Parameters:
    

**select** (_bool_) – Select or de-select.

Note

Currently this only flushes down, so selecting a face will select all its vertices but de-selecting a vertex won’t de-select all the faces that use it, before finishing with a mesh typically flushing is still needed.

edges
    

Edges of this face, (read-only).

Type:
    

`bmesh.types.BMElemSeq` of `bmesh.types.BMEdge`

hide
    

Hidden state of this element.

Type:
    

bool

index
    

Index of this element.

Type:
    

int

Note

This value is not necessarily valid, while editing the mesh it can become _dirty_.

It’s also possible to assign any number to this attribute for a scripts internal logic.

To ensure the value is up to date - see `bmesh.types.BMElemSeq.index_update`.

is_valid
    

True when this element is valid (hasn’t been removed).

Type:
    

bool

loops
    

Loops of this face, (read-only).

Type:
    

`bmesh.types.BMElemSeq` of `bmesh.types.BMLoop`

material_index
    

The face’s material index.

Type:
    

int

normal
    

The normal for this face as a 3D, wrapped vector.

Type:
    

[`mathutils.Vector`](mathutils.md#mathutils.Vector "mathutils.Vector")

select
    

Selected state of this element.

Type:
    

bool

smooth
    

Smooth state of this element.

Type:
    

bool

tag
    

Generic attribute scripts can use for own logic

Type:
    

bool

uv_select
    

UV selected state of this element.

Type:
    

bool

verts
    

Verts of this face, (read-only).

Type:
    

`bmesh.types.BMElemSeq` of `bmesh.types.BMVert`

_class _bmesh.types.BMLoop
    

This is normally accessed from `bmesh.types.BMFace.loops` where each face loop represents a corner of the face.

calc_angle()
    

Return the angle at this loops corner of the face. This is calculated so sharper corners give lower angles.

Returns:
    

The angle in radians.

Return type:
    

float

calc_normal()
    

Return normal at this loops corner of the face. Falls back to the face normal for straight lines.

Returns:
    

a normalized vector.

Return type:
    

[`mathutils.Vector`](mathutils.md#mathutils.Vector "mathutils.Vector")

calc_tangent()
    

Return the tangent at this loops corner of the face (pointing inward into the face). Falls back to the face normal for straight lines.

Returns:
    

a normalized vector.

Return type:
    

[`mathutils.Vector`](mathutils.md#mathutils.Vector "mathutils.Vector")

copy_from(_other_)
    

Copy values from another element of matching type.

copy_from_face_interp(_face_ , _vert =True_, _multires =True_)
    

Interpolate the customdata from a face onto this loop (the loops vert should overlap the face).

Parameters:
    

  * **face** (`bmesh.types.BMFace`) – The face to interpolate data from.

  * **vert** (_bool_) – When enabled, interpolate the loops vertex data (optional).

  * **multires** (_bool_) – When enabled, interpolate the loops multires data (optional).


uv_select_edge_set(_select_)
    

Set the UV edge selection state.

Parameters:
    

**select** (_bool_) – Select or de-select.

Note

This only flushes down, so selecting an edge will select all its vertices but de-selecting a vertex won’t de-select the faces that use it, before finishing with a mesh typically flushing with `bmesh.types.BMesh.uv_select_flush_mode` is still needed.

uv_select_vert_set(_select_)
    

Select the UV vertex.

Parameters:
    

**select** (_bool_) – Select or de-select.

Note

Currently this only flushes down, so selecting an edge will select all its vertices but de-selecting a vertex won’t de-select the edges & faces that use it, before finishing with a mesh typically flushing with `bmesh.types.BMesh.uv_select_flush_mode` is still needed.

edge
    

The loop’s edge (between this loop and the next), (read-only).

Type:
    

`bmesh.types.BMEdge`

face
    

The face this loop makes (read-only).

Type:
    

`bmesh.types.BMFace`

index
    

Index of this element.

Type:
    

int

Note

This value is not necessarily valid, while editing the mesh it can become _dirty_.

It’s also possible to assign any number to this attribute for a scripts internal logic.

To ensure the value is up to date - see `bmesh.types.BMElemSeq.index_update`.

is_convex
    

True when this loop is at the convex corner of a face, depends on a valid face normal (read-only).

Type:
    

bool

is_valid
    

True when this element is valid (hasn’t been removed).

Type:
    

bool

link_loop_next
    

The next face corner (read-only).

Type:
    

`bmesh.types.BMLoop`

link_loop_prev
    

The previous face corner (read-only).

Type:
    

`bmesh.types.BMLoop`

link_loop_radial_next
    

The next loop around the edge (read-only).

Type:
    

`bmesh.types.BMLoop`

link_loop_radial_prev
    

The previous loop around the edge (read-only).

Type:
    

`bmesh.types.BMLoop`

link_loops
    

Loops connected to this loop, (read-only).

Type:
    

`bmesh.types.BMElemSeq` of `bmesh.types.BMLoop`

tag
    

Generic attribute scripts can use for own logic

Type:
    

bool

uv_select_edge
    

UV selected state of this element.

Type:
    

bool

uv_select_vert
    

UV selected state of this element.

Type:
    

bool

vert
    

The loop’s vertex (read-only).

Type:
    

`bmesh.types.BMVert`

## Sequence Accessors

_class _bmesh.types.BMElemSeq
    

General sequence type used for accessing any sequence of `bmesh.types.BMVert`, `bmesh.types.BMEdge`, `bmesh.types.BMFace`, `bmesh.types.BMLoop`.

When accessed via `bmesh.types.BMesh.verts`, `bmesh.types.BMesh.edges`, `bmesh.types.BMesh.faces` there are also functions to create/remove items.

index_update()
    

Initialize the index values of this sequence.

This is the equivalent of looping over all elements and assigning the index values.
    
    
    for index, ele in enumerate(sequence):
        ele.index = index
    

Note

Running this on sequences besides `bmesh.types.BMesh.verts`, `bmesh.types.BMesh.edges`, `bmesh.types.BMesh.faces` works but won’t result in each element having a valid index, instead its order in the sequence will be set.

_class _bmesh.types.BMVertSeq
    

ensure_lookup_table()
    

Ensure internal data needed for int subscription is initialized with verts/edges/faces, eg `bm.verts[index]`.

This needs to be called again after adding/removing data in this sequence.

index_update()
    

Initialize the index values of this sequence.

This is the equivalent of looping over all elements and assigning the index values.
    
    
    for index, ele in enumerate(sequence):
        ele.index = index
    

Note

Running this on sequences besides `bmesh.types.BMesh.verts`, `bmesh.types.BMesh.edges`, `bmesh.types.BMesh.faces` works but won’t result in each element having a valid index, instead its order in the sequence will be set.

new(_co =(0.0, 0.0, 0.0)_, _example =None_)
    

Create a new vertex.

Parameters:
    

  * **co** (_float triplet_) – The initial location of the vertex (optional argument).

  * **example** (`bmesh.types.BMVert`) – Existing vert to initialize settings.


Returns:
    

The newly created vertex.

Return type:
    

`bmesh.types.BMVert`

remove(_vert_)
    

Remove a vert.

sort(_*_ , _key =None_, _reverse =False_)
    

Sort the elements of this sequence, using an optional custom sort key. Indices of elements are not changed, `bmesh.types.BMElemSeq.index_update` can be used for that.

Parameters:
    

  * **key** (Callable[[`bmesh.types.BMVert` | `bmesh.types.BMEdge` | `bmesh.types.BMFace`], int] | None) – The key that sets the ordering of the elements.

  * **reverse** (_bool_) – Reverse the order of the elements


Note

When the ‘key’ argument is not provided, the elements are reordered following their current index value. In particular this can be used by setting indices manually before calling this method.

Warning

Existing references to the N’th element, will continue to point the data at that index.

layers
    

custom-data layers (read-only).

Type:
    

`bmesh.types.BMLayerAccessVert`

_class _bmesh.types.BMEdgeSeq
    

ensure_lookup_table()
    

Ensure internal data needed for int subscription is initialized with verts/edges/faces, eg `bm.verts[index]`.

This needs to be called again after adding/removing data in this sequence.

get(_verts_ , _fallback =None_)
    

Return an edge which uses the **verts** passed.

Parameters:
    

  * **verts** (Sequence[`bmesh.types.BMVert`]) – Sequence of verts.

  * **fallback** – Return this value if nothing is found.


Returns:
    

The edge found or None

Return type:
    

`bmesh.types.BMEdge`

index_update()
    

Initialize the index values of this sequence.

This is the equivalent of looping over all elements and assigning the index values.
    
    
    for index, ele in enumerate(sequence):
        ele.index = index
    

Note

Running this on sequences besides `bmesh.types.BMesh.verts`, `bmesh.types.BMesh.edges`, `bmesh.types.BMesh.faces` works but won’t result in each element having a valid index, instead its order in the sequence will be set.

new(_verts_ , _example =None_)
    

Create a new edge from a given pair of verts.

Parameters:
    

  * **verts** (Sequence[`bmesh.types.BMVert`]) – Vertex pair.

  * **example** (`bmesh.types.BMEdge`) – Existing edge to initialize settings (optional argument).


Returns:
    

The newly created edge.

Return type:
    

`bmesh.types.BMEdge`

remove(_edge_)
    

Remove an edge.

sort(_*_ , _key =None_, _reverse =False_)
    

Sort the elements of this sequence, using an optional custom sort key. Indices of elements are not changed, `bmesh.types.BMElemSeq.index_update` can be used for that.

Parameters:
    

  * **key** (Callable[[`bmesh.types.BMVert` | `bmesh.types.BMEdge` | `bmesh.types.BMFace`], int] | None) – The key that sets the ordering of the elements.

  * **reverse** (_bool_) – Reverse the order of the elements


Note

When the ‘key’ argument is not provided, the elements are reordered following their current index value. In particular this can be used by setting indices manually before calling this method.

Warning

Existing references to the N’th element, will continue to point the data at that index.

layers
    

custom-data layers (read-only).

Type:
    

`bmesh.types.BMLayerAccessEdge`

_class _bmesh.types.BMFaceSeq
    

ensure_lookup_table()
    

Ensure internal data needed for int subscription is initialized with verts/edges/faces, eg `bm.verts[index]`.

This needs to be called again after adding/removing data in this sequence.

get(_verts_ , _fallback =None_)
    

Return a face which uses the **verts** passed.

Parameters:
    

  * **verts** (Sequence[`bmesh.types.BMVert`]) – Sequence of verts.

  * **fallback** – Return this value if nothing is found.


Returns:
    

The face found or None

Return type:
    

`bmesh.types.BMFace`

index_update()
    

Initialize the index values of this sequence.

This is the equivalent of looping over all elements and assigning the index values.
    
    
    for index, ele in enumerate(sequence):
        ele.index = index
    

Note

Running this on sequences besides `bmesh.types.BMesh.verts`, `bmesh.types.BMesh.edges`, `bmesh.types.BMesh.faces` works but won’t result in each element having a valid index, instead its order in the sequence will be set.

new(_verts_ , _example =None_)
    

Create a new face from a given set of verts.

Parameters:
    

  * **verts** (Sequence[`bmesh.types.BMVert`]) – Sequence of 3 or more verts.

  * **example** (`bmesh.types.BMFace`) – Existing face to initialize settings (optional argument).


Returns:
    

The newly created face.

Return type:
    

`bmesh.types.BMFace`

remove(_face_)
    

Remove a face.

sort(_*_ , _key =None_, _reverse =False_)
    

Sort the elements of this sequence, using an optional custom sort key. Indices of elements are not changed, `bmesh.types.BMElemSeq.index_update` can be used for that.

Parameters:
    

  * **key** (Callable[[`bmesh.types.BMVert` | `bmesh.types.BMEdge` | `bmesh.types.BMFace`], int] | None) – The key that sets the ordering of the elements.

  * **reverse** (_bool_) – Reverse the order of the elements


Note

When the ‘key’ argument is not provided, the elements are reordered following their current index value. In particular this can be used by setting indices manually before calling this method.

Warning

Existing references to the N’th element, will continue to point the data at that index.

active
    

active face.

Type:
    

`bmesh.types.BMFace` | None

layers
    

custom-data layers (read-only).

Type:
    

`bmesh.types.BMLayerAccessFace`

_class _bmesh.types.BMLoopSeq
    

layers
    

custom-data layers (read-only).

Type:
    

`bmesh.types.BMLayerAccessLoop`

_class _bmesh.types.BMIter
    

Internal BMesh type for looping over verts/faces/edges, used for iterating over `bmesh.types.BMElemSeq` types.

## Selection History

_class _bmesh.types.BMEditSelSeq
    

add(_element_)
    

Add an element to the selection history (no action taken if its already added).

clear()
    

Empties the selection history.

discard(_element_)
    

Discard an element from the selection history.

Like remove but doesn’t raise an error when the elements not in the selection list.

remove(_element_)
    

Remove an element from the selection history.

validate()
    

Ensures all elements in the selection history are selected.

active
    

The last selected element or None (read-only).

Type:
    

`bmesh.types.BMVert`, `bmesh.types.BMEdge` or `bmesh.types.BMFace`

_class _bmesh.types.BMEditSelIter
    

## Custom-Data Layer Access

_class _bmesh.types.BMLayerAccessVert
    

Exposes custom-data layer attributes.

bool
    

Generic boolean custom-data layer.

Type:
    

`bmesh.types.BMLayerCollection` of boolean

color
    

Generic RGBA color with 8-bit precision custom-data layer.

Type:
    

`bmesh.types.BMLayerCollection` of [`mathutils.Vector`](mathutils.md#mathutils.Vector "mathutils.Vector")

deform
    

Vertex deform weight `bmesh.types.BMDeformVert` (TODO).

Type:
    

`bmesh.types.BMLayerCollection` of `bmesh.types.BMDeformVert`

float
    

Generic float custom-data layer.

Type:
    

`bmesh.types.BMLayerCollection` of float

float_color
    

Generic RGBA color with float precision custom-data layer.

Type:
    

`bmesh.types.BMLayerCollection` of [`mathutils.Vector`](mathutils.md#mathutils.Vector "mathutils.Vector")

float_vector
    

Generic 3D vector with float precision custom-data layer.

Type:
    

`bmesh.types.BMLayerCollection` of [`mathutils.Vector`](mathutils.md#mathutils.Vector "mathutils.Vector")

int
    

Generic int custom-data layer.

Type:
    

`bmesh.types.BMLayerCollection` of int

shape
    

Vertex shape-key absolute location (as a 3D Vector).

Type:
    

`bmesh.types.BMLayerCollection` of [`mathutils.Vector`](mathutils.md#mathutils.Vector "mathutils.Vector")

skin
    

Accessor for skin layer.

Type:
    

`bmesh.types.BMLayerCollection` of `bmesh.types.BMVertSkin`

string
    

Generic string custom-data layer (exposed as bytes, 255 max length).

Type:
    

`bmesh.types.BMLayerCollection` of bytes

_class _bmesh.types.BMLayerAccessEdge
    

Exposes custom-data layer attributes.

bool
    

Generic boolean custom-data layer.

Type:
    

`bmesh.types.BMLayerCollection` of boolean

color
    

Generic RGBA color with 8-bit precision custom-data layer.

Type:
    

`bmesh.types.BMLayerCollection` of [`mathutils.Vector`](mathutils.md#mathutils.Vector "mathutils.Vector")

float
    

Generic float custom-data layer.

Type:
    

`bmesh.types.BMLayerCollection` of float

float_color
    

Generic RGBA color with float precision custom-data layer.

Type:
    

`bmesh.types.BMLayerCollection` of [`mathutils.Vector`](mathutils.md#mathutils.Vector "mathutils.Vector")

float_vector
    

Generic 3D vector with float precision custom-data layer.

Type:
    

`bmesh.types.BMLayerCollection` of [`mathutils.Vector`](mathutils.md#mathutils.Vector "mathutils.Vector")

int
    

Generic int custom-data layer.

Type:
    

`bmesh.types.BMLayerCollection` of int

string
    

Generic string custom-data layer (exposed as bytes, 255 max length).

Type:
    

`bmesh.types.BMLayerCollection` of bytes

_class _bmesh.types.BMLayerAccessFace
    

Exposes custom-data layer attributes.

bool
    

Generic boolean custom-data layer.

Type:
    

`bmesh.types.BMLayerCollection` of boolean

color
    

Generic RGBA color with 8-bit precision custom-data layer.

Type:
    

`bmesh.types.BMLayerCollection` of [`mathutils.Vector`](mathutils.md#mathutils.Vector "mathutils.Vector")

float
    

Generic float custom-data layer.

Type:
    

`bmesh.types.BMLayerCollection` of float

float_color
    

Generic RGBA color with float precision custom-data layer.

Type:
    

`bmesh.types.BMLayerCollection` of [`mathutils.Vector`](mathutils.md#mathutils.Vector "mathutils.Vector")

float_vector
    

Generic 3D vector with float precision custom-data layer.

Type:
    

`bmesh.types.BMLayerCollection` of [`mathutils.Vector`](mathutils.md#mathutils.Vector "mathutils.Vector")

int
    

Generic int custom-data layer.

Type:
    

`bmesh.types.BMLayerCollection` of int

string
    

Generic string custom-data layer (exposed as bytes, 255 max length).

Type:
    

`bmesh.types.BMLayerCollection` of bytes

_class _bmesh.types.BMLayerAccessLoop
    

Exposes custom-data layer attributes.

bool
    

Generic boolean custom-data layer.

Type:
    

`bmesh.types.BMLayerCollection` of boolean

color
    

Generic RGBA color with 8-bit precision custom-data layer.

Type:
    

`bmesh.types.BMLayerCollection` of [`mathutils.Vector`](mathutils.md#mathutils.Vector "mathutils.Vector")

float
    

Generic float custom-data layer.

Type:
    

`bmesh.types.BMLayerCollection` of float

float_color
    

Generic RGBA color with float precision custom-data layer.

Type:
    

`bmesh.types.BMLayerCollection` of [`mathutils.Vector`](mathutils.md#mathutils.Vector "mathutils.Vector")

float_vector
    

Generic 3D vector with float precision custom-data layer.

Type:
    

`bmesh.types.BMLayerCollection` of [`mathutils.Vector`](mathutils.md#mathutils.Vector "mathutils.Vector")

int
    

Generic int custom-data layer.

Type:
    

`bmesh.types.BMLayerCollection` of int

string
    

Generic string custom-data layer (exposed as bytes, 255 max length).

Type:
    

`bmesh.types.BMLayerCollection` of bytes

uv
    

Accessor for `bmesh.types.BMLoopUV` UV (as a 2D Vector).

Type:
    

`bmesh.types.BMLayerCollection` of `bmesh.types.BMLoopUV`

_class _bmesh.types.BMLayerCollection
    

Gives access to a collection of custom-data layers of the same type and behaves like Python dictionaries, except for the ability to do list like index access.

get(_key_ , _default =None_)
    

Returns the value of the layer matching the key or default when not found (matches Python’s dictionary function of the same name).

Parameters:
    

  * **key** (_str_) – The key associated with the layer.

  * **default** (_Any_) – Optional argument for the value to return if _key_ is not found.


items()
    

Return the identifiers of collection members (matching Python’s dict.items() functionality).

Returns:
    

(key, value) pairs for each member of this collection.

Return type:
    

list[tuple[str, `bmesh.types.BMLayerItem`]]

keys()
    

Return the identifiers of collection members (matching Python’s dict.keys() functionality).

Returns:
    

the identifiers for each member of this collection.

Return type:
    

list[str]

new(_name_)
    

Create a new layer

Parameters:
    

**name** (_str_) – Optional name argument (will be made unique).

Returns:
    

The newly created layer.

Return type:
    

`bmesh.types.BMLayerItem`

remove(_layer_)
    

Remove a layer

Parameters:
    

**layer** (`bmesh.types.BMLayerItem`) – The layer to remove.

values()
    

Return the values of collection (matching Python’s dict.values() functionality).

Returns:
    

the members of this collection.

Return type:
    

list[`bmesh.types.BMLayerItem`]

verify()
    

Create a new layer or return an existing active layer

Returns:
    

The newly verified layer.

Return type:
    

`bmesh.types.BMLayerItem`

active
    

The active layer of this type (read-only).

Type:
    

`bmesh.types.BMLayerItem`

is_singleton
    

True if there can exists only one layer of this type (read-only).

Type:
    

bool

_class _bmesh.types.BMLayerItem
    

Exposes a single custom data layer, their main purpose is for use as item accessors to custom-data when used with vert/edge/face/loop data.

copy_from(_other_)
    

Return a copy of the layer

Parameters:
    

**other** (`bmesh.types.BMLayerItem`) – Another layer to copy from.

name
    

The layers unique name (read-only).

Type:
    

str

## Custom-Data Layer Types

_class _bmesh.types.BMLoopUV
    

pin_uv
    

UV pin state.

Type:
    

bool

uv
    

Loops UV (as a 2D Vector).

Type:
    

[`mathutils.Vector`](mathutils.md#mathutils.Vector "mathutils.Vector")

_class _bmesh.types.BMDeformVert
    

clear()
    

Clears all weights.

get(_key_ , _default =None_)
    

Returns the deform weight matching the key or default when not found (matches Python’s dictionary function of the same name).

Parameters:
    

  * **key** (_int_) – The key associated with deform weight.

  * **default** (_Any_) – Optional argument for the value to return if _key_ is not found.


items()
    

Return (group, weight) pairs for this vertex (matching Python’s dict.items() functionality).

Returns:
    

(key, value) pairs for each deform weight of this vertex.

Return type:
    

list[tuple[int, float]]

keys()
    

Return the group indices used by this vertex (matching Python’s dict.keys() functionality).

Returns:
    

the deform group this vertex uses

Return type:
    

list[int]

values()
    

Return the weights of the deform vertex (matching Python’s dict.values() functionality).

Returns:
    

The weights that influence this vertex

Return type:
    

list[float]
  *[*]: Keyword-only parameters separator (PEP 3102)
  *[/]: Positional-only parameter separator (PEP 570)
