# Extensions Operators

bpy.ops.extensions.package_disable()
    

Turn off this extension

File:
    

[addons_core/bl_pkg/bl_extension_ops.py:3588](https://projects.blender.org/blender/blender/src/branch/main/scripts/addons_core/bl_pkg/bl_extension_ops.py#L3588)

bpy.ops.extensions.package_install(_*_ , _repo_directory =''_, _repo_index =-1_, _pkg_id =''_, _enable_on_install =True_, _url =''_, _do_legacy_replace =False_)
    

Download and install the extension

Parameters:
    

  * **repo_directory** (_string_ _,__(__optional_ _,__never None_ _)_) – Repo Directory

  * **repo_index** (_int in_ _[__-inf_ _,__inf_ _]__,__(__optional_ _)_) – Repo Index

  * **pkg_id** (_string_ _,__(__optional_ _,__never None_ _)_) – Package ID

  * **enable_on_install** (_boolean_ _,__(__optional_ _)_) – Enable on Install, Enable after installing

  * **url** (_string_ _,__(__optional_ _,__never None_ _)_) – URL

  * **do_legacy_replace** (_boolean_ _,__(__optional_ _)_) – Do Legacy Replace


File:
    

[addons_core/bl_pkg/bl_extension_ops.py:1500](https://projects.blender.org/blender/blender/src/branch/main/scripts/addons_core/bl_pkg/bl_extension_ops.py#L1500)

bpy.ops.extensions.package_install_files(_*_ , _filter_glob ='*.zip;*.py'_, _directory =''_, _files =None_, _filepath =''_, _repo =''_, _enable_on_install =True_, _target =''_, _overwrite =True_, _url =''_)
    

Install extensions from files into a locally managed repository

Parameters:
    

  * **filter_glob** (_string_ _,__(__optional_ _,__never None_ _)_) – filter_glob

  * **directory** (_string_ _,__(__optional_ _,__never None_ _)_) – Directory

  * **files** (`bpy_prop_collection` of `OperatorFileListElement`, (optional)) – files

  * **filepath** (_string_ _,__(__optional_ _,__never None_ _)_) – filepath

  * **repo** (_enum in_ _[__]__,__(__optional_ _)_) – User Repository, The user repository to install extensions into

  * **enable_on_install** (_boolean_ _,__(__optional_ _)_) – Enable on Install, Enable after installing

  * **target** (_enum in_ _[__]__,__(__optional_ _)_) – Legacy Target Path, Path to install legacy add-on packages to

  * **overwrite** (_boolean_ _,__(__optional_ _)_) – Legacy Overwrite, Remove existing add-ons with the same ID

  * **url** (_string_ _,__(__optional_ _,__never None_ _)_) – URL


File:
    

[addons_core/bl_pkg/bl_extension_ops.py:1500](https://projects.blender.org/blender/blender/src/branch/main/scripts/addons_core/bl_pkg/bl_extension_ops.py#L1500)

bpy.ops.extensions.package_install_marked(_*_ , _enable_on_install =True_)
    

Undocumented, consider [contributing](https://developer.blender.org/).

Parameters:
    

**enable_on_install** (_boolean_ _,__(__optional_ _)_) – Enable on Install, Enable after installing

File:
    

[addons_core/bl_pkg/bl_extension_ops.py:1500](https://projects.blender.org/blender/blender/src/branch/main/scripts/addons_core/bl_pkg/bl_extension_ops.py#L1500)

bpy.ops.extensions.package_mark_clear(_*_ , _pkg_id =''_, _repo_index =-1_)
    

Undocumented, consider [contributing](https://developer.blender.org/).

Parameters:
    

  * **pkg_id** (_string_ _,__(__optional_ _,__never None_ _)_) – Package ID

  * **repo_index** (_int in_ _[__-inf_ _,__inf_ _]__,__(__optional_ _)_) – Repo Index


File:
    

[addons_core/bl_pkg/bl_extension_ops.py:3675](https://projects.blender.org/blender/blender/src/branch/main/scripts/addons_core/bl_pkg/bl_extension_ops.py#L3675)

bpy.ops.extensions.package_mark_clear_all()
    

Undocumented, consider [contributing](https://developer.blender.org/).

File:
    

[addons_core/bl_pkg/bl_extension_ops.py:3722](https://projects.blender.org/blender/blender/src/branch/main/scripts/addons_core/bl_pkg/bl_extension_ops.py#L3722)

bpy.ops.extensions.package_mark_set(_*_ , _pkg_id =''_, _repo_index =-1_)
    

Undocumented, consider [contributing](https://developer.blender.org/).

Parameters:
    

  * **pkg_id** (_string_ _,__(__optional_ _,__never None_ _)_) – Package ID

  * **repo_index** (_int in_ _[__-inf_ _,__inf_ _]__,__(__optional_ _)_) – Repo Index


File:
    

[addons_core/bl_pkg/bl_extension_ops.py:3661](https://projects.blender.org/blender/blender/src/branch/main/scripts/addons_core/bl_pkg/bl_extension_ops.py#L3661)

bpy.ops.extensions.package_mark_set_all()
    

Undocumented, consider [contributing](https://developer.blender.org/).

File:
    

[addons_core/bl_pkg/bl_extension_ops.py:3686](https://projects.blender.org/blender/blender/src/branch/main/scripts/addons_core/bl_pkg/bl_extension_ops.py#L3686)

bpy.ops.extensions.package_obsolete_marked()
    

Zeroes package versions, useful for development - to test upgrading

File:
    

[addons_core/bl_pkg/bl_extension_ops.py:3779](https://projects.blender.org/blender/blender/src/branch/main/scripts/addons_core/bl_pkg/bl_extension_ops.py#L3779)

bpy.ops.extensions.package_show_clear(_*_ , _pkg_id =''_, _repo_index =-1_)
    

Undocumented, consider [contributing](https://developer.blender.org/).

Parameters:
    

  * **pkg_id** (_string_ _,__(__optional_ _,__never None_ _)_) – Package ID

  * **repo_index** (_int in_ _[__-inf_ _,__inf_ _]__,__(__optional_ _)_) – Repo Index


File:
    

[addons_core/bl_pkg/bl_extension_ops.py:3748](https://projects.blender.org/blender/blender/src/branch/main/scripts/addons_core/bl_pkg/bl_extension_ops.py#L3748)

bpy.ops.extensions.package_show_set(_*_ , _pkg_id =''_, _repo_index =-1_)
    

Undocumented, consider [contributing](https://developer.blender.org/).

Parameters:
    

  * **pkg_id** (_string_ _,__(__optional_ _,__never None_ _)_) – Package ID

  * **repo_index** (_int in_ _[__-inf_ _,__inf_ _]__,__(__optional_ _)_) – Repo Index


File:
    

[addons_core/bl_pkg/bl_extension_ops.py:3734](https://projects.blender.org/blender/blender/src/branch/main/scripts/addons_core/bl_pkg/bl_extension_ops.py#L3734)

bpy.ops.extensions.package_show_settings(_*_ , _pkg_id =''_, _repo_index =-1_)
    

Undocumented, consider [contributing](https://developer.blender.org/).

Parameters:
    

  * **pkg_id** (_string_ _,__(__optional_ _,__never None_ _)_) – Package ID

  * **repo_index** (_int in_ _[__-inf_ _,__inf_ _]__,__(__optional_ _)_) – Repo Index


File:
    

[addons_core/bl_pkg/bl_extension_ops.py:3762](https://projects.blender.org/blender/blender/src/branch/main/scripts/addons_core/bl_pkg/bl_extension_ops.py#L3762)

bpy.ops.extensions.package_theme_disable(_*_ , _pkg_id =''_, _repo_index =-1_)
    

Turn off this theme

Parameters:
    

  * **pkg_id** (_string_ _,__(__optional_ _,__never None_ _)_) – Package ID

  * **repo_index** (_int in_ _[__-inf_ _,__inf_ _]__,__(__optional_ _)_) – Repo Index


File:
    

[addons_core/bl_pkg/bl_extension_ops.py:3616](https://projects.blender.org/blender/blender/src/branch/main/scripts/addons_core/bl_pkg/bl_extension_ops.py#L3616)

bpy.ops.extensions.package_theme_enable(_*_ , _pkg_id =''_, _repo_index =-1_)
    

Turn off this theme

Parameters:
    

  * **pkg_id** (_string_ _,__(__optional_ _,__never None_ _)_) – Package ID

  * **repo_index** (_int in_ _[__-inf_ _,__inf_ _]__,__(__optional_ _)_) – Repo Index


File:
    

[addons_core/bl_pkg/bl_extension_ops.py:3601](https://projects.blender.org/blender/blender/src/branch/main/scripts/addons_core/bl_pkg/bl_extension_ops.py#L3601)

bpy.ops.extensions.package_uninstall(_*_ , _repo_directory =''_, _repo_index =-1_, _pkg_id =''_)
    

Disable and uninstall the extension

Parameters:
    

  * **repo_directory** (_string_ _,__(__optional_ _,__never None_ _)_) – Repo Directory

  * **repo_index** (_int in_ _[__-inf_ _,__inf_ _]__,__(__optional_ _)_) – Repo Index

  * **pkg_id** (_string_ _,__(__optional_ _,__never None_ _)_) – Package ID


File:
    

[addons_core/bl_pkg/bl_extension_ops.py:1500](https://projects.blender.org/blender/blender/src/branch/main/scripts/addons_core/bl_pkg/bl_extension_ops.py#L1500)

bpy.ops.extensions.package_uninstall_marked()
    

Undocumented, consider [contributing](https://developer.blender.org/).

File:
    

[addons_core/bl_pkg/bl_extension_ops.py:1500](https://projects.blender.org/blender/blender/src/branch/main/scripts/addons_core/bl_pkg/bl_extension_ops.py#L1500)

bpy.ops.extensions.package_uninstall_system()
    

Undocumented, consider [contributing](https://developer.blender.org/).

File:
    

[addons_core/bl_pkg/bl_extension_ops.py:3579](https://projects.blender.org/blender/blender/src/branch/main/scripts/addons_core/bl_pkg/bl_extension_ops.py#L3579)

bpy.ops.extensions.package_upgrade_all(_*_ , _use_active_only =False_)
    

Upgrade all the extensions to their latest version for all the remote repositories

Parameters:
    

**use_active_only** (_boolean_ _,__(__optional_ _)_) – Active Only, Only sync the active repository

File:
    

[addons_core/bl_pkg/bl_extension_ops.py:1500](https://projects.blender.org/blender/blender/src/branch/main/scripts/addons_core/bl_pkg/bl_extension_ops.py#L1500)

bpy.ops.extensions.repo_enable_from_drop(_*_ , _repo_index =-1_)
    

Undocumented, consider [contributing](https://developer.blender.org/).

Parameters:
    

**repo_index** (_int in_ _[__-inf_ _,__inf_ _]__,__(__optional_ _)_) – Repo Index

File:
    

[addons_core/bl_pkg/bl_extension_ops.py:1830](https://projects.blender.org/blender/blender/src/branch/main/scripts/addons_core/bl_pkg/bl_extension_ops.py#L1830)

bpy.ops.extensions.repo_lock_all()
    

Lock repositories - to test locking

File:
    

[addons_core/bl_pkg/bl_extension_ops.py:3848](https://projects.blender.org/blender/blender/src/branch/main/scripts/addons_core/bl_pkg/bl_extension_ops.py#L3848)

bpy.ops.extensions.repo_refresh_all(_*_ , _use_active_only =False_)
    

Scan extension & legacy add-ons for changes to modules & meta-data (similar to restarting). Any issues are reported as warnings

Parameters:
    

**use_active_only** (_boolean_ _,__(__optional_ _)_) – Active Only, Only refresh the active repository

File:
    

[addons_core/bl_pkg/bl_extension_ops.py:1743](https://projects.blender.org/blender/blender/src/branch/main/scripts/addons_core/bl_pkg/bl_extension_ops.py#L1743)

bpy.ops.extensions.repo_sync(_*_ , _repo_directory =''_, _repo_index =-1_)
    

Undocumented, consider [contributing](https://developer.blender.org/).

Parameters:
    

  * **repo_directory** (_string_ _,__(__optional_ _,__never None_ _)_) – Repo Directory

  * **repo_index** (_int in_ _[__-inf_ _,__inf_ _]__,__(__optional_ _)_) – Repo Index


File:
    

[addons_core/bl_pkg/bl_extension_ops.py:1500](https://projects.blender.org/blender/blender/src/branch/main/scripts/addons_core/bl_pkg/bl_extension_ops.py#L1500)

bpy.ops.extensions.repo_sync_all(_*_ , _use_active_only =False_)
    

Refresh the list of extensions for all the remote repositories

Parameters:
    

**use_active_only** (_boolean_ _,__(__optional_ _)_) – Active Only, Only sync the active repository

File:
    

[addons_core/bl_pkg/bl_extension_ops.py:1500](https://projects.blender.org/blender/blender/src/branch/main/scripts/addons_core/bl_pkg/bl_extension_ops.py#L1500)

bpy.ops.extensions.repo_unlock()
    

Remove the repository file-system lock

File:
    

[addons_core/bl_pkg/bl_extension_ops.py:1917](https://projects.blender.org/blender/blender/src/branch/main/scripts/addons_core/bl_pkg/bl_extension_ops.py#L1917)

bpy.ops.extensions.repo_unlock_all()
    

Unlock repositories - to test unlocking

File:
    

[addons_core/bl_pkg/bl_extension_ops.py:3874](https://projects.blender.org/blender/blender/src/branch/main/scripts/addons_core/bl_pkg/bl_extension_ops.py#L3874)

bpy.ops.extensions.status_clear()
    

Undocumented, consider [contributing](https://developer.blender.org/).

File:
    

[addons_core/bl_pkg/bl_extension_ops.py:3647](https://projects.blender.org/blender/blender/src/branch/main/scripts/addons_core/bl_pkg/bl_extension_ops.py#L3647)

bpy.ops.extensions.status_clear_errors()
    

Undocumented, consider [contributing](https://developer.blender.org/).

File:
    

[addons_core/bl_pkg/bl_extension_ops.py:3636](https://projects.blender.org/blender/blender/src/branch/main/scripts/addons_core/bl_pkg/bl_extension_ops.py#L3636)

bpy.ops.extensions.userpref_allow_online()
    

Allow internet access. Blender may access configured online extension repositories. Installed third party add-ons may access the internet for their own functionality

File:
    

[addons_core/bl_pkg/bl_extension_ops.py:3999](https://projects.blender.org/blender/blender/src/branch/main/scripts/addons_core/bl_pkg/bl_extension_ops.py#L3999)

bpy.ops.extensions.userpref_allow_online_popup()
    

Allow internet access. Blender may access configured online extension repositories. Installed third party add-ons may access the internet for their own functionality

File:
    

[addons_core/bl_pkg/bl_extension_ops.py:4013](https://projects.blender.org/blender/blender/src/branch/main/scripts/addons_core/bl_pkg/bl_extension_ops.py#L4013)

bpy.ops.extensions.userpref_show_for_update()
    

Open extensions preferences

File:
    

[addons_core/bl_pkg/bl_extension_ops.py:3939](https://projects.blender.org/blender/blender/src/branch/main/scripts/addons_core/bl_pkg/bl_extension_ops.py#L3939)

bpy.ops.extensions.userpref_show_online()
    

Show system preferences “Network” panel to allow online access

File:
    

[addons_core/bl_pkg/bl_extension_ops.py:3979](https://projects.blender.org/blender/blender/src/branch/main/scripts/addons_core/bl_pkg/bl_extension_ops.py#L3979)

bpy.ops.extensions.userpref_tags_set(_*_ , _value =False_, _data_path =''_)
    

Set the value of all tags

Parameters:
    

  * **value** (_boolean_ _,__(__optional_ _)_) – Value, Enable or disable all tags

  * **data_path** (_string_ _,__(__optional_ _,__never None_ _)_) – Data Path


File:
    

[addons_core/bl_pkg/bl_extension_ops.py:3908](https://projects.blender.org/blender/blender/src/branch/main/scripts/addons_core/bl_pkg/bl_extension_ops.py#L3908)
  *[*]: Keyword-only parameters separator (PEP 3102)
