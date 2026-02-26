# Script Operators

bpy.ops.script.execute_preset(_*_ , _filepath =''_, _menu_idname =''_)
    

Load a preset

Parameters:
    

  * **filepath** (_string_ _,__(__optional_ _,__never None_ _)_) – filepath

  * **menu_idname** (_string_ _,__(__optional_ _,__never None_ _)_) – Menu ID Name, ID name of the menu this was called from


File:
    

[startup/bl_operators/presets.py:285](https://projects.blender.org/blender/blender/src/branch/main/scripts/startup/bl_operators/presets.py#L285)

bpy.ops.script.python_file_run(_*_ , _filepath =''_)
    

Run Python file

Parameters:
    

**filepath** (_string_ _,__(__optional_ _,__never None_ _)_) – Path

bpy.ops.script.reload()
    

Reload scripts
  *[*]: Keyword-only parameters separator (PEP 3102)
