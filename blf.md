# Font Drawing (blf)

This module provides access to Blender’s text drawing functions.

## Hello World Text Example

Example of using the blf module. For this module to work we need to use the GPU module [`gpu`](gpu.md#module-gpu "gpu") as well.
    
    
    # Import stand alone modules.
    import blf
    import bpy
    
    font_info = {
        "font_id": 0,
        "handler": None,
    }
    
    
    def init():
        """init function - runs once"""
        import os
        # Create a new font object, use external TTF file.
        font_path = bpy.path.abspath('//Zeyada.ttf')
        # Store the font index - to use later.
        if os.path.exists(font_path):
            font_info["font_id"] = blf.load(font_path)
        else:
            # Default font.
            font_info["font_id"] = 0
    
        # Set the font drawing routine to run every frame.
        font_info["handler"] = bpy.types.SpaceView3D.draw_handler_add(
            draw_callback_px, (None, None), 'WINDOW', 'POST_PIXEL')
    
    
    def draw_callback_px(self, context):
        """Draw on the viewports"""
        # BLF drawing routine.
        font_id = font_info["font_id"]
        blf.position(font_id, 2, 80, 0)
        blf.size(font_id, 50.0)
        blf.draw(font_id, "Hello World")
    
    
    if __name__ == '__main__':
        init()
    

## Drawing Text to an Image

Example showing how text can be draw into an image. This can be done by binding an image buffer ([`imbuf`](imbuf.md#module-imbuf "imbuf")) to the font’s ID.
    
    
    import blf
    import imbuf
    
    image_size = 512, 512
    font_size = 20
    
    ibuf = imbuf.new(image_size)
    
    font_id = blf.load("/path/to/font.ttf")
    
    blf.color(font_id, 1.0, 1.0, 1.0, 1.0)
    blf.size(font_id, font_size)
    blf.position(font_id, 0, image_size[0] - font_size, 0)
    
    blf.enable(font_id, blf.WORD_WRAP)
    blf.word_wrap(font_id, image_size[0])
    
    with blf.bind_imbuf(font_id, ibuf, display_name="sRGB"):
        blf.draw_buffer(font_id, "Lots of wrapped text. " * 50)
    
    imbuf.write(ibuf, filepath="/path/to/image.png")
    

blf.aspect(_fontid_ , _aspect_)
    

Set the aspect for drawing text.

Parameters:
    

  * **fontid** (_int_) – The id of the typeface as returned by `blf.load()`, for default font use 0.

  * **aspect** (_float_) – The aspect ratio for text drawing to use.


blf.bind_imbuf(_fontid_ , _image_)
    

Context manager to draw text into an image buffer instead of the GPU’s context.

Parameters:
    

  * **fontid** (_int_) – The id of the typeface as returned by `blf.load()`, for default font use 0.

  * **imbuf** (`imbuf.types.ImBuf`) – The image to draw into.


Returns:
    

The BLF ImBuf context manager.

Return type:
    

BLFImBufContext

blf.clipping(_fontid_ , _xmin_ , _ymin_ , _xmax_ , _ymax_)
    

Set the clipping, enable/disable using CLIPPING.

Parameters:
    

  * **fontid** (_int_) – The id of the typeface as returned by `blf.load()`, for default font use 0.

  * **xmin** (_float_) – Clip the drawing area by these bounds.

  * **ymin** (_float_) – Clip the drawing area by these bounds.

  * **xmax** (_float_) – Clip the drawing area by these bounds.

  * **ymax** (_float_) – Clip the drawing area by these bounds.


blf.color(_fontid_ , _r_ , _g_ , _b_ , _a_)
    

Set the color for drawing text.

Parameters:
    

  * **fontid** (_int_) – The id of the typeface as returned by `blf.load()`, for default font use 0.

  * **r** (_float_) – red channel 0.0 - 1.0.

  * **g** (_float_) – green channel 0.0 - 1.0.

  * **b** (_float_) – blue channel 0.0 - 1.0.

  * **a** (_float_) – alpha channel 0.0 - 1.0.


blf.dimensions(_fontid_ , _text_)
    

Return the width and height of the text.

Parameters:
    

  * **fontid** (_int_) – The id of the typeface as returned by `blf.load()`, for default font use 0.

  * **text** (_str_) – the text to draw.


Returns:
    

the width and height of the text.

Return type:
    

tuple[float, float]

blf.disable(_fontid_ , _option_)
    

Disable option.

Parameters:
    

  * **fontid** (_int_) – The id of the typeface as returned by `blf.load()`, for default font use 0.

  * **option** (_int_) – One of ROTATION, CLIPPING, SHADOW or KERNING_DEFAULT.


blf.draw(_fontid_ , _text_)
    

Draw text in the current context.

Parameters:
    

  * **fontid** (_int_) – The id of the typeface as returned by `blf.load()`, for default font use 0.

  * **text** (_str_) – the text to draw.


blf.draw_buffer(_fontid_ , _text_)
    

Draw text into the buffer bound to the fontid.

Parameters:
    

  * **fontid** (_int_) – The id of the typeface as returned by `blf.load()`, for default font use 0.

  * **text** (_str_) – the text to draw.


blf.enable(_fontid_ , _option_)
    

Enable option.

Parameters:
    

  * **fontid** (_int_) – The id of the typeface as returned by `blf.load()`, for default font use 0.

  * **option** (_int_) – One of ROTATION, CLIPPING, SHADOW or KERNING_DEFAULT.


blf.load(_filepath_)
    

Load a new font.

Parameters:
    

**filepath** (_str_ _|__bytes_) – the filepath of the font.

Returns:
    

the new font’s fontid or -1 if there was an error.

Return type:
    

int

blf.position(_fontid_ , _x_ , _y_ , _z_)
    

Set the position for drawing text.

Parameters:
    

  * **fontid** (_int_) – The id of the typeface as returned by `blf.load()`, for default font use 0.

  * **x** (_float_) – X axis position to draw the text.

  * **y** (_float_) – Y axis position to draw the text.

  * **z** (_float_) – Z axis position to draw the text.


blf.rotation(_fontid_ , _angle_)
    

Set the text rotation angle, enable/disable using ROTATION.

Parameters:
    

  * **fontid** (_int_) – The id of the typeface as returned by `blf.load()`, for default font use 0.

  * **angle** (_float_) – The angle for text drawing to use.


blf.shadow(_fontid_ , _level_ , _r_ , _g_ , _b_ , _a_)
    

Shadow options, enable/disable using SHADOW .

Parameters:
    

  * **fontid** (_int_) – The id of the typeface as returned by `blf.load()`, for default font use 0.

  * **level** (_int_) – The blur level (0, 3, 5) or outline (6).

  * **r** (_float_) – Shadow color (red channel 0.0 - 1.0).

  * **g** (_float_) – Shadow color (green channel 0.0 - 1.0).

  * **b** (_float_) – Shadow color (blue channel 0.0 - 1.0).

  * **a** (_float_) – Shadow color (alpha channel 0.0 - 1.0).


blf.shadow_offset(_fontid_ , _x_ , _y_)
    

Set the offset for shadow text.

Parameters:
    

  * **fontid** (_int_) – The id of the typeface as returned by `blf.load()`, for default font use 0.

  * **x** (_float_) – Vertical shadow offset value in pixels.

  * **y** (_float_) – Horizontal shadow offset value in pixels.


blf.size(_fontid_ , _size_)
    

Set the size for drawing text.

Parameters:
    

  * **fontid** (_int_) – The id of the typeface as returned by `blf.load()`, for default font use 0.

  * **size** (_float_) – Point size of the font.


blf.unload(_filepath_)
    

Unload an existing font.

Parameters:
    

**filepath** (_str_ _|__bytes_) – the filepath of the font.

blf.word_wrap(_fontid_ , _wrap_width_)
    

Set the wrap width, enable/disable using WORD_WRAP.

Parameters:
    

  * **fontid** (_int_) – The id of the typeface as returned by `blf.load()`, for default font use 0.

  * **wrap_width** (_int_) – The width (in pixels) to wrap words at.


blf.CLIPPING
    

Constant value 2

blf.MONOCHROME
    

Constant value 128

blf.ROTATION
    

Constant value 1

blf.SHADOW
    

Constant value 4

blf.WORD_WRAP
    

Constant value 64
