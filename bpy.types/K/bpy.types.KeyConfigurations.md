# KeyConfigurations(bpy_struct)

base class — [[bpy_struct]]

_class _bpy.types.KeyConfigurations(_bpy_struct_)
    

Collection of KeyConfigs

active
    

Active key configuration (preset)

Type:
    

[[KeyConfig]]

addon
    

Key configuration that can be extended by add-ons, and is added to the active configuration when handling events

Type:
    

[[KeyConfig]], (readonly)

default
    

Default builtin key configuration

Type:
    

[[KeyConfig]], (readonly)

user
    

Final key configuration that combines keymaps from the active and add-on configurations, and can be edited by the user

Type:
    

[[KeyConfig]], (readonly)

new(_name_)
    

new

Parameters:
    

**name** (_string_ _,__(__never None_ _)_) – Name

Returns:
    

Key Configuration, Added key configuration

Return type:
    

[[KeyConfig]]

remove(_keyconfig_)
    

remove

Parameters:
    

**keyconfig** ([[KeyConfig]], (never None)) – Key Configuration, Removed key configuration

find_item_from_operator(_idname_ , _*_ , _context ='INVOKE_DEFAULT'_, _properties =None_, _include ={'ACTIONZONE', 'KEYBOARD', 'MOUSE', 'NDOF'}_, _exclude ={}_)
    

find_item_from_operator

Parameters:
    

  * **idname** (_string_ _,__(__never None_ _)_) – Operator Identifier

  * **context** (enum in [Operator Context Items](../../bpy_types_enum_items/operator_context_items.md#rna-enum-operator-context-items), (optional)) – context

  * **include** (enum set in [Event Type Mask Items](../../bpy_types_enum_items/event_type_mask_items.md#rna-enum-event-type-mask-items), (optional)) – Include

  * **exclude** (enum set in [Event Type Mask Items](../../bpy_types_enum_items/event_type_mask_items.md#rna-enum-event-type-mask-items), (optional)) – Exclude


Returns:
    

`keymap`, [[KeyMap]]

`item`, [[KeyMapItem]]

Return type:
    

([[KeyMap]], [[KeyMapItem]])

update(_*_ , _keep_properties =False_)
    

update

Parameters:
    

**keep_properties** (_boolean_ _,__(__optional_ _)_) – Keep Properties, Operator properties are kept to allow the operators to be registered again in the future

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

  * [[WindowManager.keyconfigs]]

| 


  
---|---
  *[*]: Keyword-only parameters separator (PEP 3102)
  *[/]: Positional-only parameter separator (PEP 570)
