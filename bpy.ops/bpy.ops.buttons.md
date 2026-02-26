# Buttons Operators

bpy.ops.buttons.clear_filter()
    

Clear the search filter

bpy.ops.buttons.context_menu()
    

Display properties editor context_menu

bpy.ops.buttons.directory_browse(_*_ , _directory =''_, _hide_props_region =True_, _check_existing =False_, _filter_blender =False_, _filter_backup =False_, _filter_image =False_, _filter_movie =False_, _filter_python =False_, _filter_font =False_, _filter_sound =False_, _filter_text =False_, _filter_archive =False_, _filter_btx =False_, _filter_alembic =False_, _filter_usd =False_, _filter_obj =False_, _filter_volume =False_, _filter_folder =False_, _filter_blenlib =False_, _filemode =9_, _relative_path =True_, _display_type ='DEFAULT'_, _sort_method =''_)
    

Open a directory browser, hold Shift to open the file, Alt to browse containing directory

Parameters:
    

  * **directory** (_string_ _,__(__optional_ _,__never None_ _)_) – Directory, Directory of the file

  * **hide_props_region** (_boolean_ _,__(__optional_ _)_) – Hide Operator Properties, Collapse the region displaying the operator settings

  * **check_existing** (_boolean_ _,__(__optional_ _)_) – Check Existing, Check and warn on overwriting existing files

  * **filter_blender** (_boolean_ _,__(__optional_ _)_) – Filter .blend files

  * **filter_backup** (_boolean_ _,__(__optional_ _)_) – Filter .blend files

  * **filter_image** (_boolean_ _,__(__optional_ _)_) – Filter image files

  * **filter_movie** (_boolean_ _,__(__optional_ _)_) – Filter movie files

  * **filter_python** (_boolean_ _,__(__optional_ _)_) – Filter Python files

  * **filter_font** (_boolean_ _,__(__optional_ _)_) – Filter font files

  * **filter_sound** (_boolean_ _,__(__optional_ _)_) – Filter sound files

  * **filter_text** (_boolean_ _,__(__optional_ _)_) – Filter text files

  * **filter_archive** (_boolean_ _,__(__optional_ _)_) – Filter archive files

  * **filter_btx** (_boolean_ _,__(__optional_ _)_) – Filter btx files

  * **filter_alembic** (_boolean_ _,__(__optional_ _)_) – Filter Alembic files

  * **filter_usd** (_boolean_ _,__(__optional_ _)_) – Filter USD files

  * **filter_obj** (_boolean_ _,__(__optional_ _)_) – Filter OBJ files

  * **filter_volume** (_boolean_ _,__(__optional_ _)_) – Filter OpenVDB volume files

  * **filter_folder** (_boolean_ _,__(__optional_ _)_) – Filter folders

  * **filter_blenlib** (_boolean_ _,__(__optional_ _)_) – Filter Blender IDs

  * **filemode** (_int in_ _[__1_ _,__9_ _]__,__(__optional_ _)_) – File Browser Mode, The setting for the file browser mode to load a .blend file, a library or a special file

  * **relative_path** (_boolean_ _,__(__optional_ _)_) – Relative Path, Select the file relative to the blend file

  * **display_type** (enum in [`'DEFAULT'`, `'LIST_VERTICAL'`, `'LIST_HORIZONTAL'`, `'THUMBNAIL'`], (optional)) – 

Display Type

    * `DEFAULT` Default – Automatically determine display type for files.

    * `LIST_VERTICAL` Short List – Display files as short list.

    * `LIST_HORIZONTAL` Long List – Display files as a detailed list.

    * `THUMBNAIL` Thumbnails – Display files as thumbnails.

  * **sort_method** (_enum in_ _[__]__,__(__optional_ _)_) – File sorting mode


bpy.ops.buttons.file_browse(_*_ , _filepath =''_, _hide_props_region =True_, _check_existing =False_, _filter_blender =False_, _filter_backup =False_, _filter_image =False_, _filter_movie =False_, _filter_python =False_, _filter_font =False_, _filter_sound =False_, _filter_text =False_, _filter_archive =False_, _filter_btx =False_, _filter_alembic =False_, _filter_usd =False_, _filter_obj =False_, _filter_volume =False_, _filter_folder =False_, _filter_blenlib =False_, _filemode =9_, _relative_path =True_, _display_type ='DEFAULT'_, _sort_method =''_, _filter_glob =''_)
    

Open a file browser, hold Shift to open the file, Alt to browse containing directory

Parameters:
    

  * **filepath** (_string_ _,__(__optional_ _,__never None_ _)_) – File Path, Path to file

  * **hide_props_region** (_boolean_ _,__(__optional_ _)_) – Hide Operator Properties, Collapse the region displaying the operator settings

  * **check_existing** (_boolean_ _,__(__optional_ _)_) – Check Existing, Check and warn on overwriting existing files

  * **filter_blender** (_boolean_ _,__(__optional_ _)_) – Filter .blend files

  * **filter_backup** (_boolean_ _,__(__optional_ _)_) – Filter .blend files

  * **filter_image** (_boolean_ _,__(__optional_ _)_) – Filter image files

  * **filter_movie** (_boolean_ _,__(__optional_ _)_) – Filter movie files

  * **filter_python** (_boolean_ _,__(__optional_ _)_) – Filter Python files

  * **filter_font** (_boolean_ _,__(__optional_ _)_) – Filter font files

  * **filter_sound** (_boolean_ _,__(__optional_ _)_) – Filter sound files

  * **filter_text** (_boolean_ _,__(__optional_ _)_) – Filter text files

  * **filter_archive** (_boolean_ _,__(__optional_ _)_) – Filter archive files

  * **filter_btx** (_boolean_ _,__(__optional_ _)_) – Filter btx files

  * **filter_alembic** (_boolean_ _,__(__optional_ _)_) – Filter Alembic files

  * **filter_usd** (_boolean_ _,__(__optional_ _)_) – Filter USD files

  * **filter_obj** (_boolean_ _,__(__optional_ _)_) – Filter OBJ files

  * **filter_volume** (_boolean_ _,__(__optional_ _)_) – Filter OpenVDB volume files

  * **filter_folder** (_boolean_ _,__(__optional_ _)_) – Filter folders

  * **filter_blenlib** (_boolean_ _,__(__optional_ _)_) – Filter Blender IDs

  * **filemode** (_int in_ _[__1_ _,__9_ _]__,__(__optional_ _)_) – File Browser Mode, The setting for the file browser mode to load a .blend file, a library or a special file

  * **relative_path** (_boolean_ _,__(__optional_ _)_) – Relative Path, Select the file relative to the blend file

  * **display_type** (enum in [`'DEFAULT'`, `'LIST_VERTICAL'`, `'LIST_HORIZONTAL'`, `'THUMBNAIL'`], (optional)) – 

Display Type

    * `DEFAULT` Default – Automatically determine display type for files.

    * `LIST_VERTICAL` Short List – Display files as short list.

    * `LIST_HORIZONTAL` Long List – Display files as a detailed list.

    * `THUMBNAIL` Thumbnails – Display files as thumbnails.

  * **sort_method** (_enum in_ _[__]__,__(__optional_ _)_) – File sorting mode

  * **filter_glob** (_string_ _,__(__optional_ _,__never None_ _)_) – Glob Filter, Custom filter


bpy.ops.buttons.start_filter()
    

Start entering filter text

bpy.ops.buttons.toggle_pin()
    

Keep the current data-block displayed
  *[*]: Keyword-only parameters separator (PEP 3102)
