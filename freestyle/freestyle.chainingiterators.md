# Freestyle Chaining Iterators (freestyle.chainingiterators)

This module contains chaining iterators used for the chaining operation to construct long strokes by concatenating feature edges according to selected chaining rules. The module is also intended to be a collection of examples for defining chaining iterators in Python.

_class _freestyle.chainingiterators.ChainPredicateIterator
    

Class hierarchy: `freestyle.types.Iterator` > `freestyle.types.ViewEdgeIterator` > `freestyle.types.ChainingIterator` > `ChainPredicateIterator`

A “generic” user-controlled ViewEdge iterator. This iterator is in particular built from a unary predicate and a binary predicate. First, the unary predicate is evaluated for all potential next ViewEdges in order to only keep the ones respecting a certain constraint. Then, the binary predicate is evaluated on the current ViewEdge together with each ViewEdge of the previous selection. The first ViewEdge respecting both the unary predicate and the binary predicate is kept as the next one. If none of the potential next ViewEdge respects these two predicates, None is returned.

__init__(_upred_ , _bpred_ , _restrict_to_selection =True_, _restrict_to_unvisited =True_, _begin =None_, _orientation =True_)
__init__(_brother_)
    

Builds a ChainPredicateIterator from a unary predicate, a binary predicate, a starting ViewEdge and its orientation or using the copy constructor.

Parameters:
    

  * **upred** (`freestyle.types.UnaryPredicate1D`) – The unary predicate that the next ViewEdge must satisfy.

  * **bpred** (`freestyle.types.BinaryPredicate1D`) – The binary predicate that the next ViewEdge must satisfy together with the actual pointed ViewEdge.

  * **restrict_to_selection** (_bool_) – Indicates whether to force the chaining to stay within the set of selected ViewEdges or not.

  * **restrict_to_unvisited** (_bool_) – Indicates whether a ViewEdge that has already been chained must be ignored ot not.

  * **begin** (`freestyle.types.ViewEdge` | None) – The ViewEdge from where to start the iteration.

  * **orientation** (_bool_) – If true, we’ll look for the next ViewEdge among the ViewEdges that surround the ending ViewVertex of begin. If false, we’ll search over the ViewEdges surrounding the ending ViewVertex of begin.

  * **brother** (`ChainPredicateIterator`) – A ChainPredicateIterator object.


_class _freestyle.chainingiterators.ChainSilhouetteIterator
    

Class hierarchy: `freestyle.types.Iterator` > `freestyle.types.ViewEdgeIterator` > `freestyle.types.ChainingIterator` > `ChainSilhouetteIterator`

A ViewEdge Iterator used to follow ViewEdges the most naturally. For example, it will follow visible ViewEdges of same nature. As soon, as the nature or the visibility changes, the iteration stops (by setting the pointed ViewEdge to 0). In the case of an iteration over a set of ViewEdge that are both Silhouette and Crease, there will be a precedence of the silhouette over the crease criterion.

__init__(_restrict_to_selection =True_, _begin =None_, _orientation =True_)
__init__(_brother_)
    

Builds a ChainSilhouetteIterator from the first ViewEdge used for iteration and its orientation or the copy constructor.

Parameters:
    

  * **restrict_to_selection** (_bool_) – Indicates whether to force the chaining to stay within the set of selected ViewEdges or not.

  * **begin** (`freestyle.types.ViewEdge` | None) – The ViewEdge from where to start the iteration.

  * **orientation** (_bool_) – If true, we’ll look for the next ViewEdge among the ViewEdges that surround the ending ViewVertex of begin. If false, we’ll search over the ViewEdges surrounding the ending ViewVertex of begin.

  * **brother** (`ChainSilhouetteIterator`) – A ChainSilhouetteIterator object.


_class _freestyle.chainingiterators.pyChainSilhouetteIterator
    

Natural chaining iterator that follows the edges of the same nature following the topology of objects, with decreasing priority for silhouettes, then borders, then suggestive contours, then all other edge types. A ViewEdge is only chained once.

init()
    

traverse(_iter_)
    

