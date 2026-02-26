# Freestyle Shaders (freestyle.shaders)

This module contains stroke shaders used for creation of stylized strokes. It is also intended to be a collection of examples for shader definition in Python.

User-defined stroke shaders inherit the `freestyle.types.StrokeShader` class.

_class _freestyle.shaders.BackboneStretcherShader
    

Class hierarchy: `freestyle.types.StrokeShader` > `BackboneStretcherShader`

[Geometry shader]

__init__(_amount =2.0_)
    

Builds a BackboneStretcherShader object.

Parameters:
    

**amount** (_float_) – The stretching amount value.

shade(_stroke_)
    

Stretches the stroke at its two extremities and following the respective directions: v(1)v(0) and v(n-1)v(n).

Parameters:
    

**stroke** (`freestyle.types.Stroke`) – A Stroke object.

_class _freestyle.shaders.BezierCurveShader
    

Class hierarchy: `freestyle.types.StrokeShader` > `BezierCurveShader`

[Geometry shader]

__init__(_error =4.0_)
    

Builds a BezierCurveShader object.

Parameters:
    

**error** (_float_) – The error we’re allowing for the approximation. This error is the max distance allowed between the new curve and the original geometry.

shade(_stroke_)
    

Transforms the stroke backbone geometry so that it corresponds to a Bezier Curve approximation of the original backbone geometry.

Parameters:
    

**stroke** (`freestyle.types.Stroke`) – A Stroke object.

_class _freestyle.shaders.BlenderTextureShader
    

Class hierarchy: `freestyle.types.StrokeShader` > `BlenderTextureShader`

[Texture shader]

__init__(_texture_)
    

Builds a BlenderTextureShader object.

Parameters:
    

