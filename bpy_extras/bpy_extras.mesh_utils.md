# bpy_extras submodule (bpy_extras.mesh_utils)

bpy_extras.mesh_utils.mesh_linked_uv_islands(_mesh_)
    

Returns lists of polygon indices connected by UV islands.

Parameters:
    

**mesh** ([[bpy.types.Mesh]]) – the mesh used to group with.

Returns:
    

list of lists containing polygon indices

Return type:
    

list[list[int]]

bpy_extras.mesh_utils.mesh_linked_triangles(_mesh_)
    

Splits the mesh into connected triangles, use this for separating cubes from other mesh elements within 1 mesh data-block.

Parameters:
    

**mesh** ([[bpy.types.Mesh]]) – the mesh used to group with.

Returns:
    

Lists of lists containing triangles.

Return type:
    

list[list[[[bpy.types.MeshLoopTriangle]]]]

bpy_extras.mesh_utils.edge_face_count_dict(_mesh_)
    

Returns:
    

Dictionary of edge keys with their value set to the number of faces using each edge.

Return type:
    

dict[tuple[int, int], int]

bpy_extras.mesh_utils.edge_face_count(_mesh_)
    

Returns:
    

list face users for each item in mesh.edges.

Return type:
    

list[int]

bpy_extras.mesh_utils.edge_loops_from_edges(_mesh_ , _edges =None_)
    

Edge loops defined by edges

Takes me.edges or a list of edges and returns the edge loops

return a list of vertex indices. [ [1, 6, 7, 2], …]

closed loops have matching start and end values.

bpy_extras.mesh_utils.ngon_tessellate(_from_data_ , _indices_ , _fix_loops =True_, _debug_print =True_)
    

Takes a poly-line of indices (ngon) and returns a list of face index lists. Designed to be used for importers that need indices for an ngon to create from existing verts.

Parameters:
    

  * **from_data** ([[bpy.types.Mesh]] | list[Sequence[float]] | tuple[Sequence[float]]) – Either a mesh, or a list/tuple of 3D vectors.

  * **indices** (_list_ _[__int_ _]_) – a list of indices to use this list is the ordered closed poly-line to fill, and can be a subset of the data given.

  * **fix_loops** (_bool_) – If this is enabled poly-lines that use loops to make multiple poly-lines are dealt with correctly.


bpy_extras.mesh_utils.triangle_random_points(_num_points_ , _loop_triangles_)
    

Generates a list of random points over mesh loop triangles.

Parameters:
    

  * **num_points** (_int_) – The number of random points to generate on each triangle.

  * **loop_triangles** (Sequence[[[bpy.types.MeshLoopTriangle]]]) – Sequence of the triangles to generate points on.


Returns:
    

List of random points over all triangles.

Return type:
    

list[[[mathutils.Vector]]]
