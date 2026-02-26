# BlendData(bpy_struct)

base class — [`bpy_struct`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct "bpy.types.bpy_struct")

_class _bpy.types.BlendData(_bpy_struct_)
    

Main data structure representing a .blend file and all its data-blocks

actions
    

Action data-blocks

Type:
    

[`BlendDataActions`](bpy.types.BlendDataActions.md#bpy.types.BlendDataActions "bpy.types.BlendDataActions") [`bpy_prop_collection`](../_other/bpy.types.bpy_prop_collection.md#bpy.types.bpy_prop_collection "bpy.types.bpy_prop_collection") of [`Action`](../A/bpy.types.Action.md#bpy.types.Action "bpy.types.Action"), (readonly)

annotations
    

Annotation data-blocks (legacy Grease Pencil)

Type:
    

[`BlendDataAnnotations`](bpy.types.BlendDataAnnotations.md#bpy.types.BlendDataAnnotations "bpy.types.BlendDataAnnotations") [`bpy_prop_collection`](../_other/bpy.types.bpy_prop_collection.md#bpy.types.bpy_prop_collection "bpy.types.bpy_prop_collection") of [`Annotation`](../A/bpy.types.Annotation.md#bpy.types.Annotation "bpy.types.Annotation"), (readonly)

armatures
    

Armature data-blocks

Type:
    

[`BlendDataArmatures`](bpy.types.BlendDataArmatures.md#bpy.types.BlendDataArmatures "bpy.types.BlendDataArmatures") [`bpy_prop_collection`](../_other/bpy.types.bpy_prop_collection.md#bpy.types.bpy_prop_collection "bpy.types.bpy_prop_collection") of [`Armature`](../A/bpy.types.Armature.md#bpy.types.Armature "bpy.types.Armature"), (readonly)

brushes
    

Brush data-blocks

Type:
    

[`BlendDataBrushes`](bpy.types.BlendDataBrushes.md#bpy.types.BlendDataBrushes "bpy.types.BlendDataBrushes") [`bpy_prop_collection`](../_other/bpy.types.bpy_prop_collection.md#bpy.types.bpy_prop_collection "bpy.types.bpy_prop_collection") of [`Brush`](bpy.types.Brush.md#bpy.types.Brush "bpy.types.Brush"), (readonly)

cache_files
    

Cache Files data-blocks

Type:
    

[`BlendDataCacheFiles`](bpy.types.BlendDataCacheFiles.md#bpy.types.BlendDataCacheFiles "bpy.types.BlendDataCacheFiles") [`bpy_prop_collection`](../_other/bpy.types.bpy_prop_collection.md#bpy.types.bpy_prop_collection "bpy.types.bpy_prop_collection") of [`CacheFile`](../C/bpy.types.CacheFile.md#bpy.types.CacheFile "bpy.types.CacheFile"), (readonly)

cameras
    

Camera data-blocks

Type:
    

[`BlendDataCameras`](bpy.types.BlendDataCameras.md#bpy.types.BlendDataCameras "bpy.types.BlendDataCameras") [`bpy_prop_collection`](../_other/bpy.types.bpy_prop_collection.md#bpy.types.bpy_prop_collection "bpy.types.bpy_prop_collection") of [`Camera`](../C/bpy.types.Camera.md#bpy.types.Camera "bpy.types.Camera"), (readonly)

collections
    

Collection data-blocks

Type:
    

[`BlendDataCollections`](bpy.types.BlendDataCollections.md#bpy.types.BlendDataCollections "bpy.types.BlendDataCollections") [`bpy_prop_collection`](../_other/bpy.types.bpy_prop_collection.md#bpy.types.bpy_prop_collection "bpy.types.bpy_prop_collection") of [`Collection`](../C/bpy.types.Collection.md#bpy.types.Collection "bpy.types.Collection"), (readonly)

colorspace
    

Information about the color space used for data-blocks in a blend file

Type:
    

[`BlendFileColorspace`](bpy.types.BlendFileColorspace.md#bpy.types.BlendFileColorspace "bpy.types.BlendFileColorspace"), (readonly, never None)

curves
    

Curve data-blocks

Type:
    

[`BlendDataCurves`](bpy.types.BlendDataCurves.md#bpy.types.BlendDataCurves "bpy.types.BlendDataCurves") [`bpy_prop_collection`](../_other/bpy.types.bpy_prop_collection.md#bpy.types.bpy_prop_collection "bpy.types.bpy_prop_collection") of [`Curve`](../C/bpy.types.Curve.md#bpy.types.Curve "bpy.types.Curve"), (readonly)

filepath
    

Path to the .blend file

Type:
    

string, default “”, (readonly, never None)

fonts
    

Vector font data-blocks

Type:
    

[`BlendDataFonts`](bpy.types.BlendDataFonts.md#bpy.types.BlendDataFonts "bpy.types.BlendDataFonts") [`bpy_prop_collection`](../_other/bpy.types.bpy_prop_collection.md#bpy.types.bpy_prop_collection "bpy.types.bpy_prop_collection") of [`VectorFont`](../V/bpy.types.VectorFont.md#bpy.types.VectorFont "bpy.types.VectorFont"), (readonly)

grease_pencils
    

Grease Pencil data-blocks

Type:
    

[`BlendDataGreasePencilsV3`](bpy.types.BlendDataGreasePencilsV3.md#bpy.types.BlendDataGreasePencilsV3 "bpy.types.BlendDataGreasePencilsV3") [`bpy_prop_collection`](../_other/bpy.types.bpy_prop_collection.md#bpy.types.bpy_prop_collection "bpy.types.bpy_prop_collection") of [`GreasePencil`](../G/bpy.types.GreasePencil.md#bpy.types.GreasePencil "bpy.types.GreasePencil"), (readonly)

hair_curves
    

Hair curve data-blocks

Type:
    

[`BlendDataHairCurves`](bpy.types.BlendDataHairCurves.md#bpy.types.BlendDataHairCurves "bpy.types.BlendDataHairCurves") [`bpy_prop_collection`](../_other/bpy.types.bpy_prop_collection.md#bpy.types.bpy_prop_collection "bpy.types.bpy_prop_collection") of [`Curves`](../C/bpy.types.Curves.md#bpy.types.Curves "bpy.types.Curves"), (readonly)

images
    

Image data-blocks

Type:
    

[`BlendDataImages`](bpy.types.BlendDataImages.md#bpy.types.BlendDataImages "bpy.types.BlendDataImages") [`bpy_prop_collection`](../_other/bpy.types.bpy_prop_collection.md#bpy.types.bpy_prop_collection "bpy.types.bpy_prop_collection") of [`Image`](../I/bpy.types.Image.md#bpy.types.Image "bpy.types.Image"), (readonly)

is_dirty
    

Have recent edits been saved to disk

Type:
    

boolean, default False, (readonly)

is_saved
    

Has the current session been saved to disk as a .blend file

Type:
    

boolean, default False, (readonly)

lattices
    

Lattice data-blocks

Type:
    

[`BlendDataLattices`](bpy.types.BlendDataLattices.md#bpy.types.BlendDataLattices "bpy.types.BlendDataLattices") [`bpy_prop_collection`](../_other/bpy.types.bpy_prop_collection.md#bpy.types.bpy_prop_collection "bpy.types.bpy_prop_collection") of [`Lattice`](../L/bpy.types.Lattice.md#bpy.types.Lattice "bpy.types.Lattice"), (readonly)

libraries
    

Library data-blocks

Type:
    

[`BlendDataLibraries`](bpy.types.BlendDataLibraries.md#bpy.types.BlendDataLibraries "bpy.types.BlendDataLibraries") [`bpy_prop_collection`](../_other/bpy.types.bpy_prop_collection.md#bpy.types.bpy_prop_collection "bpy.types.bpy_prop_collection") of [`Library`](../L/bpy.types.Library.md#bpy.types.Library "bpy.types.Library"), (readonly)

lightprobes
    

Light Probe data-blocks

Type:
    

[`BlendDataProbes`](bpy.types.BlendDataProbes.md#bpy.types.BlendDataProbes "bpy.types.BlendDataProbes") [`bpy_prop_collection`](../_other/bpy.types.bpy_prop_collection.md#bpy.types.bpy_prop_collection "bpy.types.bpy_prop_collection") of [`LightProbe`](../L/bpy.types.LightProbe.md#bpy.types.LightProbe "bpy.types.LightProbe"), (readonly)

lights
    

Light data-blocks

Type:
    

[`BlendDataLights`](bpy.types.BlendDataLights.md#bpy.types.BlendDataLights "bpy.types.BlendDataLights") [`bpy_prop_collection`](../_other/bpy.types.bpy_prop_collection.md#bpy.types.bpy_prop_collection "bpy.types.bpy_prop_collection") of [`Light`](../L/bpy.types.Light.md#bpy.types.Light "bpy.types.Light"), (readonly)

linestyles
    

Line Style data-blocks

Type:
    

[`BlendDataLineStyles`](bpy.types.BlendDataLineStyles.md#bpy.types.BlendDataLineStyles "bpy.types.BlendDataLineStyles") [`bpy_prop_collection`](../_other/bpy.types.bpy_prop_collection.md#bpy.types.bpy_prop_collection "bpy.types.bpy_prop_collection") of [`FreestyleLineStyle`](../F/bpy.types.FreestyleLineStyle.md#bpy.types.FreestyleLineStyle "bpy.types.FreestyleLineStyle"), (readonly)

masks
    

Masks data-blocks

Type:
    

[`BlendDataMasks`](bpy.types.BlendDataMasks.md#bpy.types.BlendDataMasks "bpy.types.BlendDataMasks") [`bpy_prop_collection`](../_other/bpy.types.bpy_prop_collection.md#bpy.types.bpy_prop_collection "bpy.types.bpy_prop_collection") of [`Mask`](../M/bpy.types.Mask.md#bpy.types.Mask "bpy.types.Mask"), (readonly)

materials
    

Material data-blocks

Type:
    

[`BlendDataMaterials`](bpy.types.BlendDataMaterials.md#bpy.types.BlendDataMaterials "bpy.types.BlendDataMaterials") [`bpy_prop_collection`](../_other/bpy.types.bpy_prop_collection.md#bpy.types.bpy_prop_collection "bpy.types.bpy_prop_collection") of [`Material`](../M/bpy.types.Material.md#bpy.types.Material "bpy.types.Material"), (readonly)

meshes
    

Mesh data-blocks

Type:
    

[`BlendDataMeshes`](bpy.types.BlendDataMeshes.md#bpy.types.BlendDataMeshes "bpy.types.BlendDataMeshes") [`bpy_prop_collection`](../_other/bpy.types.bpy_prop_collection.md#bpy.types.bpy_prop_collection "bpy.types.bpy_prop_collection") of [`Mesh`](../M/bpy.types.Mesh.md#bpy.types.Mesh "bpy.types.Mesh"), (readonly)

metaballs
    

Metaball data-blocks

Type:
    

[`BlendDataMetaBalls`](bpy.types.BlendDataMetaBalls.md#bpy.types.BlendDataMetaBalls "bpy.types.BlendDataMetaBalls") [`bpy_prop_collection`](../_other/bpy.types.bpy_prop_collection.md#bpy.types.bpy_prop_collection "bpy.types.bpy_prop_collection") of [`MetaBall`](../M/bpy.types.MetaBall.md#bpy.types.MetaBall "bpy.types.MetaBall"), (readonly)

movieclips
    

Movie Clip data-blocks

Type:
    

[`BlendDataMovieClips`](bpy.types.BlendDataMovieClips.md#bpy.types.BlendDataMovieClips "bpy.types.BlendDataMovieClips") [`bpy_prop_collection`](../_other/bpy.types.bpy_prop_collection.md#bpy.types.bpy_prop_collection "bpy.types.bpy_prop_collection") of [`MovieClip`](../M/bpy.types.MovieClip.md#bpy.types.MovieClip "bpy.types.MovieClip"), (readonly)

node_groups
    

Node group data-blocks

Type:
    

[`BlendDataNodeTrees`](bpy.types.BlendDataNodeTrees.md#bpy.types.BlendDataNodeTrees "bpy.types.BlendDataNodeTrees") [`bpy_prop_collection`](../_other/bpy.types.bpy_prop_collection.md#bpy.types.bpy_prop_collection "bpy.types.bpy_prop_collection") of [`NodeTree`](../N/bpy.types.NodeTree.md#bpy.types.NodeTree "bpy.types.NodeTree"), (readonly)

objects
    

Object data-blocks

Type:
    

[`BlendDataObjects`](bpy.types.BlendDataObjects.md#bpy.types.BlendDataObjects "bpy.types.BlendDataObjects") [`bpy_prop_collection`](../_other/bpy.types.bpy_prop_collection.md#bpy.types.bpy_prop_collection "bpy.types.bpy_prop_collection") of [`Object`](../O/bpy.types.Object.md#bpy.types.Object "bpy.types.Object"), (readonly)

paint_curves
    

Paint Curves data-blocks

Type:
    

[`BlendDataPaintCurves`](bpy.types.BlendDataPaintCurves.md#bpy.types.BlendDataPaintCurves "bpy.types.BlendDataPaintCurves") [`bpy_prop_collection`](../_other/bpy.types.bpy_prop_collection.md#bpy.types.bpy_prop_collection "bpy.types.bpy_prop_collection") of [`PaintCurve`](../P/bpy.types.PaintCurve.md#bpy.types.PaintCurve "bpy.types.PaintCurve"), (readonly)

palettes
    

Palette data-blocks

Type:
    

[`BlendDataPalettes`](bpy.types.BlendDataPalettes.md#bpy.types.BlendDataPalettes "bpy.types.BlendDataPalettes") [`bpy_prop_collection`](../_other/bpy.types.bpy_prop_collection.md#bpy.types.bpy_prop_collection "bpy.types.bpy_prop_collection") of [`Palette`](../P/bpy.types.Palette.md#bpy.types.Palette "bpy.types.Palette"), (readonly)

particles
    

Particle data-blocks

Type:
    

[`BlendDataParticles`](bpy.types.BlendDataParticles.md#bpy.types.BlendDataParticles "bpy.types.BlendDataParticles") [`bpy_prop_collection`](../_other/bpy.types.bpy_prop_collection.md#bpy.types.bpy_prop_collection "bpy.types.bpy_prop_collection") of [`ParticleSettings`](../P/bpy.types.ParticleSettings.md#bpy.types.ParticleSettings "bpy.types.ParticleSettings"), (readonly)

pointclouds
    

Point cloud data-blocks

Type:
    

[`BlendDataPointClouds`](bpy.types.BlendDataPointClouds.md#bpy.types.BlendDataPointClouds "bpy.types.BlendDataPointClouds") [`bpy_prop_collection`](../_other/bpy.types.bpy_prop_collection.md#bpy.types.bpy_prop_collection "bpy.types.bpy_prop_collection") of [`PointCloud`](../P/bpy.types.PointCloud.md#bpy.types.PointCloud "bpy.types.PointCloud"), (readonly)

scenes
    

Scene data-blocks

Type:
    

[`BlendDataScenes`](bpy.types.BlendDataScenes.md#bpy.types.BlendDataScenes "bpy.types.BlendDataScenes") [`bpy_prop_collection`](../_other/bpy.types.bpy_prop_collection.md#bpy.types.bpy_prop_collection "bpy.types.bpy_prop_collection") of [`Scene`](../S/bpy.types.Scene.md#bpy.types.Scene "bpy.types.Scene"), (readonly)

screens
    

Screen data-blocks

Type:
    

[`BlendDataScreens`](bpy.types.BlendDataScreens.md#bpy.types.BlendDataScreens "bpy.types.BlendDataScreens") [`bpy_prop_collection`](../_other/bpy.types.bpy_prop_collection.md#bpy.types.bpy_prop_collection "bpy.types.bpy_prop_collection") of [`Screen`](../S/bpy.types.Screen.md#bpy.types.Screen "bpy.types.Screen"), (readonly)

shape_keys
    

Shape Key data-blocks

Type:
    

[`bpy_prop_collection`](../_other/bpy.types.bpy_prop_collection.md#bpy.types.bpy_prop_collection "bpy.types.bpy_prop_collection") of [`Key`](../K/bpy.types.Key.md#bpy.types.Key "bpy.types.Key"), (readonly)

sounds
    

Sound data-blocks

Type:
    

[`BlendDataSounds`](bpy.types.BlendDataSounds.md#bpy.types.BlendDataSounds "bpy.types.BlendDataSounds") [`bpy_prop_collection`](../_other/bpy.types.bpy_prop_collection.md#bpy.types.bpy_prop_collection "bpy.types.bpy_prop_collection") of [`Sound`](../S/bpy.types.Sound.md#bpy.types.Sound "bpy.types.Sound"), (readonly)

speakers
    

Speaker data-blocks

Type:
    

[`BlendDataSpeakers`](bpy.types.BlendDataSpeakers.md#bpy.types.BlendDataSpeakers "bpy.types.BlendDataSpeakers") [`bpy_prop_collection`](../_other/bpy.types.bpy_prop_collection.md#bpy.types.bpy_prop_collection "bpy.types.bpy_prop_collection") of [`Speaker`](../S/bpy.types.Speaker.md#bpy.types.Speaker "bpy.types.Speaker"), (readonly)

texts
    

Text data-blocks

Type:
    

[`BlendDataTexts`](bpy.types.BlendDataTexts.md#bpy.types.BlendDataTexts "bpy.types.BlendDataTexts") [`bpy_prop_collection`](../_other/bpy.types.bpy_prop_collection.md#bpy.types.bpy_prop_collection "bpy.types.bpy_prop_collection") of [`Text`](../T/bpy.types.Text.md#bpy.types.Text "bpy.types.Text"), (readonly)

textures
    

Texture data-blocks

Type:
    

[`BlendDataTextures`](bpy.types.BlendDataTextures.md#bpy.types.BlendDataTextures "bpy.types.BlendDataTextures") [`bpy_prop_collection`](../_other/bpy.types.bpy_prop_collection.md#bpy.types.bpy_prop_collection "bpy.types.bpy_prop_collection") of [`Texture`](../T/bpy.types.Texture.md#bpy.types.Texture "bpy.types.Texture"), (readonly)

use_autopack
    

Automatically pack all external data into .blend file

Type:
    

boolean, default False

version
    

File format version the .blend file was saved with

Type:
    

int array of 3 items in [0, inf], default (0, 0, 0), (readonly)

volumes
    

Volume data-blocks

Type:
    

[`BlendDataVolumes`](bpy.types.BlendDataVolumes.md#bpy.types.BlendDataVolumes "bpy.types.BlendDataVolumes") [`bpy_prop_collection`](../_other/bpy.types.bpy_prop_collection.md#bpy.types.bpy_prop_collection "bpy.types.bpy_prop_collection") of [`Volume`](../V/bpy.types.Volume.md#bpy.types.Volume "bpy.types.Volume"), (readonly)

window_managers
    

Window manager data-blocks

Type:
    

[`BlendDataWindowManagers`](bpy.types.BlendDataWindowManagers.md#bpy.types.BlendDataWindowManagers "bpy.types.BlendDataWindowManagers") [`bpy_prop_collection`](../_other/bpy.types.bpy_prop_collection.md#bpy.types.bpy_prop_collection "bpy.types.bpy_prop_collection") of [`WindowManager`](../W/bpy.types.WindowManager.md#bpy.types.WindowManager "bpy.types.WindowManager"), (readonly)

workspaces
    

Workspace data-blocks

Type:
    

[`BlendDataWorkSpaces`](bpy.types.BlendDataWorkSpaces.md#bpy.types.BlendDataWorkSpaces "bpy.types.BlendDataWorkSpaces") [`bpy_prop_collection`](../_other/bpy.types.bpy_prop_collection.md#bpy.types.bpy_prop_collection "bpy.types.bpy_prop_collection") of [`WorkSpace`](../W/bpy.types.WorkSpace.md#bpy.types.WorkSpace "bpy.types.WorkSpace"), (readonly)

worlds
    

World data-blocks

Type:
    

[`BlendDataWorlds`](bpy.types.BlendDataWorlds.md#bpy.types.BlendDataWorlds "bpy.types.BlendDataWorlds") [`bpy_prop_collection`](../_other/bpy.types.bpy_prop_collection.md#bpy.types.bpy_prop_collection "bpy.types.bpy_prop_collection") of [`World`](../W/bpy.types.World.md#bpy.types.World "bpy.types.World"), (readonly)

pack_linked_ids_hierarchy(_root_id_)
    

Pack the given linked ID and its dependencies into current blendfile

Parameters:
    

**root_id** ([`ID`](../I/bpy.types.ID.md#bpy.types.ID "bpy.types.ID")) – Root linked ID to pack

Returns:
    

The packed ID matching the given root ID

Return type:
    

[`ID`](../I/bpy.types.ID.md#bpy.types.ID "bpy.types.ID")

batch_remove(_ids_)
    

Remove (delete) several IDs at once.

Note that this function is quicker than individual calls to `remove()` (from `bpy.types.BlendData` ID collections), but less safe/versatile (it can break Blender, e.g. by removing all scenes…).

Parameters:
    

**ids** (Sequence[[`bpy.types.ID`](../I/bpy.types.ID.md#bpy.types.ID "bpy.types.ID")]) – Sequence of IDs (types can be mixed).

_classmethod _bl_rna_get_subclass(_id_ , _default =None_, _/_)
    

Parameters:
    

**id** (_str_) – The RNA type identifier.

Returns:
    

The RNA type or default when not found.

Return type:
    

[`bpy.types.Struct`](../S/bpy.types.Struct.md#bpy.types.Struct "bpy.types.Struct") subclass

_classmethod _bl_rna_get_subclass_py(_id_ , _default =None_, _/_)
    

Parameters:
    

**id** (_str_) – The RNA type identifier.

Returns:
    

The class or default when not found.

Return type:
    

type

file_path_foreach(_visit_path_fn_ , _*_ , _subset =None_, _visit_types =None_, _flags ={'SKIP_PACKED', 'SKIP_WEAK_REFERENCES'}_)
    

Call `visit_path_fn` for the file paths used by all ID data-blocks in current `bpy.data`.

For list of valid set members for visit_types, see: [`bpy.types.KeyingSetPath.id_type`](../K/bpy.types.KeyingSetPath.md#bpy.types.KeyingSetPath.id_type "bpy.types.KeyingSetPath.id_type").

Parameters:
    

  * **visit_path_fn** (Callable[[[`bpy.types.ID`](../I/bpy.types.ID.md#bpy.types.ID "bpy.types.ID"), str, Any], str|None]) – function that takes three parameters: the data-block, a file path, and a placeholder for future use. The function should return either `None` or a `str`. In the latter case, the visited file path will be replaced with the returned string.

  * **subset** (_set_ _[__str_ _]_) – When given, only these data-blocks and their used file paths will be visited.

  * **visit_types** (_set_ _[__str_ _]_) – When given, only visit data-blocks of these types. Ignored if `subset` is also given.

  * **flags** (_set_ _[__str_ _]_) – Set of flags that influence which data-blocks are visited. See [File Path Foreach Flag Items](../../bpy_types_enum_items/file_path_foreach_flag_items.md#rna-enum-file-path-foreach-flag-items).


file_path_map(_*_ , _subset =None_, _key_types =None_, _include_libraries =False_)
    

Returns a mapping of all ID data-blocks in current `bpy.data` to a set of all file paths used by them.

For list of valid set members for key_types, see: [`bpy.types.KeyingSetPath.id_type`](../K/bpy.types.KeyingSetPath.md#bpy.types.KeyingSetPath.id_type "bpy.types.KeyingSetPath.id_type").

Parameters:
    

  * **subset** (_sequence_) – When given, only these data-blocks and their used file paths will be included as keys/values in the map.

  * **key_types** (_set_ _[__str_ _]_) – When given, filter the keys mapped by ID types. Ignored if `subset` is also given.

  * **include_libraries** (_bool_) – Include library file paths of linked data. False by default.


Returns:
    

dictionary of [`bpy.types.ID`](../I/bpy.types.ID.md#bpy.types.ID "bpy.types.ID") instances, with sets of file path strings as their values.

Return type:
    

dict

orphans_purge()
    

Remove (delete) all IDs with no user.

Parameters:
    

  * **do_local_ids** (_bool_ _,__optional_) – Include unused local IDs in the deletion, defaults to True

  * **do_linked_ids** (_bool_ _,__optional_) – Include unused linked IDs in the deletion, defaults to True

  * **do_recursive** (_bool_ _,__optional_) – Recursively check for unused IDs, ensuring no orphaned one remain after a single run of that function, defaults to False


Returns:
    

The number of deleted IDs.

temp_data(_*_ , _filepath =None_)
    

A context manager that temporarily creates blender file data.

Parameters:
    

**filepath** (_str_ _|__bytes_ _|__None_) – The file path for the newly temporary data. When None, the path of the currently open file is used.

Returns:
    

Blend file data which is freed once the context exists.

Return type:
    

`bpy.types.BlendData`

user_map(_*_ , _subset =None_, _key_types =None_, _value_types =None_)
    

Returns a mapping of all ID data-blocks in current `bpy.data` to a set of all data-blocks using them.

For list of valid set members for key_types & value_types, see: [`bpy.types.KeyingSetPath.id_type`](../K/bpy.types.KeyingSetPath.md#bpy.types.KeyingSetPath.id_type "bpy.types.KeyingSetPath.id_type").

Parameters:
    

  * **subset** (Sequence[[`bpy.types.ID`](../I/bpy.types.ID.md#bpy.types.ID "bpy.types.ID")]) – When passed, only these data-blocks and their users will be included as keys/values in the map.

  * **key_types** (_set_ _[__str_ _]_) – Filter the keys mapped by ID types.

  * **value_types** (_set_ _[__str_ _]_) – Filter the values in the set by ID types.


Returns:
    

dictionary that maps data-blocks ID’s to their users.

Return type:
    

dict[[`bpy.types.ID`](../I/bpy.types.ID.md#bpy.types.ID "bpy.types.ID"), set[[`bpy.types.ID`](../I/bpy.types.ID.md#bpy.types.ID "bpy.types.ID")]]

## Inherited Properties

  * [`bpy_struct.id_data`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.id_data "bpy.types.bpy_struct.id_data")

| 


  
---|---  
  
## Inherited Functions

  * [`bpy_struct.as_pointer`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.as_pointer "bpy.types.bpy_struct.as_pointer")
  * [`bpy_struct.driver_add`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.driver_add "bpy.types.bpy_struct.driver_add")
  * [`bpy_struct.driver_remove`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.driver_remove "bpy.types.bpy_struct.driver_remove")
  * [`bpy_struct.get`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.get "bpy.types.bpy_struct.get")
  * [`bpy_struct.id_properties_clear`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.id_properties_clear "bpy.types.bpy_struct.id_properties_clear")
  * [`bpy_struct.id_properties_ensure`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.id_properties_ensure "bpy.types.bpy_struct.id_properties_ensure")
  * [`bpy_struct.id_properties_ui`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.id_properties_ui "bpy.types.bpy_struct.id_properties_ui")
  * [`bpy_struct.is_property_hidden`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.is_property_hidden "bpy.types.bpy_struct.is_property_hidden")
  * [`bpy_struct.is_property_overridable_library`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.is_property_overridable_library "bpy.types.bpy_struct.is_property_overridable_library")
  * [`bpy_struct.is_property_readonly`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.is_property_readonly "bpy.types.bpy_struct.is_property_readonly")
  * [`bpy_struct.is_property_set`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.is_property_set "bpy.types.bpy_struct.is_property_set")
  * [`bpy_struct.items`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.items "bpy.types.bpy_struct.items")

| 

  * [`bpy_struct.keyframe_delete`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.keyframe_delete "bpy.types.bpy_struct.keyframe_delete")
  * [`bpy_struct.keyframe_insert`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.keyframe_insert "bpy.types.bpy_struct.keyframe_insert")
  * [`bpy_struct.keys`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.keys "bpy.types.bpy_struct.keys")
  * [`bpy_struct.path_from_id`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.path_from_id "bpy.types.bpy_struct.path_from_id")
  * [`bpy_struct.path_from_module`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.path_from_module "bpy.types.bpy_struct.path_from_module")
  * [`bpy_struct.path_resolve`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.path_resolve "bpy.types.bpy_struct.path_resolve")
  * [`bpy_struct.pop`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.pop "bpy.types.bpy_struct.pop")
  * [`bpy_struct.property_overridable_library_set`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.property_overridable_library_set "bpy.types.bpy_struct.property_overridable_library_set")
  * [`bpy_struct.property_unset`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.property_unset "bpy.types.bpy_struct.property_unset")
  * [`bpy_struct.rna_ancestors`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.rna_ancestors "bpy.types.bpy_struct.rna_ancestors")
  * [`bpy_struct.type_recast`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.type_recast "bpy.types.bpy_struct.type_recast")
  * [`bpy_struct.values`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.values "bpy.types.bpy_struct.values")

  
---|---  
  
## References

  * [`Context.blend_data`](../C/bpy.types.Context.md#bpy.types.Context.blend_data "bpy.types.Context.blend_data")

| 

  * [`RenderEngine.update`](../R/bpy.types.RenderEngine.md#bpy.types.RenderEngine.update "bpy.types.RenderEngine.update")

  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
  *[*]: Keyword-only parameters separator (PEP 3102)
