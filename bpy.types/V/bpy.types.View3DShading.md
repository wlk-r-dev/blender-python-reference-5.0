# View3DShading(bpy_struct)

base class — [[bpy_struct]]

_class _bpy.types.View3DShading(_bpy_struct_)
    

Settings for shading in the 3D viewport

aov_name
    

Name of the active Shader AOV

Type:
    

string, default “”, (never None)

background_color
    

Color for custom background color

Type:
    

[[mathutils.Color]] of 3 items in [0, 1], default (0.05, 0.05, 0.05)

background_type
    

Way to display the background

  * `THEME` Theme – Use the theme for background color.

  * `WORLD` World – Use the world for background color.

  * `VIEWPORT` Custom – Use a custom color limited to this viewport only.


Type:
    

enum in [`'THEME'`, `'WORLD'`, `'VIEWPORT'`], default `'THEME'`

cavity_ridge_factor
    

Factor for the cavity ridges

Type:
    

float in [0, 250], default 1.0

cavity_type
    

Way to display the cavity shading

  * `WORLD` World – Cavity shading computed in world space, useful for larger-scale occlusion.

  * `SCREEN` Screen – Curvature-based shading, useful for making fine details more visible.

  * `BOTH` Both – Use both effects simultaneously.


Type:
    

enum in [`'WORLD'`, `'SCREEN'`, `'BOTH'`], default `'SCREEN'`

cavity_valley_factor
    

Factor for the cavity valleys

Type:
    

float in [0, 250], default 1.0

color_type
    

Color Type

  * `MATERIAL` Material – Show material color.

  * `OBJECT` Object – Show object color.

  * `RANDOM` Random – Show random object color.

  * `VERTEX` Attribute – Show active color attribute.

  * `TEXTURE` Texture – Show the texture from the active image texture node using the active UV map coordinates.

  * `SINGLE` Custom – Show scene in a single custom color.


Type:
    

enum in [`'MATERIAL'`, `'OBJECT'`, `'RANDOM'`, `'VERTEX'`, `'TEXTURE'`, `'SINGLE'`], default `'MATERIAL'`

curvature_ridge_factor
    

Factor for the curvature ridges

Type:
    

float in [0, 2], default 1.0

curvature_valley_factor
    

Factor for the curvature valleys

Type:
    

float in [0, 2], default 1.0

cycles
    

Type:
    

`CyclesView3DShadingSettings`, (readonly)

light
    

Lighting Method for Solid/Texture Viewport Shading

  * `STUDIO` Studio – Display using studio lighting.

  * `MATCAP` MatCap – Display using matcap material and lighting.

  * `FLAT` Flat – Display using flat lighting.


Type:
    

enum in [`'STUDIO'`, `'MATCAP'`, `'FLAT'`], default `'STUDIO'`

object_outline_color
    

Color for object outline

Type:
    

[[mathutils.Color]] of 3 items in [0, 1], default (0.0, 0.0, 0.0)

render_pass
    

Render Pass to show in the viewport

Type:
    

enum in [`'COMBINED'`, `'EMISSION'`, `'ENVIRONMENT'`, `'AO'`, `'SHADOW'`, `'TRANSPARENT'`, `'DIFFUSE_LIGHT'`, `'DIFFUSE_COLOR'`, `'SPECULAR_LIGHT'`, `'SPECULAR_COLOR'`, `'VOLUME_LIGHT'`, `'POSITION'`, `'NORMAL'`, `'MIST'`, `'CryptoObject'`, `'CryptoAsset'`, `'CryptoMaterial'`, `'AOV'`], default `'COMBINED'`

selected_studio_light
    

Selected StudioLight

Type:
    

[[StudioLight]], (readonly)

shadow_intensity
    

Darkness of shadows

Type:
    

float in [0, 1], default 0.5

show_backface_culling
    

Use back face culling to hide the back side of faces

Type:
    

boolean, default False

