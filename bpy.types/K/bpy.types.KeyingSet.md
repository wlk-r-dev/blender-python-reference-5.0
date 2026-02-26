# KeyingSet(bpy_struct)

base class — [[bpy_struct]]

_class _bpy.types.KeyingSet(_bpy_struct_)
    

Settings that should be keyframed together

bl_description
    

A short description of the keying set

Type:
    

string, default “”, (never None)

bl_idname
    

If this is set, the Keying Set gets a custom ID, otherwise it takes the name of the class used to define the Keying Set (for example, if the class name is “BUILTIN_KSI_location”, and bl_idname is not set by the script, then bl_idname = “BUILTIN_KSI_location”)

Type:
    

string, default “”, (never None)

bl_label
    

Type:
    

string, default “”, (never None)

is_path_absolute
    

Keying Set defines specific paths/settings to be keyframed (i.e. is not reliant on context info)

Type:
    

boolean, default False, (readonly)

paths
    

Keying Set Paths to define settings that get keyframed together

Type:
    

[[KeyingSetPaths]] [[bpy_prop_collection]] of [[KeyingSetPath]], (readonly)

type_info
    

Callback function defines for built-in Keying Sets

Type:
    

[[KeyingSetInfo]], (readonly)

use_insertkey_needed
    

Only insert keyframes where they’re needed in the relevant F-Curves

Type:
    

boolean, default False

use_insertkey_override_needed
    

Override default setting to only insert keyframes where they’re needed in the relevant F-Curves

Type:
    

boolean, default False

use_insertkey_override_visual
    

Override default setting to insert keyframes based on ‘visual transforms’

Type:
    

boolean, default False

use_insertkey_visual
    

Insert keyframes based on ‘visual transforms’

Type:
    

boolean, default False

refresh()
    

Refresh Keying Set to ensure that it is valid for the current context (call before each use of one)

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

  * [[KeyingSetInfo.generate]]
  * [[KeyingSetInfo.iterator]]
  * [[KeyingSets.active]]
  * [[KeyingSets.new]]

| 

  * [[KeyingSetsAll.active]]
  * [[Scene.keying_sets]]
  * [[Scene.keying_sets_all]]

  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
