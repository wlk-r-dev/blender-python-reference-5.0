# Freestyle Predicates (freestyle.predicates)

This module contains predicates operating on vertices (0D elements) and polylines (1D elements). It is also intended to be a collection of examples for predicate definition in Python.

User-defined predicates inherit one of the following base classes, depending on the object type (0D or 1D) to operate on and the arity (unary or binary):

  * `freestyle.types.BinaryPredicate0D`

  * `freestyle.types.BinaryPredicate1D`

  * `freestyle.types.UnaryPredicate0D`

  * `freestyle.types.UnaryPredicate1D`


_class _freestyle.predicates.AndBP1D
    

_class _freestyle.predicates.AndUP1D
    

_class _freestyle.predicates.ContourUP1D
    

Class hierarchy: `freestyle.types.UnaryPredicate1D` > `ContourUP1D`

__call__(_inter_)
    

Returns true if the Interface1D is a contour. An Interface1D is a contour if it is bordered by a different shape on each of its sides.

Parameters:
    

**inter** (`freestyle.types.Interface1D`) – An Interface1D object.

Returns:
    

True if the Interface1D is a contour, false otherwise.

Return type:
    

bool

_class _freestyle.predicates.DensityLowerThanUP1D
    

Class hierarchy: `freestyle.types.UnaryPredicate1D` > `DensityLowerThanUP1D`

__init__(_threshold_ , _sigma =2.0_)
    

Builds a DensityLowerThanUP1D object.

Parameters:
    

  * **threshold** (_float_) – The value of the threshold density. Any Interface1D having a density lower than this threshold will match.

  * **sigma** (_float_) – The sigma value defining the density evaluation window size used in the `freestyle.functions.DensityF0D` functor.


__call__(_inter_)
    

Returns true if the density evaluated for the Interface1D is less than a user-defined density value.

Parameters:
    

**inter** (`freestyle.types.Interface1D`) – An Interface1D object.

Returns:
    

True if the density is lower than a threshold.

Return type:
    

bool

_class _freestyle.predicates.EqualToChainingTimeStampUP1D
    

Class hierarchy: `freestyle.types.UnaryPredicate1D` > `freestyle.types.EqualToChainingTimeStampUP1D`

__init__(_ts_)
    

Builds a EqualToChainingTimeStampUP1D object.

Parameters:
    

**ts** (_int_) – A time stamp value.

__call__(_inter_)
    

Returns true if the Interface1D’s time stamp is equal to a certain user-defined value.

Parameters:
    

**inter** (`freestyle.types.Interface1D`) – An Interface1D object.

Returns:
    

True if the time stamp is equal to a user-defined value.

Return type:
    

bool

_class _freestyle.predicates.EqualToTimeStampUP1D
    

Class hierarchy: `freestyle.types.UnaryPredicate1D` > `EqualToTimeStampUP1D`

__init__(_ts_)
    

Builds a EqualToTimeStampUP1D object.

Parameters:
    

**ts** (_int_) – A time stamp value.

__call__(_inter_)
    

Returns true if the Interface1D’s time stamp is equal to a certain user-defined value.

Parameters:
    

**inter** (`freestyle.types.Interface1D`) – An Interface1D object.

Returns:
    

True if the time stamp is equal to a user-defined value.

Return type:
    

bool

_class _freestyle.predicates.ExternalContourUP1D
    

Class hierarchy: `freestyle.types.UnaryPredicate1D` > `ExternalContourUP1D`

__call__(_inter_)
    

Returns true if the Interface1D is an external contour. An Interface1D is an external contour if it is bordered by no shape on one of its sides.

Parameters:
    

**inter** (`freestyle.types.Interface1D`) – An Interface1D object.

Returns:
    

True if the Interface1D is an external contour, false otherwise.

Return type:
    

bool

_class _freestyle.predicates.FalseBP1D
    

Class hierarchy: `freestyle.types.BinaryPredicate1D` > `FalseBP1D`

__call__(_inter1_ , _inter2_)
    

Always returns false.

Parameters:
    

  * **inter1** (`freestyle.types.Interface1D`) – The first Interface1D object.

  * **inter2** (`freestyle.types.Interface1D`) – The second Interface1D object.


Returns:
    

False.

Return type:
    

bool

_class _freestyle.predicates.FalseUP0D
    

Class hierarchy: `freestyle.types.UnaryPredicate0D` > `FalseUP0D`

__call__(_it_)
    

Always returns false.

Parameters:
    

**it** (`freestyle.types.Interface0DIterator`) – An Interface0DIterator object.

Returns:
    

