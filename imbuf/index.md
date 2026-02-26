# Image Buffer (imbuf)

This module provides access to Blender’s image manipulation API.

It provides access to image buffers outside of Blender’s [`bpy.types.Image`](../bpy.types/I/bpy.types.Image.md#bpy.types.Image "bpy.types.Image") data-block context.

Submodules

  * [Image Buffer Types (imbuf.types)](imbuf.types.md)


imbuf.load(_filepath_)
    

Load an image from a file.

Parameters:
    

**filepath** (_str_ _|__bytes_) – the filepath of the image.

Returns:
    

the newly loaded image.

Return type:
    

`ImBuf`

imbuf.load_from_buffer(_buffer_)
    

Load an image from a buffer.

Parameters:
    

**buffer** (_collections.abc.Buffer_) – A buffer containing the image data.

Returns:
    

the newly loaded image.

Return type:
    

`ImBuf`

imbuf.new(_size_)
    

Load a new image.

Parameters:
    

**size** (_tuple_ _[__int_ _,__int_ _]_) – The size of the image in pixels.

Returns:
    

the newly loaded image.

Return type:
    

`ImBuf`

imbuf.write(_image_ , _*_ , _filepath =image.filepath_)
    

Write an image.

Parameters:
    

  * **image** (`ImBuf`) – the image to write.

  * **filepath** (_str_ _|__bytes_ _|__None_) – Optional filepath of the image (fallback to the images file path).


  *[*]: Keyword-only parameters separator (PEP 3102)
