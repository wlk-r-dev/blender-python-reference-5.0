# Geometry Utilities (mathutils.geometry)

The Blender geometry module.

mathutils.geometry.area_tri(_v1_ , _v2_ , _v3_ , _/_)
    

Returns the area size of the 2D or 3D triangle defined.

Parameters:
    

  * **v1** ([[mathutils.Vector]]) – Point1

  * **v2** ([[mathutils.Vector]]) – Point2

  * **v3** ([[mathutils.Vector]]) – Point3


Return type:
    

float

mathutils.geometry.barycentric_transform(_point_ , _tri_a1_ , _tri_a2_ , _tri_a3_ , _tri_b1_ , _tri_b2_ , _tri_b3_ , _/_)
    

Return a transformed point, the transformation is defined by 2 triangles.

Parameters:
    

  * **point** ([[mathutils.Vector]]) – The point to transform.

  * **tri_a1** ([[mathutils.Vector]]) – source triangle vertex.

  * **tri_a2** ([[mathutils.Vector]]) – source triangle vertex.

  * **tri_a3** ([[mathutils.Vector]]) – source triangle vertex.

  * **tri_b1** ([[mathutils.Vector]]) – target triangle vertex.

  * **tri_b2** ([[mathutils.Vector]]) – target triangle vertex.

  * **tri_b3** ([[mathutils.Vector]]) – target triangle vertex.


Returns:
    

The transformed point

Return type:
    

[[mathutils.Vector]]

mathutils.geometry.box_fit_2d(_points_ , _/_)
    

Returns an angle that best fits the points to an axis aligned rectangle

Parameters:
    

**points** (_Sequence_ _[__Sequence_ _[__float_ _]__]_) – Sequence of 2D points.

Returns:
    

angle

Return type:
    

float

mathutils.geometry.box_pack_2d(_boxes_ , _/_)
    

Returns a tuple with the width and height of the packed bounding box.

Parameters:
    

**boxes** (_list_ _[__list_ _[__float_ _]__]_) – list of boxes, each box is a list where the first 4 items are [X, Y, width, height, …] other items are ignored. The X & Y values in this list are modified to set the packed positions.

Returns:
    

The width and height of the packed bounding box.

Return type:
    

tuple[float, float]

mathutils.geometry.closest_point_on_tri(_pt_ , _tri_p1_ , _tri_p2_ , _tri_p3_ , _/_)
    

Takes 4 vectors: one is the point and the next 3 define the triangle.

Parameters:
    

  * **pt** ([[mathutils.Vector]]) – Point

  * **tri_p1** ([[mathutils.Vector]]) – First point of the triangle

  * **tri_p2** ([[mathutils.Vector]]) – Second point of the triangle

  * **tri_p3** ([[mathutils.Vector]]) – Third point of the triangle


Returns:
    

The closest point of the triangle.

Return type:
    

[[mathutils.Vector]]

mathutils.geometry.convex_hull_2d(_points_)
    

Returns a list of indices into the list given

Parameters:
    

**points** (_Sequence_ _[__Sequence_ _[__float_ _]__]_) – Sequence of 2D points.

Returns:
    

a list of indices

Return type:
    

list[int]

mathutils.geometry.delaunay_2d_cdt(_vert_coords_ , _edges_ , _faces_ , _output_type_ , _epsilon_ , _need_ids =True_, _/_)
    

Computes the Constrained Delaunay Triangulation of a set of vertices, with edges and faces that must appear in the triangulation. Some triangles may be eaten away, or combined with other triangles, according to output type. The returned verts may be in a different order from input verts, may be moved slightly, and may be merged with other nearby verts. The three returned orig lists give, for each of verts, edges, and faces, the list of input element indices corresponding to the positionally same output element. For edges, the orig indices start with the input edges and then continue with the edges implied by each of the faces (n of them for an n-gon). If the need_ids argument is supplied, and False, then the code skips the preparation of the orig arrays, which may save some time.

Parameters:
    

  * **vert_coords** (Sequence[[[mathutils.Vector]]]) – Vertex coordinates (2d)

  * **edges** (_Sequence_ _[__Sequence_ _[__int_ _,__int_ _]__]_) – Edges, as pairs of indices in `vert_coords`

  * **faces** (_Sequence_ _[__Sequence_ _[__int_ _]__]_) – Faces, each sublist is a face, as indices in `vert_coords` (CCW oriented).

  * **output_type** (_int_) – What output looks like. 0 => triangles with convex hull. 1 => triangles inside constraints. 2 => the input constraints, intersected. 3 => like 2 but detect holes and omit them from output. 4 => like 2 but with extra edges to make valid BMesh faces. 5 => like 4 but detect holes and omit them from output.

  * **epsilon** (_float_) – For nearness tests; should not be zero

  * **need_ids** (_bool_) – are the orig output arrays needed?