False.

Return type:
    

bool

_class _freestyle.predicates.FalseUP1D
    

Class hierarchy: `freestyle.types.UnaryPredicate1D` > `FalseUP1D`

__call__(_inter_)
    

Always returns false.

Parameters:
    

**inter** (`freestyle.types.Interface1D`) – An Interface1D object.

Returns:
    

False.

Return type:
    

bool

_class _freestyle.predicates.Length2DBP1D
    

Class hierarchy: `freestyle.types.BinaryPredicate1D` > `Length2DBP1D`

__call__(_inter1_ , _inter2_)
    

Returns true if the 2D length of inter1 is less than the 2D length of inter2.

Parameters:
    

  * **inter1** (`freestyle.types.Interface1D`) – The first Interface1D object.

  * **inter2** (`freestyle.types.Interface1D`) – The second Interface1D object.


Returns:
    

True or false.

Return type:
    

bool

_class _freestyle.predicates.MaterialBP1D
    

Checks whether the two supplied ViewEdges have the same material.

_class _freestyle.predicates.NotBP1D
    

_class _freestyle.predicates.NotUP1D
    

_class _freestyle.predicates.ObjectNamesUP1D
    

_class _freestyle.predicates.OrBP1D
    

_class _freestyle.predicates.OrUP1D
    

_class _freestyle.predicates.QuantitativeInvisibilityRangeUP1D
    

_class _freestyle.predicates.QuantitativeInvisibilityUP1D
    

Class hierarchy: `freestyle.types.UnaryPredicate1D` > `QuantitativeInvisibilityUP1D`

__init__(_qi =0_)
    

Builds a QuantitativeInvisibilityUP1D object.

Parameters:
    

**qi** (_int_) – The Quantitative Invisibility you want the Interface1D to have.

__call__(_inter_)
    

Returns true if the Quantitative Invisibility evaluated at an Interface1D, using the `freestyle.functions.QuantitativeInvisibilityF1D` functor, equals a certain user-defined value.

Parameters:
    

**inter** (`freestyle.types.Interface1D`) – An Interface1D object.

Returns:
    

True if Quantitative Invisibility equals a user-defined value.

Return type:
    

bool

_class _freestyle.predicates.SameShapeIdBP1D
    

Class hierarchy: `freestyle.types.BinaryPredicate1D` > `SameShapeIdBP1D`

__call__(_inter1_ , _inter2_)
    

Returns true if inter1 and inter2 belong to the same shape.

Parameters:
    

  * **inter1** (`freestyle.types.Interface1D`) – The first Interface1D object.

  * **inter2** (`freestyle.types.Interface1D`) – The second Interface1D object.


Returns:
    

True or false.

Return type:
    

bool

_class _freestyle.predicates.ShapeUP1D
    

Class hierarchy: `freestyle.types.UnaryPredicate1D` > `ShapeUP1D`

__init__(_first_ , _second =0_)
    

Builds a ShapeUP1D object.

Parameters:
    

  * **first** (_int_) – The first Id component.

  * **second** (_int_) – The second Id component.


__call__(_inter_)
    

Returns true if the shape to which the Interface1D belongs to has the same `freestyle.types.Id` as the one specified by the user.

Parameters:
    

**inter** (`freestyle.types.Interface1D`) – An Interface1D object.

Returns:
    

True if Interface1D belongs to the shape of the user-specified Id.

Return type:
    

bool

_class _freestyle.predicates.TrueBP1D
    

Class hierarchy: `freestyle.types.BinaryPredicate1D` > `TrueBP1D`

__call__(_inter1_ , _inter2_)
    

Always returns true.

Parameters:
    

  * **inter1** (`freestyle.types.Interface1D`) – The first Interface1D object.

  * **inter2** (`freestyle.types.Interface1D`) – The second Interface1D object.


Returns:
    

True.

Return type:
    

bool

_class _freestyle.predicates.TrueUP0D
    

Class hierarchy: `freestyle.types.UnaryPredicate0D` > `TrueUP0D`

__call__(_it_)
    

Always returns true.

Parameters:
    

**it** (`freestyle.types.Interface0DIterator`) – An Interface0DIterator object.

Returns:
    

True.

Return type:
    

bool

_class _freestyle.predicates.TrueUP1D
    

Class hierarchy: `freestyle.types.UnaryPredicate1D` > `TrueUP1D`

__call__(_inter_)
    

Always returns true.

Parameters:
    

**inter** (`freestyle.types.Interface1D`) – An Interface1D object.

Returns:
    

True.

Return type:
    

bool

