# bpy_prop_collection

_class _bpy.types.bpy_prop_collection
    

built-in class used for all collections.

Note

Note that `bpy.types.bpy_prop_collection` is not actually available from within Blender, it only exists for the purpose of documentation.

find(_key_)
    

Returns the index of a key in a collection or -1 when not found (matches Python’s string find function of the same name).

Parameters:
    

**key** (_str_) – The identifier for the collection member.

Returns:
    

index of the key.

Return type:
    

int

foreach_get(_attr_ , _seq_)
    

This is a function to give fast access to attributes within a collection.

Only works for ‘basic type’ properties (bool, int and float)! Multi-dimensional arrays (like array of vectors) will be flattened into seq.
    
    
    collection.foreach_get(attr, some_seq)
    
    # Python equivalent.
    for i in range(len(seq)):
        some_seq[i] = getattr(collection[i], attr)
    

foreach_set(_attr_ , _seq_)
    

This is a function to give fast access to attributes within a collection.

Only works for ‘basic type’ properties (bool, int and float)! seq must be uni-dimensional, multi-dimensional arrays (like array of vectors) will be re-created from it.
    
    
    collection.foreach_set(attr, some_seq)
    
    # Python equivalent.
    for i in range(len(some_seq)):
        setattr(collection[i], attr, some_seq[i])
    

get(_key_ , _default =None_)
    

Returns the value of the item assigned to key or default when not found (matches Python’s dictionary function of the same name).

Parameters:
    

  * **key** (_str_) – The identifier for the collection member.

  * **default** (_Any_) – Optional argument for the value to return if _key_ is not found.


items()
    

Return the identifiers of collection members (matching Python’s dict.items() functionality).

Returns:
    

(key, value) pairs for each member of this collection.

Return type:
    

list[tuple[str, [[bpy.types.bpy_struct]]]]

keys()
    

Return the identifiers of collection members (matching Python’s dict.keys() functionality).

Returns:
    

the identifiers for each member of this collection.

Return type:
    

list[str]

values()
    

Return the values of collection (matching Python’s dict.values() functionality).

Returns:
    

The members of this collection.

Return type:
    

list[[[bpy.types.bpy_struct]] | None]
