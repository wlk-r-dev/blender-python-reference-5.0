# Path Utilities (bpy.path)

This module has a similar scope to os.path, containing utility functions for dealing with paths in Blender.

bpy.path.abspath(_path_ , _*_ , _start =None_, _library =None_)
    

Returns the absolute path relative to the current blend file using the “//” prefix.

Parameters:
    

  * **start** (_str_ _|__bytes_) – Relative to this path, when not set the current filename is used.

  * **library** ([[bpy.types.Library]]) – The library this path is from. This is only included for convenience, when the library is not None its path replaces _start_.


Returns:
    

The absolute path.

Return type:
    

str

bpy.path.basename(_path_)
    

Equivalent to `os.path.basename`, but skips a “//” prefix.

Use for Windows compatibility.

Returns:
    

The base name of the given path.

Return type:
    

str

bpy.path.clean_name(_name_ , _*_ , _replace ='_'_)
    

Returns a name with characters replaced that may cause problems under various circumstances, such as writing to a file.

All characters besides A-Z/a-z, 0-9 are replaced with “_” or the _replace_ argument if defined.

Parameters:
    

  * **name** (_str_ _|__bytes_) – The path name.

  * **replace** (_str_) – The replacement for non-valid characters.


Returns:
    

The cleaned name.

Return type:
    

str

bpy.path.display_name(_name_ , _*_ , _has_ext =True_, _title_case =True_)
    

Creates a display string from name to be used menus and the user interface. Intended for use with filenames and module names.

Parameters:
    

  * **name** (_str_) – The name to be used for displaying the user interface.

  * **has_ext** (_bool_) – Remove file extension from name.

  * **title_case** (_bool_) – Convert lowercase names to title case.


Returns:
    

The display string.

Return type:
    

str

bpy.path.display_name_to_filepath(_name_)
    

Performs the reverse of display_name using literal versions of characters which aren’t supported in a filepath.

Parameters:
    

**name** (_str_) – The display name to convert.

Returns:
    

The file path.

Return type:
    

str

bpy.path.display_name_from_filepath(_name_)
    

Returns the path stripped of directory and extension, ensured to be utf8 compatible.

Parameters:
    

**name** (_str_) – The file path to convert.

Returns:
    

The display name.

Return type:
    

str

bpy.path.ensure_ext(_filepath_ , _ext_ , _*_ , _case_sensitive =False_)
    

Return the path with the extension added if it is not already set.

Parameters:
    

  * **filepath** (_str_) – The file path.

  * **ext** (_str_) – The extension to check for, can be a compound extension. Should start with a dot, such as `.blend` or `.tar.gz`.

  * **case_sensitive** (_bool_) – Check for matching case when comparing extensions.


Returns:
    

The file path with the given extension.

Return type:
    

str

bpy.path.is_subdir(_path_ , _directory_)
    

Returns true if _path_ in a subdirectory of _directory_. Both paths must be absolute.

Parameters:
    

**path** (_str_ _|__bytes_) – An absolute path.

Returns:
    

Whether or not the path is a subdirectory.

Return type:
    

bool

bpy.path.module_names(_path_ , _*_ , _recursive =False_, _package =''_)
    

Return a list of modules which can be imported from _path_.

Parameters:
    

  * **path** (_str_) – a directory to scan.

  * **recursive** (_bool_) – Also return submodule names for packages.

  * **package** (_str_) – Optional string, used as the prefix for module names (without the trailing “.”).


Returns:
    

a list of string pairs (module_name, module_file).

Return type:
    

list[tuple[str, str]]

bpy.path.native_pathsep(_path_)
    

Replace the path separator with the systems native `os.sep`.

Parameters:
    

**path** (_str_) – The path to replace.

Returns:
    

The path with system native separators.

Return type:
    

str

bpy.path.reduce_dirs(_dirs_)
    

Given a sequence of directories, remove duplicates and any directories nested in one of the other paths. (Useful for recursive path searching).

Parameters:
    

**dirs** (_Sequence_ _[__str_ _]_) – Sequence of directory paths.

Returns:
    

A unique list of paths.

Return type:
    

list[str]

bpy.path.relpath(_path_ , _*_ , _start =None_)
    

Returns the path relative to the current blend file using the “//” prefix.

Parameters:
    

  * **path** (_str_ _|__bytes_) – An absolute path.

  * **start** (_str_ _|__bytes_) – Relative to this path, when not set the current filename is used.


Returns:
    

The relative path.

Return type:
    

str

bpy.path.resolve_ncase(_path_)
    

Resolve a case insensitive path on a case sensitive system, returning a string with the path if found else return the original path.

Parameters:
    

**path** (_str_) – The path name to resolve.

Returns:
    

The resolved path.

Return type:
    

str
  *[*]: Keyword-only parameters separator (PEP 3102)
