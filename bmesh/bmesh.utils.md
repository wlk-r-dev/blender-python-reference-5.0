# BMesh Utilities (bmesh.utils)

This module provides access to blenders bmesh data structures.

bmesh.utils.edge_rotate(_edge_ , _ccw =False_)
    

Rotate the edge and return the newly created edge. If rotating the edge fails, None will be returned.

Parameters:
    

  * **edge** (`bmesh.types.BMEdge`) – The edge to rotate.

  * **ccw** (_bool_) – When True the edge will be rotated counter clockwise.


Returns:
    

The newly rotated edge.

Return type:
    

`bmesh.types.BMEdge`

bmesh.utils.edge_split(_edge_ , _vert_ , _fac_)
    

Split an edge, return the newly created data.

Parameters:
    

  * **edge** (`bmesh.types.BMEdge`) – The edge to split.

  * **vert** (`bmesh.types.BMVert`) – One of the verts on the edge, defines the split direction.

  * **fac** (_float_) – The point on the edge where the new vert will be created [0 - 1].


Returns:
    

The newly created (edge, vert) pair.

Return type:
    

tuple[`bmesh.types.BMEdge`, `bmesh.types.BMVert`]

bmesh.utils.face_flip(_faces_)
    

Flip the faces direction.

Parameters:
    

**face** (`bmesh.types.BMFace`) – Face to flip.

bmesh.utils.face_join(_faces_ , _remove =True_)
    

Joins a sequence of faces.

Parameters:
    

  * **faces** (`bmesh.types.BMFace`) – Sequence of faces.

  * **remove** (_bool_) – Remove the edges and vertices between the faces.


Returns:
    

The newly created face or None on failure.

Return type:
    

`bmesh.types.BMFace`

bmesh.utils.face_split(_face_ , _vert_a_ , _vert_b_ , _*_ , _coords =()_, _use_exist =True_, _example =None_)
    

Face split with optional intermediate points.

Parameters:
    

  * **face** (`bmesh.types.BMFace`) – The face to cut.

  * **vert_a** (`bmesh.types.BMVert`) – First vertex to cut in the face (face must contain the vert).

  * **vert_b** (`bmesh.types.BMVert`) – Second vertex to cut in the face (face must contain the vert).

  * **coords** (_Sequence_ _[__Sequence_ _[__float_ _]__]_) – Optional sequence of 3D points in between _vert_a_ and _vert_b_.

  * **use_exist** (_bool_) – .Use an existing edge if it exists (Only used when _coords_ argument is empty or omitted)

  * **example** (`bmesh.types.BMEdge`) – Newly created edge will copy settings from this one.


Returns:
    

The newly created face or None on failure.

Return type:
    

tuple[`bmesh.types.BMFace`, `bmesh.types.BMLoop`]

bmesh.utils.face_split_edgenet(_face_ , _edgenet_)
    

Splits a face into any number of regions defined by an edgenet.

Parameters:
    

  * **face** (`bmesh.types.BMFace`) – The face to split.

  * **face** – The face to split.

  * **edgenet** (Sequence[`bmesh.types.BMEdge`]) – Sequence of edges.


Returns:
    

The newly created faces.

Return type:
    

tuple[`bmesh.types.BMFace`, …]

Note

Regions defined by edges need to connect to the face, otherwise they’re ignored as loose edges.

bmesh.utils.face_vert_separate(_face_ , _vert_)
    

Rip a vertex in a face away and add a new vertex.

Parameters:
    

  * **face** (`bmesh.types.BMFace`) – The face to separate.

  * **vert** (`bmesh.types.BMVert`) – A vertex in the face to separate.


Return vert:
    

The newly created vertex or None on failure.

Rtype vert:
    

`bmesh.types.BMVert`

Note

This is the same as loop_separate, and has only been added for convenience.

bmesh.utils.loop_separate(_loop_)
    

Rip a vertex in a face away and add a new vertex.

Parameters:
    

**loop** (`bmesh.types.BMLoop`) – The loop to separate.

Return vert:
    

The newly created vertex or None on failure.

Rtype vert:
    

`bmesh.types.BMVert`

bmesh.utils.uv_select_check(_bm_ , _/_ , _*_ , _sync =True_, _flush =False_, _contiguous =False_)
    

Split an edge, return the newly created data.

Parameters:
    

  * **sync** (_bool_) – Check the data is properly synchronized between UV’s and the underlying mesh. Failure to synchronize with the mesh selection may cause tools not to behave properly.

  * **flush** (_bool_) – Check the selection has been properly flushed between elements (based on the current `BMesh.select_mode`).

  * **contiguous** (_bool_) – Check connected UV’s and edges have a matching selection state.


Returns:
    

An error dictionary or None when there are no errors found.

Return type:
    

dict[str, int] | None

bmesh.utils.vert_collapse_edge(_vert_ , _edge_)
    

Collapse a vertex into an edge.

Parameters:
    

  * **vert** (`bmesh.types.BMVert`) – The vert that will be collapsed.

  * **edge** (`bmesh.types.BMEdge`) – The edge to collapse into.


Returns:
    

The resulting edge from the collapse operation.

Return type:
    

`bmesh.types.BMEdge`

bmesh.utils.vert_collapse_faces(_vert_ , _edge_ , _fac_ , _join_faces_)
    

Collapses a vertex that has only two manifold edges onto a vertex it shares an edge with.

Parameters:
    

  * **vert** (`bmesh.types.BMVert`) – The vert that will be collapsed.

  * **edge** (`bmesh.types.BMEdge`) – The edge to collapse into.

  * **fac** (_float_) – The factor to use when merging customdata [0 - 1].

  * **join_faces** (_bool_) – When true the faces around the vertex will be joined otherwise collapse the vertex by merging the 2 edges this vertex connects to into one.


Returns:
    

The resulting edge from the collapse operation.

Return type:
    

`bmesh.types.BMEdge`

bmesh.utils.vert_dissolve(_vert_)
    

Dissolve this vertex (will be removed).

Parameters:
    

**vert** (`bmesh.types.BMVert`) – The vert to be dissolved.

Returns:
    

True when the vertex dissolve is successful.

Return type:
    

bool

bmesh.utils.vert_separate(_vert_ , _edges_)
    

Separate this vertex at every edge.

Parameters:
    

  * **vert** (`bmesh.types.BMVert`) – The vert to be separated.

  * **edges** (`bmesh.types.BMEdge`) – The edges to separated.


Returns:
    

The newly separated verts (including the vertex passed).

Return type:
    

tuple[`bmesh.types.BMVert`, …]

bmesh.utils.vert_splice(_vert_ , _vert_target_)
    

Splice vert into vert_target.

Parameters:
    

  * **vert** (`bmesh.types.BMVert`) – The vertex to be removed.

  * **vert_target** (`bmesh.types.BMVert`) – The vertex to use.


Note

The verts mustn’t share an edge or face.
  *[*]: Keyword-only parameters separator (PEP 3102)
  *[/]: Positional-only parameter separator (PEP 570)
