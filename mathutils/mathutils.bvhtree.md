# BVHTree Utilities (mathutils.bvhtree)

BVH tree structures for proximity searches and ray casts on geometry.

_class _mathutils.bvhtree.BVHTree
    

_classmethod _FromBMesh(_bmesh_ , _*_ , _epsilon =0.0_)
    

BVH tree based on `BMesh` data.

Parameters:
    

  * **bmesh** (`BMesh`) – BMesh data.

  * **epsilon** (_float_) – Increase the threshold for detecting overlap and raycast hits.


_classmethod _FromObject(_object_ , _depsgraph_ , _*_ , _deform =True_, _render =False_, _cage =False_, _epsilon =0.0_)
    

BVH tree based on `Object` data.

Parameters:
    

  * **object** (`Object`) – Object data.

  * **depsgraph** (`Depsgraph`) – Depsgraph to use for evaluating the mesh.

  * **deform** (_bool_) – Use mesh with deformations.

  * **cage** (_bool_) – Use modifiers cage.

  * **epsilon** (_float_) – Increase the threshold for detecting overlap and raycast hits.


_classmethod _FromPolygons(_vertices_ , _polygons_ , _*_ , _all_triangles =False_, _epsilon =0.0_)
    

BVH tree constructed geometry passed in as arguments.

Parameters:
    

  * **vertices** (_Sequence_ _[__Sequence_ _[__float_ _]__]_) – float triplets each representing `(x, y, z)`

  * **polygons** (_Sequence_ _[__Sequence_ _[__int_ _]__]_) – Sequence of polygons, each containing indices to the vertices argument.

  * **all_triangles** (_bool_) – Use when all **polygons** are triangles for more efficient conversion.

  * **epsilon** (_float_) – Increase the threshold for detecting overlap and raycast hits.


find_nearest(_origin_ , _distance =1.84467e+19_, _/_)
    

Find the nearest element (typically face index) to a point.

Parameters:
    

  * **co** (`Vector`) – Find nearest element to this point.

  * **distance** (_float_) – Maximum distance threshold.


Returns:
    

Returns a tuple: (position, normal, index, distance), Values will all be None if no hit is found.

Return type:
    

tuple[`Vector` | None, `Vector` | None, int | None, float | None]

find_nearest_range(_origin_ , _distance =1.84467e+19_, _/_)
    

Find the nearest elements (typically face index) to a point in the distance range.

Parameters:
    

  * **co** (`Vector`) – Find nearest elements to this point.

  * **distance** (_float_) – Maximum distance threshold.


Returns:
    

Returns a list of tuples (position, normal, index, distance)

Return type:
    

list[tuple[`Vector`, `Vector`, int, float]]

overlap(_other_tree_ , _/_)
    

Find overlapping indices between 2 trees.

Parameters:
    

**other_tree** (`BVHTree`) – Other tree to perform overlap test on.

Returns:
    

Returns a list of unique index pairs, the first index referencing this tree, the second referencing the **other_tree**.

Return type:
    

list[tuple[int, int]]

ray_cast(_origin_ , _direction_ , _distance =sys.float_info.max_, _/_)
    

Cast a ray onto the mesh.

Parameters:
    

  * **origin** (`Vector`) – Start location of the ray in object space.

  * **direction** (`Vector`) – Direction of the ray in object space.

  * **distance** (_float_) – Maximum distance threshold.


Returns:
    

Returns a tuple: (position, normal, index, distance), Values will all be None if no hit is found.

Return type:
    

tuple[`Vector` | None, `Vector` | None, int | None, float | None]
  *[*]: Keyword-only parameters separator (PEP 3102)
  *[/]: Positional-only parameter separator (PEP 570)
