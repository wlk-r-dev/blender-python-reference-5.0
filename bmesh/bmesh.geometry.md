# BMesh Geometry Utilities (bmesh.geometry)

This module provides access to bmesh geometry evaluation functions.

bmesh.geometry.intersect_face_point(_face_ , _point_)
    

Tests if the projection of a point is inside a face (using the face’s normal).

Parameters:
    

  * **face** (`bmesh.types.BMFace`) – The face to test.

  * **point** (_float triplet_) – The point to test.


Returns:
    

True when the projection of the point is in the face.

Return type:
    

bool
