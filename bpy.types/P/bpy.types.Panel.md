# Panel(bpy_struct)

## Basic Panel Example

This script is a simple panel which will draw into the object properties section.

Notice the ‘CATEGORY_PT_name’ `Panel.bl_idname`, this is a naming convention for panels.

Note

Panel subclasses must be registered for Blender to use them.
    
    
    import bpy
    
    
    class HelloWorldPanel(bpy.types.Panel):
        bl_idname = "OBJECT_PT_hello_world"
        bl_label = "Hello World"
        bl_space_type = 'PROPERTIES'
        bl_region_type = 'WINDOW'
        bl_context = "object"
    
        def draw(self, context):
            self.layout.label(text="Hello World")
    
    
    bpy.utils.register_class(HelloWorldPanel)
    

## Simple Object Panel

This panel has a `Panel.poll` and `Panel.draw_header` function, even though the contents is basic this closely resembles blenders panels.
    
    
    import bpy
    
    
    class ObjectSelectPanel(bpy.types.Panel):
        bl_idname = "OBJECT_PT_select"
        bl_label = "Select"
        bl_space_type = 'PROPERTIES'
        bl_region_type = 'WINDOW'
        bl_context = "object"
        bl_options = {'DEFAULT_CLOSED'}
    
        @classmethod
        def poll(cls, context):
            return (context.object is not None)
    
        def draw_header(self, context):
            layout = self.layout
            layout.label(text="My Select Panel")
    
        def draw(self, context):
            layout = self.layout
    
            box = layout.box()
            box.label(text="Selection Tools")
            box.operator("object.select_all").action = 'TOGGLE'
            row = box.row()
            row.operator("object.select_all").action = 'INVERT'
            row.operator("object.select_random")
    
    
    bpy.utils.register_class(ObjectSelectPanel)
    

## Mix-in Classes

A mix-in parent class can be used to share common properties and [`Menu.poll`](../M/bpy.types.Menu.md#bpy.types.Menu.poll "bpy.types.Menu.poll") function.
    
    
    import bpy
    
    
    class View3DPanel:
        bl_space_type = 'VIEW_3D'
        bl_region_type = 'UI'
        bl_category = "Tool"
    
        @classmethod
        def poll(cls, context):
            return (context.object is not None)
    
    
    class PanelOne(View3DPanel, bpy.types.Panel):
        bl_idname = "VIEW3D_PT_test_1"
        bl_label = "Panel One"
    
        def draw(self, context):
            self.layout.label(text="Small Class")
    
    
    class PanelTwo(View3DPanel, bpy.types.Panel):
        bl_idname = "VIEW3D_PT_test_2"
        bl_label = "Panel Two"
    
        def draw(self, context):
            self.layout.label(text="Also Small Class")
    
    
    bpy.utils.register_class(PanelOne)
    bpy.utils.register_class(PanelTwo)
    

base class — [`bpy_struct`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct "bpy.types.bpy_struct")

_class _bpy.types.Panel(_bpy_struct_)
    

Panel containing UI elements

bl_category
    

The category (tab) in which the panel will be displayed, when applicable

Type:
    

string, default “”, (never None)

bl_context
    

The context in which the panel belongs to. (TODO: explain the possible combinations bl_context/bl_region_type/bl_space_type)

Type:
    

string, default “”, (never None)

bl_description
    

The panel tooltip

Type:
    

string, default “”

bl_idname
    

If this is set, the panel gets a custom ID, otherwise it takes the name of the class used to define the panel. For example, if the class name is “OBJECT_PT_hello”, and bl_idname is not set by the script, then bl_idname = “OBJECT_PT_hello”.

Type:
    

string, default “”, (never None)

bl_label
    

The panel label, shows up in the panel header at the right of the triangle used to collapse the panel

Type:
    

string, default “”, (never None)

bl_options
    

Options for this panel type

  * `DEFAULT_CLOSED` Default Closed – Defines if the panel has to be open or collapsed at the time of its creation.

  * `HIDE_HEADER` Hide Header – If set to False, the panel shows a header, which contains a clickable arrow to collapse the panel and the label (see bl_label).

  * `INSTANCED` Instanced Panel – Multiple panels with this type can be used as part of a list depending on data external to the UI. Used to create panels for the modifiers and other stacks..

  * `HEADER_LAYOUT_EXPAND` Expand Header Layout – Allow buttons in the header to stretch and shrink to fill the entire layout width.


Type:
    

enum set in {`'DEFAULT_CLOSED'`, `'HIDE_HEADER'`, `'INSTANCED'`, `'HEADER_LAYOUT_EXPAND'`}, default set()

bl_order
    

Panels with lower numbers are default ordered before panels with higher numbers

Type:
    

int in [0, inf], default 0

bl_owner_id
    

The ID owning the data displayed in the panel, if any

Type:
    

string, default “”, (never None)

bl_parent_id
    

If this is set, the panel becomes a sub-panel

Type:
    

string, default “”, (never None)

bl_region_type
    

The region where the panel is going to be used in

Type:
    

enum in [Region Type Items](../../bpy_types_enum_items/region_type_items.md#rna-enum-region-type-items), default `'WINDOW'`

bl_space_type
    

The space where the panel is going to be used in

Type:
    

enum in [Space Type Items](../../bpy_types_enum_items/space_type_items.md#rna-enum-space-type-items), default `'EMPTY'`

bl_translation_context
    

Specific translation context, only define when the label needs to be disambiguated from others using the exact same label

Type:
    

string, default “*”, (never None)

bl_ui_units_x
    

When set, defines popup panel width

Type:
    

int in [0, inf], default 0

custom_data
    

Panel data

Type:
    

[`Constraint`](../C/bpy.types.Constraint.md#bpy.types.Constraint "bpy.types.Constraint"), (readonly)

is_popover
    

Type:
    

boolean, default False, (readonly)

layout
    

Defines the structure of the panel in the UI

Type:
    

[`UILayout`](../U/bpy.types.UILayout.md#bpy.types.UILayout "bpy.types.UILayout"), (readonly)

text
    

XXX todo

Type:
    

string, default “”, (never None)

use_pin
    

Show the panel on all tabs

Type:
    

boolean, default False

_classmethod _poll(_context_)
    

If this method returns a non-null output, then the panel can be drawn

Return type:
    

boolean

draw(_context_)
    

Draw UI elements into the panel UI layout

draw_header(_context_)
    

Draw UI elements into the panel’s header UI layout

draw_header_preset(_context_)
    

Draw UI elements for presets in the panel’s header

_classmethod _append(_draw_func_)
    

Append a draw function to this menu, takes the same arguments as the menus draw function

_classmethod _is_extended()
    

_classmethod _prepend(_draw_func_)
    

Prepend a draw function to this menu, takes the same arguments as the menus draw function

_classmethod _remove(_draw_func_)
    

Remove a draw function that has been added to this menu.

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

### Inherited Properties

  * [`bpy_struct.id_data`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.id_data "bpy.types.bpy_struct.id_data")

| 


  
---|---  
  
### Inherited Functions

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
  *[/]: Positional-only parameter separator (PEP 570)
