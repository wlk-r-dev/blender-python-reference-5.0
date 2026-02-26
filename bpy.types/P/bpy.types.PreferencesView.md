# PreferencesView(bpy_struct)

base class — [`bpy_struct`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct "bpy.types.bpy_struct")

_class _bpy.types.PreferencesView(_bpy_struct_)
    

Preferences related to viewing data

border_width
    

Size of the padding around each editor.

Type:
    

int in [1, 10], default 2

color_picker_type
    

Different styles of displaying the color picker widget

  * `CIRCLE_HSV` Circle (HSV) – A circular Hue/Saturation color wheel, with Value slider.

  * `CIRCLE_HSL` Circle (HSL) – A circular Hue/Saturation color wheel, with Lightness slider.

  * `SQUARE_SV` Square (SV + H) – A square showing Saturation/Value, with Hue slider.

  * `SQUARE_HS` Square (HS + V) – A square showing Hue/Saturation, with Value slider.

  * `SQUARE_HV` Square (HV + S) – A square showing Hue/Value, with Saturation slider.


Type:
    

enum in [`'CIRCLE_HSV'`, `'CIRCLE_HSL'`, `'SQUARE_SV'`, `'SQUARE_HS'`, `'SQUARE_HV'`], default `'CIRCLE_HSV'`

factor_display_type
    

How factor values are displayed

  * `FACTOR` Factor – Display factors as values between 0 and 1.

  * `PERCENTAGE` Percentage – Display factors as percentages.


Type:
    

enum in [`'FACTOR'`, `'PERCENTAGE'`], default `'FACTOR'`

filebrowser_display_type
    

Default location where the File Editor will be displayed in

  * `SCREEN` Maximized Area – Open the temporary editor in a maximized screen.

  * `WINDOW` New Window – Open the temporary editor in a new window.


Type:
    

enum in [`'SCREEN'`, `'WINDOW'`], default `'WINDOW'`

font_path_ui
    

Path to interface font

Type:
    

string, default “”, (never None)

font_path_ui_mono
    

Path to interface monospaced Font

Type:
    

string, default “”, (never None)

gizmo_size
    

Diameter of the gizmo

Type:
    

int in [10, 200], default 75

gizmo_size_navigate_v3d
    

The Navigate Gizmo size

Type:
    

int in [30, 200], default 80

header_align
    

Default header position for new space-types

  * `NONE` Keep Existing – Keep existing header alignment.

  * `TOP` Top – Top aligned on load.

  * `BOTTOM` Bottom – Bottom align on load (except for property editors).


Type:
    

enum in [`'NONE'`, `'TOP'`, `'BOTTOM'`], default `'BOTTOM'`

language
    

