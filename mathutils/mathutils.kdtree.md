# KDTree Utilities (mathutils.kdtree)

Generic 3-dimensional kd-tree to perform spatial searches.
    
    
    import mathutils
    
    # Create a KD-tree from a mesh.
    from bpy import context
    obj = context.object
    
    mesh = obj.data
    size = len(mesh.vertices)
    kd = mathutils.kdtree.KDTree(size)
    
    for i, v in enumerate(mesh.vertices):
        kd.insert(v.co, i)
    
    kd.balance()
    
    
    # Find the closest point to the center.
    co_find = (0.0, 0.0, 0.0)
    co, index, dist = kd.find(co_find)
    print("Close to center:", co, index, dist)
    
    # 3D cursor relative to the object data.
    co_find = obj.matrix_world.inverted() @ context.scene.cursor.location
    
    # Find the closest 10 points to the 3D cursor.
    print("Close 10 points")
    for (co, index, dist) in kd.find_n(co_find, 10):
        print("    ", co, index, dist)
    
    
    # Find points within a radius of the 3D cursor.
    print("Close points within 0.5 distance")
    for (co, index, dist) in kd.find_range(co_find, 0.5):
        print("    ", co, index, dist)
    

_class _mathutils.kdtree.KDTree
    

KdTree(size) -> new kd-tree initialized to hold `size` items.

> arg size:
>     
> 
> Number of items.
> 
> type size:
>     
> 
> int

Note

`KDTree.balance` must have been called before using any of the `find` methods.

balance()
    

Balance the tree.

Note

This builds the entire tree, avoid calling after each insertion.

find(_co_ , _*_ , _filter =None_)
    

Find nearest point to `co`.

Parameters:
    

  * **co** (_Sequence_ _[__float_ _]_) – 3D coordinates.

  * **filter** (_Callable_ _[__[__int_ _]__,__bool_ _]_) – function which takes an index and returns True for indices to include in the search.


Returns:
    

Returns (position, index, distance).

Return type:
    

tuple[`Vector`, int, float]

find_n(_co_ , _n_)
    

Find nearest `n` points to `co`.

Parameters:
    

  * **co** (_Sequence_ _[__float_ _]_) – 3D coordinates.

  * **n** (_int_) – Number of points to find.


Returns:
    

Returns a list of tuples (position, index, distance).

Return type:
    

list[tuple[`Vector`, int, float]]

find_range(_co_ , _radius_)
    

Find all points within `radius` of `co`.

Parameters:
    

  * **co** (_Sequence_ _[__float_ _]_) – 3D coordinates.

  * **radius** (_float_) – Distance to search for points.


Returns:
    

Returns a list of tuples (position, index, distance).

Return type:
    

list[tuple[`Vector`, int, float]]

insert(_co_ , _index_)
    

Insert a point into the KDTree.

Parameters:
    

  * **co** (_Sequence_ _[__float_ _]_) – Point 3d position.

  * **index** (_int_) – The index of the point.


  *[*]: Keyword-only parameters separator (PEP 3102)
