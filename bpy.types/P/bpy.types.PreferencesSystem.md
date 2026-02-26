# PreferencesSystem(bpy_struct)

base class — [[bpy_struct]]

_class _bpy.types.PreferencesSystem(_bpy_struct_)
    

Graphics driver and operating system settings

anisotropic_filter
    

Quality of anisotropic filtering

Type:
    

enum in [`'FILTER_0'`, `'FILTER_2'`, `'FILTER_4'`, `'FILTER_8'`, `'FILTER_16'`], default `'FILTER_2'`

audio_channels
    

Audio channel count

  * `MONO` Mono – Set audio channels to mono.

  * `STEREO` Stereo – Set audio channels to stereo.

  * `SURROUND4` 4 Channels – Set audio channels to 4 channels.

  * `SURROUND51` 5.1 Surround – Set audio channels to 5.1 surround sound.

  * `SURROUND71` 7.1 Surround – Set audio channels to 7.1 surround sound.


Type:
    

enum in [`'MONO'`, `'STEREO'`, `'SURROUND4'`, `'SURROUND51'`, `'SURROUND71'`], default `'STEREO'`

audio_device
    

Audio output device

  * `None` None – No device - there will be no audio output.


Type:
    

enum in [`'None'`], default `'None'`

audio_mixing_buffer
    

Number of samples used by the audio mixing buffer

  * `SAMPLES_256` 256 Samples – Set audio mixing buffer size to 256 samples.

  * `SAMPLES_512` 512 Samples – Set audio mixing buffer size to 512 samples.

  * `SAMPLES_1024` 1024 Samples – Set audio mixing buffer size to 1024 samples.

  * `SAMPLES_2048` 2048 Samples – Set audio mixing buffer size to 2048 samples.

  * `SAMPLES_4096` 4096 Samples – Set audio mixing buffer size to 4096 samples.

  * `SAMPLES_8192` 8192 Samples – Set audio mixing buffer size to 8192 samples.

  * `SAMPLES_16384` 16384 Samples – Set audio mixing buffer size to 16384 samples.

  * `SAMPLES_32768` 32768 Samples – Set audio mixing buffer size to 32768 samples.


Type:
    

enum in [`'SAMPLES_256'`, `'SAMPLES_512'`, `'SAMPLES_1024'`, `'SAMPLES_2048'`, `'SAMPLES_4096'`, `'SAMPLES_8192'`, `'SAMPLES_16384'`, `'SAMPLES_32768'`], default `'SAMPLES_2048'`

audio_sample_format
    

Audio sample format

  * `U8` 8-bit Unsigned – Set audio sample format to 8-bit unsigned integer.

  * `S16` 16-bit Signed – Set audio sample format to 16-bit signed integer.

  * `S24` 24-bit Signed – Set audio sample format to 24-bit signed integer.

  * `S32` 32-bit Signed – Set audio sample format to 32-bit signed integer.

  * `FLOAT` 32-bit Float – Set audio sample format to 32-bit float.

  * `DOUBLE` 64-bit Float – Set audio sample format to 64-bit float.


Type:
    

enum in [`'U8'`, `'S16'`, `'S24'`, `'S32'`, `'FLOAT'`, `'DOUBLE'`], default `'FLOAT'`

audio_sample_rate
    

Audio sample rate

  * `RATE_44100` 44.1 kHz – Set audio sampling rate to 44100 samples per second.

  * `RATE_48000` 48 kHz – Set audio sampling rate to 48000 samples per second.

  * `RATE_96000` 96 kHz – Set audio sampling rate to 96000 samples per second.

  * `RATE_192000` 192 kHz – Set audio sampling rate to 192000 samples per second.


Type:
    

enum in [`'RATE_44100'`, `'RATE_48000'`, `'RATE_96000'`, `'RATE_192000'`], default `'RATE_48000'`

dpi
    

Type:
    

int in [-inf, inf], default 0, (readonly)

gl_clip_alpha
    

Clip alpha below this threshold in the 3D textured view

Type:
    

float in [0, 1], default 0.004

gl_texture_limit
    

Limit the texture size to save graphics memory

Type:
    

