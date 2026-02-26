# ID Property Access (idprop.types)

_class _idprop.types.IDPropertyArray
    

to_list()
    

Return the array as a list.

typecode
    

The type of the data in the array {‘f’: float, ‘d’: double, ‘i’: int, ‘b’: bool}.

_class _idprop.types.IDPropertyGroup
    

clear()
    

Clear all members from this group.

get(_key_ , _default =None_)
    

Return the value for key, if it exists, else default.

items()
    

Iterate through the items in the dict; behaves like dictionary method items.

keys()
    

Return the keys associated with this group as a list of strings.

pop(_key_ , _default_)
    

Remove an item from the group, returning a Python representation.

Raises:
    

**KeyError** – When the item doesn’t exist.

Parameters:
    

  * **key** (_str_) – Name of item to remove.

  * **default** (_Any_) – Value to return when key isn’t found, otherwise raise an exception.


to_dict()
    

Return a purely Python version of the group.

update(_other_)
    

Update key, values.

Parameters:
    

**other** (`IDPropertyGroup` | dict[str, Any]) – Updates the values in the group with this.

values()
    

Return the values associated with this group.

name
    

The name of this Group.

_class _idprop.types.IDPropertyGroupIterItems
    

_class _idprop.types.IDPropertyGroupIterKeys
    

_class _idprop.types.IDPropertyGroupIterValues
    

_class _idprop.types.IDPropertyGroupViewItems
    

_class _idprop.types.IDPropertyGroupViewKeys
    

_class _idprop.types.IDPropertyGroupViewValues