_class _freestyle.chainingiterators.pyChainSilhouetteGenericIterator
    

Natural chaining iterator that follows the edges of the same nature following the topology of objects, with decreasing priority for silhouettes, then borders, then suggestive contours, then all other edge types.

__init__(_self_ , _stayInSelection =True_, _stayInUnvisited =True_)
    

Builds a pyChainSilhouetteGenericIterator object.

Parameters:
    

  * **stayInSelection** (_bool_) – True if it is allowed to go out of the selection

  * **stayInUnvisited** (_bool_) – May the same ViewEdge be chained twice


init()
    

traverse(_iter_)
    

_class _freestyle.chainingiterators.pyExternalContourChainingIterator
    

Chains by external contour

checkViewEdge(_ve_ , _orientation_)
    

init()
    

traverse(_iter_)
    

_class _freestyle.chainingiterators.pySketchyChainSilhouetteIterator
    

Natural chaining iterator with a sketchy multiple touch. It chains the same ViewEdge multiple times to achieve a sketchy effect.

__init__(_self_ , _nRounds =3_, _stayInSelection =True_)
    

Builds a pySketchyChainSilhouetteIterator object.

Parameters:
    

  * **nRounds** (_int_) – Number of times every Viewedge is chained.

  * **stayInSelection** (_bool_) – if False, edges outside of the selection can be chained.


init()
    

make_sketchy(_ve_)
    

Creates the sketchy effect by causing the chain to run from the start again. (loop over itself again)

traverse(_iter_)
    

_class _freestyle.chainingiterators.pySketchyChainingIterator
    

Chaining iterator designed for sketchy style. It chains the same ViewEdge several times in order to produce multiple strokes per ViewEdge.

init()
    

traverse(_iter_)
    

_class _freestyle.chainingiterators.pyFillOcclusionsRelativeChainingIterator
    

Chaining iterator that fills small occlusions

__init__(_self_ , _percent_)
    

Builds a pyFillOcclusionsRelativeChainingIterator object.

Parameters:
    

**percent** (_float_) – The maximal length of the occluded part, expressed in a percentage of the total chain length.

init()
    

traverse(_iter_)
    

_class _freestyle.chainingiterators.pyFillOcclusionsAbsoluteChainingIterator
    

Chaining iterator that fills small occlusions

__init__(_self_ , _length_)
    

Builds a pyFillOcclusionsAbsoluteChainingIterator object.

Parameters:
    

**length** (_int_) – The maximum length of the occluded part in pixels.

init()
    

traverse(_iter_)
    

_class _freestyle.chainingiterators.pyFillOcclusionsAbsoluteAndRelativeChainingIterator
    

Chaining iterator that fills small occlusions regardless of the selection.

__init__(_self_ , _percent_ , _l_)
    

Builds a pyFillOcclusionsAbsoluteAndRelativeChainingIterator object.

Parameters:
    

  * **percent** (_float_) – The maximal length of the occluded part as a percentage of the total chain length.

  * **l** (_float_) – Absolute length.


init()
    

traverse(_iter_)
    

_class _freestyle.chainingiterators.pyFillQi0AbsoluteAndRelativeChainingIterator
    

Chaining iterator that fills small occlusions regardless of the selection.

__init__(_self_ , _percent_ , _l_)
    

Builds a pyFillQi0AbsoluteAndRelativeChainingIterator object.

Parameters:
    

  * **percent** (_float_) – The maximal length of the occluded part as a percentage of the total chain length.

  * **l** (_float_) – Absolute length.


init()
    

traverse(_iter_)
    

_class _freestyle.chainingiterators.pyNoIdChainSilhouetteIterator
    

Natural chaining iterator that follows the edges of the same nature following the topology of objects, with decreasing priority for silhouettes, then borders, then suggestive contours, then all other edge types. It won’t chain the same ViewEdge twice.

__init__(_self_ , _stayInSelection =True_)
    

Builds a pyNoIdChainSilhouetteIterator object.

Parameters:
    

**stayInSelection** (_bool_) – True if it is allowed to go out of the selection

init()
    

traverse(_iter_)
