# GPU Types (gpu.types)

_class _gpu.types.Buffer(_format_ , _dimensions_ , _data_)
    

For Python access to GPU functions requiring a pointer.

Parameters:
    

  * **format** (_str_) – Format type to interpret the buffer. Possible values are `FLOAT`, `INT`, `UINT`, `UBYTE`, `UINT_24_8` & `10_11_11_REV`. `UINT_24_8` is deprecated, use `FLOAT` instead.

  * **dimensions** (_int_) – Array describing the dimensions.

  * **data** (_Buffer_ _|__Sequence_ _[__float_ _]__|__Sequence_ _[__int_ _]_) – Optional data array.


return the buffer as a list

dimensions
    

Undocumented, consider [contributing](https://developer.blender.org/).

_class _gpu.types.GPUBatch(_type_ , _buf_ , _elem =None_)
    

Reusable container for drawable geometry.

Parameters:
    

  * **type** (_str_) – The primitive type of geometry to be drawn. Possible values are `POINTS`, `LINES`, `TRIS`, `LINE_STRIP`, `LINE_LOOP`, `TRI_STRIP`, `TRI_FAN`, `LINES_ADJ`, `TRIS_ADJ` and `LINE_STRIP_ADJ`.

  * **buf** (`gpu.types.GPUVertBuf`) – Vertex buffer containing all or some of the attributes required for drawing.

  * **elem** (`gpu.types.GPUIndexBuf`) – An optional index buffer.


draw(_shader =None_)
    

Run the drawing shader with the parameters assigned to the batch.

Parameters:
    

**shader** – Shader that performs the drawing operations. If `None` is passed, the last shader set to this batch will run.

draw_instanced(_program_ , _*_ , _instance_start =0_, _instance_count =0_)
    

Draw multiple instances of the drawing program with the parameters assigned to the batch. In the vertex shader, `gl_InstanceID` will contain the instance number being drawn.

Parameters:
    

  * **program** (`gpu.types.GPUShader`) – Program that performs the drawing operations.

  * **instance_start** (_int_) – Number of the first instance to draw.

  * **instance_count** (_int_) – Number of instances to draw. When not provided or set to 0 the number of instances will be determined by the number of rows in the first vertex buffer.


draw_range(_program_ , _*_ , _elem_start =0_, _elem_count =0_)
    

Run the drawing program with the parameters assigned to the batch. Only draw the `elem_count` elements of the index buffer starting at `elem_start`.

Parameters:
    

  * **program** (`gpu.types.GPUShader`) – Program that performs the drawing operations.

  * **elem_start** (_int_) – First index to draw. When not provided or set to 0 drawing will start from the first element of the index buffer.

  * **elem_count** (_int_) – Number of elements of the index buffer to draw. When not provided or set to 0 all elements from `elem_start` to the end of the index buffer will be drawn.


program_set(_program_)
    

Assign a shader to this batch that will be used for drawing when not overwritten later. Note: This method has to be called in the draw context that the batch will be drawn in. This function does not need to be called when you always set the shader when calling `gpu.types.GPUBatch.draw()`.

Parameters:
    

**program** (`gpu.types.GPUShader`) – The program/shader the batch will use in future draw calls.

vertbuf_add(_buf_)
    

Add another vertex buffer to the Batch. It is not possible to add more vertices to the batch using this method. Instead it can be used to add more attributes to the existing vertices. A good use case would be when you have a separate vertex buffer for vertex positions and vertex normals. Current a batch can have at most GPU_BATCH_VBO_MAX_LEN vertex buffers.

Parameters:
    

**buf** (`gpu.types.GPUVertBuf`) – The vertex buffer that will be added to the batch.

_class _gpu.types.GPUFrameBuffer(_*_ , _depth_slot =None_, _color_slots =None_)
    

This object gives access to framebuffer functionalities. When a ‘layer’ is specified in a argument, a single layer of a 3D or array texture is attached to the frame-buffer. For cube map textures, layer is translated into a cube map face.

Parameters:
    

  * **depth_slot** (`gpu.types.GPUTexture` | dict[] | None) – GPUTexture to attach or a `dict` containing keywords: ‘texture’, ‘layer’ and ‘mip’.

  * **color_slots** (`gpu.types.GPUTexture` | dict[str, int | `gpu.types.GPUTexture`] | Sequence[`gpu.types.GPUTexture` | dict[str, int | `gpu.types.GPUTexture`]] | None) – Tuple where each item can be a GPUTexture or a `dict` containing keywords: ‘texture’, ‘layer’ and ‘mip’.


bind()
    

Context manager to ensure balanced bind calls, even in the case of an error.

clear(_*_ , _color =None_, _depth =None_, _stencil =None_)
    

Fill color, depth and stencil textures with specific value. Common values: color=(0.0, 0.0, 0.0, 1.0), depth=1.0, stencil=0.

Parameters:
    

  * **color** (_Sequence_ _[__float_ _]_) – Sequence of 3 or 4 floats representing `(r, g, b, a)`.

  * **depth** (_float_) – depth value.

  * **stencil** (_int_) – stencil value.


read_color(_x_ , _y_ , _xsize_ , _ysize_ , _channels_ , _slot_ , _format_ , _*_ , _data =data_)
    

Read a block of pixels from the frame buffer.

Parameters:
    

  * **y** (_x_ _,_) – Lower left corner of a rectangular block of pixels.

  * **ysize** (_xsize_ _,_) – Dimensions of the pixel rectangle.

  * **channels** (_int_) – Number of components to read.

  * **slot** (_int_) – The framebuffer slot to read data from.

  * **format** (_str_) – The format that describes the content of a single channel. Possible values are `FLOAT`, `INT`, `UINT`, `UBYTE`, `UINT_24_8` & `10_11_11_REV`. `UINT_24_8` is deprecated, use `FLOAT` instead.

  * **data** (`gpu.types.Buffer`) – Optional Buffer object to fill with the pixels values.


Returns:
    

The Buffer with the read pixels.

Return type:
    

`gpu.types.Buffer`

read_depth(_x_ , _y_ , _xsize_ , _ysize_ , _*_ , _data =data_)
    

Read a pixel depth block from the frame buffer.

Parameters:
    

  * **y** (_x_ _,_) – Lower left corner of a rectangular block of pixels.

  * **ysize** (_xsize_ _,_) – Dimensions of the pixel rectangle.

  * **data** (`gpu.types.Buffer`) – Optional Buffer object to fill with the pixels values.


Returns:
    

The Buffer with the read pixels.

Return type:
    

`gpu.types.Buffer`

viewport_get()
    

Returns position and dimension to current viewport.

viewport_set(_x_ , _y_ , _xsize_ , _ysize_)
    

Set the viewport for this framebuffer object. Note: The viewport state is not saved upon framebuffer rebind.

Parameters:
    

  * **y** (_x_ _,_) – lower left corner of the viewport_set rectangle, in pixels.

  * **ysize** (_xsize_ _,_) – width and height of the viewport_set.


is_bound
    

Checks if this is the active frame-buffer in the context.

_class _gpu.types.GPUIndexBuf(_type_ , _seq_)
    

Contains an index buffer.

Parameters:
    

  * **type** (_str_) – The primitive type this index buffer is composed of. Possible values are [`POINTS`, `LINES`, `TRIS`, `LINES_ADJ`, `TRIS_ADJ`].

  * **seq** (_Buffer_ _|__Sequence_ _[__int_ _]__|__Sequence_ _[__Sequence_ _[__int_ _]__]_) – Indices this index buffer will contain. Whether a 1D or 2D sequence is required depends on the type. Optionally the sequence can support the buffer protocol.


_class _gpu.types.GPUOffScreen(_width_ , _height_ , _*_ , _format ='RGBA8'_)
    

This object gives access to off screen buffers.

Parameters:
    

  * **width** (_int_) – Horizontal dimension of the buffer.

  * **height** (_int_) – Vertical dimension of the buffer.

  * **format** (_str_) – Internal data format inside GPU memory for color attachment texture. Possible values are: `RGBA8`, `RGBA16`, `RGBA16F`, `RGBA32F`.


bind()
    

Context manager to ensure balanced bind calls, even in the case of an error.

draw_view3d(_scene_ , _view_layer_ , _view3d_ , _region_ , _view_matrix_ , _projection_matrix_ , _*_ , _do_color_management =False_, _draw_background =True_)
    

Draw the 3d viewport in the offscreen object.

Parameters:
    

  * **scene** ([`bpy.types.Scene`](../bpy.types/S/bpy.types.Scene.md#bpy.types.Scene "bpy.types.Scene")) – Scene to draw.

  * **view_layer** ([`bpy.types.ViewLayer`](../bpy.types/V/bpy.types.ViewLayer.md#bpy.types.ViewLayer "bpy.types.ViewLayer")) – View layer to draw.

  * **view3d** ([`bpy.types.SpaceView3D`](../bpy.types/S/bpy.types.SpaceView3D.md#bpy.types.SpaceView3D "bpy.types.SpaceView3D")) – 3D View to get the drawing settings from.

  * **region** ([`bpy.types.Region`](../bpy.types/R/bpy.types.Region.md#bpy.types.Region "bpy.types.Region")) – Region of the 3D View (required as temporary draw target).

  * **view_matrix** ([`mathutils.Matrix`](mathutils.md#mathutils.Matrix "mathutils.Matrix")) – View Matrix (e.g. `camera.matrix_world.inverted()`).

  * **projection_matrix** ([`mathutils.Matrix`](mathutils.md#mathutils.Matrix "mathutils.Matrix")) – Projection Matrix (e.g. `camera.calc_matrix_camera(...)`).

  * **do_color_management** (_bool_) – Color manage the output.

  * **draw_background** (_bool_) – Draw background.


free()
    

Free the offscreen object. The framebuffer, texture and render objects will no longer be accessible.

unbind(_*_ , _restore =True_)
    

Unbind the offscreen object.

Parameters:
    

**restore** (_bool_) – Restore the OpenGL state, can only be used when the state has been saved before.

height
    

Height of the texture.

Type:
    

int

texture_color
    

The color texture attached.

Type:
    

`gpu.types.GPUTexture`

width
    

Width of the texture.

Type:
    

int

_class _gpu.types.GPUShader
    

attr_from_name(_name_)
    

Get attribute location by name.

Parameters:
    

**name** (_str_) – The name of the attribute variable whose location is to be queried.

Returns:
    

The location of an attribute variable.

Return type:
    

int

attrs_info_get()
    

Information about the attributes used in the Shader.

Returns:
    

tuples containing information about the attributes in order (name, type)

Return type:
    

tuple[tuple[str, str | None], …]

bind()
    

Bind the shader object. Required to be able to change uniforms of this shader.

format_calc()
    

Build a new format based on the attributes of the shader.

Returns:
    

vertex attribute format for the shader

Return type:
    

`gpu.types.GPUVertFormat`

image(_name_ , _texture_)
    

Specify the value of an image variable for the current GPUShader.

Parameters:
    

  * **name** (_str_) – Name of the image variable to which the texture is to be bound.

  * **texture** (`gpu.types.GPUTexture`) – Texture to attach.


uniform_block(_name_ , _ubo_)
    

Specify the value of an uniform buffer object variable for the current GPUShader.

Parameters:
    

  * **name** (_str_) – name of the uniform variable whose UBO is to be specified.

  * **ubo** – Uniform Buffer to attach.


uniform_block_from_name(_name_)
    

Get uniform block location by name.

Parameters:
    

**name** (_str_) – Name of the uniform block variable whose location is to be queried.

Returns:
    

The location of the uniform block variable.

Return type:
    

int

uniform_bool(_name_ , _value_)
    

Specify the value of a uniform variable for the current program object.

Parameters:
    

  * **name** (_str_) – Name of the uniform variable whose value is to be changed.

  * **value** (_bool_ _|__Sequence_ _[__bool_ _]_) – Value that will be used to update the specified uniform variable.


uniform_float(_name_ , _value_)
    

Specify the value of a uniform variable for the current program object.

Parameters:
    

  * **name** (_str_) – Name of the uniform variable whose value is to be changed.

  * **value** (_float_ _|__Sequence_ _[__float_ _]_) – Value that will be used to update the specified uniform variable.


uniform_from_name(_name_)
    

Get uniform location by name.

Parameters:
    

**name** (_str_) – Name of the uniform variable whose location is to be queried.

Returns:
    

Location of the uniform variable.

Return type:
    

int

uniform_int(_name_ , _seq_)
    

Specify the value of a uniform variable for the current program object.

Parameters:
    

  * **name** (_str_) – name of the uniform variable whose value is to be changed.

  * **seq** (_Sequence_ _[__int_ _]_) – Value that will be used to update the specified uniform variable.


uniform_sampler(_name_ , _texture_)
    

Specify the value of a texture uniform variable for the current GPUShader.

Parameters:
    

  * **name** (_str_) – name of the uniform variable whose texture is to be specified.

  * **texture** (`gpu.types.GPUTexture`) – Texture to attach.


uniform_vector_float(_location_ , _buffer_ , _length_ , _count_)
    

Set the buffer to fill the uniform.

Parameters:
    

  * **location** (_int_) – Location of the uniform variable to be modified.

  * **buffer** (_Sequence_ _[__float_ _]_) – The data that should be set. Can support the buffer protocol.

  * **length** (_int_) – 

Size of the uniform data type:

    * 1: float

    * 2: vec2 or float[2]

    * 3: vec3 or float[3]

    * 4: vec4 or float[4]

    * 9: mat3

    * 16: mat4

  * **count** (_int_) – Specifies the number of elements, vector or matrices that are to be modified.


uniform_vector_int(_location_ , _buffer_ , _length_ , _count_)
    

See GPUShader.uniform_vector_float(…) description.

name
    

The name of the shader object for debugging purposes (read-only).

Type:
    

str

program
    

The name of the program object for use by the OpenGL API (read-only). This is deprecated and will always return -1.

Type:
    

int

_class _gpu.types.GPUShaderCreateInfo
    

Stores and describes types and variables that are used in shader sources.

compute_source(_source_)
    

compute shader source code written in GLSL.

Example:
    
    
    """void main() {
       int2 index = int2(gl_GlobalInvocationID.xy);
       vec4 color = vec4(0.0, 0.0, 0.0, 1.0);
       imageStore(img_output, index, color);
    }"""
    

Parameters:
    

**source** (_str_) – The compute shader source code.

See also

[GLSL Cross Compilation](https://developer.blender.org/docs/features/gpu/glsl_cross_compilation/)

define(_name_ , _value_)
    

Add a preprocessing define directive. In GLSL it would be something like:
    
    
    #define name value
    

Parameters:
    

  * **name** (_str_) – Token name.

  * **value** (_str_) – Text that replaces token occurrences.


depth_write(_value_)
    

Specify a depth write behavior when modifying gl_FragDepth.

There is a common optimization for GPUs that relies on an early depth test to be run before the fragment shader so that the shader evaluation can be skipped if the fragment ends up being discarded because it is occluded.

This optimization does not affect the final rendering, and is typically possible when the fragment does not change the depth programmatically. There are, however a class of operations on the depth in the shader which could still be performed while allowing the early depth test to operate.

This function alters the behavior of the optimization to allow those operations to be performed.

Parameters:
    

**value** – Depth write value. It can be ‘UNCHANGED’ (default), ‘ANY’, ‘GREATER’ or ‘LESS’. :UNCHANGED: disables depth write in a fragment shader and execution of thefragments can be optimized away. :ANY: enables depth write in a fragment shader for any fragments :GREATER: enables depth write in a fragment shader for depth values thatare greater than the depth value in the output buffer. :LESS: enables depth write in a fragment shader for depth values thatare less than the depth value in the output buffer.

fragment_out(_slot_ , _type_ , _name_ , _*_ , _blend ='NONE'_)
    

Specify a fragment output corresponding to a framebuffer target slot.

Parameters:
    

  * **slot** (_int_) – The attribute index.

  * **type** (_str_) – 

One of these types:

    * `FLOAT`

    * `VEC2`

    * `VEC3`

    * `VEC4`

    * `MAT3`

    * `MAT4`

    * `UINT`

    * `UVEC2`

    * `UVEC3`

    * `UVEC4`

    * `INT`

    * `IVEC2`

    * `IVEC3`

    * `IVEC4`

    * `BOOL`

  * **name** (_str_) – Name of the attribute.

  * **blend** (_str_) – Dual Source Blending Index. It can be ‘NONE’, ‘SRC_0’ or ‘SRC_1’.


fragment_source(_source_)
    

Fragment shader source code written in GLSL.

Example:
    
    
    "void main {fragColor = vec4(0.0, 0.0, 0.0, 1.0);}"
    

Parameters:
    

**source** (_str_) – The fragment shader source code.

See also

[GLSL Cross Compilation](https://developer.blender.org/docs/features/gpu/glsl_cross_compilation/)

image(_slot_ , _format_ , _type_ , _name_ , _*_ , _qualifiers ={'NO_RESTRICT'}_)
    

Specify an image resource used for arbitrary load and store operations.

Parameters:
    

  * **slot** (_int_) – The image resource index.

  * **format** (_str_) – 

The GPUTexture format that is passed to the shader. Possible values are:

    * `RGBA8UI`

    * `RGBA8I`

    * `RGBA8`

    * `RGBA32UI`

    * `RGBA32I`

    * `RGBA32F`

    * `RGBA16UI`

    * `RGBA16I`

    * `RGBA16F`

    * `RGBA16`

    * `RG8UI`

    * `RG8I`

    * `RG8`

    * `RG32UI`

    * `RG32I`

    * `RG32F`

    * `RG16UI`

    * `RG16I`

    * `RG16F`

    * `RG16`

    * `R8UI`

    * `R8I`

    * `R8`

    * `R32UI`

    * `R32I`

    * `R32F`

    * `R16UI`

    * `R16I`

    * `R16F`

    * `R16`

    * `R11F_G11F_B10F`

    * `DEPTH32F_STENCIL8`

    * `DEPTH24_STENCIL8` (deprecated, use `DEPTH32F_STENCIL8`)

    * `SRGB8_A8`

    * `RGB16F`

    * `SRGB8_A8_DXT1`

    * `SRGB8_A8_DXT3`

    * `SRGB8_A8_DXT5`

    * `RGBA8_DXT1`

    * `RGBA8_DXT3`

    * `RGBA8_DXT5`

    * `DEPTH_COMPONENT32F`

    * `DEPTH_COMPONENT24` (deprecated, use `DEPTH_COMPONENT32F`)

    * `DEPTH_COMPONENT16`

  * **type** (_str_) – 

The data type describing how the image is to be read in the shader. Possible values are:

    * `FLOAT_BUFFER`

    * `FLOAT_1D`

    * `FLOAT_1D_ARRAY`

    * `FLOAT_2D`

    * `FLOAT_2D_ARRAY`

    * `FLOAT_3D`

    * `FLOAT_CUBE`

    * `FLOAT_CUBE_ARRAY`

    * `INT_BUFFER`

    * `INT_1D`

    * `INT_1D_ARRAY`

    * `INT_2D`

    * `INT_2D_ARRAY`

    * `INT_3D`

    * `INT_CUBE`

    * `INT_CUBE_ARRAY`

    * `UINT_BUFFER`

    * `UINT_1D`

    * `UINT_1D_ARRAY`

    * `UINT_2D`

    * `UINT_2D_ARRAY`

    * `UINT_3D`

    * `UINT_CUBE`

    * `UINT_CUBE_ARRAY`

    * `SHADOW_2D`

    * `SHADOW_2D_ARRAY`

    * `SHADOW_CUBE`

    * `SHADOW_CUBE_ARRAY`

    * `DEPTH_2D`

    * `DEPTH_2D_ARRAY`

    * `DEPTH_CUBE`

    * `DEPTH_CUBE_ARRAY`

  * **name** (_str_) – The image resource name.

  * **qualifiers** (_set_ _[__str_ _]_) – Set containing values that describe how the image resource is to be read or written. Possible values are: \- `NO_RESTRICT` \- `READ` \- `WRITE`


local_group_size(_x_ , _y =1_, _z =1_)
    

Specify the local group size for compute shaders.

Parameters:
    

  * **x** (_int_) – The local group size in the x dimension.

  * **y** (_int_) – The local group size in the y dimension. Optional. Defaults to 1.

  * **z** (_int_) – The local group size in the z dimension. Optional. Defaults to 1.


push_constant(_type_ , _name_ , _size =0_)
    

Specify a global access constant.

Parameters:
    

  * **type** (_str_) – 

One of these types:

    * `FLOAT`

    * `VEC2`

    * `VEC3`

    * `VEC4`

    * `MAT3`

    * `MAT4`

    * `UINT`

    * `UVEC2`

    * `UVEC3`

    * `UVEC4`

    * `INT`

    * `IVEC2`

    * `IVEC3`

    * `IVEC4`

    * `BOOL`

  * **name** (_str_) – Name of the constant.

  * **size** (_int_) – If not zero, indicates that the constant is an array with the specified size.


sampler(_slot_ , _type_ , _name_)
    

Specify an image texture sampler.

Parameters:
    

  * **slot** (_int_) – The image texture sampler index.

  * **type** (_str_) – 

The data type describing the format of each sampler unit. Possible values are:

    * `FLOAT_BUFFER`

    * `FLOAT_1D`

    * `FLOAT_1D_ARRAY`

    * `FLOAT_2D`

    * `FLOAT_2D_ARRAY`

    * `FLOAT_3D`

    * `FLOAT_CUBE`

    * `FLOAT_CUBE_ARRAY`

    * `INT_BUFFER`

    * `INT_1D`

    * `INT_1D_ARRAY`

    * `INT_2D`

    * `INT_2D_ARRAY`

    * `INT_3D`

    * `INT_CUBE`

    * `INT_CUBE_ARRAY`

    * `UINT_BUFFER`

    * `UINT_1D`

    * `UINT_1D_ARRAY`

    * `UINT_2D`

    * `UINT_2D_ARRAY`

    * `UINT_3D`

    * `UINT_CUBE`

    * `UINT_CUBE_ARRAY`

    * `SHADOW_2D`

    * `SHADOW_2D_ARRAY`

    * `SHADOW_CUBE`

    * `SHADOW_CUBE_ARRAY`

    * `DEPTH_2D`

    * `DEPTH_2D_ARRAY`

    * `DEPTH_CUBE`

    * `DEPTH_CUBE_ARRAY`

  * **name** (_str_) – The image texture sampler name.


typedef_source(_source_)
    

Source code included before resource declaration. Useful for defining structs used by Uniform Buffers.

Example:
    
    
    "struct MyType {int foo; float bar;};"
    

Parameters:
    

**source** (_str_) – The source code defining types.

uniform_buf(_slot_ , _type_name_ , _name_)
    

Specify a uniform variable whose type can be one of those declared in `gpu.types.GPUShaderCreateInfo.typedef_source()`.

Parameters:
    

  * **slot** (_int_) – The uniform variable index.

  * **type_name** (_str_) – Name of the data type. It can be a struct type defined in the source passed through the `gpu.types.GPUShaderCreateInfo.typedef_source()`.

  * **name** (_str_) – The uniform variable name.


vertex_in(_slot_ , _type_ , _name_)
    

Add a vertex shader input attribute.

Parameters:
    

  * **slot** (_int_) – The attribute index.

  * **type** (_str_) – 

One of these types:

    * `FLOAT`

    * `VEC2`

    * `VEC3`

    * `VEC4`

    * `MAT3`

    * `MAT4`

    * `UINT`

    * `UVEC2`

    * `UVEC3`

    * `UVEC4`

    * `INT`

    * `IVEC2`

    * `IVEC3`

    * `IVEC4`

    * `BOOL`

  * **name** (_str_) – name of the attribute.


vertex_out(_interface_)
    

Add a vertex shader output interface block.

Parameters:
    

**interface** (`gpu.types.GPUStageInterfaceInfo`) – Object describing the block.

vertex_source(_source_)
    

Vertex shader source code written in GLSL.

Example:
    
    
    "void main {gl_Position = vec4(pos, 1.0);}"
    

Parameters:
    

**source** (_str_) – The vertex shader source code.

See also

[GLSL Cross Compilation](https://developer.blender.org/docs/features/gpu/glsl_cross_compilation/)

_class _gpu.types.GPUStageInterfaceInfo(_name_)
    

List of varyings between shader stages.

Parameters:
    

**name** – Name of the interface block.

flat(_type_ , _name_)
    

Add an attribute with qualifier of type `flat` to the interface block.

Parameters:
    

  * **type** (_str_) – 

One of these types:

    * `FLOAT`

    * `VEC2`

    * `VEC3`

    * `VEC4`

    * `MAT3`

    * `MAT4`

    * `UINT`

    * `UVEC2`

    * `UVEC3`

    * `UVEC4`

    * `INT`

    * `IVEC2`

    * `IVEC3`

    * `IVEC4`

    * `BOOL`

  * **name** (_str_) – name of the attribute.


no_perspective(_type_ , _name_)
    

Add an attribute with qualifier of type `no_perspective` to the interface block.

Parameters:
    

  * **type** (_str_) – 

One of these types:

    * `FLOAT`

    * `VEC2`

    * `VEC3`

    * `VEC4`

    * `MAT3`

    * `MAT4`

    * `UINT`

    * `UVEC2`

    * `UVEC3`

    * `UVEC4`

    * `INT`

    * `IVEC2`

    * `IVEC3`

    * `IVEC4`

    * `BOOL`

  * **name** (_str_) – name of the attribute.


smooth(_type_ , _name_)
    

Add an attribute with qualifier of type _smooth_ to the interface block.

Parameters:
    

  * **type** (_str_) – 

One of these types:

    * `FLOAT`

    * `VEC2`

    * `VEC3`

    * `VEC4`

    * `MAT3`

    * `MAT4`

    * `UINT`

    * `UVEC2`

    * `UVEC3`

    * `UVEC4`

    * `INT`

    * `IVEC2`

    * `IVEC3`

    * `IVEC4`

    * `BOOL`

  * **name** (_str_) – name of the attribute.


name
    

Name of the interface block.

Type:
    

str

_class _gpu.types.GPUTexture(_size_ , _*_ , _layers =0_, _is_cubemap =False_, _format ='RGBA8'_, _data =None_)
    

This object gives access to off GPU textures.

Parameters:
    

  * **size** (_int_ _|__Sequence_ _[__int_ _]_) – Dimensions of the texture 1D, 2D, 3D or cubemap.

  * **layers** (_int_) – Number of layers in texture array or number of cubemaps in cubemap array

  * **is_cubemap** (_int_) – Indicates the creation of a cubemap texture.

  * **format** (_str_) – Internal data format inside GPU memory. Possible values are: `RGBA8UI`, `RGBA8I`, `RGBA8`, `RGBA32UI`, `RGBA32I`, `RGBA32F`, `RGBA16UI`, `RGBA16I`, `RGBA16F`, `RGBA16`, `RG8UI`, `RG8I`, `RG8`, `RG32UI`, `RG32I`, `RG32F`, `RG16UI`, `RG16I`, `RG16F`, `RG16`, `R8UI`, `R8I`, `R8`, `R32UI`, `R32I`, `R32F`, `R16UI`, `R16I`, `R16F`, `R16`, `R11F_G11F_B10F`, `DEPTH32F_STENCIL8`, `DEPTH24_STENCIL8` (deprecated, use `DEPTH32F_STENCIL8`), `SRGB8_A8`, `RGB16F`, `SRGB8_A8_DXT1`, `SRGB8_A8_DXT3`, `SRGB8_A8_DXT5`, `RGBA8_DXT1`, `RGBA8_DXT3`, `RGBA8_DXT5`, `DEPTH_COMPONENT32F`, `DEPTH_COMPONENT24`, (deprecated, use `DEPTH_COMPONENT32F`), `DEPTH_COMPONENT16`.

  * **data** (`gpu.types.Buffer`) – Buffer object to fill the texture.


clear(_format ='FLOAT'_, _value =(0.0, 0.0, 0.0, 1.0)_)
    

Fill texture with specific value.

Parameters:
    

  * **format** (_str_) – The format that describes the content of a single item. Possible values are `FLOAT`, `INT`, `UINT`, `UBYTE`, `UINT_24_8` & `10_11_11_REV`. `UINT_24_8` is deprecated, use `FLOAT` instead.

  * **value** (_Sequence_ _[__float_ _]_) – Sequence each representing the value to fill. Sizes 1..4 are supported.


read()
    

Creates a buffer with the value of all pixels.

format
    

Format of the texture.

Type:
    

str

height
    

Height of the texture.

Type:
    

int

width
    

Width of the texture.

Type:
    

int

_class _gpu.types.GPUUniformBuf(_data_)
    

This object gives access to off uniform buffers.

Parameters:
    

**data** (_object exposing buffer interface_) – Data to fill the buffer.

update(_data_)
    

Update the data of the uniform buffer object.

_class _gpu.types.GPUVertBuf(_format_ , _len_)
    

Contains a VBO.

Parameters:
    

  * **format** (`gpu.types.GPUVertFormat`) – Vertex format.

  * **len** (_int_) – Amount of vertices that will fit into this buffer.


attr_fill(_id_ , _data_)
    

Insert data into the buffer for a single attribute.

Parameters:
    

  * **id** (_int_ _|__str_) – Either the name or the id of the attribute.

  * **data** (_Buffer_ _|__Sequence_ _[__float_ _]__|__Sequence_ _[__int_ _]__|__Sequence_ _[__Sequence_ _[__float_ _]__]__|__Sequence_ _[__Sequence_ _[__int_ _]__]_) – Buffer or sequence of data that should be stored in the buffer


_class _gpu.types.GPUVertFormat
    

This object contains information about the structure of a vertex buffer.

attr_add(_id_ , _comp_type_ , _len_ , _fetch_mode_)
    

Add a new attribute to the format.

Parameters:
    

  * **id** (_str_) – Name the attribute. Often `position`, `normal`, …

  * **comp_type** (_str_) – The data type that will be used store the value in memory. Possible values are `I8`, `U8`, `I16`, `U16`, `I32`, `U32`, `F32` & `I10`.

  * **len** (_int_) – How many individual values the attribute consists of (e.g. 2 for uv coordinates).

  * **fetch_mode** (_str_) – How values from memory will be converted when used in the shader. This is mainly useful for memory optimizations when you want to store values with reduced precision. E.g. you can store a float in only 1 byte but it will be converted to a normal 4 byte float when used. Possible values are `FLOAT`, `INT` or `INT_TO_FLOAT_UNIT`.


  *[*]: Keyword-only parameters separator (PEP 3102)
