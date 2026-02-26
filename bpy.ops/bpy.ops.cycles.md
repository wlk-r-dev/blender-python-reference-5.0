# Cycles Operators

bpy.ops.cycles.denoise_animation(_*_ , _input_filepath =''_, _output_filepath =''_)
    

Denoise rendered animation sequence using current scene and view layer settings. Requires denoising data passes and output to OpenEXR multilayer files

Parameters:
    

  * **input_filepath** (_string_ _,__(__optional_ _,__never None_ _)_) – Input Filepath, File path for image to denoise. If not specified, uses the render file path and frame range from the scene

  * **output_filepath** (_string_ _,__(__optional_ _,__never None_ _)_) – Output Filepath, If not specified, renders will be denoised in-place


File:
    

[addons_core/cycles/operators.py:49](https://projects.blender.org/blender/blender/src/branch/main/scripts/addons_core/cycles/operators.py#L49)

bpy.ops.cycles.merge_images(_*_ , _input_filepath1 =''_, _input_filepath2 =''_, _output_filepath =''_)
    

Combine OpenEXR multi-layer images rendered with different sample ranges into one image with reduced noise

Parameters:
    

  * **input_filepath1** (_string_ _,__(__optional_ _,__never None_ _)_) – Input Filepath, File path for image to merge

  * **input_filepath2** (_string_ _,__(__optional_ _,__never None_ _)_) – Input Filepath, File path for image to merge

  * **output_filepath** (_string_ _,__(__optional_ _,__never None_ _)_) – Output Filepath, File path for merged image


File:
    

[addons_core/cycles/operators.py:137](https://projects.blender.org/blender/blender/src/branch/main/scripts/addons_core/cycles/operators.py#L137)

bpy.ops.cycles.use_shading_nodes()
    

Enable nodes on a light

File:
    

[addons_core/cycles/operators.py:23](https://projects.blender.org/blender/blender/src/branch/main/scripts/addons_core/cycles/operators.py#L23)
  *[*]: Keyword-only parameters separator (PEP 3102)
