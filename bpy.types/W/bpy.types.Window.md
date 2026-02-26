# Window(bpy_struct)

base class — [`bpy_struct`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct "bpy.types.bpy_struct")

_class _bpy.types.Window(_bpy_struct_)
    

Open window

height
    

Window height

Type:
    

int in [0, 32767], default 0, (readonly)

modal_operators
    

A list of currently running modal operators

Type:
    

[`bpy_prop_collection`](../_other/bpy.types.bpy_prop_collection.md#bpy.types.bpy_prop_collection "bpy.types.bpy_prop_collection") of [`Operator`](../O/bpy.types.Operator.md#bpy.types.Operator "bpy.types.Operator"), (readonly)

parent
    

Active workspace and scene follow this window

Type:
    

`Window`, (readonly)

scene
    

Active scene to be edited in the window

Type:
    

[`Scene`](../S/bpy.types.Scene.md#bpy.types.Scene "bpy.types.Scene"), (never None)

screen
    

Active workspace screen showing in the window

Type:
    

[`Screen`](../S/bpy.types.Screen.md#bpy.types.Screen "bpy.types.Screen"), (never None)

stereo_3d_display
    

Settings for stereo 3D display

Type:
    

[`Stereo3dDisplay`](../S/bpy.types.Stereo3dDisplay.md#bpy.types.Stereo3dDisplay "bpy.types.Stereo3dDisplay"), (readonly, never None)

support_hdr_color
    

The window has a HDR graphics buffer that wide gamut and high dynamic range colors can be written to, in extended sRGB color space.

Type:
    

boolean, default False, (readonly)

view_layer
    

The active workspace view layer showing in the window

Type:
    

[`ViewLayer`](../V/bpy.types.ViewLayer.md#bpy.types.ViewLayer "bpy.types.ViewLayer"), (never None)

width
    

Window width

Type:
    

int in [0, 32767], default 0, (readonly)

workspace
    

Active workspace showing in the window

Type:
    

[`WorkSpace`](bpy.types.WorkSpace.md#bpy.types.WorkSpace "bpy.types.WorkSpace"), (never None)

x
    

Horizontal location of the window

Type:
    

int in [-32768, 32767], default 0, (readonly)

y
    

Vertical location of the window

Type:
    

int in [-32768, 32767], default 0, (readonly)

cursor_warp(_x_ , _y_)
    

Set the cursor position

cursor_set(_cursor_)
    

Set the cursor

Parameters:
    

**cursor** (enum in [Window Cursor Items](../../bpy_types_enum_items/window_cursor_items.md#rna-enum-window-cursor-items)) – cursor

cursor_modal_set(_cursor_)
    

Set the cursor, so the previous cursor can be restored

Parameters:
    

**cursor** (enum in [Window Cursor Items](../../bpy_types_enum_items/window_cursor_items.md#rna-enum-window-cursor-items)) – cursor

cursor_modal_restore()
    

Restore the previous cursor after calling `cursor_modal_set`

event_simulate(_type_ , _value_ , _*_ , _unicode =''_, _x =0_, _y =0_, _shift =False_, _ctrl =False_, _alt =False_, _oskey =False_, _hyper =False_)
    

event_simulate

Parameters:
    

  * **type** (enum in [Event Type Items](../../bpy_types_enum_items/event_type_items.md#rna-enum-event-type-items)) – Type

  * **value** (enum in [Event Value Items](../../bpy_types_enum_items/event_value_items.md#rna-enum-event-value-items)) – Value

  * **shift** (_boolean_ _,__(__optional_ _)_) – Shift

  * **ctrl** (_boolean_ _,__(__optional_ _)_) – Ctrl

  * **alt** (_boolean_ _,__(__optional_ _)_) – Alt

  * **oskey** (_boolean_ _,__(__optional_ _)_) – OS Key

  * **hyper** (_boolean_ _,__(__optional_ _)_) – Hyper


Returns:
    

Item, Added key map item

Return type:
    

[`Event`](../E/bpy.types.Event.md#bpy.types.Event "bpy.types.Event")

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

  * [`Context.window`](../C/bpy.types.Context.md#bpy.types.Context.window "bpy.types.Context.window")
  * `Window.parent`

| 

  * [`WindowManager.event_timer_add`](bpy.types.WindowManager.md#bpy.types.WindowManager.event_timer_add "bpy.types.WindowManager.event_timer_add")
  * [`WindowManager.windows`](bpy.types.WindowManager.md#bpy.types.WindowManager.windows "bpy.types.WindowManager.windows")

  
---|---
  *[*]: Keyword-only parameters separator (PEP 3102)
  *[/]: Positional-only parameter separator (PEP 570)
