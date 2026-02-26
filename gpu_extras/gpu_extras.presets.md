# gpu_extras submodule (gpu_extras.presets)

gpu_extras.presets.draw_circle_2d(_position_ , _color_ , _radius_ , _*_ , _segments =None_)
    

Draw a circle.

Parameters:
    

  * **position** (_Sequence_ _[__float_ _]_) – 2D position where the circle will be drawn.

  * **color** (_Sequence_ _[__float_ _]_) – Color of the circle (RGBA). To use transparency blend must be set to `ALPHA`, see: [`gpu.state.blend_set()`](../gpu/gpu.state.md#gpu.state.blend_set "gpu.state.blend_set").

  * **radius** (_float_) – Radius of the circle.

  * **segments** (_int_ _|__None_) – How many segments will be used to draw the circle. Higher values give better results but the drawing will take longer. If None or not specified, an automatic value will be calculated.


gpu_extras.presets.draw_texture_2d(_texture_ , _position_ , _width_ , _height_ , _is_scene_linear_with_rec709_srgb_target =False_)
    

Draw a 2d texture.

Parameters:
    

  * **texture** ([`gpu.types.GPUTexture`](../gpu/gpu.types.md#gpu.types.GPUTexture "gpu.types.GPUTexture")) – GPUTexture to draw (e.g. gpu.texture.from_image(image) for [`bpy.types.Image`](../bpy.types/I/bpy.types.Image.md#bpy.types.Image "bpy.types.Image")).

  * **position** (_2D Vector_) – Position of the lower left corner.

  * **width** (_float_) – Width of the image when drawn (not necessarily the original width of the texture).

  * **height** (_float_) – Height of the image when drawn.

  * **is_scene_linear_with_rec709_srgb_target** (_bool_) – True if the texture is stored in scene linear color space and the destination framebuffer uses the Rec.709 sRGB color space (which is true when drawing textures acquired from [`bpy.types.Image`](../bpy.types/I/bpy.types.Image.md#bpy.types.Image "bpy.types.Image") inside a ‘PRE_VIEW’, ‘POST_VIEW’ or ‘POST_PIXEL’ draw handler). Otherwise the color space is assumed to match the one of the framebuffer. (default=False)


  *[*]: Keyword-only parameters separator (PEP 3102)
