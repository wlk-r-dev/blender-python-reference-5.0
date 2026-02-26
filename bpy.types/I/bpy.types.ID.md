# ID(bpy_struct)

base class — [[bpy_struct]]

subclasses — [[Action]], [[Annotation]], [[Armature]], [[Brush]], [[CacheFile]], [[Camera]], [[Collection]], [[Curve]], [[Curves]], [[FreestyleLineStyle]], [[GreasePencil]], [[Image]], [[Key]], [[Lattice]], [[Library]], [[Light]], [[LightProbe]], [[Mask]], [[Material]], [[Mesh]], [[MetaBall]], [[MovieClip]], [[NodeTree]], [[Object]], [[PaintCurve]], [[Palette]], [[ParticleSettings]], [[PointCloud]], [[Scene]], [[Screen]], [[Sound]], [[Speaker]], [[Text]], [[Texture]], [[VectorFont]], [[Volume]], [[WindowManager]], [[WorkSpace]], [[World]]

_class _bpy.types.ID(_bpy_struct_)
    

Base type for data-blocks, defining a unique name, linking from other libraries and garbage collection

asset_data
    

Additional data for an asset data-block

Type:
    

[[AssetMetaData]]

id_type
    

Type identifier of this data-block

Type:
    

enum in [Id Type Items](../../bpy_types_enum_items/id_type_items.md#rna-enum-id-type-items), default `'ACTION'`, (readonly)

is_editable
    

This data-block is editable in the user interface. Linked data-blocks are not editable, except if they were loaded as editable assets.

Type:
    

boolean, default False, (readonly)

is_embedded_data
    

This data-block is not an independent one, but is actually a sub-data of another ID (typical example: root node trees or master collections)

Type:
    

boolean, default False, (readonly)

is_evaluated
    

Whether this ID is runtime-only, evaluated data-block, or actual data from .blend file

Type:
    

boolean, default False, (readonly)

is_library_indirect
    

Is this ID block linked indirectly

Type:
    

boolean, default False, (readonly)

is_linked_packed
    

This data-block is linked and packed into the .blend file

Type:
    

boolean, default False, (readonly)

is_missing
    

This data-block is a place-holder for missing linked data (i.e. it is [an override of] a linked data that could not be found anymore)

Type:
    

boolean, default False, (readonly)

is_runtime_data
    

This data-block is runtime data, i.e. it won’t be saved in .blend file. Note that e.g. evaluated IDs are always runtime, so this value is only editable for data-blocks in Main data-base.

Type:
    

boolean, default False

library
    

Library file the data-block is linked from

Type:
    

[[Library]], (readonly)

library_weak_reference
    

Weak reference to a data-block in another library .blend file (used to re-use already appended data instead of appending new copies)

Type:
    

[[LibraryWeakReference]], (readonly)

name
    

Unique data-block ID name (within a same type and library)

Type:
    

string, default “”, (never None)

name_full
    

Unique data-block ID name, including library one if any

Type:
    

string, default “”, (readonly, never None)

original
    

Actual data-block from .blend file (Main database) that generated that evaluated one

Type:
    

`ID`, (readonly)

override_library
    

Library override data

Type:
    

[[IDOverrideLibrary]], (readonly)

preview
    

Preview image and icon of this data-block (always None if not supported for this type of data)

Type:
    

[[ImagePreview]], (readonly)

session_uid
    

A session-wide unique identifier for the data block that remains the same across renames and internal reallocations, unchanged when reloading the file

Type:
    

int in [-inf, inf], default 0, (readonly)

tag
    

Tools can use this to tag data for their own purposes (initial state is undefined)

Type:
    

boolean, default False

use_extra_user
    

Indicates whether an extra user is set or not (mainly for internal/debug usages)

Type:
    

boolean, default False

use_fake_user
    

Save this data-block even if it has no users

Type:
    

boolean, default False

users
    

Number of times this data-block is referenced

Type:
    

int in [0, inf], default 0, (readonly)

bl_system_properties_get(_*_ , _do_create =False_)
    

DEBUG ONLY. Internal access to runtime-defined RNA data storage, intended solely for testing and debugging purposes. Do not access it in regular scripting work, and in particular, do not assume that it contains writable data

Parameters:
    

**do_create** (_boolean_ _,__(__optional_ _)_) – Ensure that system properties are created if they do not exist yet

Returns:
    

The system properties root container, or None if there are no system properties stored in this data yet, and its creation was not requested

Return type:
    

[[PropertyGroup]]

rename(_name_ , _*_ , _mode ='NEVER'_)
    

More refined handling in case the new name collides with another ID’s name

Parameters:
    

  * **name** (_string_ _,__(__never None_ _)_) – New name to rename the ID to, if empty will re-use the current ID name

  * **mode** (enum in [`'NEVER'`, `'ALWAYS'`, `'SAME_ROOT'`], (optional)) – 

How to handle name collision, in case the requested new name is already used by another ID of the same type

    * `NEVER` Never Rename – Never rename an existing ID whose name would conflict, the currently renamed ID will get a numeric suffix appended to its new name.

    * `ALWAYS` Always Rename – Always rename an existing ID whose name would conflict, ensuring that the currently renamed ID will get requested name.

    * `SAME_ROOT` Rename If Same Root – Only rename an existing ID whose name would conflict if its name root (everything besides the numerical suffix) is the same as the existing name of the currently renamed ID.


Returns:
    

How did the renaming of the data-block went on

  * `UNCHANGED` Unchanged – The ID was not renamed, e.g. because it is already named as requested.

  * `UNCHANGED_COLLISION` Unchanged Due to Collision – The ID was not renamed, because requested name would have collided with another existing ID’s name, and the automatically adjusted name was the same as the current ID’s name.

  * `RENAMED_NO_COLLISION` Renamed Without Collision – The ID was renamed as requested, without creating any name collision.

  * `RENAMED_COLLISION_ADJUSTED` Renamed With Collision – The ID was renamed with adjustment of the requested name, to avoid a name collision.

  * `RENAMED_COLLISION_FORCED` Renamed Enforced With Collision – The ID was renamed as requested, also renaming another ID to avoid a name collision.


Return type:
    

enum in [`'UNCHANGED'`, `'UNCHANGED_COLLISION'`, `'RENAMED_NO_COLLISION'`, `'RENAMED_COLLISION_ADJUSTED'`, `'RENAMED_COLLISION_FORCED'`]

evaluated_get(_depsgraph_)
    

Get corresponding evaluated ID from the given dependency graph. Note that this does not ensure the dependency graph is fully evaluated, it just returns the result of the last evaluation.

Parameters:
    

**depsgraph** ([[Depsgraph]], (never None)) – Dependency graph to perform lookup in

Returns:
    

New copy of the ID

Return type:
    

`ID`

copy()
    

Create a copy of this data-block (not supported for all data-blocks). The result is added to the Blend-File Data (Main database), with all references to other data-blocks ensured to be from within the same Blend-File Data.

Returns:
    

New copy of the ID

Return type:
    

`ID`

asset_mark()
    

Enable easier reuse of the data-block through the Asset Browser, with the help of customizable metadata (like previews, descriptions and tags)

asset_clear()
    

Delete all asset metadata and turn the asset data-block back into a normal data-block

asset_generate_preview()
    

Generate preview image (might be scheduled in a background thread)

override_create(_*_ , _remap_local_usages =False_)
    

Create an overridden local copy of this linked data-block (not supported for all data-blocks)

Parameters:
    

**remap_local_usages** (_boolean_ _,__(__optional_ _)_) – Whether local usages of the linked ID should be remapped to the new library override of it

Returns:
    

New overridden local copy of the ID

Return type:
    

`ID`

override_hierarchy_create(_scene_ , _view_layer_ , _*_ , _reference =None_, _do_fully_editable =False_)
    

Create an overridden local copy of this linked data-block, and most of its dependencies when it is a Collection or and Object

Parameters:
    

  * **scene** ([[Scene]], (never None)) – In which scene the new overrides should be instantiated

  * **view_layer** ([[ViewLayer]], (never None)) – In which view layer the new overrides should be instantiated

  * **reference** (`ID`, (optional)) – Another ID (usually an Object or Collection) used as a hint to decide where to instantiate the new overrides

  * **do_fully_editable** (_boolean_ _,__(__optional_ _)_) – Make all library overrides generated by this call fully editable by the user (none will be ‘system overrides’)


Returns:
    

New overridden local copy of the root ID

Return type:
    

`ID`

user_clear()
    

Clear the user count of a data-block so its not saved, on reload the data will be removed

This function is for advanced use only, misuse can crash Blender since the user count is used to prevent data being removed when it is used.
    
    
    # This example shows what _not_ to do, and will crash Blender.
    import bpy
    
    # Object which is in the scene.
    obj = bpy.data.objects["Cube"]
    
    # Without this, removal would raise an error.
    obj.user_clear()
    
    # Runs without an exception but will crash on redraw.
    bpy.data.objects.remove(obj)
    

user_remap(_new_id_)
    

Replace all usage in the .blend file of this ID by new given one

Parameters:
    

**new_id** (`ID`, (never None)) – New ID to use

make_local(_*_ , _clear_proxy =True_, _clear_liboverride =False_, _clear_asset_data =True_)
    

Make this data-block local, return local one (may be a copy of the original, in case it is also indirectly used)

Parameters:
    

  * **clear_proxy** (_boolean_ _,__(__optional_ _)_) – Deprecated, has no effect

  * **clear_liboverride** (_boolean_ _,__(__optional_ _)_) – Remove potential library override data from the newly made local data

  * **clear_asset_data** (_boolean_ _,__(__optional_ _)_) – Remove potential asset metadata so the newly local data-block is not treated as asset data-block and won’t show up in asset libraries


Returns:
    

This ID, or the new ID if it was copied

Return type:
    

`ID`

user_of_id(_id_)
    

Count the number of times that ID uses/references given one

Parameters:
    

**id** (`ID`, (never None)) – ID to count usages

Returns:
    

Number of usages/references of given id by current data-block

Return type:
    

int in [0, inf]

animation_data_create()
    

Create animation data to this ID, note that not all ID types support this

Returns:
    

New animation data or nullptr

Return type:
    

[[AnimData]]

animation_data_clear()
    

Clear animation on this ID

update_tag(_*_ , _refresh ={}_)
    

Tag the ID to update its display data, e.g. when calling `bpy.types.Scene.update`

Parameters:
    

**refresh** (enum set in {`'OBJECT'`, `'DATA'`, `'TIME'`}, (optional)) – Type of updates to perform

preview_ensure()
    

Ensure that this ID has preview data (if ID type supports it)

Returns:
    

The existing or created preview

Return type:
    

[[ImagePreview]]

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
  
## References

  * [[bpy.context.annotation_data_owner]]
  * [[bpy.context.id]]
  * [[bpy.context.selected_ids]]
  * [[bpy.context.texture_user]]
  * [[Action.fcurve_ensure_for_datablock]]
  * [[ActionSlot.users]]
  * [[AssetRepresentation.local_id]]
  * [[BlendData.pack_linked_ids_hierarchy]]
  * [[BlendData.pack_linked_ids_hierarchy]]
  * [[BlendDataObjects.new]]
  * [[BlendImportContextItem.id]]
  * [[BlendImportContextItem.library_override_id]]
  * [[BlendImportContextItem.reusable_local_id]]
  * [[Depsgraph.id_eval_get]]
  * [[Depsgraph.id_eval_get]]
  * [[Depsgraph.ids]]
  * [[DepsgraphUpdate.id]]
  * [[DopeSheet.source]]
  * [[DriverTarget.id]]
  * `ID.copy`
  * `ID.evaluated_get`
  * `ID.make_local`
  * `ID.original`
  * `ID.override_create`
  * `ID.override_hierarchy_create`
  * `ID.override_hierarchy_create`

| 

  * `ID.user_of_id`
  * `ID.user_remap`
  * [[IDOverrideLibrary.hierarchy_root]]
  * [[IDOverrideLibrary.reference]]
  * [[IDOverrideLibraryPropertyOperation.subitem_local_id]]
  * [[IDOverrideLibraryPropertyOperation.subitem_reference_id]]
  * [[IDOverrideLibraryPropertyOperations.add]]
  * [[IDOverrideLibraryPropertyOperations.add]]
  * [[IDViewerPathElem.id]]
  * [[Key.user]]
  * [[KeyingSetPath.id]]
  * [[KeyingSetPaths.add]]
  * [[MaskParent.id]]
  * [[NodeTree.get_from_context]]
  * [[NodeTree.get_from_context]]
  * [[NodesModifierDataBlock.id]]
  * [[Object.data]]
  * [[PropertyGroupItem.id]]
  * [[SpaceFileBrowser.activate_asset_by_id]]
  * [[SpaceNodeEditor.id]]
  * [[SpaceNodeEditor.id_from]]
  * [[SpaceProperties.pin_id]]
  * [[UILayout.template_action]]
  * [[UILayout.template_path_builder]]
  * [[UILayout.template_preview]]
  * [[UILayout.template_preview]]

  
---|---
  *[*]: Keyword-only parameters separator (PEP 3102)
  *[/]: Positional-only parameter separator (PEP 570)