_class _freestyle.predicates.ViewMapGradientNormBP1D
    

Class hierarchy: `freestyle.types.BinaryPredicate1D` > `ViewMapGradientNormBP1D`

__init__(_level_ , _integration_type =IntegrationType.MEAN_, _sampling =2.0_)
    

Builds a ViewMapGradientNormBP1D object.

Parameters:
    

  * **level** (_int_) – The level of the pyramid from which the pixel must be read.

  * **integration_type** (`freestyle.types.IntegrationType`) – The integration method used to compute a single value from a set of values.

  * **sampling** (_float_) – The resolution used to sample the chain: GetViewMapGradientNormF0D is evaluated at each sample point and the result is obtained by combining the resulting values into a single one, following the method specified by integration_type.


__call__(_inter1_ , _inter2_)
    

Returns true if the evaluation of the Gradient norm Function is higher for inter1 than for inter2.

Parameters:
    

  * **inter1** (`freestyle.types.Interface1D`) – The first Interface1D object.

  * **inter2** (`freestyle.types.Interface1D`) – The second Interface1D object.


Returns:
    

True or false.

Return type:
    

bool

_class _freestyle.predicates.WithinImageBoundaryUP1D
    

Class hierarchy: `freestyle.types.UnaryPredicate1D` > `WithinImageBoundaryUP1D`

__init__(_xmin_ , _ymin_ , _xmax_ , _ymax_)
    

Builds an WithinImageBoundaryUP1D object.

Parameters:
    

  * **xmin** (_float_) – X lower bound of the image boundary.

  * **ymin** (_float_) – Y lower bound of the image boundary.

  * **xmax** (_float_) – X upper bound of the image boundary.

  * **ymax** (_float_) – Y upper bound of the image boundary.


__call__(_inter_)
    

Returns true if the Interface1D intersects with image boundary.

_class _freestyle.predicates.pyBackTVertexUP0D
    

Check whether an Interface0DIterator references a TVertex and is the one that is hidden (inferred from the context).

_class _freestyle.predicates.pyClosedCurveUP1D
    

_class _freestyle.predicates.pyDensityFunctorUP1D
    

_class _freestyle.predicates.pyDensityUP1D
    

_class _freestyle.predicates.pyDensityVariableSigmaUP1D
    

_class _freestyle.predicates.pyHighDensityAnisotropyUP1D
    

_class _freestyle.predicates.pyHighDirectionalViewMapDensityUP1D
    

_class _freestyle.predicates.pyHighSteerableViewMapDensityUP1D
    

_class _freestyle.predicates.pyHighViewMapDensityUP1D
    

_class _freestyle.predicates.pyHighViewMapGradientNormUP1D
    

_class _freestyle.predicates.pyHigherCurvature2DAngleUP0D
    

_class _freestyle.predicates.pyHigherLengthUP1D
    

_class _freestyle.predicates.pyHigherNumberOfTurnsUP1D
    

_class _freestyle.predicates.pyIsInOccludersListUP1D
    

_class _freestyle.predicates.pyIsOccludedByIdListUP1D
    

_class _freestyle.predicates.pyIsOccludedByItselfUP1D
    

_class _freestyle.predicates.pyIsOccludedByUP1D
    

_class _freestyle.predicates.pyLengthBP1D
    

_class _freestyle.predicates.pyLowDirectionalViewMapDensityUP1D
    

_class _freestyle.predicates.pyLowSteerableViewMapDensityUP1D
    

_class _freestyle.predicates.pyNFirstUP1D
    

_class _freestyle.predicates.pyNatureBP1D
    

_class _freestyle.predicates.pyNatureUP1D
    

_class _freestyle.predicates.pyParameterUP0D
    

_class _freestyle.predicates.pyParameterUP0DGoodOne
    

_class _freestyle.predicates.pyProjectedXBP1D
    

_class _freestyle.predicates.pyProjectedYBP1D
    

_class _freestyle.predicates.pyShapeIdListUP1D
    

_class _freestyle.predicates.pyShapeIdUP1D
    

_class _freestyle.predicates.pyShuffleBP1D
    

_class _freestyle.predicates.pySilhouetteFirstBP1D
    

_class _freestyle.predicates.pyUEqualsUP0D
    

_class _freestyle.predicates.pyVertexNatureUP0D
    

_class _freestyle.predicates.pyViewMapGradientNormBP1D
    

_class _freestyle.predicates.pyZBP1D
    

_class _freestyle.predicates.pyZDiscontinuityBP1D
    

_class _freestyle.predicates.pyZSmallerUP1D