show_cavity
    

Show Cavity

Type:
    

boolean, default False

show_object_outline
    

Show Object Outline

Type:
    

boolean, default False

show_shadows
    

Show Shadow

Type:
    

boolean, default False

show_specular_highlight
    

Render specular highlights

Type:
    

boolean, default True

show_xray
    

Show whole scene transparent

Type:
    

boolean, default False

show_xray_wireframe
    

Show whole scene transparent

Type:
    

boolean, default True

single_color
    

Color for single color mode

Type:
    

[[mathutils.Color]] of 3 items in [0, 1], default (0.8, 0.8, 0.8)

studio_light
    

Studio lighting setup

Type:
    

enum in [`'DEFAULT'`], default `'DEFAULT'`

studiolight_background_alpha
    

Show the studiolight in the background

Type:
    

float in [0, 1], default 0.0

studiolight_background_blur
    

Blur the studiolight in the background

Type:
    

float in [0, 1], default 0.5

studiolight_intensity
    

Strength of the studiolight

Type:
    

float in [0, inf], default 1.0

studiolight_rotate_z
    

Rotation of the studiolight around the Z-Axis

Type:
    

float in [-3.14159, 3.14159], default 0.0

type
    

Method to display/shade objects in the 3D View

Type:
    

enum in [Shading Type Items](../../bpy_types_enum_items/shading_type_items.md#rna-enum-shading-type-items), default `'SOLID'`

use_compositor
    

When to preview the compositor output inside the viewport

  * `DISABLED` Disabled – The compositor is disabled.

  * `CAMERA` Camera – The compositor is enabled only in camera view.

  * `ALWAYS` Always – The compositor is always enabled regardless of the view.


Type:
    

enum in [`'DISABLED'`, `'CAMERA'`, `'ALWAYS'`], default `'DISABLED'`

use_dof
    

Use depth of field on viewport using the values from the active camera

Type:
    

boolean, default False

use_scene_lights
    

Render lights and light probes of the scene

Type:
    

boolean, default False

use_scene_lights_render
    

Render lights and light probes of the scene

Type:
    

boolean, default True

use_scene_world
    

Use scene world for lighting

Type:
    

boolean, default False

use_scene_world_render
    

Use scene world for lighting

Type:
    

boolean, default True

use_studiolight_view_rotation
    

Make the HDR rotation fixed and not follow the camera

Type:
    

boolean, default True

use_world_space_lighting
    

Make the lighting fixed and not follow the camera

Type:
    

boolean, default False

wireframe_color_type
    

Wire Color Type

  * `THEME` Theme – Show scene wireframes with the theme’s wire color.

  * `OBJECT` Object – Show object color on wireframe.

  * `RANDOM` Random – Show random object color on wireframe.


Type:
    

enum in [`'THEME'`, `'OBJECT'`, `'RANDOM'`], default `'THEME'`

xray_alpha
    

Amount of opacity to use

Type:
    

float in [0, 1], default 0.5

xray_alpha_wireframe
    

Amount of opacity to use

Type:
    

float in [0, 1], default 0.5

bl_system_properties_get(_*_ , _do_create =False_)
    

DEBUG ONLY. Internal access to runtime-defined RNA data storage, intended solely for testing and debugging purposes. Do not access it in regular scripting work, and in particular, do not assume that it contains writable data

Parameters:
    

**do_create** (_boolean_ _,__(__optional_ _)_) – Ensure that system properties are created if they do not exist yet

Returns:
    

The system properties root container, or None if there are no system properties stored in this data yet, and its creation was not requested

Return type:
    

[[PropertyGroup]]

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

  * [[SceneDisplay.shading]]
  * [[SpaceView3D.shading]]

| 

  * [[XrSessionSettings.shading]]

  
---|---
  *[*]: Keyword-only parameters separator (PEP 3102)
  *[/]: Positional-only parameter separator (PEP 570)
