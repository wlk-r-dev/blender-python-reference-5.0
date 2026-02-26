# GPU State Utilities (gpu.state)

This module provides access to the gpu state.

gpu.state.active_framebuffer_get(_enable_)
    

Return the active frame-buffer in context.

gpu.state.blend_get()
    

Current blending equation.

gpu.state.blend_set(_mode_)
    

Defines the fixed pipeline blending equation.

Parameters:
    

**mode** (_str_) – 

The type of blend mode.

  * `NONE` No blending.

  * `ALPHA` The original color channels are interpolated according to the alpha value.

  * `ALPHA_PREMULT` The original color channels are interpolated according to the alpha value with the new colors pre-multiplied by this value.

  * `ADDITIVE` The original color channels are added by the corresponding ones.

  * `ADDITIVE_PREMULT` The original color channels are added by the corresponding ones that are pre-multiplied by the alpha value.

  * `MULTIPLY` The original color channels are multiplied by the corresponding ones.

  * `SUBTRACT` The original color channels are subtracted by the corresponding ones.

  * `INVERT` The original color channels are replaced by its complementary color.


gpu.state.clip_distances_set(_distances_enabled_)
    

Sets the number of `gl_ClipDistance` planes used for clip geometry.

Parameters:
    

**distances_enabled** (_int_) – Number of clip distances enabled.

gpu.state.color_mask_set(_r_ , _g_ , _b_ , _a_)
    

Enable or disable writing of frame buffer color components.

Parameters:
    

**a** (_r_ _,__g_ _,__b_ _,_) – components red, green, blue, and alpha.

gpu.state.depth_mask_get()
    

Writing status in the depth component.

gpu.state.depth_mask_set(_value_)
    

Write to depth component.

Parameters:
    

**value** – True for writing to the depth component.

gpu.state.depth_test_get()
    

Current depth_test equation.

gpu.state.depth_test_set(_mode_)
    

Defines the depth_test equation.

Parameters:
    

**mode** (_str_) – The depth test equation name. Possible values are `NONE`, `ALWAYS`, `LESS`, `LESS_EQUAL`, `EQUAL`, `GREATER` and `GREATER_EQUAL`.

gpu.state.face_culling_set(_culling_)
    

Specify whether none, front-facing or back-facing facets can be culled.

Parameters:
    

**mode** (_str_) – `NONE`, `FRONT` or `BACK`.

gpu.state.front_facing_set(_invert_)
    

Specifies the orientation of front-facing polygons.

Parameters:
    

**invert** – True for clockwise polygons as front-facing.

gpu.state.line_width_get()
    

Current width of rasterized lines.

gpu.state.line_width_set(_width_)
    

Specify the width of rasterized lines.

Parameters:
    

**size** – New width.

gpu.state.point_size_set(_size_)
    

Specify the diameter of rasterized points.

Parameters:
    

**size** – New diameter.

gpu.state.program_point_size_set(_enable_)
    

If enabled, the derived point size is taken from the (potentially clipped) shader builtin gl_PointSize.

Parameters:
    

**enable** (_bool_) – True for shader builtin gl_PointSize.

gpu.state.scissor_get()
    

Retrieve the scissors of the active framebuffer. Note: Only valid between ‘scissor_set’ and a framebuffer rebind.

Returns:
    

The scissor of the active framebuffer as a tuple (x, y, xsize, ysize). x, y: lower left corner of the scissor rectangle, in pixels. xsize, ysize: width and height of the scissor rectangle.

Return type:
    

tuple[int, int, int, int]

gpu.state.scissor_set(_x_ , _y_ , _xsize_ , _ysize_)
    

Specifies the scissor area of the active framebuffer. Note: The scissor state is not saved upon framebuffer rebind.

Parameters:
    

  * **y** (_x_ _,_) – lower left corner of the scissor rectangle, in pixels.

  * **ysize** (_xsize_ _,_) – width and height of the scissor rectangle.


gpu.state.scissor_test_set(_enable_)
    

Enable/disable scissor testing on the active framebuffer.

Parameters:
    

**enable** (_bool_) – True - enable scissor testing. False - disable scissor testing.

gpu.state.viewport_get()
    

Viewport of the active framebuffer.

gpu.state.viewport_set(_x_ , _y_ , _xsize_ , _ysize_)
    

Specifies the viewport of the active framebuffer. Note: The viewport state is not saved upon framebuffer rebind.

Parameters:
    

  * **y** (_x_ _,_) – lower left corner of the viewport_set rectangle, in pixels.

  * **ysize** (_xsize_ _,_) – width and height of the viewport_set.
