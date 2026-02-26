# PropertyGroupItem(bpy_struct)

base class — [[bpy_struct]]

_class _bpy.types.PropertyGroupItem(_bpy_struct_)
    

Property that stores arbitrary, user defined properties

bool
    

Type:
    

boolean, default False

bool_array
    

Type:
    

boolean array of 1 items, default (False,)

collection
    

Type:
    

[[bpy_prop_collection]] of [[PropertyGroup]], (readonly)

double
    

Type:
    

float in [-inf, inf], default 0.0

double_array
    

Type:
    

float array of 1 items in [-inf, inf], default (0.0)

enum
    

Type:
    

enum in [`'DEFAULT'`], default `'DEFAULT'`

float
    

Type:
    

float in [-inf, inf], default 0.0

float_array
    

Type:
    

float array of 1 items in [-inf, inf], default (0.0)

group
    

Type:
    

[[PropertyGroup]], (readonly)

id
    

Type:
    

[[ID]]

idp_array
    

Type:
    

[[bpy_prop_collection]] of [[PropertyGroup]], (readonly)

int
    

Type:
    

int in [-inf, inf], default 0

int_array
    

Type:
    

int array of 1 items in [-inf, inf], default (0,)

string
    

Type:
    

string, default “”, (never None)

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
  *[/]: Positional-only parameter separator (PEP 570)
