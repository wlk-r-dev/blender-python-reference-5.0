# bpy_extras submodule (bpy_extras.anim_utils)

bpy_extras.anim_utils.bake_action(_obj_ , _*_ , _action_ , _frames_ , _bake_options_)
    

Parameters:
    

  * **obj** ([`bpy.types.Object`](../bpy.types/O/bpy.types.Object.md#bpy.types.Object "bpy.types.Object")) – Object to bake.

  * **action** ([`bpy.types.Action`](../bpy.types/A/bpy.types.Action.md#bpy.types.Action "bpy.types.Action") | None) – An action to bake the data into, or None for a new action to be created.

  * **frames** (_int_) – Frames to bake.

  * **bake_options** (`anim_utils.BakeOptions`) – Options for baking.


Returns:
    

Action or None.

Return type:
    

[`bpy.types.Action`](../bpy.types/A/bpy.types.Action.md#bpy.types.Action "bpy.types.Action") | None

bpy_extras.anim_utils.bake_action_objects(_object_action_pairs_ , _*_ , _frames_ , _bake_options_)
    

A version of `bake_action_objects_iter()` that takes frames and returns the output.

Parameters:
    

  * **frames** (_iterable_ _of_ _int_) – Frames to bake.

  * **bake_options** (`anim_utils.BakeOptions`) – Options for baking.


Returns:
    

A sequence of Action or None types (aligned with `object_action_pairs`)

Return type:
    

Sequence[[`bpy.types.Action`](../bpy.types/A/bpy.types.Action.md#bpy.types.Action "bpy.types.Action")]

bpy_extras.anim_utils.bake_action_iter(_obj_ , _*_ , _action_ , _bake_options_)
    

An coroutine that bakes action for a single object.

Parameters:
    

  * **obj** ([`bpy.types.Object`](../bpy.types/O/bpy.types.Object.md#bpy.types.Object "bpy.types.Object")) – Object to bake.

  * **action** ([`bpy.types.Action`](../bpy.types/A/bpy.types.Action.md#bpy.types.Action "bpy.types.Action") | None) – An action to bake the data into, or None for a new action to be created.

  * **bake_options** (`anim_utils.BakeOptions`) – Boolean options of what to include into the action bake.


Returns:
    

an action or None

Return type:
    

[`bpy.types.Action`](../bpy.types/A/bpy.types.Action.md#bpy.types.Action "bpy.types.Action")

bpy_extras.anim_utils.bake_action_objects_iter(_object_action_pairs_ , _bake_options_)
    

An coroutine that bakes actions for multiple objects.

Parameters:
    

  * **object_action_pairs** (Sequence of ([`bpy.types.Object`](../bpy.types/O/bpy.types.Object.md#bpy.types.Object "bpy.types.Object"), [`bpy.types.Action`](../bpy.types/A/bpy.types.Action.md#bpy.types.Action "bpy.types.Action"))) – Sequence of object action tuples, action is the destination for the baked data. When None a new action will be created.

  * **bake_options** (`anim_utils.BakeOptions`) – Options for baking.


_class _bpy_extras.anim_utils.AutoKeying
    

Auto-keying support.

Retrieve the lock status for 4D rotation.

_class _bpy_extras.anim_utils.BakeOptions
    

BakeOptions(only_selected: bool, do_pose: bool, do_object: bool, do_visual_keying: bool, do_constraint_clear: bool, do_parents_clear: bool, do_clean: bool, do_location: bool, do_rotation: bool, do_scale: bool, do_bbone: bool, do_custom_props: bool)
  *[*]: Keyword-only parameters separator (PEP 3102)
