# BMesh Operators (bmesh.ops)

This module gives access to low level bmesh operations.

Most operators take input and return output, they can be chained together to perform useful operations.

## Operator Example

This script shows how operators can be used to model a link of a chain.
    
    
    # This script uses bmesh operators to make 2 links of a chain.
    
    import bpy
    import bmesh
    import math
    import mathutils
    
    # Make a new BMesh
    bm = bmesh.new()
    
    # Add a circle XXX, should return all geometry created, not just verts.
    bmesh.ops.create_circle(
        bm,
        cap_ends=False,
        radius=0.2,
        segments=8)
    
    
    # Spin and deal with geometry on side 'a'
    edges_start_a = bm.edges[:]
    geom_start_a = bm.verts[:] + edges_start_a
    ret = bmesh.ops.spin(
        bm,
        geom=geom_start_a,
        angle=math.radians(180.0),
        steps=8,
        axis=(1.0, 0.0, 0.0),
        cent=(0.0, 1.0, 0.0))
    edges_end_a = [ele for ele in ret["geom_last"]
                   if isinstance(ele, bmesh.types.BMEdge)]
    del ret
    
    
    # Extrude and create geometry on side 'b'
    ret = bmesh.ops.extrude_edge_only(
        bm,
        edges=edges_start_a)
    geom_extrude_mid = ret["geom"]
    del ret
    
    
    # Collect the edges to spin XXX, 'extrude_edge_only' could return this.
    verts_extrude_b = [ele for ele in geom_extrude_mid
                       if isinstance(ele, bmesh.types.BMVert)]
    edges_extrude_b = [ele for ele in geom_extrude_mid
                       if isinstance(ele, bmesh.types.BMEdge) and ele.is_boundary]
    bmesh.ops.translate(
        bm,
        verts=verts_extrude_b,
        vec=(0.0, 0.0, 1.0))
    
    
    # Create the circle on side 'b'
    ret = bmesh.ops.spin(
        bm,
        geom=verts_extrude_b + edges_extrude_b,
        angle=-math.radians(180.0),
        steps=8,
        axis=(1.0, 0.0, 0.0),
        cent=(0.0, 1.0, 1.0))
    edges_end_b = [ele for ele in ret["geom_last"]
                   if isinstance(ele, bmesh.types.BMEdge)]
    del ret
    
    
    # Bridge the resulting edge loops of both spins 'a & b'
    bmesh.ops.bridge_loops(
        bm,
        edges=edges_end_a + edges_end_b)
    
    
    # Now we have made a links of the chain, make a copy and rotate it
    # (so this looks something like a chain)
    
    ret = bmesh.ops.duplicate(
        bm,
        geom=bm.verts[:] + bm.edges[:] + bm.faces[:])
    geom_dupe = ret["geom"]
    verts_dupe = [ele for ele in geom_dupe if isinstance(ele, bmesh.types.BMVert)]
    del ret
    
    # position the new link
    bmesh.ops.translate(
        bm,
        verts=verts_dupe,
        vec=(0.0, 0.0, 2.0))
    bmesh.ops.rotate(
        bm,
        verts=verts_dupe,
        cent=(0.0, 1.0, 0.0),
        matrix=mathutils.Matrix.Rotation(math.radians(90.0), 3, 'Z'))
    
    # Done with creating the mesh, simply link it into the scene so we can see it
    
    # Finish up, write the bmesh into a new mesh
    me = bpy.data.meshes.new("Mesh")
    bm.to_mesh(me)
    bm.free()
    
    
    # Add the mesh to the scene
    obj = bpy.data.objects.new("Object", me)
    bpy.context.collection.objects.link(obj)
    
    # Select and make active
    bpy.context.view_layer.objects.active = obj
    obj.select_set(True)
    

bmesh.ops.smooth_vert(_bm_ , _verts =[]_, _factor =0_, _mirror_clip_x =False_, _mirror_clip_y =False_, _mirror_clip_z =False_, _clip_dist =0_, _use_axis_x =False_, _use_axis_y =False_, _use_axis_z =False_)
    

Vertex Smooth.

Smooths vertices by using a basic vertex averaging scheme.

Parameters:
    

  * **bm** (`bmesh.types.BMesh`) – The bmesh to operate on.

  * **verts** (list of (`bmesh.types.BMVert`)) – Input vertices.

  * **factor** (_float_) – Smoothing factor.

  * **mirror_clip_x** (_bool_) – Set vertices close to the x axis before the operation to 0.

  * **mirror_clip_y** (_bool_) – Set vertices close to the y axis before the operation to 0.

  * **mirror_clip_z** (_bool_) – Set vertices close to the z axis before the operation to 0.

  * **clip_dist** (_float_) – Clipping threshold for the above three slots.

  * **use_axis_x** (_bool_) – Smooth vertices along X axis.

  * **use_axis_y** (_bool_) – Smooth vertices along Y axis.

  * **use_axis_z** (_bool_) – Smooth vertices along Z axis.


bmesh.ops.smooth_laplacian_vert(_bm_ , _verts =[]_, _lambda_factor =0_, _lambda_border =0_, _use_x =False_, _use_y =False_, _use_z =False_, _preserve_volume =False_)
    

Vertex Smooth Laplacian.

Smooths vertices by using Laplacian smoothing propose by. Desbrun, et al. Implicit Fairing of Irregular Meshes using Diffusion and Curvature Flow.

Parameters:
    

  * **bm** (`bmesh.types.BMesh`) – The bmesh to operate on.

  * **verts** (list of (`bmesh.types.BMVert`)) – Input vertices.

  * **lambda_factor** (_float_) – Lambda parameter.

  * **lambda_border** (_float_) – Lambda param in border.

  * **use_x** (_bool_) – Smooth object along X axis.

  * **use_y** (_bool_) – Smooth object along Y axis.

  * **use_z** (_bool_) – Smooth object along Z axis.

  * **preserve_volume** (_bool_) – Apply volume preservation after smooth.


bmesh.ops.recalc_face_normals(_bm_ , _faces =[]_)
    

Right-Hand Faces.

Computes an “outside” normal for the specified input faces.

Parameters:
    

  * **bm** (`bmesh.types.BMesh`) – The bmesh to operate on.

  * **faces** (list of (`bmesh.types.BMFace`)) – Input faces.


bmesh.ops.planar_faces(_bm_ , _faces =[]_, _iterations =0_, _factor =0_)
    

Planar Faces.

Iteratively flatten faces.

Parameters:
    

  * **bm** (`bmesh.types.BMesh`) – The bmesh to operate on.

  * **faces** (list of (`bmesh.types.BMFace`)) – Input geometry.

  * **iterations** (_int_) – Number of times to flatten faces (for when connected faces are used)

  * **factor** (_float_) – Influence for making planar each iteration


Returns:
    

  * `geom`: Output slot, computed boundary geometry.

**type** list of (`bmesh.types.BMVert`, `bmesh.types.BMEdge`, `bmesh.types.BMFace`)


Return type:
    

dict[str, Any]

bmesh.ops.region_extend(_bm_ , _geom =[]_, _use_contract =False_, _use_faces =False_, _use_face_step =False_)
    

Region Extend.

used to implement the select more/less tools. this puts some geometry surrounding regions of geometry in geom into geom.out.

if use_faces is 0 then geom.out spits out verts and edges, otherwise it spits out faces.

Parameters:
    

  * **bm** (`bmesh.types.BMesh`) – The bmesh to operate on.

  * **geom** (list of (`bmesh.types.BMVert`, `bmesh.types.BMEdge`, `bmesh.types.BMFace`)) – Input geometry.

  * **use_contract** (_bool_) – Find boundary inside the regions, not outside.

  * **use_faces** (_bool_) – Extend from faces instead of edges.

  * **use_face_step** (_bool_) – Step over connected faces.


Returns:
    

  * `geom`: Output slot, computed boundary geometry.

**type** list of (`bmesh.types.BMVert`, `bmesh.types.BMEdge`, `bmesh.types.BMFace`)


Return type:
    

dict[str, Any]

bmesh.ops.rotate_edges(_bm_ , _edges =[]_, _use_ccw =False_)
    

Edge Rotate.

Rotates edges topologically. Also known as “spin edge” to some people. Simple example: `[/] becomes [|] then [\]`.

Parameters:
    

  * **bm** (`bmesh.types.BMesh`) – The bmesh to operate on.

  * **edges** (list of (`bmesh.types.BMEdge`)) – Input edges.

  * **use_ccw** (_bool_) – Rotate edge counter-clockwise if true, otherwise clockwise.


Returns:
    

  * `edges`: Newly spun edges.

**type** list of (`bmesh.types.BMEdge`)


Return type:
    

dict[str, Any]

bmesh.ops.reverse_faces(_bm_ , _faces =[]_, _flip_multires =False_)
    

Reverse Faces.

Reverses the winding (vertex order) of faces. This has the effect of flipping the normal.

Parameters:
    

  * **bm** (`bmesh.types.BMesh`) – The bmesh to operate on.

  * **faces** (list of (`bmesh.types.BMFace`)) – Input faces.

  * **flip_multires** (_bool_) – Maintain multi-res offset.


bmesh.ops.flip_quad_tessellation(_bm_ , _faces =[]_)
    

Flip Quad Tessellation

Flip the tessellation direction of the selected quads.

Parameters:
    

  * **bm** (`bmesh.types.BMesh`) – The bmesh to operate on.

  * **faces** (list of (`bmesh.types.BMFace`)) – Input faces.


