# bpy_extras submodule (bpy_extras.view3d_utils)

bpy_extras.view3d_utils.region_2d_to_vector_3d(_region_ , _rv3d_ , _coord_)
    

Return a direction vector from the viewport at the specific 2d region coordinate.

Parameters:
    

  * **region** ([`bpy.types.Region`](../bpy.types/R/bpy.types.Region.md#bpy.types.Region "bpy.types.Region")) – region of the 3D viewport, typically bpy.context.region.

  * **rv3d** ([`bpy.types.RegionView3D`](../bpy.types/R/bpy.types.RegionView3D.md#bpy.types.RegionView3D "bpy.types.RegionView3D")) – 3D region data, typically bpy.context.space_data.region_3d.

  * **coord** (_2d vector_) – 2d coordinates relative to the region: (event.mouse_region_x, event.mouse_region_y) for example.


Returns:
    

normalized 3d vector.

Return type:
    

[`mathutils.Vector`](mathutils.md#mathutils.Vector "mathutils.Vector")

bpy_extras.view3d_utils.region_2d_to_origin_3d(_region_ , _rv3d_ , _coord_ , _*_ , _clamp =None_)
    

Return the 3d view origin from the region relative 2d coords.

Note

Orthographic views have a less obvious origin, the far clip is used to define the viewport near/far extents. Since far clip can be a very large value, the result may give with numeric precision issues.

To avoid this problem, you can optionally clamp the far clip to a smaller value based on the data you’re operating on.

Parameters:
    

  * **region** ([`bpy.types.Region`](../bpy.types/R/bpy.types.Region.md#bpy.types.Region "bpy.types.Region")) – region of the 3D viewport, typically bpy.context.region.

  * **rv3d** ([`bpy.types.RegionView3D`](../bpy.types/R/bpy.types.RegionView3D.md#bpy.types.RegionView3D "bpy.types.RegionView3D")) – 3D region data, typically bpy.context.space_data.region_3d.

  * **coord** (_Sequence_ _[__float_ _]_) – 2D coordinates relative to the region; (event.mouse_region_x, event.mouse_region_y) for example.

  * **clamp** (_float_ _|__None_) – Clamp the maximum far-clip value used. (negative value will move the offset away from the view_location)


Returns:
    

The origin of the viewpoint in 3d space.

Return type:
    

[`mathutils.Vector`](mathutils.md#mathutils.Vector "mathutils.Vector")

bpy_extras.view3d_utils.region_2d_to_location_3d(_region_ , _rv3d_ , _coord_ , _depth_location_)
    

Return a 3d location from the region relative 2d coords, aligned with _depth_location_.

Parameters:
    

  * **region** ([`bpy.types.Region`](../bpy.types/R/bpy.types.Region.md#bpy.types.Region "bpy.types.Region")) – region of the 3D viewport, typically bpy.context.region.

  * **rv3d** ([`bpy.types.RegionView3D`](../bpy.types/R/bpy.types.RegionView3D.md#bpy.types.RegionView3D "bpy.types.RegionView3D")) – 3D region data, typically bpy.context.space_data.region_3d.

  * **coord** (_2d vector_) – 2d coordinates relative to the region; (event.mouse_region_x, event.mouse_region_y) for example.

  * **depth_location** (_3d vector_) – the returned vectors depth is aligned with this since there is no defined depth with a 2d region input.


Returns:
    

normalized 3d vector.

Return type:
    

[`mathutils.Vector`](mathutils.md#mathutils.Vector "mathutils.Vector")

bpy_extras.view3d_utils.location_3d_to_region_2d(_region_ , _rv3d_ , _coord_ , _*_ , _default =None_)
    

Return the _region_ relative 2d location of a 3d position.

Parameters:
    

  * **region** ([`bpy.types.Region`](../bpy.types/R/bpy.types.Region.md#bpy.types.Region "bpy.types.Region")) – region of the 3D viewport, typically bpy.context.region.

  * **rv3d** ([`bpy.types.RegionView3D`](../bpy.types/R/bpy.types.RegionView3D.md#bpy.types.RegionView3D "bpy.types.RegionView3D")) – 3D region data, typically bpy.context.space_data.region_3d.

  * **coord** (_3d vector_) – 3d world-space location.

  * **default** – Return this value if `coord` is behind the origin of a perspective view.


Returns:
    

2d location

Return type:
    

[`mathutils.Vector`](mathutils.md#mathutils.Vector "mathutils.Vector") | Any
  *[*]: Keyword-only parameters separator (PEP 3102)