enum in [`'CLAMP_OFF'`, `'CLAMP_8192'`, `'CLAMP_4096'`, `'CLAMP_2048'`, `'CLAMP_1024'`, `'CLAMP_512'`, `'CLAMP_256'`, `'CLAMP_128'`], default `'CLAMP_OFF'`

gpu_backend
    

GPU backend to use (requires restarting Blender for changes to take effect)

  * `OPENGL` OpenGL – Use OpenGL backend.

  * `METAL` Metal – Use Metal backend.

  * `VULKAN` Vulkan – Use Vulkan backend.


Type:
    

enum in [`'OPENGL'`, `'METAL'`, `'VULKAN'`], default `'OPENGL'`

gpu_preferred_device
    

Preferred device to select during detection (requires restarting Blender for changes to take effect)

  * `AUTO` Auto – Auto detect best GPU for running Blender.


Type:
    

enum in [`'AUTO'`], default `'AUTO'`

gpu_shader_workers
    

Number of shader compilation threads or subprocesses, clamped at the max threads supported by the CPU (requires restarting Blender for changes to take effect). A higher number increases the RAM usage while reducing compilation time. A value of 0 will use automatic configuration. (OpenGL only)

Type:
    

int in [0, 32], default 0

image_draw_method
    

Method used for displaying images on the screen

  * `AUTO` Automatic – Automatically choose method based on GPU and image.

  * `2DTEXTURE` 2D Texture – Use CPU for display transform and display image with 2D texture.

  * `GLSL` GLSL – Use GLSL shaders for display transform and display image with 2D texture.


Type:
    

enum in [`'AUTO'`, `'2DTEXTURE'`, `'GLSL'`], default `'AUTO'`

is_microsoft_store_install
    

Whether this blender installation is a sandboxed Microsoft Store version

Type:
    

boolean, default False, (readonly)

legacy_compute_device_type
    

For backwards compatibility only

Type:
    

int in [-inf, inf], default 0, (readonly)

light_ambient
    

Color of the ambient light that uniformly lit the scene

Type:
    

[[mathutils.Color]] of 3 items in [0, inf], default (0.0, 0.0, 0.0)

memory_cache_limit
    

Memory cache limit (in megabytes)

Type:
    

int in [0, inf], default 4096

network_connection_limit
    

Limit the number of simultaneous internet connections online operations may make at once. Zero disables the limit.

Type:
    

int in [0, 255], default 0

network_timeout
    

The time in seconds to wait for online operations before a connection may fail with a time-out error. Zero uses the systems default.

Type:
    

int in [0, 255], default 0

pixel_size
    

Type:
    

float in [-inf, inf], default 1.0, (readonly)

register_all_users
    

Make this Blender version open blend files for all users. Requires elevated privileges.

Type:
    

boolean, default False

scrollback
    

Maximum number of lines to store for the console buffer

Type:
    

int in [32, 32768], default 256

sequencer_proxy_setup
    

When and how proxies are created

  * `MANUAL` Manual – Set up proxies manually.

  * `AUTOMATIC` Automatic – Build proxies for added movie and image strips in each preview size.


Type:
    

enum in [`'MANUAL'`, `'AUTOMATIC'`], default `'AUTOMATIC'`

shader_compilation_method
    

Compilation method used for compiling shaders in parallel. Subprocess requires a lot more RAM for each worker but might compile shaders faster on some systems. Requires restarting Blender for changes to take effect. (OpenGL only)

  * `THREAD` Thread – Use threads for compiling shaders.

  * `SUBPROCESS` Subprocess – Use subprocesses for compiling shaders.


Type:
    

enum in [`'THREAD'`, `'SUBPROCESS'`], default `'THREAD'`

solid_lights
    

Lights used to display objects in solid shading mode

Type:
    

[[bpy_prop_collection]] of [[UserSolidLight]], (readonly)

texture_collection_rate
    

Number of seconds between each run of the GL texture garbage collector

Type:
    

int in [1, 3600], default 60

texture_time_out
    

Time since last access of a GL texture in seconds after which it is freed (set to 0 to keep textures allocated)

Type:
    

int in [0, 3600], default 120

ui_line_width
    

Suggested line thickness and point size in pixels, for add-ons displaying custom user interface elements, based on operating system settings and Blender UI scale

