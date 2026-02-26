# Macro(bpy_struct)

## Example Macro

This example creates a simple macro operator that moves the active object and then rotates it. It demonstrates:

  * Defining a macro operator class.

  * Registering it and defining sub-operators.

  * Setting property values for each step.


    
    
    import bpy
    
    
    class OBJECT_OT_simple_macro(bpy.types.Macro):
        bl_idname = "object.simple_macro"
        bl_label = "Simple Transform Macro"
        bl_options = {'REGISTER', 'UNDO'}
    
        @classmethod
        def poll(cls, context):
            return context.active_object is not None
    
    
    def register():
        bpy.utils.register_class(OBJECT_OT_simple_macro)
    
        # Define steps after registration and set operator values via .properties
        step = OBJECT_OT_simple_macro.define("transform.translate")
        props = step.properties
        props.value = (1.0, 0.0, 0.0)
        props.constraint_axis = (True, False, False)
    
        step = OBJECT_OT_simple_macro.define("transform.rotate")
        props = step.properties
        props.value = 0.785398  # 45 degrees in radians
        props.orient_axis = 'Z'
    
    
    def unregister():
        bpy.utils.unregister_class(OBJECT_OT_simple_macro)
    
    
    if __name__ == "__main__":
        register()
    
        # To run the macro:
        bpy.ops.object.simple_macro()
    

base class — [[bpy_struct]]

_class _bpy.types.Macro(_bpy_struct_)
    

Storage of a macro operator being executed, or registered after execution

bl_cursor_pending
    

Cursor to use when waiting for the user to select a location to activate the operator (when `bl_options` has `DEPENDS_ON_CURSOR` set)

Type:
    

enum in [Window Cursor Items](../../bpy_types_enum_items/window_cursor_items.md#rna-enum-window-cursor-items), default `'DEFAULT'`

bl_description
    

Type:
    

string, default “”, (never None)

bl_idname
    

Type:
    

string, default “”, (never None)

bl_label
    

Type:
    

string, default “”, (never None)

bl_options
    

Options for this operator type

Type:
    

enum set in [Operator Type Flag Items](../../bpy_types_enum_items/operator_type_flag_items.md#rna-enum-operator-type-flag-items), default set()

bl_translation_context
    

Type:
    

string, default “Operator”, (never None)

bl_undo_group
    

Type:
    

string, default “”, (never None)

has_reports
    

Operator has a set of reports (warnings and errors) from last execution

Type:
    

boolean, default False, (readonly)

name
    

Type:
    

string, default “”, (readonly, never None)

properties
    

Type:
    

[[OperatorProperties]], (readonly, never None)

report(_type_ , _message_)
    

report

Parameters:
    

  * **type** (enum set in [Wm Report Items](../../bpy_types_enum_items/wm_report_items.md#rna-enum-wm-report-items)) – Type

  * **message** (_string_ _,__(__never None_ _)_) – Report Message


_classmethod _poll(_context_)
    

Test if the operator can be called or not

Return type:
    

boolean

draw(_context_)
    

Draw function for the operator

_classmethod _define(_operator_)
    

Append an operator to a registered macro class.

Parameters:
    

**operator** (_str_) – Identifier of the operator. This does not have to be defined when this function is called.

Returns:
    

The operator macro for property access.

Return type:
    

[[OperatorMacro]]

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

### Inherited Properties

  * [[bpy_struct.id_data]]

| 


  
---|---  
  
### Inherited Functions

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
  
### References

  * [[Operator.macros]]

| 


  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
