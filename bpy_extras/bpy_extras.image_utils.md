# bpy_extras submodule (bpy_extras.image_utils)

bpy_extras.image_utils.load_image(_imagepath_ , _dirname =''_, _place_holder =False_, _recursive =False_, _ncase_cmp =True_, _convert_callback =None_, _verbose =False_, _relpath =None_, _check_existing =False_, _force_reload =False_)
    

Return an image from the file path with options to search multiple paths and return a placeholder if its not found.

Parameters:
    

  * **filepath** (_str_) – The image filename If a path precedes it, this will be searched as well.

  * **dirname** (_str_) – is the directory where the image may be located - any file at the end will be ignored.

  * **place_holder** (_bool_) – if True a new place holder image will be created. this is useful so later you can relink the image to its original data.

  * **recursive** (_bool_) – If True, directories will be recursively searched. Be careful with this if you have files in your root directory because it may take a long time.

  * **ncase_cmp** (_bool_) – on non windows systems, find the correct case for the file.

  * **convert_callback** (_function_) – a function that takes an existing path and returns a new one. Use this when loading image formats blender may not support, the CONVERT_CALLBACK can take the path for a GIF (for example), convert it to a PNG and return the PNG’s path. For formats blender can read, simply return the path that is given.

  * **relpath** (_str_ _|__None_) – If not None, make the file relative to this path.

  * **check_existing** (_bool_) – If true, returns already loaded image data-block if possible (based on file path).

  * **force_reload** (_bool_) – If true, force reloading of image (only useful when `check_existing` is also enabled).


Returns:
    

an image or None

Return type:
    

[`bpy.types.Image`](../bpy.types/I/bpy.types.Image.md#bpy.types.Image "bpy.types.Image") | None