Language used for translation

  * `DEFAULT` Automatic – Automatically choose the system-defined language if available, or fall-back to English (US).

  * `ab` Abkhaz - Аԥсуа бызшәа – Locale code: ab. Translation progress: 0%.

  * `ar_EG` Arabic - ﺔﻴﺑﺮﻌﻟﺍ – Locale code: ar_EG. Translation progress: 24%.

  * `eu_EU` Basque - Euskara – Locale code: eu_EU. Translation progress: 1%.

  * `be` Belarusian - беларуску – Locale code: be. Translation progress: 0%.

  * `bg_BG` Bulgarian - Български – Locale code: bg_BG. Translation progress: 2%.

  * `ca_AD` Catalan - Català – Locale code: ca_AD. Translation progress: 100%.

  * `zh_HANS` Chinese (Simplified) - 简体中文 – Locale code: zh_HANS. Translation progress: 100%.

  * `zh_HANT` Chinese (Traditional) - 繁體中文 – Locale code: zh_HANT. Translation progress: 51%.

  * `hr_HR` Croatian - Hrvatski – Locale code: hr_HR. Translation progress: 0%.

  * `cs_CZ` Czech - Čeština – Locale code: cs_CZ. Translation progress: 27%.

  * `da` Danish - Dansk – Locale code: da. Translation progress: 3%.

  * `nl_NL` Dutch - Nederlands – Locale code: nl_NL. Translation progress: 5%.

  * `en_GB` English (UK) – Locale code: en_GB. Translation progress: 92%.

  * `en_US` English (US) – Locale code: en_US. Translation progress: 100%.

  * `eo` Esperanto - Esperanto – Locale code: eo. Translation progress: 0%.

  * `fi_FI` Finnish - Suomi – Locale code: fi_FI. Translation progress: 11%.

  * `fr_FR` French - Français – Locale code: fr_FR. Translation progress: 100%.

  * `ka` Georgian - ქართული – Locale code: ka. Translation progress: 100%.

  * `de_DE` German - Deutsch – Locale code: de_DE. Translation progress: 37%.

  * `el_GR` Greek - Ελληνικά – Locale code: el_GR. Translation progress: 1%.

  * `ha` Hausa - Hausa – Locale code: ha. Translation progress: 0%.

  * `he_IL` Hebrew - תירִבְעִ – Locale code: he_IL. Translation progress: 1%.

  * `hi_IN` Hindi - हिन्दी – Locale code: hi_IN. Translation progress: 4%.

  * `hu_HU` Hungarian - Magyar – Locale code: hu_HU. Translation progress: 11%.

  * `id_ID` Indonesian - Bahasa indonesia – Locale code: id_ID. Translation progress: 20%.

  * `it_IT` Italian - Italiano – Locale code: it_IT. Translation progress: 44%.

  * `ja_JP` Japanese - 日本語 – Locale code: ja_JP. Translation progress: 100%.

  * `km` Khmer - ខ្មែរ – Locale code: km. Translation progress: 0%.

  * `ko_KR` Korean - 한국어 – Locale code: ko_KR. Translation progress: 50%.

  * `ky_KG` Kyrgyz - Кыргыз тили – Locale code: ky_KG. Translation progress: 2%.

  * `lt` Lithuanian - Lietuviškai – Locale code: lt. Translation progress: 3%.

  * `ml` Malayalam - മലയാളം – Locale code: ml. Translation progress: 0%.

  * `ne_NP` Nepali - नेपाली – Locale code: ne_NP. Translation progress: 0%.

  * `fa_IR` Persian - ﯽﺳﺭﺎﻓ – Locale code: fa_IR. Translation progress: 3%.

  * `pl_PL` Polish - Polski – Locale code: pl_PL. Translation progress: 18%.

  * `pt_BR` Portuguese (Brazil) - Português brasileiro – Locale code: pt_BR. Translation progress: 44%.

  * `pt_PT` Portuguese (Portugal) - Português europeu – Locale code: pt_PT. Translation progress: 71%.

  * `ro_RO` Romanian - Român – Locale code: ro_RO. Translation progress: 2%.

  * `ru_RU` Russian - Русский – Locale code: ru_RU. Translation progress: 100%.

  * `sr_RS` Serbian (Cyrillic) - Српски – Locale code: sr_RS. Translation progress: 16%.

  * `sr_RS@latin` Serbian (Latin) - Srpski latinica – Locale code: [sr_RS@latin](mailto:sr_RS%40latin). Translation progress: 16%.

  * `sk_SK` Slovak - Slovenčina – Locale code: sk_SK. Translation progress: 100%.

  * `sl` Slovenian - Slovenščina – Locale code: sl. Translation progress: 50%.

  * `es` Spanish - Español – Locale code: es. Translation progress: 100%.

  * `sw` Swahili - Kiswahili – Locale code: sw. Translation progress: 73%.

  * `sv_SE` Swedish - Svenska – Locale code: sv_SE. Translation progress: 22%.

  * `ta` Tamil - தமிழ் – Locale code: ta. Translation progress: 95%.

  * `th_TH` Thai - ภาษาไทย – Locale code: th_TH. Translation progress: 3%.

  * `tr_TR` Turkish - Türkçe – Locale code: tr_TR. Translation progress: 80%.

  * `uk_UA` Ukrainian - Українська – Locale code: uk_UA. Translation progress: 58%.

  * `ur` Urdu - وُدرُا – Locale code: ur. Translation progress: 88%.

  * `vi_VN` Vietnamese - Tiếng Việt – Locale code: vi_VN. Translation progress: 95%.


Type:
    