Returns:
    

Output tuple, (vert_coords, edges, faces, orig_verts, orig_edges, orig_faces)

Return type:
    

tuple[list[[[mathutils.Vector]]], list[tuple[int, int]], list[list[int]], list[list[int]], list[list[int]], list[list[int]]]

mathutils.geometry.distance_point_to_plane(_pt_ , _plane_co_ , _plane_no_ , _/_)
    

Returns the signed distance between a point and a plane (negative when below the normal).

Parameters:
    

  * **pt** ([[mathutils.Vector]]) – Point

  * **plane_co** ([[mathutils.Vector]]) – A point on the plane

  * **plane_no** ([[mathutils.Vector]]) – The direction the plane is facing


Return type:
    

float

mathutils.geometry.interpolate_bezier(_knot1_ , _handle1_ , _handle2_ , _knot2_ , _resolution_ , _/_)
    

Interpolate a bezier spline segment.

Parameters:
    

  * **knot1** ([[mathutils.Vector]]) – First bezier spline point.

  * **handle1** ([[mathutils.Vector]]) – First bezier spline handle.

  * **handle2** ([[mathutils.Vector]]) – Second bezier spline handle.

  * **knot2** ([[mathutils.Vector]]) – Second bezier spline point.

  * **resolution** (_int_) – Number of points to return.


Returns:
    

The interpolated points.

Return type:
    

list[[[mathutils.Vector]]]

mathutils.geometry.intersect_line_line(_v1_ , _v2_ , _v3_ , _v4_ , _/_)
    

Returns a tuple with the points on each line respectively closest to the other.

Parameters:
    

  * **v1** ([[mathutils.Vector]]) – First point of the first line

  * **v2** ([[mathutils.Vector]]) – Second point of the first line

  * **v3** ([[mathutils.Vector]]) – First point of the second line

  * **v4** ([[mathutils.Vector]]) – Second point of the second line


Returns:
    

The intersection on each line or None when the lines are co-linear.

Return type:
    

tuple[[[mathutils.Vector]], [[mathutils.Vector]]] | None

mathutils.geometry.intersect_line_line_2d(_lineA_p1_ , _lineA_p2_ , _lineB_p1_ , _lineB_p2_ , _/_)
    

Takes 2 segments (defined by 4 vectors) and returns a vector for their point of intersection or None.

Warning

Despite its name, this function works on segments, and not on lines.

Parameters:
    

  * **lineA_p1** ([[mathutils.Vector]]) – First point of the first line

  * **lineA_p2** ([[mathutils.Vector]]) – Second point of the first line

  * **lineB_p1** ([[mathutils.Vector]]) – First point of the second line

  * **lineB_p2** ([[mathutils.Vector]]) – Second point of the second line


Returns:
    

The point of intersection or None when not found

Return type:
    

[[mathutils.Vector]] | None

mathutils.geometry.intersect_line_plane(_line_a_ , _line_b_ , _plane_co_ , _plane_no_ , _no_flip =False_, _/_)
    

Calculate the intersection between a line (as 2 vectors) and a plane. Returns a vector for the intersection or None.

Parameters:
    

  * **line_a** ([[mathutils.Vector]]) – First point of the first line

  * **line_b** ([[mathutils.Vector]]) – Second point of the first line

  * **plane_co** ([[mathutils.Vector]]) – A point on the plane

  * **plane_no** ([[mathutils.Vector]]) – The direction the plane is facing

  * **no_flip** (_bool_) – Not implemented


Returns:
    

The point of intersection or None when not found

Return type:
    

[[mathutils.Vector]] | None

mathutils.geometry.intersect_line_sphere(_line_a_ , _line_b_ , _sphere_co_ , _sphere_radius_ , _clip =True_, _/_)
    

Takes a line (as 2 points) and a sphere (as a point and a radius) and returns the intersection

Parameters:
    

  * **line_a** ([[mathutils.Vector]]) – First point of the line

  * **line_b** ([[mathutils.Vector]]) – Second point of the line

  * **sphere_co** ([[mathutils.Vector]]) – The center of the sphere

  * **sphere_radius** (_float_) – Radius of the sphere

  * **clip** (_bool_) – When False, don’t restrict the intersection to the area of the sphere.