Type:
    

float in [-inf, inf], default 1.0, (readonly)

ui_scale
    

Size multiplier to use when displaying custom user interface elements, so that they are scaled correctly on screens with different DPI. This value is based on operating system DPI settings and Blender display scale.

Type:
    

float in [-inf, inf], default 0.0, (readonly)

use_edit_mode_smooth_wire
    

Enable edit mode edge smoothing, reducing aliasing (requires restart)

Type:
    

boolean, default True

use_gpu_subdivision
    

Enable GPU acceleration for evaluating the last subdivision surface modifiers in the stack

Type:
    

boolean, default True

use_online_access
    

Allow Blender to access the internet. Add-ons that follow this setting will only connect to the internet if enabled. However, Blender cannot prevent third-party add-ons from violating this rule.

Type:
    

boolean, default False

use_overlay_smooth_wire
    

Enable overlay smooth wires, reducing aliasing

Type:
    

boolean, default True

use_region_overlap
    

Display tool/property regions over the main region

Type:
    

boolean, default True

use_studio_light_edit
    

View the result of the studio light editor in the viewport

Type:
    

boolean, default False

vbo_collection_rate
    

Number of seconds between each run of the GL vertex buffer object garbage collector

Type:
    

int in [1, 3600], default 60

vbo_time_out
    

Time since last access of a GL vertex buffer object in seconds after which it is freed (set to 0 to keep VBO allocated)

Type:
    

int in [0, 3600], default 120

viewport_aa
    

Method of anti-aliasing in 3d viewport

  * `OFF` No Anti-Aliasing – Scene will be rendering without any anti-aliasing.

  * `FXAA` Single Pass Anti-Aliasing – Scene will be rendered using a single pass anti-aliasing method (FXAA).

  * `5` 5 Samples – Scene will be rendered using 5 anti-aliasing samples.

  * `8` 8 Samples – Scene will be rendered using 8 anti-aliasing samples.

  * `11` 11 Samples – Scene will be rendered using 11 anti-aliasing samples.

  * `16` 16 Samples – Scene will be rendered using 16 anti-aliasing samples.

  * `32` 32 Samples – Scene will be rendered using 32 anti-aliasing samples.


Type:
    

enum in [`'OFF'`, `'FXAA'`, `'5'`, `'8'`, `'11'`, `'16'`, `'32'`], default `'8'`

_classmethod _bl_rna_get_subclass(_id_ , _default =None_, _/_)
    

Parameters:
    

**id** (_str_) – The RNA type identifier.

Returns:
    

The RNA type or default when not found.

Return type:
    

[[bpy.types.Struct]] subclass

_classmethod _bl_rna_get_subclass_py(_id_ , _default =None_, _/_)
    

Parameters:
    

**id** (_str_) – The RNA type identifier.

Returns:
    

The class or default when not found.

Return type:
    

type

## Inherited Properties

  * [[bpy_struct.id_data]]

| 


  
---|---  
  
## Inherited Functions

  * [[bpy_struct.as_pointer]]
  * [[bpy_struct.driver_add]]
  * [[bpy_struct.driver_remove]]
  * [[bpy_struct.get]]
  * [[bpy_struct.id_properties_clear]]
  * [[bpy_struct.id_properties_ensure]]
  * [[bpy_struct.id_properties_ui]]
  * [[bpy_struct.is_property_hidden]]
  * [[bpy_struct.is_property_overridable_library]]
  * [[bpy_struct.is_property_readonly]]
  * [[bpy_struct.is_property_set]]
  * [[bpy_struct.items]]

| 

  * [[bpy_struct.keyframe_delete]]
  * [[bpy_struct.keyframe_insert]]
  * [[bpy_struct.keys]]
  * [[bpy_struct.path_from_id]]
  * [[bpy_struct.path_from_module]]
  * [[bpy_struct.path_resolve]]
  * [[bpy_struct.pop]]
  * [[bpy_struct.property_overridable_library_set]]
  * [[bpy_struct.property_unset]]
  * [[bpy_struct.rna_ancestors]]
  * [[bpy_struct.type_recast]]
  * [[bpy_struct.values]]

  
---|---  
  
## References

  * [[Preferences.system]]

| 


  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