enum in [`'DEFAULT'`, `'ab'`, `'ar_EG'`, `'eu_EU'`, `'be'`, `'bg_BG'`, `'ca_AD'`, `'zh_HANS'`, `'zh_HANT'`, `'hr_HR'`, `'cs_CZ'`, `'da'`, `'nl_NL'`, `'en_GB'`, `'en_US'`, `'eo'`, `'fi_FI'`, `'fr_FR'`, `'ka'`, `'de_DE'`, `'el_GR'`, `'ha'`, `'he_IL'`, `'hi_IN'`, `'hu_HU'`, `'id_ID'`, `'it_IT'`, `'ja_JP'`, `'km'`, `'ko_KR'`, `'ky_KG'`, `'lt'`, `'ml'`, `'ne_NP'`, `'fa_IR'`, `'pl_PL'`, `'pt_BR'`, `'pt_PT'`, `'ro_RO'`, `'ru_RU'`, `'sr_RS'`, `'sr_RS@latin'`, `'sk_SK'`, `'sl'`, `'es'`, `'sw'`, `'sv_SE'`, `'ta'`, `'th_TH'`, `'tr_TR'`, `'uk_UA'`, `'ur'`, `'vi_VN'`], default `'DEFAULT'`

lookdev_sphere_size
    

Diameter of the HDRI reference spheres

Type:
    

int in [50, 400], default 150

menu_close_leave
    

Close menus when the mouse is moved out of the region.

Type:
    

boolean, default False

mini_axis_brightness
    

Brightness of the icon

Type:
    

int in [0, 10], default 8

mini_axis_size
    

The axes icon’s size

Type:
    

int in [10, 64], default 25

mini_axis_type
    

Show small rotating 3D axes in the top right corner of the 3D viewport

Type:
    

enum in [`'NONE'`, `'MINIMAL'`, `'GIZMO'`], default `'GIZMO'`

open_sublevel_delay
    

Time delay in 1/10 seconds before automatically opening sub level menus

Type:
    

int in [1, 40], default 2

open_toplevel_delay
    

Time delay in 1/10 seconds before automatically opening top level menus

Type:
    

int in [1, 40], default 5

pie_animation_timeout
    

Time needed to fully animate the pie to unfolded state (in 1/100ths of sec)

Type:
    

int in [0, 1000], default 6

pie_initial_timeout
    

Pie menus will use the initial mouse position as center for this amount of time (in 1/100ths of sec)

Type:
    

int in [0, 1000], default 0

pie_menu_confirm
    

Distance threshold after which selection is made (zero to disable)

Type:
    

int in [0, 1000], default 0

pie_menu_radius
    

Pie menu size in pixels

Type:
    

int in [0, 1000], default 100

pie_menu_threshold
    

Distance from center needed before a selection can be made

Type:
    

int in [0, 1000], default 12

pie_tap_timeout
    

Pie menu button held longer than this will dismiss menu on release (in 1/100ths of sec)

Type:
    

int in [0, 1000], default 20

playback_fps_samples
    

The number of frames to use for calculating FPS average. Zero to calculate this automatically, where the number of samples matches the target FPS.

Type:
    

int in [0, 5000], default 8

preferences_display_type
    

Default location where the Preferences will be displayed in

  * `SCREEN` Maximized Area – Open the temporary editor in a maximized screen.

  * `WINDOW` New Window – Open the temporary editor in a new window.


Type:
    

enum in [`'SCREEN'`, `'WINDOW'`], default `'WINDOW'`

render_display_type
    

Default location where rendered images will be displayed in

  * `NONE` Keep User Interface – Images are rendered without changing the user interface.

  * `SCREEN` Maximized Area – Images are rendered in a maximized Image Editor.

  * `AREA` Image Editor – Images are rendered in an Image Editor.

  * `WINDOW` New Window – Images are rendered in a new window.


Type:
    

enum in [`'NONE'`, `'SCREEN'`, `'AREA'`, `'WINDOW'`], default `'WINDOW'`

rotation_angle
    

Rotation step for numerical pad keys (2 4 6 8)

Type:
    

float in [0, 90], default 15.0

show_addons_enabled_only
    

Only show enabled add-ons. Un-check to see all installed add-ons.

Type:
    

boolean, default False

show_area_handle
    

Show visible area maintenance corner handles

Type:
    

boolean, default False

show_column_layout
    

Use a column layout for toolbox

Type:
    

boolean, default True

show_developer_ui
    

Display advanced settings and tools for developers

Type:
    

boolean, default False

show_extensions_updates
    

Show Extensions Update Count

Type:
    

boolean, default True

show_gizmo
    

Use transform gizmos by default

Type:
    

boolean, default True

show_navigate_ui
    

Show navigation controls in 2D and 3D views which do not have scroll bars

Type:
    

boolean, default True

show_number_arrows
    

Display arrows in numeric input fields for increasing or decreasing values

Type:
    

boolean, default False

show_object_info
    

Include the name of the active object and the current frame number in the text info overlay