Returns:
    

The intersection points as a pair of vectors or None when there is no intersection

Return type:
    

tuple[[[mathutils.Vector]] | None, [[mathutils.Vector]] | None]

mathutils.geometry.intersect_line_sphere_2d(_line_a_ , _line_b_ , _sphere_co_ , _sphere_radius_ , _clip =True_, _/_)
    

Takes a line (as 2 points) and a sphere (as a point and a radius) and returns the intersection

Parameters:
    

  * **line_a** ([[mathutils.Vector]]) – First point of the line

  * **line_b** ([[mathutils.Vector]]) – Second point of the line

  * **sphere_co** ([[mathutils.Vector]]) – The center of the sphere

  * **sphere_radius** (_float_) – Radius of the sphere

  * **clip** (_bool_) – When False, don’t restrict the intersection to the area of the sphere.


Returns:
    

The intersection points as a pair of vectors or None when there is no intersection

Return type:
    

tuple[[[mathutils.Vector]] | None, [[mathutils.Vector]] | None]

mathutils.geometry.intersect_plane_plane(_plane_a_co_ , _plane_a_no_ , _plane_b_co_ , _plane_b_no_ , _/_)
    

Return the intersection between two planes

Parameters:
    

  * **plane_a_co** ([[mathutils.Vector]]) – Point on the first plane

  * **plane_a_no** ([[mathutils.Vector]]) – Normal of the first plane

  * **plane_b_co** ([[mathutils.Vector]]) – Point on the second plane

  * **plane_b_no** ([[mathutils.Vector]]) – Normal of the second plane


Returns:
    

The line of the intersection represented as a point and a vector or None if the intersection can’t be calculated

Return type:
    

tuple[[[mathutils.Vector]], [[mathutils.Vector]]] | tuple[None, None]

mathutils.geometry.intersect_point_line(_pt_ , _line_p1_ , _line_p2_ , _/_)
    

Takes a point and a line and returns the closest point on the line and its distance from the first point of the line as a percentage of the length of the line.

Parameters:
    

  * **pt** ([[mathutils.Vector]]) – Point

  * **line_p1** ([[mathutils.Vector]]) – First point of the line

  * **line_p2** ([[mathutils.Vector]]) – Second point of the line


Return type:
    

tuple[[[mathutils.Vector]], float]

mathutils.geometry.intersect_point_line_segment(_pt_ , _seg_p1_ , _seg_p2_ , _/_)
    

Takes a point and a segment and returns the closest point on the segment and the distance to the segment.

Parameters:
    

  * **pt** ([[mathutils.Vector]]) – Point

  * **seg_p1** ([[mathutils.Vector]]) – First point of the segment

  * **seg_p2** ([[mathutils.Vector]]) – Second point of the segment


Return type:
    

tuple[[[mathutils.Vector]], float]

mathutils.geometry.intersect_point_quad_2d(_pt_ , _quad_p1_ , _quad_p2_ , _quad_p3_ , _quad_p4_ , _/_)
    

Takes 5 vectors (using only the x and y coordinates): one is the point and the next 4 define the quad, only the x and y are used from the vectors. Returns 1 if the point is within the quad, otherwise 0. Works only with convex quads without singular edges.

Parameters:
    

  * **pt** ([[mathutils.Vector]]) – Point

  * **quad_p1** ([[mathutils.Vector]]) – First point of the quad

  * **quad_p2** ([[mathutils.Vector]]) – Second point of the quad

  * **quad_p3** ([[mathutils.Vector]]) – Third point of the quad

  * **quad_p4** ([[mathutils.Vector]]) – Fourth point of the quad


Return type:
    

int

mathutils.geometry.intersect_point_tri(_pt_ , _tri_p1_ , _tri_p2_ , _tri_p3_ , _/_)
    

Takes 4 vectors: one is the point and the next 3 define the triangle. Projects the point onto the triangle plane and checks if it is within the triangle.

Parameters:
    

  * **pt** ([[mathutils.Vector]]) – Point

  * **tri_p1** ([[mathutils.Vector]]) – First point of the triangle

  * **tri_p2** ([[mathutils.Vector]]) – Second point of the triangle

  * **tri_p3** ([[mathutils.Vector]]) – Third point of the triangle


Returns:
    

Point on the triangles plane or None if its outside the triangle

Return type:
    

[[mathutils.Vector]] | None

