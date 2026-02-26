# ActionChannelbagFCurves(bpy_struct)

base class — [[bpy_struct]]

_class _bpy.types.ActionChannelbagFCurves(_bpy_struct_)
    

Collection of F-Curves for a specific action slot, on a specific strip

new(_data_path_ , _*_ , _index =0_, _group_name =''_)
    

Add an F-Curve to the channelbag

Parameters:
    

  * **data_path** (_string_ _,__(__never None_ _)_) – Data Path, F-Curve data path to use

  * **index** (_int in_ _[__0_ _,__inf_ _]__,__(__optional_ _)_) – Index, Array index

  * **group_name** (_string_ _,__(__optional_ _,__never None_ _)_) – Group Name, Name of the Group for this F-Curve, will be created if it does not exist yet


Returns:
    

Newly created F-Curve

Return type:
    

[[FCurve]]

new_from_fcurve(_source_ , _*_ , _data_path =''_)
    

Copy an F-Curve into the channelbag. The original F-Curve is unchanged

Parameters:
    

  * **source** ([[FCurve]]) – Source F-Curve, The F-Curve to copy

  * **data_path** (_string_ _,__(__optional_ _,__never None_ _)_) – Data Path, F-Curve data path to use. If not provided, this will use the same data path as the given F-Curve


Returns:
    

Newly created F-Curve

Return type:
    

[[FCurve]]

ensure(_data_path_ , _*_ , _index =0_, _group_name =''_)
    

Returns the F-Curve if it already exists, and creates it if necessary

Parameters:
    

  * **data_path** (_string_ _,__(__never None_ _)_) – Data Path, F-Curve data path to use

  * **index** (_int in_ _[__0_ _,__inf_ _]__,__(__optional_ _)_) – Index, Array index

  * **group_name** (_string_ _,__(__optional_ _,__never None_ _)_) – Group Name, Name of the Group for this F-Curve, will be created if it does not exist yet. This parameter is ignored if the F-Curve already exists


Returns:
    

Found or newly created F-Curve

Return type:
    

[[FCurve]]

find(_data_path_ , _*_ , _index =0_)
    

Find an F-Curve. Note that this function performs a linear scan of all F-Curves in the channelbag.

Parameters:
    

  * **data_path** (_string_ _,__(__never None_ _)_) – Data Path, F-Curve data path

  * **index** (_int in_ _[__0_ _,__inf_ _]__,__(__optional_ _)_) – Index, Array index


Returns:
    

The found F-Curve, or None if it does not exist

Return type:
    

[[FCurve]]

remove(_fcurve_)
    

Remove F-Curve

Parameters:
    

**fcurve** ([[FCurve]], (never None)) – F-Curve to remove

clear()
    

Remove all F-Curves from this channelbag

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

  * [[ActionChannelbag.fcurves]]

| 


  
---|---
  *[*]: Keyword-only parameters separator (PEP 3102)
  *[/]: Positional-only parameter separator (PEP 570)
