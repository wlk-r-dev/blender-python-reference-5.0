# gpu_extras submodule (gpu_extras.batch)

gpu_extras.batch.batch_for_shader(_shader_ , _type_ , _content_ , _*_ , _indices =None_)
    

Return a batch already configured and compatible with the shader.

Parameters:
    

  * **shader** (`gpu.types.GPUShader`) – shader for which a compatible format will be computed.

  * **type** (_str_) – “‘POINTS’, ‘LINES’, ‘TRIS’ or ‘LINES_ADJ’”.

  * **content** (_dict_ _[__str_ _,__Buffer_ _|__Sequence_ _[__float_ _]__|__Sequence_ _[__int_ _]__|__Sequence_ _[__Sequence_ _[__float_ _]__]__|__Sequence_ _[__Sequence_ _[__int_ _]__]__]_) – Maps the name of the shader attribute with the data to fill the vertex buffer. For the dictionary values see documentation for [`gpu.types.GPUVertBuf.attr_fill`](../gpu/gpu.types.md#gpu.types.GPUVertBuf.attr_fill "gpu.types.GPUVertBuf.attr_fill") data argument.


Returns:
    

compatible batch

Return type:
    

[`gpu.types.GPUBatch`](../gpu/gpu.types.md#gpu.types.GPUBatch "gpu.types.GPUBatch")
  *[*]: Keyword-only parameters separator (PEP 3102)