mathutils.geometry.intersect_point_tri_2d(_pt_ , _tri_p1_ , _tri_p2_ , _tri_p3_ , _/_)
    

Takes 4 vectors (using only the x and y coordinates): one is the point and the next 3 define the triangle. Returns 1 if the point is within the triangle, otherwise 0.

Parameters:
    

  * **pt** ([[mathutils.Vector]]) – Point

  * **tri_p1** ([[mathutils.Vector]]) – First point of the triangle

  * **tri_p2** ([[mathutils.Vector]]) – Second point of the triangle

  * **tri_p3** ([[mathutils.Vector]]) – Third point of the triangle


Return type:
    

int

mathutils.geometry.intersect_ray_tri(_v1_ , _v2_ , _v3_ , _ray_ , _orig_ , _clip =True_, _/_)
    

Returns the intersection between a ray and a triangle, if possible, returns None otherwise.

Parameters:
    

  * **v1** ([[mathutils.Vector]]) – Point1

  * **v2** ([[mathutils.Vector]]) – Point2

  * **v3** ([[mathutils.Vector]]) – Point3

  * **ray** ([[mathutils.Vector]]) – Direction of the projection

  * **orig** ([[mathutils.Vector]]) – Origin

  * **clip** (_bool_) – When False, don’t restrict the intersection to the area of the triangle, use the infinite plane defined by the triangle.


Returns:
    

The point of intersection or None if no intersection is found

Return type:
    

[[mathutils.Vector]] | None

mathutils.geometry.intersect_sphere_sphere_2d(_p_a_ , _radius_a_ , _p_b_ , _radius_b_ , _/_)
    

Returns 2 points on between intersecting circles.

Parameters:
    

  * **p_a** ([[mathutils.Vector]]) – Center of the first circle

  * **radius_a** (_float_) – Radius of the first circle

  * **p_b** ([[mathutils.Vector]]) – Center of the second circle

  * **radius_b** (_float_) – Radius of the second circle


Returns:
    

2 points on between intersecting circles or None when there is no intersection.

Return type:
    

tuple[[[mathutils.Vector]], [[mathutils.Vector]]] | tuple[None, None]

mathutils.geometry.intersect_tri_tri_2d(_tri_a1_ , _tri_a2_ , _tri_a3_ , _tri_b1_ , _tri_b2_ , _tri_b3_ , _/_)
    

Check if two 2D triangles intersect.

Return type:
    

bool

mathutils.geometry.normal(_* vectors_)
    

Returns the normal of a 3D polygon.

Parameters:
    

**vectors** (_Sequence_ _[__Sequence_ _[__float_ _]__]_) – 3 or more vectors to calculate normals.

Return type:
    

[[mathutils.Vector]]

mathutils.geometry.points_in_planes(_planes_ , _epsilon_coplanar =1e-4_, _epsilon_isect =1e-6_, _/_)
    

Returns a list of points inside all planes given and a list of index values for the planes used.

Parameters:
    

  * **planes** (list[[[mathutils.Vector]]]) – List of planes (4D vectors).

  * **epsilon_coplanar** (_float_) – Epsilon value for interpreting plane pairs as co-plannar.

  * **epsilon_isect** (_float_) – Epsilon value for intersection.


Returns:
    

Two lists, once containing the 3D coordinates inside the planes, another containing the plane indices used.

Return type:
    

tuple[list[[[mathutils.Vector]]], list[int]]

mathutils.geometry.tessellate_polygon(_polylines_ , _/_)
    

Takes a list of polylines (each point a pair or triplet of numbers) and returns the point indices for a polyline filled with triangles. Does not handle degenerate geometry (such as zero-length lines due to consecutive identical points).

Parameters:
    

**polylines** (_Sequence_ _[__Sequence_ _[__Sequence_ _[__float_ _]__]__]__:return: A list_ _of_ _triangles._) – Polygons where each polygon is a sequence of 2D or 3D points.

Return type:
    

list[tuple[int, int, int]]

mathutils.geometry.volume_tetrahedron(_v1_ , _v2_ , _v3_ , _v4_ , _/_)
    

Return the volume formed by a tetrahedron (points can be in any order).

Parameters:
    

  * **v1** ([[mathutils.Vector]]) – Point1

  * **v2** ([[mathutils.Vector]]) – Point2

  * **v3** ([[mathutils.Vector]]) – Point3

  * **v4** ([[mathutils.Vector]]) – Point4


Return type:
    

float
  *[/]: Positional-only parameter separator (PEP 570)
