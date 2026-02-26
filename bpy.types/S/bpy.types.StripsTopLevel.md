# StripsTopLevel(bpy_struct)

base class — [`bpy_struct`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct "bpy.types.bpy_struct")

_class _bpy.types.StripsTopLevel(_bpy_struct_)
    

Collection of Strips

new_clip(_name_ , _clip_ , _channel_ , _frame_start_)
    

Add a new movie clip strip

Parameters:
    

  * **name** (_string_ _,__(__never None_ _)_) – Name for the new strip

  * **clip** ([`MovieClip`](../M/bpy.types.MovieClip.md#bpy.types.MovieClip "bpy.types.MovieClip"), (never None)) – Movie clip to add

  * **channel** (_int in_ _[__1_ _,__128_ _]_) – Channel, The channel for the new strip

  * **frame_start** (_int in_ _[__-1048574_ _,__1048574_ _]_) – The start frame for the new strip


Returns:
    

New Strip

Return type:
    

[`Strip`](bpy.types.Strip.md#bpy.types.Strip "bpy.types.Strip")

new_mask(_name_ , _mask_ , _channel_ , _frame_start_)
    

Add a new mask strip

Parameters:
    

  * **name** (_string_ _,__(__never None_ _)_) – Name for the new strip

  * **mask** ([`Mask`](../M/bpy.types.Mask.md#bpy.types.Mask "bpy.types.Mask"), (never None)) – Mask to add

  * **channel** (_int in_ _[__1_ _,__128_ _]_) – Channel, The channel for the new strip

  * **frame_start** (_int in_ _[__-1048574_ _,__1048574_ _]_) – The start frame for the new strip


Returns:
    

New Strip

Return type:
    

[`Strip`](bpy.types.Strip.md#bpy.types.Strip "bpy.types.Strip")

new_scene(_name_ , _scene_ , _channel_ , _frame_start_)
    

Add a new scene strip

Parameters:
    

  * **name** (_string_ _,__(__never None_ _)_) – Name for the new strip

  * **scene** ([`Scene`](bpy.types.Scene.md#bpy.types.Scene "bpy.types.Scene"), (never None)) – Scene to add

  * **channel** (_int in_ _[__1_ _,__128_ _]_) – Channel, The channel for the new strip

  * **frame_start** (_int in_ _[__-1048574_ _,__1048574_ _]_) – The start frame for the new strip


Returns:
    

New Strip

Return type:
    

[`Strip`](bpy.types.Strip.md#bpy.types.Strip "bpy.types.Strip")

new_image(_name_ , _filepath_ , _channel_ , _frame_start_ , _*_ , _fit_method ='ORIGINAL'_)
    

Add a new image strip

Parameters:
    

  * **name** (_string_ _,__(__never None_ _)_) – Name for the new strip

  * **filepath** (_string_ _,__(__never None_ _)_) – Filepath to image

  * **channel** (_int in_ _[__1_ _,__128_ _]_) – Channel, The channel for the new strip

  * **frame_start** (_int in_ _[__-1048574_ _,__1048574_ _]_) – The start frame for the new strip

  * **fit_method** (enum in [Strip Scale Method Items](../../bpy_types_enum_items/strip_scale_method_items.md#rna-enum-strip-scale-method-items), (optional)) – Image Fit Method


Returns:
    

New Strip

Return type:
    

[`Strip`](bpy.types.Strip.md#bpy.types.Strip "bpy.types.Strip")

new_movie(_name_ , _filepath_ , _channel_ , _frame_start_ , _*_ , _fit_method ='ORIGINAL'_)
    

Add a new movie strip

Parameters:
    

  * **name** (_string_ _,__(__never None_ _)_) – Name for the new strip

  * **filepath** (_string_ _,__(__never None_ _)_) – Filepath to movie

  * **channel** (_int in_ _[__1_ _,__128_ _]_) – Channel, The channel for the new strip

  * **frame_start** (_int in_ _[__-1048574_ _,__1048574_ _]_) – The start frame for the new strip

  * **fit_method** (enum in [Strip Scale Method Items](../../bpy_types_enum_items/strip_scale_method_items.md#rna-enum-strip-scale-method-items), (optional)) – Image Fit Method


Returns:
    

New Strip

Return type:
    

[`Strip`](bpy.types.Strip.md#bpy.types.Strip "bpy.types.Strip")

new_sound(_name_ , _filepath_ , _channel_ , _frame_start_)
    

Add a new sound strip

Parameters:
    

  * **name** (_string_ _,__(__never None_ _)_) – Name for the new strip

  * **filepath** (_string_ _,__(__never None_ _)_) – Filepath to movie

  * **channel** (_int in_ _[__1_ _,__128_ _]_) – Channel, The channel for the new strip

  * **frame_start** (_int in_ _[__-1048574_ _,__1048574_ _]_) – The start frame for the new strip


Returns:
    

New Strip

Return type:
    

[`Strip`](bpy.types.Strip.md#bpy.types.Strip "bpy.types.Strip")

new_meta(_name_ , _channel_ , _frame_start_)
    

Add a new meta strip

Parameters:
    

  * **name** (_string_ _,__(__never None_ _)_) – Name for the new strip

  * **channel** (_int in_ _[__1_ _,__128_ _]_) – Channel, The channel for the new strip

  * **frame_start** (_int in_ _[__-1048574_ _,__1048574_ _]_) – The start frame for the new strip


Returns:
    

New Strip

Return type:
    

[`Strip`](bpy.types.Strip.md#bpy.types.Strip "bpy.types.Strip")

new_effect(_name_ , _type_ , _channel_ , _frame_start_ , _*_ , _length =0_, _input1 =None_, _input2 =None_)
    

Add a new effect strip

Parameters:
    

  * **name** (_string_ _,__(__never None_ _)_) – Name for the new strip

  * **type** (enum in [`'CROSS'`, `'ADD'`, `'SUBTRACT'`, `'ALPHA_OVER'`, `'ALPHA_UNDER'`, `'GAMMA_CROSS'`, `'MULTIPLY'`, `'WIPE'`, `'GLOW'`, `'COLOR'`, `'SPEED'`, `'MULTICAM'`, `'ADJUSTMENT'`, `'GAUSSIAN_BLUR'`, `'TEXT'`, `'COLORMIX'`]) – 

Type, type for the new strip

    * `CROSS` Crossfade – Fade out of one video, fading into another.

    * `ADD` Add – Add together color channels from two videos.

    * `SUBTRACT` Subtract – Subtract one strip’s color from another.

    * `ALPHA_OVER` Alpha Over – Blend alpha on top of another video.

    * `ALPHA_UNDER` Alpha Under – Blend alpha below another video.

    * `GAMMA_CROSS` Gamma Crossfade – Crossfade with color correction.

    * `MULTIPLY` Multiply – Multiply color channels from two videos.

    * `WIPE` Wipe – Sweep a transition line across the frame.

    * `GLOW` Glow – Add blur and brightness to light areas.

    * `COLOR` Color – Add a simple color strip.

    * `SPEED` Speed – Timewarp video strips, modifying playback speed.

    * `MULTICAM` Multicam Selector – Control active camera angles.

    * `ADJUSTMENT` Adjustment Layer – Apply nondestructive effects.

    * `GAUSSIAN_BLUR` Gaussian Blur – Soften details along axes.

    * `TEXT` Text – Add a simple text strip.

    * `COLORMIX` Color Mix – Combine two strips using blend modes.

  * **channel** (_int in_ _[__1_ _,__128_ _]_) – Channel, The channel for the new strip

  * **frame_start** (_int in_ _[__-inf_ _,__inf_ _]_) – The start frame for the new strip

  * **length** (_int in_ _[__-inf_ _,__inf_ _]__,__(__optional_ _)_) – Length of the strip in frames, or the length of each strip if multiple are added

  * **input1** ([`Strip`](bpy.types.Strip.md#bpy.types.Strip "bpy.types.Strip"), (optional)) – First input strip for effect

  * **input2** ([`Strip`](bpy.types.Strip.md#bpy.types.Strip "bpy.types.Strip"), (optional)) – Second input strip for effect


Returns:
    

New Strip

Return type:
    

[`Strip`](bpy.types.Strip.md#bpy.types.Strip "bpy.types.Strip")

remove(_sequence_)
    

Remove a Strip

Parameters:
    

**sequence** ([`Strip`](bpy.types.Strip.md#bpy.types.Strip "bpy.types.Strip"), (never None)) – Strip to remove

_classmethod _bl_rna_get_subclass(_id_ , _default =None_, _/_)
    

Parameters:
    

**id** (_str_) – The RNA type identifier.

Returns:
    

The RNA type or default when not found.

Return type:
    

[`bpy.types.Struct`](bpy.types.Struct.md#bpy.types.Struct "bpy.types.Struct") subclass

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

  * [`SequenceEditor.strips`](bpy.types.SequenceEditor.md#bpy.types.SequenceEditor.strips "bpy.types.SequenceEditor.strips")

| 


  
---|---
  *[*]: Keyword-only parameters separator (PEP 3102)
  *[/]: Positional-only parameter separator (PEP 570)