Type:
    

boolean, default True

show_playback_fps
    

Include the number of frames displayed per second in the text info overlay while animation is played back

Type:
    

boolean, default True

show_splash
    

Display splash screen on startup

Type:
    

boolean, default True

show_statusbar_memory
    

Show Blender memory usage

Type:
    

boolean, default False

show_statusbar_scene_duration
    

Show scene duration

Type:
    

boolean, default False

show_statusbar_stats
    

Show scene statistics

Type:
    

boolean, default False

show_statusbar_version
    

Show Blender version string

Type:
    

boolean, default True

show_statusbar_vram
    

Show GPU video memory usage

Type:
    

boolean, default False

show_tooltips
    

Display tooltips (when disabled, hold Alt then hover to force display)

Type:
    

boolean, default True

show_tooltips_python
    

Show Python references in tooltips

Type:
    

boolean, default False

show_view_name
    

Include the name of the view orientation in the text info overlay

Type:
    

boolean, default True

smooth_view
    

Time to animate the view in milliseconds, zero to disable

Type:
    

int in [0, 1000], default 200

text_hinting
    

Method for making user interface text render sharp

Type:
    

enum in [`'AUTO'`, `'NONE'`, `'SLIGHT'`, `'FULL'`], default `'AUTO'`

timecode_style
    

Format of timecode displayed when not displaying timing in terms of frames

  * `MINIMAL` Minimal Info – Most compact representation, uses ‘+’ as separator for sub-second frame numbers, with left and right truncation of the timecode as necessary.

  * `SMPTE` SMPTE (Full) – Full SMPTE timecode (format is HH:MM:SS:FF).

  * `SMPTE_COMPACT` SMPTE (Compact) – SMPTE timecode showing minutes, seconds, and frames only - hours are also shown if necessary, but not by default.

  * `MILLISECONDS` Compact with Decimals – Similar to SMPTE (Compact), except that the decimal part of the second is shown instead of frames.

  * `SECONDS_ONLY` Only Seconds – Direct conversion of frame numbers to seconds.


Type:
    

enum in [`'MINIMAL'`, `'SMPTE'`, `'SMPTE_COMPACT'`, `'MILLISECONDS'`, `'SECONDS_ONLY'`], default `'MINIMAL'`

ui_line_width
    

Changes the thickness of widget outlines, lines and dots in the interface

  * `THIN` Thin – Thinner lines than the default.

  * `AUTO` Default – Automatic line width based on UI scale.

  * `THICK` Thick – Thicker lines than the default.


Type:
    

enum in [`'THIN'`, `'AUTO'`, `'THICK'`], default `'AUTO'`

ui_scale
    

Changes the size of the fonts and widgets in the interface

Type:
    

float in [0.5, 6], default 1.0

use_filter_brushes_by_tool
    

Only show brushes applicable for the currently active tool in the asset shelf. Stored in the Preferences, which may have to be saved manually if Auto-Save Preferences is disabled

Type:
    

boolean, default False

use_fresnel_edit
    

Enable a fresnel effect on edit mesh overlays. It improves shape readability of very dense meshes, but increases eye fatigue when modeling lower poly

Type:
    

boolean, default False

use_mouse_over_open
    

Open menu buttons and pull-downs automatically when the mouse is hovering

Type:
    

boolean, default False

use_reduce_motion
    

Avoid animations and other motion effects in the interface

Type:
    

boolean, default False

use_save_prompt
    

Ask for confirmation when quitting with unsaved changes

Type:
    

boolean, default True

use_text_antialiasing
    

Smooth jagged edges of user interface text

Type:
    

boolean, default True

use_text_render_subpixelaa
    

Render text for optimal horizontal placement

Type:
    

boolean, default False

use_translate_interface
    

Translate all labels in menus, buttons and panels (note that this might make it hard to follow tutorials or the manual)

Type:
    

boolean, default True

use_translate_new_dataname
    

Translate the names of new data-blocks (objects, materials…)

Type:
    

boolean, default True

use_translate_reports
    

Translate additional information, such as error messages

Type:
    

boolean, default True

use_translate_tooltips
    

Translate the descriptions when hovering UI elements (recommended)

Type:
    

boolean, default True

use_weight_color_range
    

Enable color range used for weight visualization in weight painting mode

Type:
    

boolean, default False

view2d_grid_spacing_min
    

Minimum number of pixels between each gridline in 2D Viewports

