# bpy_extras submodule (bpy_extras.io_utils)

bpy_extras.io_utils.orientation_helper(_axis_forward ='Y'_, _axis_up ='Z'_)
    

A decorator for import/export classes, generating properties needed by the axis conversion system and IO helpers, with specified default values (axes).

bpy_extras.io_utils.axis_conversion(_from_forward ='Y'_, _from_up ='Z'_, _to_forward ='Y'_, _to_up ='Z'_)
    

Each argument is an axis in [‘X’, ‘Y’, ‘Z’, ‘-X’, ‘-Y’, ‘-Z’] where the first 2 are a source and the second 2 are the target. :rtype: [[mathutils.Matrix]]

bpy_extras.io_utils.axis_conversion_ensure(_operator_ , _forward_attr_ , _up_attr_)
    

Function to ensure an operator has valid axis conversion settings, intended to be used from [[bpy.types.Operator.check]].

Parameters:
    

  * **operator** ([[bpy.types.Operator]]) – the operator to access axis attributes from.

  * **forward_attr** (_str_) – attribute storing the forward axis

  * **up_attr** (_str_) – attribute storing the up axis


Returns:
    

True if the value was modified.

Return type:
    

bool

bpy_extras.io_utils.create_derived_objects(_depsgraph_ , _objects_)
    

This function takes a sequence of objects, returning their instances.

Parameters:
    

  * **depsgraph** ([[bpy.types.Depsgraph]]) – The evaluated depsgraph.

  * **objects** (Sequence[[[bpy.types.Object]]]) – A sequencer of objects.


Returns:
    

A dictionary where each key is an object from `objects`, values are lists of (object, matrix) tuples representing instances.

Return type:
    

dict[[[bpy.types.Object]], list[tuple[[[bpy.types.Object]], [[mathutils.Matrix]]]]]

bpy_extras.io_utils.poll_file_object_drop(_context_)
    

A default implementation for FileHandler poll_drop methods. Allows for both the 3D Viewport and the Outliner (in ViewLayer display mode) to be targets for file drag and drop.

bpy_extras.io_utils.unpack_list(_list_of_tuples_)
    

bpy_extras.io_utils.unpack_face_list(_list_of_tuples_)
    

bpy_extras.io_utils.path_reference(_filepath_ , _base_src_ , _base_dst_ , _mode ='AUTO'_, _copy_subdir =''_, _copy_set =None_, _library =None_)
    

Return a filepath relative to a destination directory, for use with exporters.

Parameters:
    

  * **filepath** (_str_) – the file path to return, supporting blenders relative ‘//’ prefix.

  * **base_src** (_str_) – the directory the _filepath_ is relative too (normally the blend file).

  * **base_dst** (_str_) – the directory the _filepath_ will be referenced from (normally the export path).

  * **mode** (_str_) – the method used get the path in [‘AUTO’, ‘ABSOLUTE’, ‘RELATIVE’, ‘MATCH’, ‘STRIP’, ‘COPY’]

  * **copy_subdir** (_str_) – the subdirectory of _base_dst_ to use when mode=’COPY’.

  * **copy_set** (_set_ _[__tuple_ _[__str_ _,__str_ _]__]_) – collect from/to pairs when mode=’COPY’, pass to _path_reference_copy_ when exporting is done.

  * **library** ([[bpy.types.Library]] | None) – The library this path is relative to.


Returns:
    

the new filepath.

Return type:
    

str

bpy_extras.io_utils.path_reference_copy(_copy_set_ , _report= function print>_)
    

Execute copying files of path_reference

Parameters:
    

  * **copy_set** (_set_ _[__tuple_ _[__str_ _,__str_ _]__]_) – set of (from, to) pairs to copy.

  * **report** (_Callable_ _[__[__str_ _]__,__None_ _]_) – function used for reporting warnings, takes a string argument.


bpy_extras.io_utils.unique_name(_key_ , _name_ , _name_dict_ , _name_max =-1_, _clean_func =None_, _sep ='.'_)
    

Helper function for storing unique names which may have special characters stripped and restricted to a maximum length.

Parameters:
    

  * **key** (_Any_) – Unique item this name belongs to, name_dict[key] will be reused when available. This can be the object, mesh, material, etc instance itself. Any hashable object associated with the _name_.

  * **name** (_str_) – The name used to create a unique value in _name_dict_.

  * **name_dict** (_dict_) – This is used to cache namespace to ensure no collisions occur, this should be an empty dict initially and only modified by this function.

  * **clean_func** (_function_) – Function to call on _name_ before creating a unique value.

  * **sep** (_str_) – Separator to use when between the name and a number when a duplicate name is found.


_class _bpy_extras.io_utils.ExportHelper
    

check(__context_)
    

invoke(_context_ , __event_)
    

_class _bpy_extras.io_utils.ImportHelper
    

check(__context_)
    

invoke(_context_ , __event_)
    

invoke_popup(_context_ , _confirm_text =''_)