**texture** ([`bpy.types.LineStyleTextureSlot`](../bpy.types/L/bpy.types.LineStyleTextureSlot.md#bpy.types.LineStyleTextureSlot "bpy.types.LineStyleTextureSlot") | [`bpy.types.ShaderNodeTree`](../bpy.types/S/bpy.types.ShaderNodeTree.md#bpy.types.ShaderNodeTree "bpy.types.ShaderNodeTree")) – A line style texture slot or a shader node tree to define a set of textures.

shade(_stroke_)
    

Assigns a blender texture slot to the stroke shading in order to simulate marks.

Parameters:
    

**stroke** (`freestyle.types.Stroke`) – A Stroke object.

_class _freestyle.shaders.CalligraphicShader
    

Class hierarchy: `freestyle.types.StrokeShader` > `CalligraphicShader`

[Thickness Shader]

__init__(_thickness_min_ , _thickness_max_ , _orientation_ , _clamp_)
    

Builds a CalligraphicShader object.

Parameters:
    

  * **thickness_min** (_float_) – The minimum thickness in the direction perpendicular to the main direction.

  * **thickness_max** (_float_) – The maximum thickness in the main direction.

  * **orientation** ([`mathutils.Vector`](mathutils.md#mathutils.Vector "mathutils.Vector")) – The 2D vector giving the main direction.

  * **clamp** (_bool_) – If true, the strokes are drawn in black when the stroke direction is between -90 and 90 degrees with respect to the main direction and drawn in white otherwise. If false, the strokes are always drawn in black.


shade(_stroke_)
    

Assigns thicknesses to the stroke vertices so that the stroke looks like made with a calligraphic tool, i.e. the stroke will be the thickest in a main direction, and the thinnest in the direction perpendicular to this one, and an interpolation in between.

Parameters:
    

**stroke** (`freestyle.types.Stroke`) – A Stroke object.

_class _freestyle.shaders.ColorNoiseShader
    

Class hierarchy: `freestyle.types.StrokeShader` > `ColorNoiseShader`

[Color shader]

__init__(_amplitude_ , _period_)
    

Builds a ColorNoiseShader object.

Parameters:
    

  * **amplitude** (_float_) – The amplitude of the noise signal.

  * **period** (_float_) – The period of the noise signal.


shade(_stroke_)
    

Shader to add noise to the stroke colors.

Parameters:
    

**stroke** (`freestyle.types.Stroke`) – A Stroke object.

_class _freestyle.shaders.ConstantColorShader
    

Class hierarchy: `freestyle.types.StrokeShader` > `ConstantColorShader`

[Color shader]

__init__(_red_ , _green_ , _blue_ , _alpha =1.0_)
    

Builds a ConstantColorShader object.

Parameters:
    

  * **red** (_float_) – The red component.

  * **green** (_float_) – The green component.

  * **blue** (_float_) – The blue component.

  * **alpha** (_float_) – The alpha value.


shade(_stroke_)
    

Assigns a constant color to every vertex of the Stroke.

Parameters:
    

**stroke** (`freestyle.types.Stroke`) – A Stroke object.

_class _freestyle.shaders.ConstantThicknessShader
    

Class hierarchy: `freestyle.types.StrokeShader` > `ConstantThicknessShader`

[Thickness shader]

__init__(_thickness_)
    

Builds a ConstantThicknessShader object.

Parameters:
    

**thickness** (_float_) – The thickness that must be assigned to the stroke.

shade(_stroke_)
    

Assigns an absolute constant thickness to every vertex of the Stroke.

Parameters:
    

**stroke** (`freestyle.types.Stroke`) – A Stroke object.

_class _freestyle.shaders.ConstrainedIncreasingThicknessShader
    

Class hierarchy: `freestyle.types.StrokeShader` > `ConstrainedIncreasingThicknessShader`

[Thickness shader]

__init__(_thickness_min_ , _thickness_max_ , _ratio_)
    

Builds a ConstrainedIncreasingThicknessShader object.

Parameters:
    

  * **thickness_min** (_float_) – The minimum thickness.

  * **thickness_max** (_float_) – The maximum thickness.

  * **ratio** (_float_) – The thickness/length ratio that we don’t want to exceed.


shade(_stroke_)
    

Same as the `IncreasingThicknessShader`, but here we allow the user to control the thickness/length ratio so that we don’t get fat short lines.

Parameters:
    

**stroke** (`freestyle.types.Stroke`) – A Stroke object.

_class _freestyle.shaders.GuidingLinesShader
    

Class hierarchy: `freestyle.types.StrokeShader` > `GuidingLinesShader`

[Geometry shader]

__init__(_offset_)
    

Builds a GuidingLinesShader object.

Parameters:
    

**offset** (_float_) – The line that replaces the stroke is initially in the middle of the initial stroke bounding box. offset is the value of the displacement which is applied to this line along its normal.

shade(_stroke_)
    

Shader to modify the Stroke geometry so that it corresponds to its main direction line. This shader must be used together with the splitting operator using the curvature criterion. Indeed, the precision of the approximation will depend on the size of the stroke’s pieces. The bigger the pieces are, the rougher the approximation is.

Parameters:
    

**stroke** (`freestyle.types.Stroke`) – A Stroke object.

_class _freestyle.shaders.IncreasingColorShader
    

Class hierarchy: `freestyle.types.StrokeShader` > `IncreasingColorShader`

[Color shader]

__init__(_red_min_ , _green_min_ , _blue_min_ , _alpha_min_ , _red_max_ , _green_max_ , _blue_max_ , _alpha_max_)
    

Builds an IncreasingColorShader object.

Parameters:
    

  * **red_min** (_float_) – The first color red component.

  * **green_min** (_float_) – The first color green component.

  * **blue_min** (_float_) – The first color blue component.

  * **alpha_min** (_float_) – The first color alpha value.

  * **red_max** (_float_) – The second color red component.

  * **green_max** (_float_) – The second color green component.

  * **blue_max** (_float_) – The second color blue component.

  * **alpha_max** (_float_) – The second color alpha value.


shade(_stroke_)
    

Assigns a varying color to the stroke. The user specifies two colors A and B. The stroke color will change linearly from A to B between the first and the last vertex.

Parameters:
    

**stroke** (`freestyle.types.Stroke`) – A Stroke object.

_class _freestyle.shaders.IncreasingThicknessShader
    

Class hierarchy: `freestyle.types.StrokeShader` > `IncreasingThicknessShader`

[Thickness shader]

__init__(_thickness_A_ , _thickness_B_)
    

Builds an IncreasingThicknessShader object.

Parameters:
    

  * **thickness_A** (_float_) – The first thickness value.

  * **thickness_B** (_float_) – The second thickness value.


shade(_stroke_)
    

Assigns thicknesses values such as the thickness increases from a thickness value A to a thickness value B between the first vertex to the midpoint vertex and then decreases from B to a A between this midpoint vertex and the last vertex. The thickness is linearly interpolated from A to B.

Parameters:
    

**stroke** (`freestyle.types.Stroke`) – A Stroke object.

_class _freestyle.shaders.PolygonalizationShader
    

Class hierarchy: `freestyle.types.StrokeShader` > `PolygonalizationShader`

[Geometry shader]

__init__(_error_)
    

Builds a PolygonalizationShader object.

Parameters:
    

**error** (_float_) – The error we want our polygonal approximation to have with respect to the original geometry. The smaller, the closer the new stroke is to the original one. This error corresponds to the maximum distance between the new stroke and the old one.

shade(_stroke_)
    

Modifies the Stroke geometry so that it looks more “polygonal”. The basic idea is to start from the minimal stroke approximation consisting in a line joining the first vertex to the last one and to subdivide using the original stroke vertices until a certain error is reached.

Parameters:
    

**stroke** (`freestyle.types.Stroke`) – A Stroke object.

_class _freestyle.shaders.RoundCapShader
    

round_cap_thickness(_x_)
    

shade(_stroke_)
    

_class _freestyle.shaders.SamplingShader
    

Class hierarchy: `freestyle.types.StrokeShader` > `SamplingShader`

[Geometry shader]

__init__(_sampling_)
    

Builds a SamplingShader object.

Parameters:
    

**sampling** (_float_) – The sampling to use for the stroke resampling.

shade(_stroke_)
    

Resamples the stroke.

Parameters:
    

**stroke** (`freestyle.types.Stroke`) – A Stroke object.

_class _freestyle.shaders.SmoothingShader
    

Class hierarchy: `freestyle.types.StrokeShader` > `SmoothingShader`

[Geometry shader]

__init__(_num_iterations =100_, _factor_point =0.1_, _factor_curvature =0.0_, _factor_curvature_difference =0.2_, _aniso_point =0.0_, _aniso_normal =0.0_, _aniso_curvature =0.0_, _carricature_factor =1.0_)
    

Builds a SmoothingShader object.

Parameters:
    

  * **num_iterations** (_int_) – The number of iterations.

  * **factor_point** (_float_) – 0.1

  * **factor_curvature** (_float_) – 0.0

  * **factor_curvature_difference** (_float_) – 0.2

  * **aniso_point** (_float_) – 0.0

  * **aniso_normal** (_float_) – 0.0

  * **aniso_curvature** (_float_) – 0.0

  * **carricature_factor** (_float_) – 1.0


shade(_stroke_)
    

Smooths the stroke by moving the vertices to make the stroke smoother. Uses curvature flow to converge towards a curve of constant curvature. The diffusion method we use is anisotropic to prevent the diffusion across corners.

Parameters:
    

**stroke** (`freestyle.types.Stroke`) – A Stroke object.

_class _freestyle.shaders.SpatialNoiseShader
    

Class hierarchy: `freestyle.types.StrokeShader` > `SpatialNoiseShader`

[Geometry shader]

__init__(_amount_ , _scale_ , _num_octaves_ , _smooth_ , _pure_random_)
    

Builds a SpatialNoiseShader object.

Parameters:
    

  * **amount** (_float_) – The amplitude of the noise.

  * **scale** (_float_) – The noise frequency.

  * **num_octaves** (_int_) – The number of octaves

  * **smooth** (_bool_) – True if you want the noise to be smooth.

  * **pure_random** (_bool_) – True if you don’t want any coherence.


shade(_stroke_)
    

Spatial Noise stroke shader. Moves the vertices to make the stroke more noisy.

Parameters:
    

**stroke** (`freestyle.types.Stroke`) – A Stroke object.

_class _freestyle.shaders.SquareCapShader
    

shade(_stroke_)
    

_class _freestyle.shaders.StrokeTextureStepShader
    

Class hierarchy: `freestyle.types.StrokeShader` > `StrokeTextureStepShader`

[Texture shader]

__init__(_step_)
    

Builds a StrokeTextureStepShader object.

Parameters:
    

**step** (_float_) – The spacing along the stroke.

shade(_stroke_)
    

Assigns a spacing factor to the texture coordinates of the Stroke.

Parameters:
    

**stroke** (`freestyle.types.Stroke`) – A Stroke object.

_class _freestyle.shaders.ThicknessNoiseShader
    

Class hierarchy: `freestyle.types.StrokeShader` > `ThicknessNoiseShader`

[Thickness shader]

__init__(_amplitude_ , _period_)
    

Builds a ThicknessNoiseShader object.

Parameters:
    

  * **amplitude** (_float_) – The amplitude of the noise signal.

  * **period** (_float_) – The period of the noise signal.


shade(_stroke_)
    

Adds some noise to the stroke thickness.

Parameters:
    

**stroke** (`freestyle.types.Stroke`) – A Stroke object.

_class _freestyle.shaders.TipRemoverShader
    

Class hierarchy: `freestyle.types.StrokeShader` > `TipRemoverShader`

[Geometry shader]

__init__(_tip_length_)
    

Builds a TipRemoverShader object.

Parameters:
    

**tip_length** (_float_) – The length of the piece of stroke we want to remove at each extremity.

shade(_stroke_)
    

Removes the stroke’s extremities.

Parameters:
    

**stroke** (`freestyle.types.Stroke`) – A Stroke object.

_class _freestyle.shaders.py2DCurvatureColorShader
    

Assigns a color (grayscale) to the stroke based on the curvature. A higher curvature will yield a brighter color.

shade(_stroke_)
    

_class _freestyle.shaders.pyBackboneStretcherNoCuspShader
    

Stretches the stroke’s backbone, excluding cusp vertices (end junctions).

shade(_stroke_)
    

_class _freestyle.shaders.pyBackboneStretcherShader
    

Stretches the stroke’s backbone by a given length (in pixels).

shade(_stroke_)
    

_class _freestyle.shaders.pyBluePrintCirclesShader
    

Draws the silhouette of the object as a circle.

shade(_stroke_)
    

_class _freestyle.shaders.pyBluePrintDirectedSquaresShader
    

Replaces the stroke with a directed square.

shade(_stroke_)
    

_class _freestyle.shaders.pyBluePrintEllipsesShader
    

shade(_stroke_)
    

_class _freestyle.shaders.pyBluePrintSquaresShader
    

shade(_stroke_)
    

_class _freestyle.shaders.pyConstantColorShader
    

Assigns a constant color to the stroke.

shade(_stroke_)
    

_class _freestyle.shaders.pyConstantThicknessShader
    

Assigns a constant thickness along the stroke.

shade(_stroke_)
    

_class _freestyle.shaders.pyConstrainedIncreasingThicknessShader
    

Increasingly thickens the stroke, constrained by a ratio of the stroke’s length.

shade(_stroke_)
    

_class _freestyle.shaders.pyDecreasingThicknessShader
    

Inverse of pyIncreasingThicknessShader, decreasingly thickens the stroke.

shade(_stroke_)
    

_class _freestyle.shaders.pyDepthDiscontinuityThicknessShader
    

Assigns a thickness to the stroke based on the stroke’s distance to the camera (Z-value).

shade(_stroke_)
    

_class _freestyle.shaders.pyDiffusion2Shader
    

Iteratively adds an offset to the position of each stroke vertex in the direction perpendicular to the stroke direction at the point. The offset is scaled by the 2D curvature (i.e. how quickly the stroke curve is) at the point.

shade(_stroke_)
    

_class _freestyle.shaders.pyFXSVaryingThicknessWithDensityShader
    

Assigns thickness to a stroke based on the density of the diffuse map.

shade(_stroke_)
    

_class _freestyle.shaders.pyGuidingLineShader
    

shade(_stroke_)
    

_class _freestyle.shaders.pyHLRShader
    

Controls visibility based upon the quantitative invisibility (QI) based on hidden line removal (HLR).

shade(_stroke_)
    

_class _freestyle.shaders.pyImportance2DThicknessShader
    

Assigns thickness based on distance to a given point in 2D space. the thickness is inverted, so the vertices closest to the specified point have the lowest thickness.

shade(_stroke_)
    

_class _freestyle.shaders.pyImportance3DThicknessShader
    

Assigns thickness based on distance to a given point in 3D space.

shade(_stroke_)
    

_class _freestyle.shaders.pyIncreasingColorShader
    

Fades from one color to another along the stroke.

shade(_stroke_)
    

_class _freestyle.shaders.pyIncreasingThicknessShader
    

Increasingly thickens the stroke.

shade(_stroke_)
    

_class _freestyle.shaders.pyInterpolateColorShader
    

Fades from one color to another and back.

shade(_stroke_)
    

_class _freestyle.shaders.pyLengthDependingBackboneStretcherShader
    

Stretches the stroke’s backbone proportional to the stroke’s length NOTE: you’ll probably want an l somewhere between (0.5 - 0). A value that is too high may yield unexpected results.

shade(_stroke_)
    

_class _freestyle.shaders.pyMaterialColorShader
    

Assigns the color of the underlying material to the stroke.

shade(_stroke_)
    

_class _freestyle.shaders.pyModulateAlphaShader
    

Limits the stroke’s alpha between a min and max value.

shade(_stroke_)
    

_class _freestyle.shaders.pyNonLinearVaryingThicknessShader
    

Assigns thickness to a stroke based on an exponential function.

shade(_stroke_)
    

_class _freestyle.shaders.pyPerlinNoise1DShader
    

Displaces the stroke using the curvilinear abscissa. This means that lines with the same length and sampling interval will be identically distorted.

shade(_stroke_)
    

_class _freestyle.shaders.pyPerlinNoise2DShader
    

Displaces the stroke using the strokes coordinates. This means that in a scene no strokes will be distorted identically.

More information on the noise shaders can be found at: <https://freestyleintegration.wordpress.com/2011/09/25/development-updates-on-september-25/>

shade(_stroke_)
    

_class _freestyle.shaders.pyRandomColorShader
    

Assigns a color to the stroke based on given seed.

shade(_stroke_)
    

_class _freestyle.shaders.pySLERPThicknessShader
    

Assigns thickness to a stroke based on spherical linear interpolation.

shade(_stroke_)
    

_class _freestyle.shaders.pySamplingShader
    

Resamples the stroke, which gives the stroke the amount of vertices specified.

shade(_stroke_)
    

_class _freestyle.shaders.pySinusDisplacementShader
    

Displaces the stroke in the shape of a sine wave.

shade(_stroke_)
    

_class _freestyle.shaders.pyTVertexRemoverShader
    

Removes t-vertices from the stroke.

shade(_stroke_)
    

_class _freestyle.shaders.pyTVertexThickenerShader
    

Thickens TVertices (visual intersections between two edges).

shade(_stroke_)
    

_class _freestyle.shaders.pyTimeColorShader
    

Assigns a grayscale value that increases for every vertex. The brightness will increase along the stroke.

shade(_stroke_)
    

_class _freestyle.shaders.pyTipRemoverShader
    

Removes the tips of the stroke.

shade(_stroke_)
    

Undocumented

_class _freestyle.shaders.pyZDependingThicknessShader
    

Assigns thickness based on an object’s local Z depth (point closest to camera is 1, point furthest from camera is zero).

shade(_stroke_)
