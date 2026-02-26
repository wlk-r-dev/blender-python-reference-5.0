# freestyle.utils submodule (freestyle.utils.ContextFunctions)

The Blender Freestyle.ContextFunctions submodule

freestyle.utils.ContextFunctions.get_border()
    

Returns the border.

Returns:
    

A tuple of 4 numbers (xmin, ymin, xmax, ymax).

Return type:
    

tuple[int, int, int, int]

freestyle.utils.ContextFunctions.get_canvas_height()
    

Returns the canvas height.

Returns:
    

The canvas height.

Return type:
    

int

freestyle.utils.ContextFunctions.get_canvas_width()
    

Returns the canvas width.

Returns:
    

The canvas width.

Return type:
    

int

freestyle.utils.ContextFunctions.get_selected_fedge()
    

Returns the selected FEdge.

Returns:
    

The selected FEdge.

Return type:
    

`FEdge`

freestyle.utils.ContextFunctions.get_time_stamp()
    

Returns the system time stamp.

Returns:
    

The system time stamp.

Return type:
    

int

freestyle.utils.ContextFunctions.load_map(_file_name_ , _map_name_ , _num_levels =4_, _sigma =1.0_)
    

Loads an image map for further reading.

Parameters:
    

  * **file_name** (_str_) – The name of the image file.

  * **map_name** (_str_) – The name that will be used to access this image.

  * **num_levels** (_int_) – The number of levels in the map pyramid (default = 4). If num_levels == 0, the complete pyramid is built.

  * **sigma** (_float_) – The sigma value of the gaussian function.


freestyle.utils.ContextFunctions.read_complete_view_map_pixel(_level_ , _x_ , _y_)
    

Reads a pixel in the complete view map.

Parameters:
    

  * **level** (_int_) – The level of the pyramid in which we wish to read the pixel.

  * **x** (_int_) – The x coordinate of the pixel we wish to read. The origin is in the lower-left corner.

  * **y** (_int_) – The y coordinate of the pixel we wish to read. The origin is in the lower-left corner.


Returns:
    

The floating-point value stored for that pixel.

Return type:
    

float

freestyle.utils.ContextFunctions.read_directional_view_map_pixel(_orientation_ , _level_ , _x_ , _y_)
    

Reads a pixel in one of the oriented view map images.

Parameters:
    

  * **orientation** (_int_) – The number telling which orientation we want to check.

  * **level** (_int_) – The level of the pyramid in which we wish to read the pixel.

  * **x** (_int_) – The x coordinate of the pixel we wish to read. The origin is in the lower-left corner.

  * **y** (_int_) – The y coordinate of the pixel we wish to read. The origin is in the lower-left corner.


Returns:
    

The floating-point value stored for that pixel.

Return type:
    

float

freestyle.utils.ContextFunctions.read_map_pixel(_map_name_ , _level_ , _x_ , _y_)
    

Reads a pixel in a user-defined map.

Parameters:
    

  * **map_name** (_str_) – The name of the map.

  * **level** (_int_) – The level of the pyramid in which we wish to read the pixel.

  * **x** (_int_) – The x coordinate of the pixel we wish to read. The origin is in the lower-left corner.

  * **y** (_int_) – The y coordinate of the pixel we wish to read. The origin is in the lower-left corner.


Returns:
    

The floating-point value stored for that pixel.

Return type:
    

float
