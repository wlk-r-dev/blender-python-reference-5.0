# Interpolation Utilities (mathutils.interpolate)

The Blender interpolate module.

mathutils.interpolate.poly_3d_calc(_veclist_ , _pt_ , _/_)
    

Calculate barycentric weights for a point on a polygon.

Parameters:
    

  * **veclist** (_Sequence_ _[__Sequence_ _[__float_ _]__]_) – Sequence of 3D positions.

  * **pt** – 2D or 3D position. :type pt: Sequence[float] :return: list of per-vector weights.


Return type:
    

list[float]
  *[/]: Positional-only parameter separator (PEP 570)
