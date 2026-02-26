# bpy_prop_collection_idprop

base classes — [[bpy_prop_collection]]

_class _bpy.types.bpy_prop_collection_idprop
    

built-in class used for user defined collections.

Note

Note that `bpy.types.bpy_prop_collection_idprop` is not actually available from within Blender, it only exists for the purpose of documentation.

add()
    

This is a function to add a new item to a collection.

Returns:
    

A newly created item.

Return type:
    

Any

clear()
    

This is a function to remove all items from a collection.

move(_src_index_ , _dst_index_)
    

This is a function to move an item in a collection.

Parameters:
    

  * **src_index** (_int_) – Source item index.

  * **dst_index** (_int_) – Destination item index.


remove(_index_)
    

This is a function to remove an item from a collection.

Parameters:
    

**index** (_int_) – Index of the item to be removed.