Type:
    

int in [1, 500], default 45

view_frame_keyframes
    

Keyframes around cursor that we zoom around

Type:
    

int in [1, 500], default 0

view_frame_seconds
    

Seconds around cursor that we zoom around

Type:
    

float in [0, 10000], default 0.0

view_frame_type
    

How zooming to frame focuses around current frame

Type:
    

enum in [`'KEEP_RANGE'`, `'SECONDS'`, `'KEYFRAMES'`], default `'KEEP_RANGE'`

weight_color_range
    

Color range used for weight visualization in weight painting mode

Type:
    

[`ColorRamp`](../C/bpy.types.ColorRamp.md#bpy.types.ColorRamp "bpy.types.ColorRamp"), (readonly, never None)

_classmethod _bl_rna_get_subclass(_id_ , _default =None_, _/_)
    

Parameters:
    

**id** (_str_) – The RNA type identifier.

Returns:
    

The RNA type or default when not found.

Return type:
    

[`bpy.types.Struct`](../S/bpy.types.Struct.md#bpy.types.Struct "bpy.types.Struct") subclass

_classmethod _bl_rna_get_subclass_py(_id_ , _default =None_, _/_)
    

Parameters:
    

**id** (_str_) – The RNA type identifier.

Returns:
    

The class or default when not found.

Return type:
    

type

## Inherited Properties

  * [`bpy_struct.id_data`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.id_data "bpy.types.bpy_struct.id_data")

| 


  
---|---  
  
## Inherited Functions

  * [`bpy_struct.as_pointer`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.as_pointer "bpy.types.bpy_struct.as_pointer")
  * [`bpy_struct.driver_add`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.driver_add "bpy.types.bpy_struct.driver_add")
  * [`bpy_struct.driver_remove`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.driver_remove "bpy.types.bpy_struct.driver_remove")
  * [`bpy_struct.get`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.get "bpy.types.bpy_struct.get")
  * [`bpy_struct.id_properties_clear`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.id_properties_clear "bpy.types.bpy_struct.id_properties_clear")
  * [`bpy_struct.id_properties_ensure`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.id_properties_ensure "bpy.types.bpy_struct.id_properties_ensure")
  * [`bpy_struct.id_properties_ui`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.id_properties_ui "bpy.types.bpy_struct.id_properties_ui")
  * [`bpy_struct.is_property_hidden`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.is_property_hidden "bpy.types.bpy_struct.is_property_hidden")
  * [`bpy_struct.is_property_overridable_library`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.is_property_overridable_library "bpy.types.bpy_struct.is_property_overridable_library")
  * [`bpy_struct.is_property_readonly`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.is_property_readonly "bpy.types.bpy_struct.is_property_readonly")
  * [`bpy_struct.is_property_set`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.is_property_set "bpy.types.bpy_struct.is_property_set")
  * [`bpy_struct.items`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.items "bpy.types.bpy_struct.items")

| 

  * [`bpy_struct.keyframe_delete`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.keyframe_delete "bpy.types.bpy_struct.keyframe_delete")
  * [`bpy_struct.keyframe_insert`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.keyframe_insert "bpy.types.bpy_struct.keyframe_insert")
  * [`bpy_struct.keys`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.keys "bpy.types.bpy_struct.keys")
  * [`bpy_struct.path_from_id`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.path_from_id "bpy.types.bpy_struct.path_from_id")
  * [`bpy_struct.path_from_module`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.path_from_module "bpy.types.bpy_struct.path_from_module")
  * [`bpy_struct.path_resolve`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.path_resolve "bpy.types.bpy_struct.path_resolve")
  * [`bpy_struct.pop`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.pop "bpy.types.bpy_struct.pop")
  * [`bpy_struct.property_overridable_library_set`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.property_overridable_library_set "bpy.types.bpy_struct.property_overridable_library_set")
  * [`bpy_struct.property_unset`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.property_unset "bpy.types.bpy_struct.property_unset")
  * [`bpy_struct.rna_ancestors`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.rna_ancestors "bpy.types.bpy_struct.rna_ancestors")
  * [`bpy_struct.type_recast`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.type_recast "bpy.types.bpy_struct.type_recast")
  * [`bpy_struct.values`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.values "bpy.types.bpy_struct.values")

  
---|---  
  
## References

  * [`Preferences.view`](bpy.types.Preferences.md#bpy.types.Preferences.view "bpy.types.Preferences.view")

| 


  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
