# NodesModifier(Modifier)

base classes — [[bpy_struct]], [[Modifier]]

_class _bpy.types.NodesModifier(_Modifier_)
    

bake_directory
    

Location on disk where the bake data is stored

Type:
    

string, default “”, (never None, blend relative `//` prefix supported)

bake_target
    

Where to store the baked data

  * `PACKED` Packed – Pack the baked data into the .blend file.

  * `DISK` Disk – Store the baked data in a directory on disk.


Type:
    

enum in [`'PACKED'`, `'DISK'`], default `'PACKED'`

bakes
    

Type:
    

[[NodesModifierBakes]] [[bpy_prop_collection]] of [[NodesModifierBake]], (readonly)

node_group
    

Node group that controls what this modifier does

Type:
    

[[NodeTree]]

node_warnings
    

Type:
    

[[bpy_prop_collection]] of [[NodesModifierWarning]], (readonly)

open_bake_data_blocks_panel
    

Type:
    

boolean, default False

open_bake_panel
    

Type:
    

boolean, default False

open_manage_panel
    

Type:
    

boolean, default False

open_named_attributes_panel
    

Type:
    

boolean, default False

open_output_attributes_panel
    

Type:
    

boolean, default False

open_warnings_panel
    

Type:
    

boolean, default False

panels
    

Type:
    

[[NodesModifierPanels]] [[bpy_prop_collection]] of [[NodesModifierPanel]], (readonly)

show_group_selector
    

Type:
    

boolean, default False

show_manage_panel
    

Type:
    

boolean, default False

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
  * [[Modifier.name]]
  * [[Modifier.type]]
  * [[Modifier.show_viewport]]
  * [[Modifier.show_render]]
  * [[Modifier.show_in_editmode]]
  * [[Modifier.show_on_cage]]

| 

  * [[Modifier.show_expanded]]
  * [[Modifier.is_active]]
  * [[Modifier.use_pin_to_last]]
  * [[Modifier.is_override_data]]
  * [[Modifier.use_apply_on_spline]]
  * [[Modifier.execution_time]]
  * [[Modifier.persistent_uid]]

  
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
  * [[bpy_struct.keyframe_delete]]

| 

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
  * [[Modifier.bl_rna_get_subclass]]
  * [[Modifier.bl_rna_get_subclass_py]]

  
---|---
  *[*]: Keyword-only parameters separator (PEP 3102)
  *[/]: Positional-only parameter separator (PEP 570)
