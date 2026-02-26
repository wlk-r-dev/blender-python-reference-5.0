# Application Icons (bpy.app.icons)

bpy.app.icons.new_triangles(_range_ , _coords_ , _colors_)
    

Create a new icon from triangle geometry.

Parameters:
    

  * **range** (_tuple_ _[__int_ _,__int_ _]_) – Pair of ints.

  * **coords** (_bytes_) – Sequence of bytes (6 floats for one triangle) for (X, Y) coordinates.

  * **colors** (_bytes_) – Sequence of bytes (12 for one triangles) for RGBA.


Returns:
    

Unique icon value (pass to interface `icon_value` argument).

Return type:
    

int

bpy.app.icons.new_triangles_from_file(_filepath_)
    

Create a new icon from triangle geometry.

Parameters:
    

**filepath** (_str_ _|__bytes._) – File path.

Returns:
    

Unique icon value (pass to interface `icon_value` argument).

Return type:
    

int

bpy.app.icons.release(_icon_id_)
    

Release the icon.