bmesh.ops.bisect_edges(_bm_ , _edges =[]_, _cuts =0_, _edge_percents ={}_)
    

Edge Bisect.

Splits input edges (but doesn’t do anything else). This creates a 2-valence vert.

Parameters:
    

  * **bm** (`bmesh.types.BMesh`) – The bmesh to operate on.

  * **edges** (list of (`bmesh.types.BMEdge`)) – Input edges.

  * **cuts** (_int_) – Number of cuts.

  * **edge_percents** (_dict mapping vert/edge/face types to float_) – Undocumented.


Returns:
    

  * `geom_split`: Newly created vertices and edges.

**type** list of (`bmesh.types.BMVert`, `bmesh.types.BMEdge`, `bmesh.types.BMFace`)


Return type:
    

dict[str, Any]

bmesh.ops.mirror(_bm_ , _geom =[]_, _matrix =mathutils.Matrix.Identity(4)_, _merge_dist =0_, _axis ='X'_, _mirror_u =False_, _mirror_v =False_, _mirror_udim =False_, _use_shapekey =False_)
    

Mirror.

Mirrors geometry along an axis. The resulting geometry is welded on using merge_dist. Pairs of original/mirrored vertices are welded using the merge_dist parameter (which defines the minimum distance for welding to happen).

Parameters:
    

  * **bm** (`bmesh.types.BMesh`) – The bmesh to operate on.

  * **geom** (list of (`bmesh.types.BMVert`, `bmesh.types.BMEdge`, `bmesh.types.BMFace`)) – Input geometry.

  * **matrix** ([`mathutils.Matrix`](mathutils.md#mathutils.Matrix "mathutils.Matrix")) – Matrix defining the mirror transformation.

  * **merge_dist** (_float_) – Maximum distance for merging. does no merging if 0.

  * **axis** (_enum in_ _[__'X'__,__'Y'__,__'Z'__]__,__default 'X'_) – The axis to use.

  * **mirror_u** (_bool_) – Mirror UVs across the u axis.

  * **mirror_v** (_bool_) – Mirror UVs across the v axis.

  * **mirror_udim** (_bool_) – Mirror UVs in each tile.

  * **use_shapekey** (_bool_) – Transform shape keys too.


Returns:
    

  * `geom`: Output geometry, mirrored.

**type** list of (`bmesh.types.BMVert`, `bmesh.types.BMEdge`, `bmesh.types.BMFace`)


Return type:
    

dict[str, Any]

bmesh.ops.find_doubles(_bm_ , _verts =[]_, _keep_verts =[]_, _use_connected =False_, _dist =0_)
    

Find Doubles.

Takes input verts and find vertices they should weld to. Outputs a mapping slot suitable for use with the weld verts BMOP.

If keep_verts is used, vertices outside that set can only be merged with vertices in that set.

Parameters:
    

  * **bm** (`bmesh.types.BMesh`) – The bmesh to operate on.

  * **verts** (list of (`bmesh.types.BMVert`)) – Input vertices.

  * **keep_verts** (list of (`bmesh.types.BMVert`)) – List of verts to keep.

  * **use_connected** (_bool_) – Limit the search for doubles by connected geometry.

  * **dist** (_float_) – Maximum distance.


Returns:
    

  * `targetmap`:

**type** dict mapping vert/edge/face types to `bmesh.types.BMVert`/`bmesh.types.BMEdge`/`bmesh.types.BMFace`


Return type:
    

dict[str, Any]

bmesh.ops.remove_doubles(_bm_ , _verts =[]_, _use_connected =False_, _dist =0_)
    

Remove Doubles.

Finds groups of vertices closer than dist and merges them together, using the weld verts BMOP.

Parameters:
    

  * **bm** (`bmesh.types.BMesh`) – The bmesh to operate on.

  * **verts** (list of (`bmesh.types.BMVert`)) – Input verts.

  * **use_connected** (_bool_) – Limit the search for doubles by connected geometry.

  * **dist** (_float_) – Minimum distance.


bmesh.ops.collapse(_bm_ , _edges =[]_, _uvs =False_)
    

Collapse Connected.

Collapses connected vertices

Parameters:
    

  * **bm** (`bmesh.types.BMesh`) – The bmesh to operate on.

  * **edges** (list of (`bmesh.types.BMEdge`)) – Input edges.

  * **uvs** (_bool_) – Also collapse UVs and such.


bmesh.ops.pointmerge_facedata(_bm_ , _verts=[]_ , _vert_snap_)
    

Face-Data Point Merge.

Merge uv/vcols at a specific vertex.

Parameters:
    

  * **bm** (`bmesh.types.BMesh`) – The bmesh to operate on.

  * **verts** (list of (`bmesh.types.BMVert`)) – Input vertices.

  * **vert_snap** (`bmesh.types.BMVert`) – Snap vertex.


bmesh.ops.average_vert_facedata(_bm_ , _verts =[]_)
    

Average Vertices Face-vert Data.

Merge uv/vcols associated with the input vertices at the bounding box center. (I know, it’s not averaging but the vert_snap_to_bb_center is just too long).

Parameters:
    

  * **bm** (`bmesh.types.BMesh`) – The bmesh to operate on.

  * **verts** (list of (`bmesh.types.BMVert`)) – Input vertices.


bmesh.ops.pointmerge(_bm_ , _verts =[]_, _merge_co =mathutils.Vector()_)
    

Point Merge.

Merge verts together at a point.

Parameters:
    

  * **bm** (`bmesh.types.BMesh`) – The bmesh to operate on.

  * **verts** (list of (`bmesh.types.BMVert`)) – Input vertices (all verts will be merged into the first).

  * **merge_co** ([`mathutils.Vector`](mathutils.md#mathutils.Vector "mathutils.Vector") or any sequence of 3 floats) – Position to merge at.


bmesh.ops.collapse_uvs(_bm_ , _edges =[]_)
    

Collapse Connected UVs.

Collapses connected UV vertices.

Parameters:
    

  * **bm** (`bmesh.types.BMesh`) – The bmesh to operate on.

  * **edges** (list of (`bmesh.types.BMEdge`)) – Input edges.


bmesh.ops.weld_verts(_bm_ , _targetmap ={}_, _use_centroid =False_)
    

Weld Verts.

Welds verts together (kind-of like remove doubles, merge, etc, all of which use or will use this BMOP). You pass in mappings from vertices to the vertices they weld with.

Parameters:
    

  * **bm** (`bmesh.types.BMesh`) – The bmesh to operate on.

  * **targetmap** (dict mapping vert/edge/face types to `bmesh.types.BMVert`/`bmesh.types.BMEdge`/`bmesh.types.BMFace`) – Maps welded vertices to verts they should weld to.

  * **use_centroid** (_bool_) – Merged vertices to their centroid position, otherwise the position of the target vertex is used.


bmesh.ops.create_vert(_bm_ , _co =mathutils.Vector()_)
    

Make Vertex.

Creates a single vertex; this BMOP was necessary for click-create-vertex.

Parameters:
    

  * **bm** (`bmesh.types.BMesh`) – The bmesh to operate on.

  * **co** ([`mathutils.Vector`](mathutils.md#mathutils.Vector "mathutils.Vector") or any sequence of 3 floats) – The coordinate of the new vert.


Returns:
    

  * `vert`: The new vert.

**type** list of (`bmesh.types.BMVert`)


Return type:
    

dict[str, Any]

bmesh.ops.join_triangles(_bm_ , _faces =[]_, _cmp_seam =False_, _cmp_sharp =False_, _cmp_uvs =False_, _cmp_vcols =False_, _cmp_materials =False_, _angle_face_threshold =0_, _angle_shape_threshold =0_, _topology_influence =0_, _deselect_joined =False_, _merge_limit =0_, _neighbor_debug =0_)
    

Join Triangles.

Tries to intelligently join triangles according to angle threshold and delimiters.

Parameters:
    

  * **bm** (`bmesh.types.BMesh`) – The bmesh to operate on.

  * **faces** (list of (`bmesh.types.BMFace`)) – Input geometry.

  * **cmp_seam** (_bool_) – Compare seam

  * **cmp_sharp** (_bool_) – Compare sharp

  * **cmp_uvs** (_bool_) – Compare UVs

  * **cmp_vcols** (_bool_) – Compare VCols.

  * **cmp_materials** (_bool_) – Compare materials.

  * **angle_face_threshold** (_float_) – Undocumented.

  * **angle_shape_threshold** (_float_) – Undocumented.

  * **topology_influence** (_float_) – Undocumented.

  * **deselect_joined** (_bool_) – Undocumented.

  * **merge_limit** (_int_) – Undocumented.

  * **neighbor_debug** (_int_) – Undocumented.


Returns:
    

  * `faces`: Joined faces.

**type** list of (`bmesh.types.BMFace`)


Return type:
    

dict[str, Any]

bmesh.ops.contextual_create(_bm_ , _geom =[]_, _mat_nr =0_, _use_smooth =False_)
    

Contextual Create.

This is basically F-key, it creates new faces from vertices, makes stuff from edge nets, makes wire edges, etc. It also dissolves faces.

Three verts become a triangle, four become a quad. Two become a wire edge.

Parameters:
    

  * **bm** (`bmesh.types.BMesh`) – The bmesh to operate on.

  * **geom** (list of (`bmesh.types.BMVert`, `bmesh.types.BMEdge`, `bmesh.types.BMFace`)) – Input geometry.

  * **mat_nr** (_int_) – Material to use.

  * **use_smooth** (_bool_) – Smooth to use.


Returns:
    

  * `faces`: Newly-made face(s).

**type** list of (`bmesh.types.BMFace`)

  * `edges`: Newly-made edge(s).

**type** list of (`bmesh.types.BMEdge`)


Return type:
    

dict[str, Any]

bmesh.ops.bridge_loops(_bm_ , _edges =[]_, _use_pairs =False_, _use_cyclic =False_, _use_merge =False_, _merge_factor =0_, _twist_offset =0_)
    

Bridge edge loops with faces.

Parameters:
    

  * **bm** (`bmesh.types.BMesh`) – The bmesh to operate on.

  * **edges** (list of (`bmesh.types.BMEdge`)) – Input edges.

  * **use_pairs** (_bool_) – Undocumented.

  * **use_cyclic** (_bool_) – Undocumented.

  * **use_merge** (_bool_) – Merge rather than creating faces.

  * **merge_factor** (_float_) – Merge factor.

  * **twist_offset** (_int_) – Twist offset for closed loops.


Returns:
    

  * `faces`: New faces.

**type** list of (`bmesh.types.BMFace`)

  * `edges`: New edges.

**type** list of (`bmesh.types.BMEdge`)


Return type:
    

dict[str, Any]

bmesh.ops.grid_fill(_bm_ , _edges =[]_, _mat_nr =0_, _use_smooth =False_, _use_interp_simple =False_)
    

Grid Fill.

Create faces defined by 2 disconnected edge loops (which share edges).

Parameters:
    

  * **bm** (`bmesh.types.BMesh`) – The bmesh to operate on.

  * **edges** (list of (`bmesh.types.BMEdge`)) – Input edges.

  * **mat_nr** (_int_) – Material to use.

  * **use_smooth** (_bool_) – Smooth state to use.

  * **use_interp_simple** (_bool_) – Use simple interpolation.


Returns:
    

  * `faces`: New faces.

**type** list of (`bmesh.types.BMFace`)


Return type:
    

dict[str, Any]

bmesh.ops.holes_fill(_bm_ , _edges =[]_, _sides =0_)
    

Fill Holes.

Fill boundary edges with faces, copying surrounding custom-data.

Parameters:
    

  * **bm** (`bmesh.types.BMesh`) – The bmesh to operate on.

  * **edges** (list of (`bmesh.types.BMEdge`)) – Input edges.

  * **sides** (_int_) – Number of face sides to fill.


Returns:
    

  * `faces`: New faces.

**type** list of (`bmesh.types.BMFace`)


Return type:
    

dict[str, Any]

bmesh.ops.face_attribute_fill(_bm_ , _faces =[]_, _use_normals =False_, _use_data =False_)
    

Face Attribute Fill.

Fill in faces with data from adjacent faces.

Parameters:
    

  * **bm** (`bmesh.types.BMesh`) – The bmesh to operate on.

  * **faces** (list of (`bmesh.types.BMFace`)) – Input faces.

  * **use_normals** (_bool_) – Copy face winding.

  * **use_data** (_bool_) – Copy face data.


Returns:
    

  * `faces_fail`: Faces that could not be handled.

**type** list of (`bmesh.types.BMFace`)


Return type:
    

dict[str, Any]

bmesh.ops.edgeloop_fill(_bm_ , _edges =[]_, _mat_nr =0_, _use_smooth =False_)
    

Edge Loop Fill.

Create faces defined by one or more non overlapping edge loops.

Parameters:
    

  * **bm** (`bmesh.types.BMesh`) – The bmesh to operate on.

  * **edges** (list of (`bmesh.types.BMEdge`)) – Input edges.

  * **mat_nr** (_int_) – Material to use.

  * **use_smooth** (_bool_) – Smooth state to use.


Returns:
    

  * `faces`: New faces.

**type** list of (`bmesh.types.BMFace`)


Return type:
    

dict[str, Any]

bmesh.ops.edgenet_fill(_bm_ , _edges =[]_, _mat_nr =0_, _use_smooth =False_, _sides =0_)
    

Edge Net Fill.

Create faces defined by enclosed edges.

Parameters:
    

  * **bm** (`bmesh.types.BMesh`) – The bmesh to operate on.

  * **edges** (list of (`bmesh.types.BMEdge`)) – Input edges.

  * **mat_nr** (_int_) – Material to use.

  * **use_smooth** (_bool_) – Smooth state to use.

  * **sides** (_int_) – Number of sides.


Returns:
    

  * `faces`: New faces.

**type** list of (`bmesh.types.BMFace`)


Return type:
    

dict[str, Any]

bmesh.ops.edgenet_prepare(_bm_ , _edges =[]_)
    

Edge-net Prepare.

Identifies several useful edge loop cases and modifies them so they’ll become a face when edgenet_fill is called. The cases covered are:

  * One single loop; an edge is added to connect the ends

  * Two loops; two edges are added to connect the endpoints (based on the shortest distance between each endpoint).


Parameters:
    

  * **bm** (`bmesh.types.BMesh`) – The bmesh to operate on.

  * **edges** (list of (`bmesh.types.BMEdge`)) – Input edges.


Returns:
    

  * `edges`: New edges.

**type** list of (`bmesh.types.BMEdge`)


Return type:
    

dict[str, Any]

bmesh.ops.rotate(_bm_ , _cent =mathutils.Vector()_, _matrix =mathutils.Matrix.Identity(4)_, _verts =[]_, _space =mathutils.Matrix.Identity(4)_, _use_shapekey =False_)
    

Rotate.

Rotate vertices around a center, using a 3x3 rotation matrix.

Parameters:
    

  * **bm** (`bmesh.types.BMesh`) – The bmesh to operate on.

  * **cent** ([`mathutils.Vector`](mathutils.md#mathutils.Vector "mathutils.Vector") or any sequence of 3 floats) – Center of rotation.

  * **matrix** ([`mathutils.Matrix`](mathutils.md#mathutils.Matrix "mathutils.Matrix")) – Matrix defining rotation.

  * **verts** (list of (`bmesh.types.BMVert`)) – Input vertices.

  * **space** ([`mathutils.Matrix`](mathutils.md#mathutils.Matrix "mathutils.Matrix")) – Matrix to define the space (typically object matrix).

  * **use_shapekey** (_bool_) – Transform shape keys too.


bmesh.ops.translate(_bm_ , _vec =mathutils.Vector()_, _space =mathutils.Matrix.Identity(4)_, _verts =[]_, _use_shapekey =False_)
    

Translate.

Translate vertices by an offset.

Parameters:
    

  * **bm** (`bmesh.types.BMesh`) – The bmesh to operate on.

  * **vec** ([`mathutils.Vector`](mathutils.md#mathutils.Vector "mathutils.Vector") or any sequence of 3 floats) – Translation offset.

  * **space** ([`mathutils.Matrix`](mathutils.md#mathutils.Matrix "mathutils.Matrix")) – Matrix to define the space (typically object matrix).

  * **verts** (list of (`bmesh.types.BMVert`)) – Input vertices.

  * **use_shapekey** (_bool_) – Transform shape keys too.


bmesh.ops.scale(_bm_ , _vec =mathutils.Vector()_, _space =mathutils.Matrix.Identity(4)_, _verts =[]_, _use_shapekey =False_)
    

Scale.

Scales vertices by an offset.

Parameters:
    

  * **bm** (`bmesh.types.BMesh`) – The bmesh to operate on.

  * **vec** ([`mathutils.Vector`](mathutils.md#mathutils.Vector "mathutils.Vector") or any sequence of 3 floats) – Scale factor.

  * **space** ([`mathutils.Matrix`](mathutils.md#mathutils.Matrix "mathutils.Matrix")) – Matrix to define the space (typically object matrix).

  * **verts** (list of (`bmesh.types.BMVert`)) – Input vertices.

  * **use_shapekey** (_bool_) – Transform shape keys too.


bmesh.ops.transform(_bm_ , _matrix =mathutils.Matrix.Identity(4)_, _space =mathutils.Matrix.Identity(4)_, _verts =[]_, _use_shapekey =False_)
    

Transform.

Transforms a set of vertices by a matrix. Multiplies the vertex coordinates with the matrix.

Parameters:
    

  * **bm** (`bmesh.types.BMesh`) – The bmesh to operate on.

  * **matrix** ([`mathutils.Matrix`](mathutils.md#mathutils.Matrix "mathutils.Matrix")) – Transform matrix.

  * **space** ([`mathutils.Matrix`](mathutils.md#mathutils.Matrix "mathutils.Matrix")) – Matrix to define the space (typically object matrix).

  * **verts** (list of (`bmesh.types.BMVert`)) – Input vertices.

  * **use_shapekey** (_bool_) – Transform shape keys too.


bmesh.ops.object_load_bmesh(_bm_ , _scene_ , _object_)
    

Object Load BMesh.

Loads a bmesh into an object/mesh. This is a “private” BMOP.

Parameters:
    

  * **bm** (`bmesh.types.BMesh`) – The bmesh to operate on.

  * **scene** ([`bpy.types.Scene`](../bpy.types/S/bpy.types.Scene.md#bpy.types.Scene "bpy.types.Scene")) – Pointer to an scene structure.

  * **object** ([`bpy.types.Object`](../bpy.types/O/bpy.types.Object.md#bpy.types.Object "bpy.types.Object")) – Pointer to an object structure.


bmesh.ops.bmesh_to_mesh(_bm_ , _mesh_ , _object_)
    

BMesh to Mesh.

Converts a bmesh to a Mesh. This is reserved for exiting edit-mode.

Parameters:
    

  * **bm** (`bmesh.types.BMesh`) – The bmesh to operate on.

  * **mesh** ([`bpy.types.Mesh`](../bpy.types/M/bpy.types.Mesh.md#bpy.types.Mesh "bpy.types.Mesh")) – Pointer to a mesh structure to fill in.

  * **object** ([`bpy.types.Object`](../bpy.types/O/bpy.types.Object.md#bpy.types.Object "bpy.types.Object")) – Pointer to an object structure.


bmesh.ops.mesh_to_bmesh(_bm_ , _mesh_ , _object_ , _use_shapekey =False_)
    

Mesh to BMesh.

Load the contents of a mesh into the bmesh. this BMOP is private, it’s reserved exclusively for entering edit-mode.

Parameters:
    

  * **bm** (`bmesh.types.BMesh`) – The bmesh to operate on.

  * **mesh** ([`bpy.types.Mesh`](../bpy.types/M/bpy.types.Mesh.md#bpy.types.Mesh "bpy.types.Mesh")) – Pointer to a Mesh structure.

  * **object** ([`bpy.types.Object`](../bpy.types/O/bpy.types.Object.md#bpy.types.Object "bpy.types.Object")) – Pointer to an Object structure.

  * **use_shapekey** (_bool_) – Load active shapekey coordinates into verts.


bmesh.ops.extrude_discrete_faces(_bm_ , _faces =[]_, _use_normal_flip =False_, _use_select_history =False_)
    

Individual Face Extrude.

Extrudes faces individually.

Parameters:
    

  * **bm** (`bmesh.types.BMesh`) – The bmesh to operate on.

  * **faces** (list of (`bmesh.types.BMFace`)) – Input faces.

  * **use_normal_flip** (_bool_) – Create faces with reversed direction.

  * **use_select_history** (_bool_) – Pass to duplicate.


Returns:
    

  * `faces`: Output faces.

**type** list of (`bmesh.types.BMFace`)


Return type:
    

dict[str, Any]

bmesh.ops.extrude_edge_only(_bm_ , _edges =[]_, _use_normal_flip =False_, _use_select_history =False_)
    

Extrude Only Edges.

Extrudes Edges into faces, note that this is very simple, there’s no fancy winged extrusion.

Parameters:
    

  * **bm** (`bmesh.types.BMesh`) – The bmesh to operate on.

  * **edges** (list of (`bmesh.types.BMEdge`)) – Input vertices.

  * **use_normal_flip** (_bool_) – Create faces with reversed direction.

  * **use_select_history** (_bool_) – Pass to duplicate.


Returns:
    

  * `geom`: Output geometry.

**type** list of (`bmesh.types.BMVert`, `bmesh.types.BMEdge`, `bmesh.types.BMFace`)


Return type:
    

dict[str, Any]

bmesh.ops.extrude_vert_indiv(_bm_ , _verts =[]_, _use_select_history =False_)
    

Individual Vertex Extrude.

Extrudes wire edges from vertices.

Parameters:
    

  * **bm** (`bmesh.types.BMesh`) – The bmesh to operate on.

  * **verts** (list of (`bmesh.types.BMVert`)) – Input vertices.

  * **use_select_history** (_bool_) – Pass to duplicate.


Returns:
    

  * `edges`: Output wire edges.

**type** list of (`bmesh.types.BMEdge`)

  * `verts`: Output vertices.

**type** list of (`bmesh.types.BMVert`)


Return type:
    

dict[str, Any]

bmesh.ops.connect_verts(_bm_ , _verts =[]_, _faces_exclude =[]_, _check_degenerate =False_)
    

Connect Verts.

Split faces by adding edges that connect **verts**.

Parameters:
    

  * **bm** (`bmesh.types.BMesh`) – The bmesh to operate on.

  * **verts** (list of (`bmesh.types.BMVert`)) – Input vertices.

  * **faces_exclude** (list of (`bmesh.types.BMFace`)) – Input faces to explicitly exclude from connecting.

  * **check_degenerate** (_bool_) – Prevent splits with overlaps & intersections.


Returns:
    

  * `edges`:

**type** list of (`bmesh.types.BMEdge`)


Return type:
    

dict[str, Any]

bmesh.ops.connect_verts_concave(_bm_ , _faces =[]_)
    

Connect Verts to form Convex Faces.

Ensures all faces are convex **faces**.

Parameters:
    

  * **bm** (`bmesh.types.BMesh`) – The bmesh to operate on.

  * **faces** (list of (`bmesh.types.BMFace`)) – Input faces.


Returns:
    

  * `edges`:

**type** list of (`bmesh.types.BMEdge`)

  * `faces`:

**type** list of (`bmesh.types.BMFace`)


Return type:
    

dict[str, Any]

bmesh.ops.connect_verts_nonplanar(_bm_ , _angle_limit =0_, _faces =[]_)
    

Connect Verts Across non Planer Faces.

Split faces by connecting edges along non planer **faces**.

Parameters:
    

  * **bm** (`bmesh.types.BMesh`) – The bmesh to operate on.

  * **angle_limit** (_float_) – Total rotation angle (radians).

  * **faces** (list of (`bmesh.types.BMFace`)) – Input faces.


Returns:
    

  * `edges`:

**type** list of (`bmesh.types.BMEdge`)

  * `faces`:

**type** list of (`bmesh.types.BMFace`)


Return type:
    

dict[str, Any]

bmesh.ops.connect_vert_pair(_bm_ , _verts =[]_, _verts_exclude =[]_, _faces_exclude =[]_)
    

Connect Verts.

Split faces by adding edges that connect **verts**.

Parameters:
    

  * **bm** (`bmesh.types.BMesh`) – The bmesh to operate on.

  * **verts** (list of (`bmesh.types.BMVert`)) – Input vertices.

  * **verts_exclude** (list of (`bmesh.types.BMVert`)) – Input vertices to explicitly exclude from connecting.

  * **faces_exclude** (list of (`bmesh.types.BMFace`)) – Input faces to explicitly exclude from connecting.


Returns:
    

  * `edges`:

**type** list of (`bmesh.types.BMEdge`)


Return type:
    

dict[str, Any]

bmesh.ops.extrude_face_region(_bm_ , _geom =[]_, _edges_exclude =set()_, _use_keep_orig =False_, _use_normal_flip =False_, _use_normal_from_adjacent =False_, _use_dissolve_ortho_edges =False_, _use_select_history =False_, _skip_input_flip =False_)
    

Extrude Faces.

Extrude operator (does not transform)

Parameters:
    

  * **bm** (`bmesh.types.BMesh`) – The bmesh to operate on.

  * **geom** (list of (`bmesh.types.BMVert`, `bmesh.types.BMEdge`, `bmesh.types.BMFace`)) – Edges and faces.

  * **edges_exclude** (_set_ _of_ _vert/edge/face type_) – Input edges to explicitly exclude from extrusion.

  * **use_keep_orig** (_bool_) – Keep original geometry (requires `geom` to include edges).

  * **use_normal_flip** (_bool_) – Create faces with reversed direction.

  * **use_normal_from_adjacent** (_bool_) – Use winding from surrounding faces instead of this region.

  * **use_dissolve_ortho_edges** (_bool_) – Dissolve edges whose faces form a flat surface.

  * **use_select_history** (_bool_) – Pass to duplicate.

  * **skip_input_flip** (_bool_) – Skip flipping of input faces to preserve original orientation.


Returns:
    

  * `geom`:

**type** list of (`bmesh.types.BMVert`, `bmesh.types.BMEdge`, `bmesh.types.BMFace`)


Return type:
    

dict[str, Any]

bmesh.ops.dissolve_verts(_bm_ , _verts =[]_, _use_face_split =False_, _use_boundary_tear =False_)
    

Dissolve Verts.

Parameters:
    

  * **bm** (`bmesh.types.BMesh`) – The bmesh to operate on.

  * **verts** (list of (`bmesh.types.BMVert`)) – Input vertices.

  * **use_face_split** (_bool_) – Split off face corners to maintain surrounding geometry.

  * **use_boundary_tear** (_bool_) – Split off face corners instead of merging faces.


bmesh.ops.dissolve_edges(_bm_ , _edges =[]_, _use_verts =False_, _use_face_split =False_, _angle_threshold =0_)
    

Dissolve Edges.

Parameters:
    

  * **bm** (`bmesh.types.BMesh`) – The bmesh to operate on.

  * **edges** (list of (`bmesh.types.BMEdge`)) – Input edges.

  * **use_verts** (_bool_) – Dissolve verts left between only 2 edges.

  * **use_face_split** (_bool_) – Split off face corners to maintain surrounding geometry.

  * **angle_threshold** (_float_) – Do not dissolve verts between 2 edges when their angle exceeds this threshold. Disabled by default.


Returns:
    

  * `region`:

**type** list of (`bmesh.types.BMFace`)


Return type:
    

dict[str, Any]

bmesh.ops.dissolve_faces(_bm_ , _faces =[]_, _use_verts =False_)
    

Dissolve Faces.

Parameters:
    

  * **bm** (`bmesh.types.BMesh`) – The bmesh to operate on.

  * **faces** (list of (`bmesh.types.BMFace`)) – Input faces.

  * **use_verts** (_bool_) – Dissolve verts left between only 2 edges.


Returns:
    

  * `region`:

**type** list of (`bmesh.types.BMFace`)


Return type:
    

dict[str, Any]

bmesh.ops.dissolve_limit(_bm_ , _angle_limit =0_, _use_dissolve_boundaries =False_, _verts =[]_, _edges =[]_, _delimit =set()_)
    

Limited Dissolve.

Dissolve planar faces and co-linear edges.

Parameters:
    

  * **bm** (`bmesh.types.BMesh`) – The bmesh to operate on.

  * **angle_limit** (_float_) – Total rotation angle (radians).

  * **use_dissolve_boundaries** (_bool_) – Dissolve all vertices in between face boundaries.

  * **verts** (list of (`bmesh.types.BMVert`)) – Input vertices.

  * **edges** (list of (`bmesh.types.BMEdge`)) – Input edges.

  * **delimit** (_set_ _of_ _flags from_ _[__'NORMAL'__,__'MATERIAL'__,__'SEAM'__,__'SHARP'__,__'UV'__]__,__default set_ _(__)_) – Delimit dissolve operation.


Returns:
    

  * `region`:

**type** list of (`bmesh.types.BMFace`)


Return type:
    

dict[str, Any]

bmesh.ops.dissolve_degenerate(_bm_ , _dist =0_, _edges =[]_)
    

Degenerate Dissolve.

Dissolve edges with no length, faces with no area.

Parameters:
    

  * **bm** (`bmesh.types.BMesh`) – The bmesh to operate on.

  * **dist** (_float_) – Maximum distance to consider degenerate.

  * **edges** (list of (`bmesh.types.BMEdge`)) – Input edges.


bmesh.ops.triangulate(_bm_ , _faces =[]_, _quad_method ='BEAUTY'_, _ngon_method ='BEAUTY'_)
    

Triangulate.

Parameters:
    

  * **bm** (`bmesh.types.BMesh`) – The bmesh to operate on.

  * **faces** (list of (`bmesh.types.BMFace`)) – Input faces.

  * **quad_method** (_enum in_ _[__'BEAUTY'__,__'FIXED'__,__'ALTERNATE'__,__'SHORT_EDGE'__,__'LONG_EDGE'__]__,__default 'BEAUTY'_) – Method for splitting the quads into triangles.

  * **ngon_method** (_enum in_ _[__'BEAUTY'__,__'EAR_CLIP'__]__,__default 'BEAUTY'_) – Method for splitting the polygons into triangles.


Returns:
    

  * `edges`:

**type** list of (`bmesh.types.BMEdge`)

  * `faces`:

**type** list of (`bmesh.types.BMFace`)

  * `face_map`:

**type** dict mapping vert/edge/face types to `bmesh.types.BMVert`/`bmesh.types.BMEdge`/`bmesh.types.BMFace`

  * `face_map_double`: Duplicate faces.

**type** dict mapping vert/edge/face types to `bmesh.types.BMVert`/`bmesh.types.BMEdge`/`bmesh.types.BMFace`


Return type:
    

dict[str, Any]

bmesh.ops.unsubdivide(_bm_ , _verts =[]_, _iterations =0_)
    

Un-Subdivide.

Reduce detail in geometry containing grids.

Parameters:
    

  * **bm** (`bmesh.types.BMesh`) – The bmesh to operate on.

  * **verts** (list of (`bmesh.types.BMVert`)) – Input vertices.

  * **iterations** (_int_) – Number of times to unsubdivide.


bmesh.ops.subdivide_edges(_bm_ , _edges =[]_, _smooth =0_, _smooth_falloff ='SMOOTH'_, _fractal =0_, _along_normal =0_, _cuts =0_, _seed =0_, _custom_patterns ={}_, _edge_percents ={}_, _quad_corner_type ='STRAIGHT_CUT'_, _use_grid_fill =False_, _use_single_edge =False_, _use_only_quads =False_, _use_sphere =False_, _use_smooth_even =False_)
    

Subdivide Edges.

Advanced operator for subdividing edges with options for face patterns, smoothing and randomization.

Parameters:
    

  * **bm** (`bmesh.types.BMesh`) – The bmesh to operate on.

  * **edges** (list of (`bmesh.types.BMEdge`)) – Input edges.

  * **smooth** (_float_) – Smoothness factor.

  * **smooth_falloff** (_enum in_ _[__'SMOOTH'__,__'SPHERE'__,__'ROOT'__,__'SHARP'__,__'LINEAR'__,__'INVERSE_SQUARE'__]__,__default 'SMOOTH'_) – Smooth falloff type.

  * **fractal** (_float_) – Fractal randomness factor.

  * **along_normal** (_float_) – Apply fractal displacement along normal only.

  * **cuts** (_int_) – Number of cuts.

  * **seed** (_int_) – Seed for the random number generator.

  * **custom_patterns** (_dict mapping vert/edge/face types to unknown internal data_ _,__not compatible with Python_) – Uses custom pointers.

  * **edge_percents** (_dict mapping vert/edge/face types to float_) – Undocumented.

  * **quad_corner_type** (_enum in_ _[__'STRAIGHT_CUT'__,__'INNER_VERT'__,__'PATH'__,__'FAN'__]__,__default 'STRAIGHT_CUT'_) – Quad corner type.

  * **use_grid_fill** (_bool_) – Fill in fully-selected faces with a grid.

  * **use_single_edge** (_bool_) – Tessellate the case of one edge selected in a quad or triangle.

  * **use_only_quads** (_bool_) – Only subdivide quads (for loop-cut).

  * **use_sphere** (_bool_) – For making new primitives only.

  * **use_smooth_even** (_bool_) – Maintain even offset when smoothing.


Returns:
    

  * `geom_inner`:

**type** list of (`bmesh.types.BMVert`, `bmesh.types.BMEdge`, `bmesh.types.BMFace`)

  * `geom_split`:

**type** list of (`bmesh.types.BMVert`, `bmesh.types.BMEdge`, `bmesh.types.BMFace`)

  * `geom`: Contains all output geometry.

**type** list of (`bmesh.types.BMVert`, `bmesh.types.BMEdge`, `bmesh.types.BMFace`)


Return type:
    

dict[str, Any]

bmesh.ops.subdivide_edgering(_bm_ , _edges =[]_, _interp_mode ='LINEAR'_, _smooth =0_, _cuts =0_, _profile_shape ='SMOOTH'_, _profile_shape_factor =0_)
    

Subdivide Edge-Ring.

Take an edge-ring, and subdivide with interpolation options.

Parameters:
    

  * **bm** (`bmesh.types.BMesh`) – The bmesh to operate on.

  * **edges** (list of (`bmesh.types.BMEdge`)) – Input vertices.

  * **interp_mode** (_enum in_ _[__'LINEAR'__,__'PATH'__,__'SURFACE'__]__,__default 'LINEAR'_) – Interpolation method.

  * **smooth** (_float_) – Smoothness factor.

  * **cuts** (_int_) – Number of cuts.

  * **profile_shape** (_enum in_ _[__'SMOOTH'__,__'SPHERE'__,__'ROOT'__,__'SHARP'__,__'LINEAR'__,__'INVERSE_SQUARE'__]__,__default 'SMOOTH'_) – Profile shape type.

  * **profile_shape_factor** (_float_) – How much intermediary new edges are shrunk/expanded.


Returns:
    

  * `faces`: Output faces.

**type** list of (`bmesh.types.BMFace`)


Return type:
    

dict[str, Any]

bmesh.ops.bisect_plane(_bm_ , _geom =[]_, _dist =0_, _plane_co =mathutils.Vector()_, _plane_no =mathutils.Vector()_, _use_snap_center =False_, _clear_outer =False_, _clear_inner =False_)
    

Bisect Plane.

Bisects the mesh by a plane (cut the mesh in half).

Parameters:
    

  * **bm** (`bmesh.types.BMesh`) – The bmesh to operate on.

  * **geom** (list of (`bmesh.types.BMVert`, `bmesh.types.BMEdge`, `bmesh.types.BMFace`)) – Input geometry.

  * **dist** (_float_) – Minimum distance when testing if a vert is exactly on the plane.

  * **plane_co** ([`mathutils.Vector`](mathutils.md#mathutils.Vector "mathutils.Vector") or any sequence of 3 floats) – Point on the plane.

  * **plane_no** ([`mathutils.Vector`](mathutils.md#mathutils.Vector "mathutils.Vector") or any sequence of 3 floats) – Direction of the plane.

  * **use_snap_center** (_bool_) – Snap axis aligned verts to the center.

  * **clear_outer** (_bool_) – When enabled. remove all geometry on the positive side of the plane.

  * **clear_inner** (_bool_) – When enabled. remove all geometry on the negative side of the plane.


Returns:
    

  * `geom_cut`: Output geometry aligned with the plane (new and existing).

**type** list of (`bmesh.types.BMVert`, `bmesh.types.BMEdge`)

  * `geom`: Input and output geometry (result of cut).

**type** list of (`bmesh.types.BMVert`, `bmesh.types.BMEdge`, `bmesh.types.BMFace`)


Return type:
    

dict[str, Any]

bmesh.ops.delete(_bm_ , _geom =[]_, _context ='VERTS'_)
    

Delete Geometry.

Utility operator to delete geometry.

Parameters:
    

  * **bm** (`bmesh.types.BMesh`) – The bmesh to operate on.

  * **geom** (list of (`bmesh.types.BMVert`, `bmesh.types.BMEdge`, `bmesh.types.BMFace`)) – Input geometry.

  * **context** (_enum in_ _[__'VERTS'__,__'EDGES'__,__'FACES_ONLY'__,__'EDGES_FACES'__,__'FACES'__,__'FACES_KEEP_BOUNDARY'__,__'TAGGED_ONLY'__]__,__default 'VERTS'_) – Geometry types to delete.


bmesh.ops.duplicate(_bm_ , _geom =[]_, _dest =None_, _use_select_history =False_, _use_edge_flip_from_face =False_)
    

Duplicate Geometry.

Utility operator to duplicate geometry, optionally into a destination mesh.

Parameters:
    

  * **bm** (`bmesh.types.BMesh`) – The bmesh to operate on.

  * **geom** (list of (`bmesh.types.BMVert`, `bmesh.types.BMEdge`, `bmesh.types.BMFace`)) – Input geometry.

  * **dest** (`bmesh.types.BMesh`) – Destination bmesh, if None will use current on.

  * **use_select_history** (_bool_) – Undocumented.

  * **use_edge_flip_from_face** (_bool_) – Undocumented.


Returns:
    

  * `geom_orig`:

**type** list of (`bmesh.types.BMVert`, `bmesh.types.BMEdge`, `bmesh.types.BMFace`)

  * `geom`:

**type** list of (`bmesh.types.BMVert`, `bmesh.types.BMEdge`, `bmesh.types.BMFace`)

  * `vert_map`:

**type** dict mapping vert/edge/face types to `bmesh.types.BMVert`/`bmesh.types.BMEdge`/`bmesh.types.BMFace`

  * `edge_map`:

**type** dict mapping vert/edge/face types to `bmesh.types.BMVert`/`bmesh.types.BMEdge`/`bmesh.types.BMFace`

  * `face_map`:

**type** dict mapping vert/edge/face types to `bmesh.types.BMVert`/`bmesh.types.BMEdge`/`bmesh.types.BMFace`

  * `boundary_map`: Boundary edges from the split geometry that maps edges from the original geometry to the destination edges.

**type** dict mapping vert/edge/face types to `bmesh.types.BMVert`/`bmesh.types.BMEdge`/`bmesh.types.BMFace`

  * `isovert_map`:

**type** dict mapping vert/edge/face types to `bmesh.types.BMVert`/`bmesh.types.BMEdge`/`bmesh.types.BMFace`


Return type:
    

dict[str, Any]

bmesh.ops.split(_bm_ , _geom =[]_, _dest =None_, _use_only_faces =False_)
    

Split Off Geometry.

Disconnect geometry from adjacent edges and faces, optionally into a destination mesh.

Parameters:
    

  * **bm** (`bmesh.types.BMesh`) – The bmesh to operate on.

  * **geom** (list of (`bmesh.types.BMVert`, `bmesh.types.BMEdge`, `bmesh.types.BMFace`)) – Input geometry.

  * **dest** (`bmesh.types.BMesh`) – Destination bmesh, if None will use current one.

  * **use_only_faces** (_bool_) – When enabled. don’t duplicate loose verts/edges.


Returns:
    

  * `geom`:

**type** list of (`bmesh.types.BMVert`, `bmesh.types.BMEdge`, `bmesh.types.BMFace`)

  * `boundary_map`: Boundary edges from the split geometry that maps edges from the original geometry to the destination edges.

When the source edges have been deleted, the destination edge will be used for both the key and the value.

**type** dict mapping vert/edge/face types to `bmesh.types.BMVert`/`bmesh.types.BMEdge`/`bmesh.types.BMFace`

  * `isovert_map`:

**type** dict mapping vert/edge/face types to `bmesh.types.BMVert`/`bmesh.types.BMEdge`/`bmesh.types.BMFace`


Return type:
    

dict[str, Any]

bmesh.ops.spin(_bm_ , _geom =[]_, _cent =mathutils.Vector()_, _axis =mathutils.Vector()_, _dvec =mathutils.Vector()_, _angle =0_, _space =mathutils.Matrix.Identity(4)_, _steps =0_, _use_merge =False_, _use_normal_flip =False_, _use_duplicate =False_)
    

Spin.

Extrude or duplicate geometry a number of times, rotating and possibly translating after each step

Parameters:
    

  * **bm** (`bmesh.types.BMesh`) – The bmesh to operate on.

  * **geom** (list of (`bmesh.types.BMVert`, `bmesh.types.BMEdge`, `bmesh.types.BMFace`)) – Input geometry.

  * **cent** ([`mathutils.Vector`](mathutils.md#mathutils.Vector "mathutils.Vector") or any sequence of 3 floats) – Rotation center.

  * **axis** ([`mathutils.Vector`](mathutils.md#mathutils.Vector "mathutils.Vector") or any sequence of 3 floats) – Rotation axis.

  * **dvec** ([`mathutils.Vector`](mathutils.md#mathutils.Vector "mathutils.Vector") or any sequence of 3 floats) – Translation delta per step.

  * **angle** (_float_) – Total rotation angle (radians).

  * **space** ([`mathutils.Matrix`](mathutils.md#mathutils.Matrix "mathutils.Matrix")) – Matrix to define the space (typically object matrix).

  * **steps** (_int_) – Number of steps.

  * **use_merge** (_bool_) – Merge first/last when the angle is a full revolution.

  * **use_normal_flip** (_bool_) – Create faces with reversed direction.

  * **use_duplicate** (_bool_) – Duplicate or extrude?.


Returns:
    

  * `geom_last`: Result of last step.

**type** list of (`bmesh.types.BMVert`, `bmesh.types.BMEdge`, `bmesh.types.BMFace`)


Return type:
    

dict[str, Any]

bmesh.ops.rotate_uvs(_bm_ , _faces =[]_, _use_ccw =False_)
    

UV Rotation.

Cycle the loop UVs

Parameters:
    

  * **bm** (`bmesh.types.BMesh`) – The bmesh to operate on.

  * **faces** (list of (`bmesh.types.BMFace`)) – Input faces.

  * **use_ccw** (_bool_) – Rotate counter-clockwise if true, otherwise clockwise.


bmesh.ops.reverse_uvs(_bm_ , _faces =[]_)
    

UV Reverse.

Reverse the UVs

Parameters:
    

  * **bm** (`bmesh.types.BMesh`) – The bmesh to operate on.

  * **faces** (list of (`bmesh.types.BMFace`)) – Input faces.


bmesh.ops.rotate_colors(_bm_ , _faces =[]_, _use_ccw =False_, _color_index =0_)
    

Color Rotation.

Cycle the loop colors

Parameters:
    

  * **bm** (`bmesh.types.BMesh`) – The bmesh to operate on.

  * **faces** (list of (`bmesh.types.BMFace`)) – Input faces.

  * **use_ccw** (_bool_) – Rotate counter-clockwise if true, otherwise clockwise.

  * **color_index** (_int_) – Index into color attribute list.


bmesh.ops.reverse_colors(_bm_ , _faces =[]_, _color_index =0_)
    

Color Reverse

Reverse the loop colors.

Parameters:
    

  * **bm** (`bmesh.types.BMesh`) – The bmesh to operate on.

  * **faces** (list of (`bmesh.types.BMFace`)) – Input faces.

  * **color_index** (_int_) – Index into color attribute list.


bmesh.ops.split_edges(_bm_ , _edges =[]_, _verts =[]_, _use_verts =False_)
    

Edge Split.

Disconnects faces along input edges.

Parameters:
    

  * **bm** (`bmesh.types.BMesh`) – The bmesh to operate on.

  * **edges** (list of (`bmesh.types.BMEdge`)) – Input edges.

  * **verts** (list of (`bmesh.types.BMVert`)) – Optional tag verts, use to have greater control of splits.

  * **use_verts** (_bool_) – Use ‘verts’ for splitting, else just find verts to split from edges.


Returns:
    

  * `edges`: Old output disconnected edges.

**type** list of (`bmesh.types.BMEdge`)


Return type:
    

dict[str, Any]

bmesh.ops.create_grid(_bm_ , _x_segments =0_, _y_segments =0_, _size =0_, _matrix =mathutils.Matrix.Identity(4)_, _calc_uvs =False_)
    

Create Grid.

Creates a grid with a variable number of subdivisions

Parameters:
    

  * **bm** (`bmesh.types.BMesh`) – The bmesh to operate on.

  * **x_segments** (_int_) – Number of x segments.

  * **y_segments** (_int_) – Number of y segments.

  * **size** (_float_) – Size of the grid.

  * **matrix** ([`mathutils.Matrix`](mathutils.md#mathutils.Matrix "mathutils.Matrix")) – Matrix to multiply the new geometry with.

  * **calc_uvs** (_bool_) – Calculate default UVs.


Returns:
    

  * `verts`: Output verts.

**type** list of (`bmesh.types.BMVert`)


Return type:
    

dict[str, Any]

bmesh.ops.create_uvsphere(_bm_ , _u_segments =0_, _v_segments =0_, _radius =0_, _matrix =mathutils.Matrix.Identity(4)_, _calc_uvs =False_)
    

Create UV Sphere.

Creates a grid with a variable number of subdivisions

Parameters:
    

  * **bm** (`bmesh.types.BMesh`) – The bmesh to operate on.

  * **u_segments** (_int_) – Number of u segments.

  * **v_segments** (_int_) – Number of v segment.

  * **radius** (_float_) – Radius.

  * **matrix** ([`mathutils.Matrix`](mathutils.md#mathutils.Matrix "mathutils.Matrix")) – Matrix to multiply the new geometry with.

  * **calc_uvs** (_bool_) – Calculate default UVs.


Returns:
    

  * `verts`: Output verts.

**type** list of (`bmesh.types.BMVert`)


Return type:
    

dict[str, Any]

bmesh.ops.create_icosphere(_bm_ , _subdivisions =0_, _radius =0_, _matrix =mathutils.Matrix.Identity(4)_, _calc_uvs =False_)
    

Create Ico-Sphere.

Creates a grid with a variable number of subdivisions

Parameters:
    

  * **bm** (`bmesh.types.BMesh`) – The bmesh to operate on.

  * **subdivisions** (_int_) – How many times to recursively subdivide the sphere.

  * **radius** (_float_) – Radius.

  * **matrix** ([`mathutils.Matrix`](mathutils.md#mathutils.Matrix "mathutils.Matrix")) – Matrix to multiply the new geometry with.

  * **calc_uvs** (_bool_) – Calculate default UVs.


Returns:
    

  * `verts`: Output verts.

**type** list of (`bmesh.types.BMVert`)


Return type:
    

dict[str, Any]

bmesh.ops.create_monkey(_bm_ , _matrix =mathutils.Matrix.Identity(4)_, _calc_uvs =False_)
    

Create Suzanne.

Creates a monkey (standard blender primitive).

Parameters:
    

  * **bm** (`bmesh.types.BMesh`) – The bmesh to operate on.

  * **matrix** ([`mathutils.Matrix`](mathutils.md#mathutils.Matrix "mathutils.Matrix")) – Matrix to multiply the new geometry with.

  * **calc_uvs** (_bool_) – Calculate default UVs.


Returns:
    

  * `verts`: Output verts.

**type** list of (`bmesh.types.BMVert`)


Return type:
    

dict[str, Any]

bmesh.ops.create_cone(_bm_ , _cap_ends =False_, _cap_tris =False_, _segments =0_, _radius1 =0_, _radius2 =0_, _depth =0_, _matrix =mathutils.Matrix.Identity(4)_, _calc_uvs =False_)
    

Create Cone.

Creates a cone with variable depth at both ends

Parameters:
    

  * **bm** (`bmesh.types.BMesh`) – The bmesh to operate on.

  * **cap_ends** (_bool_) – Whether or not to fill in the ends with faces.

  * **cap_tris** (_bool_) – Fill ends with triangles instead of ngons.

  * **segments** (_int_) – Number of vertices in the base circle.

  * **radius1** (_float_) – Radius of one end.

  * **radius2** (_float_) – Radius of the opposite.

  * **depth** (_float_) – Distance between ends.

  * **matrix** ([`mathutils.Matrix`](mathutils.md#mathutils.Matrix "mathutils.Matrix")) – Matrix to multiply the new geometry with.

  * **calc_uvs** (_bool_) – Calculate default UVs.


Returns:
    

  * `verts`: Output verts.

**type** list of (`bmesh.types.BMVert`)


Return type:
    

dict[str, Any]

bmesh.ops.create_circle(_bm_ , _cap_ends =False_, _cap_tris =False_, _segments =0_, _radius =0_, _matrix =mathutils.Matrix.Identity(4)_, _calc_uvs =False_)
    

Creates a Circle.

Parameters:
    

  * **bm** (`bmesh.types.BMesh`) – The bmesh to operate on.

  * **cap_ends** (_bool_) – Whether or not to fill in the ends with faces.

  * **cap_tris** (_bool_) – Fill ends with triangles instead of ngons.

  * **segments** (_int_) – Number of vertices in the circle.

  * **radius** (_float_) – Radius of the circle.

  * **matrix** ([`mathutils.Matrix`](mathutils.md#mathutils.Matrix "mathutils.Matrix")) – Matrix to multiply the new geometry with.

  * **calc_uvs** (_bool_) – Calculate default UVs.


Returns:
    

  * `verts`: Output verts.

**type** list of (`bmesh.types.BMVert`)


Return type:
    

dict[str, Any]

bmesh.ops.create_cube(_bm_ , _size =0_, _matrix =mathutils.Matrix.Identity(4)_, _calc_uvs =False_)
    

Create Cube

Creates a cube.

Parameters:
    

  * **bm** (`bmesh.types.BMesh`) – The bmesh to operate on.

  * **size** (_float_) – Size of the cube.

  * **matrix** ([`mathutils.Matrix`](mathutils.md#mathutils.Matrix "mathutils.Matrix")) – Matrix to multiply the new geometry with.

  * **calc_uvs** (_bool_) – Calculate default UVs.


Returns:
    

  * `verts`: Output verts.

**type** list of (`bmesh.types.BMVert`)


Return type:
    

dict[str, Any]

bmesh.ops.bevel(_bm_ , _geom =[]_, _offset =0_, _offset_type ='OFFSET'_, _profile_type ='SUPERELLIPSE'_, _segments =0_, _profile =0_, _affect ='VERTICES'_, _clamp_overlap =False_, _material =0_, _loop_slide =False_, _mark_seam =False_, _mark_sharp =False_, _harden_normals =False_, _face_strength_mode ='NONE'_, _miter_outer ='SHARP'_, _miter_inner ='SHARP'_, _spread =0_, _custom_profile =None_, _vmesh_method ='ADJ'_)
    

Bevel.

Bevels edges and vertices

Parameters:
    

  * **bm** (`bmesh.types.BMesh`) – The bmesh to operate on.

  * **geom** (list of (`bmesh.types.BMVert`, `bmesh.types.BMEdge`, `bmesh.types.BMFace`)) – Input edges and vertices.

  * **offset** (_float_) – Amount to offset beveled edge.

  * **offset_type** (_enum in_ _[__'OFFSET'__,__'WIDTH'__,__'DEPTH'__,__'PERCENT'__,__'ABSOLUTE'__]__,__default 'OFFSET'_) – How to measure the offset.

  * **profile_type** (_enum in_ _[__'SUPERELLIPSE'__,__'CUSTOM'__]__,__default 'SUPERELLIPSE'_) – The profile type to use for bevel.

  * **segments** (_int_) – Number of segments in bevel.

  * **profile** (_float_) – Profile shape, 0->1 (.5=>round).

  * **affect** (_enum in_ _[__'VERTICES'__,__'EDGES'__]__,__default 'VERTICES'_) – Whether to bevel vertices or edges.

  * **clamp_overlap** (_bool_) – Do not allow beveled edges/vertices to overlap each other.

  * **material** (_int_) – Material for bevel faces, -1 means get from adjacent faces.

  * **loop_slide** (_bool_) – Prefer to slide along edges to having even widths.

  * **mark_seam** (_bool_) – Extend edge data to allow seams to run across bevels.

  * **mark_sharp** (_bool_) – Extend edge data to allow sharp edges to run across bevels.

  * **harden_normals** (_bool_) – Harden normals.

  * **face_strength_mode** (_enum in_ _[__'NONE'__,__'NEW'__,__'AFFECTED'__,__'ALL'__]__,__default 'NONE'_) – Whether to set face strength, and which faces to set if so.

  * **miter_outer** (_enum in_ _[__'SHARP'__,__'PATCH'__,__'ARC'__]__,__default 'SHARP'_) – Outer miter kind.

  * **miter_inner** (_enum in_ _[__'SHARP'__,__'PATCH'__,__'ARC'__]__,__default 'SHARP'_) – Outer miter kind.

  * **spread** (_float_) – Amount to offset beveled edge.

  * **custom_profile** ([`bpy.types.bpy_struct`](../bpy.types/_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct "bpy.types.bpy_struct")) – CurveProfile, if None ignored

  * **vmesh_method** (_enum in_ _[__'ADJ'__,__'CUTOFF'__]__,__default 'ADJ'_) – The method to use to create meshes at intersections.


Returns:
    

  * `faces`: Output faces.

**type** list of (`bmesh.types.BMFace`)

  * `edges`: Output edges.

**type** list of (`bmesh.types.BMEdge`)

  * `verts`: Output verts.

**type** list of (`bmesh.types.BMVert`)


Return type:
    

dict[str, Any]

bmesh.ops.beautify_fill(_bm_ , _faces =[]_, _edges =[]_, _use_restrict_tag =False_, _method ='AREA'_)
    

Beautify Fill.

Rotate edges to create more evenly spaced triangles.

Parameters:
    

  * **bm** (`bmesh.types.BMesh`) – The bmesh to operate on.

  * **faces** (list of (`bmesh.types.BMFace`)) – Input faces.

  * **edges** (list of (`bmesh.types.BMEdge`)) – Edges that can be flipped.

  * **use_restrict_tag** (_bool_) – Restrict edge rotation to mixed tagged vertices.

  * **method** (_enum in_ _[__'AREA'__,__'ANGLE'__]__,__default 'AREA'_) – Method to define what is beautiful.


Returns:
    

  * `geom`: New flipped faces and edges.

**type** list of (`bmesh.types.BMVert`, `bmesh.types.BMEdge`, `bmesh.types.BMFace`)


Return type:
    

dict[str, Any]

bmesh.ops.triangle_fill(_bm_ , _use_beauty =False_, _use_dissolve =False_, _edges =[]_, _normal =mathutils.Vector()_)
    

Triangle Fill.

Fill edges with triangles

Parameters:
    

  * **bm** (`bmesh.types.BMesh`) – The bmesh to operate on.

  * **use_beauty** (_bool_) – Use best triangulation division.

  * **use_dissolve** (_bool_) – Dissolve resulting faces.

  * **edges** (list of (`bmesh.types.BMEdge`)) – Input edges.

  * **normal** ([`mathutils.Vector`](mathutils.md#mathutils.Vector "mathutils.Vector") or any sequence of 3 floats) – Optionally pass the fill normal to use.


Returns:
    

  * `geom`: New faces and edges.

**type** list of (`bmesh.types.BMVert`, `bmesh.types.BMEdge`, `bmesh.types.BMFace`)


Return type:
    

dict[str, Any]

bmesh.ops.solidify(_bm_ , _geom =[]_, _thickness =0_)
    

Solidify.

Turns a mesh into a shell with thickness

Parameters:
    

  * **bm** (`bmesh.types.BMesh`) – The bmesh to operate on.

  * **geom** (list of (`bmesh.types.BMVert`, `bmesh.types.BMEdge`, `bmesh.types.BMFace`)) – Input geometry.

  * **thickness** (_float_) – Thickness.


Returns:
    

  * `geom`:

**type** list of (`bmesh.types.BMVert`, `bmesh.types.BMEdge`, `bmesh.types.BMFace`)


Return type:
    

dict[str, Any]

bmesh.ops.inset_individual(_bm_ , _faces =[]_, _thickness =0_, _depth =0_, _use_even_offset =False_, _use_interpolate =False_, _use_relative_offset =False_)
    

Face Inset (Individual).

Insets individual faces.

Parameters:
    

  * **bm** (`bmesh.types.BMesh`) – The bmesh to operate on.

  * **faces** (list of (`bmesh.types.BMFace`)) – Input faces.

  * **thickness** (_float_) – Thickness.

  * **depth** (_float_) – Depth.

  * **use_even_offset** (_bool_) – Scale the offset to give more even thickness.

  * **use_interpolate** (_bool_) – Blend face data across the inset.

  * **use_relative_offset** (_bool_) – Scale the offset by surrounding geometry.


Returns:
    

  * `faces`: Output faces.

**type** list of (`bmesh.types.BMFace`)


Return type:
    

dict[str, Any]

bmesh.ops.inset_region(_bm_ , _faces =[]_, _faces_exclude =[]_, _use_boundary =False_, _use_even_offset =False_, _use_interpolate =False_, _use_relative_offset =False_, _use_edge_rail =False_, _thickness =0_, _depth =0_, _use_outset =False_)
    

Face Inset (Regions).

Inset or outset face regions.

Parameters:
    

  * **bm** (`bmesh.types.BMesh`) – The bmesh to operate on.

  * **faces** (list of (`bmesh.types.BMFace`)) – Input faces.

  * **faces_exclude** (list of (`bmesh.types.BMFace`)) – Input faces to explicitly exclude from inset.

  * **use_boundary** (_bool_) – Inset face boundaries.

  * **use_even_offset** (_bool_) – Scale the offset to give more even thickness.

  * **use_interpolate** (_bool_) – Blend face data across the inset.

  * **use_relative_offset** (_bool_) – Scale the offset by surrounding geometry.

  * **use_edge_rail** (_bool_) – Inset the region along existing edges.

  * **thickness** (_float_) – Thickness.

  * **depth** (_float_) – Depth.

  * **use_outset** (_bool_) – Outset rather than inset.


Returns:
    

  * `faces`: Output faces.

**type** list of (`bmesh.types.BMFace`)


Return type:
    

dict[str, Any]

bmesh.ops.offset_edgeloops(_bm_ , _edges =[]_, _use_cap_endpoint =False_)
    

Edge-loop Offset.

Creates edge loops based on simple edge-outset method.

Parameters:
    

  * **bm** (`bmesh.types.BMesh`) – The bmesh to operate on.

  * **edges** (list of (`bmesh.types.BMEdge`)) – Input edges.

  * **use_cap_endpoint** (_bool_) – Extend loop around end-points.


Returns:
    

  * `edges`: Output edges.

**type** list of (`bmesh.types.BMEdge`)


Return type:
    

dict[str, Any]

bmesh.ops.wireframe(_bm_ , _faces =[]_, _thickness =0_, _offset =0_, _use_replace =False_, _use_boundary =False_, _use_even_offset =False_, _use_crease =False_, _crease_weight =0_, _use_relative_offset =False_, _material_offset =0_)
    

Wire Frame.

Makes a wire-frame copy of faces.

Parameters:
    

  * **bm** (`bmesh.types.BMesh`) – The bmesh to operate on.

  * **faces** (list of (`bmesh.types.BMFace`)) – Input faces.

  * **thickness** (_float_) – Thickness.

  * **offset** (_float_) – Offset the thickness from the center.

  * **use_replace** (_bool_) – Remove original geometry.

  * **use_boundary** (_bool_) – Inset face boundaries.

  * **use_even_offset** (_bool_) – Scale the offset to give more even thickness.

  * **use_crease** (_bool_) – Crease hub edges for improved subdivision surface.

  * **crease_weight** (_float_) – The mean crease weight for resulting edges.

  * **use_relative_offset** (_bool_) – Scale the offset by surrounding geometry.

  * **material_offset** (_int_) – Offset material index of generated faces.


Returns:
    

  * `faces`: Output faces.

**type** list of (`bmesh.types.BMFace`)


Return type:
    

dict[str, Any]

bmesh.ops.poke(_bm_ , _faces =[]_, _offset =0_, _center_mode ='MEAN_WEIGHTED'_, _use_relative_offset =False_)
    

Pokes a face.

Splits a face into a triangle fan.

Parameters:
    

  * **bm** (`bmesh.types.BMesh`) – The bmesh to operate on.

  * **faces** (list of (`bmesh.types.BMFace`)) – Input faces.

  * **offset** (_float_) – Center vertex offset along normal.

  * **center_mode** (_enum in_ _[__'MEAN_WEIGHTED'__,__'MEAN'__,__'BOUNDS'__]__,__default 'MEAN_WEIGHTED'_) – Calculation mode for center vertex.

  * **use_relative_offset** (_bool_) – Apply offset.


Returns:
    

  * `verts`: Output verts.

**type** list of (`bmesh.types.BMVert`)

  * `faces`: Output faces.

**type** list of (`bmesh.types.BMFace`)


Return type:
    

dict[str, Any]

bmesh.ops.convex_hull(_bm_ , _input =[]_, _use_existing_faces =False_)
    

Convex Hull

Builds a convex hull from the vertices in ‘input’.

If ‘use_existing_faces’ is true, the hull will not output triangles that are covered by a pre-existing face.

All hull vertices, faces, and edges are added to ‘geom.out’. Any input elements that end up inside the hull (i.e. are not used by an output face) are added to the ‘interior_geom’ slot. The ‘unused_geom’ slot will contain all interior geometry that is completely unused. Lastly, ‘holes_geom’ contains edges and faces that were in the input and are part of the hull.

Parameters:
    

  * **bm** (`bmesh.types.BMesh`) – The bmesh to operate on.

  * **input** (list of (`bmesh.types.BMVert`, `bmesh.types.BMEdge`, `bmesh.types.BMFace`)) – Input geometry.

  * **use_existing_faces** (_bool_) – Skip hull triangles that are covered by a pre-existing face.


Returns:
    

  * `geom`:

**type** list of (`bmesh.types.BMVert`, `bmesh.types.BMEdge`, `bmesh.types.BMFace`)

  * `geom_interior`:

**type** list of (`bmesh.types.BMVert`, `bmesh.types.BMEdge`, `bmesh.types.BMFace`)

  * `geom_unused`:

**type** list of (`bmesh.types.BMVert`, `bmesh.types.BMEdge`, `bmesh.types.BMFace`)

  * `geom_holes`:

**type** list of (`bmesh.types.BMVert`, `bmesh.types.BMEdge`, `bmesh.types.BMFace`)


Return type:
    

dict[str, Any]

bmesh.ops.symmetrize(_bm_ , _input =[]_, _direction ='-X'_, _dist =0_, _use_shapekey =False_)
    

Symmetrize.

Makes the mesh elements in the “input” slot symmetrical. Unlike normal mirroring, it only copies in one direction, as specified by the “direction” slot. The edges and faces that cross the plane of symmetry are split as needed to enforce symmetry.

All new vertices, edges, and faces are added to the “geom.out” slot.

Parameters:
    

  * **bm** (`bmesh.types.BMesh`) – The bmesh to operate on.

  * **input** (list of (`bmesh.types.BMVert`, `bmesh.types.BMEdge`, `bmesh.types.BMFace`)) – Input geometry.

  * **direction** (_enum in_ _[__'-X'__,__'-Y'__,__'-Z'__,__'X'__,__'Y'__,__'Z'__]__,__default '-X'_) – Axis to use.

  * **dist** (_float_) – Minimum distance.

  * **use_shapekey** (_bool_) – Transform shape keys too.


Returns:
    

  * `geom`:

**type** list of (`bmesh.types.BMVert`, `bmesh.types.BMEdge`, `bmesh.types.BMFace`)


Return type:
    

dict[str, Any]
