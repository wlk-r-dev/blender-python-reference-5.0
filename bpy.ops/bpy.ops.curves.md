# Curves Operators

bpy.ops.curves.add_bezier(_*_ , _radius =1.0_, _enter_editmode =False_, _align ='WORLD'_, _location =(0.0, 0.0, 0.0)_, _rotation =(0.0, 0.0, 0.0)_, _scale =(0.0, 0.0, 0.0)_)
    

Add new Bézier curve

Parameters:
    

  * **radius** (_float in_ _[__0_ _,__inf_ _]__,__(__optional_ _)_) – Radius

  * **enter_editmode** (_boolean_ _,__(__optional_ _)_) – Enter Edit Mode, Enter edit mode when adding this object

  * **align** (enum in [`'WORLD'`, `'VIEW'`, `'CURSOR'`], (optional)) – 

Align, The alignment of the new object

    * `WORLD` World – Align the new object to the world.

    * `VIEW` View – Align the new object to the view.

    * `CURSOR` 3D Cursor – Use the 3D cursor orientation for the new object.

  * **location** ([[mathutils.Vector]] of 3 items in [-inf, inf], (optional)) – Location, Location for the newly added object

  * **rotation** ([[mathutils.Euler]] rotation of 3 items in [-inf, inf], (optional)) – Rotation, Rotation for the newly added object

  * **scale** ([[mathutils.Vector]] of 3 items in [-inf, inf], (optional)) – Scale, Scale for the newly added object


bpy.ops.curves.add_circle(_*_ , _radius =1.0_, _enter_editmode =False_, _align ='WORLD'_, _location =(0.0, 0.0, 0.0)_, _rotation =(0.0, 0.0, 0.0)_, _scale =(0.0, 0.0, 0.0)_)
    

Add new circle curve

Parameters:
    

  * **radius** (_float in_ _[__0_ _,__inf_ _]__,__(__optional_ _)_) – Radius

  * **enter_editmode** (_boolean_ _,__(__optional_ _)_) – Enter Edit Mode, Enter edit mode when adding this object

  * **align** (enum in [`'WORLD'`, `'VIEW'`, `'CURSOR'`], (optional)) – 

Align, The alignment of the new object

    * `WORLD` World – Align the new object to the world.

    * `VIEW` View – Align the new object to the view.

    * `CURSOR` 3D Cursor – Use the 3D cursor orientation for the new object.

  * **location** ([[mathutils.Vector]] of 3 items in [-inf, inf], (optional)) – Location, Location for the newly added object

  * **rotation** ([[mathutils.Euler]] rotation of 3 items in [-inf, inf], (optional)) – Rotation, Rotation for the newly added object

  * **scale** ([[mathutils.Vector]] of 3 items in [-inf, inf], (optional)) – Scale, Scale for the newly added object


bpy.ops.curves.attribute_set(_*_ , _value_float =0.0_, _value_float_vector_2d =(0.0, 0.0)_, _value_float_vector_3d =(0.0, 0.0, 0.0)_, _value_int =0_, _value_int_vector_2d =(0, 0)_, _value_color =(1.0, 1.0, 1.0, 1.0)_, _value_bool =False_)
    

Set values of the active attribute for selected elements

Parameters:
    

  * **value_float** (_float in_ _[__-inf_ _,__inf_ _]__,__(__optional_ _)_) – Value

  * **value_float_vector_2d** (_float array_ _of_ _2 items in_ _[__-inf_ _,__inf_ _]__,__(__optional_ _)_) – Value

  * **value_float_vector_3d** (_float array_ _of_ _3 items in_ _[__-inf_ _,__inf_ _]__,__(__optional_ _)_) – Value

  * **value_int** (_int in_ _[__-inf_ _,__inf_ _]__,__(__optional_ _)_) – Value

  * **value_int_vector_2d** (_int array_ _of_ _2 items in_ _[__-inf_ _,__inf_ _]__,__(__optional_ _)_) – Value

  * **value_color** (_float array_ _of_ _4 items in_ _[__-inf_ _,__inf_ _]__,__(__optional_ _)_) – Value

  * **value_bool** (_boolean_ _,__(__optional_ _)_) – Value


bpy.ops.curves.convert_from_particle_system()
    

Add a new curves object based on the current state of the particle system

bpy.ops.curves.convert_to_particle_system()
    

Add a new or update an existing hair particle system on the surface object

bpy.ops.curves.curve_type_set(_*_ , _type ='POLY'_, _use_handles =False_)
    

Set type of selected curves

Parameters:
    

  * **type** (enum in [Curves Type Items](../bpy_types_enum_items/curves_type_items.md#rna-enum-curves-type-items), (optional)) – Type, Curve type

  * **use_handles** (_boolean_ _,__(__optional_ _)_) – Handles, Take handle information into account in the conversion


bpy.ops.curves.cyclic_toggle()
    

Make active curve closed/opened loop

bpy.ops.curves.delete()
    

Remove selected control points or curves

bpy.ops.curves.draw(_*_ , _error_threshold =0.0_, _fit_method ='REFIT'_, _corner_angle =1.22173_, _use_cyclic =True_, _stroke =None_, _wait_for_input =True_, _is_curve_2d =False_, _bezier_as_nurbs =False_)
    

Draw a freehand curve

Parameters:
    

  * **error_threshold** (_float in_ _[__0_ _,__10_ _]__,__(__optional_ _)_) – Error, Error distance threshold (in object units)

  * **fit_method** (enum in [Curve Fit Method Items](../bpy_types_enum_items/curve_fit_method_items.md#rna-enum-curve-fit-method-items), (optional)) – Fit Method

  * **corner_angle** (_float in_ _[__0_ _,__3.14159_ _]__,__(__optional_ _)_) – Corner Angle

  * **use_cyclic** (_boolean_ _,__(__optional_ _)_) – Cyclic

  * **stroke** (`bpy_prop_collection` of `OperatorStrokeElement`, (optional)) – Stroke

  * **wait_for_input** (_boolean_ _,__(__optional_ _)_) – Wait for Input

  * **is_curve_2d** (_boolean_ _,__(__optional_ _)_) – Curve 2D

  * **bezier_as_nurbs** (_boolean_ _,__(__optional_ _)_) – As NURBS


bpy.ops.curves.duplicate()
    

Copy selected points or curves

bpy.ops.curves.duplicate_move(_*_ , _CURVES_OT_duplicate =None_, _TRANSFORM_OT_translate =None_)
    

Make copies of selected elements and move them

Parameters:
    

  * **CURVES_OT_duplicate** (`CURVES_OT_duplicate`, (optional)) – Duplicate, Copy selected points or curves

  * **TRANSFORM_OT_translate** (`TRANSFORM_OT_translate`, (optional)) – Move, Move selected items


bpy.ops.curves.extrude()
    

Extrude selected control point(s)

bpy.ops.curves.extrude_move(_*_ , _CURVES_OT_extrude =None_, _TRANSFORM_OT_translate =None_)
    

Extrude curve and move result

Parameters:
    

  * **CURVES_OT_extrude** (`CURVES_OT_extrude`, (optional)) – Extrude, Extrude selected control point(s)

  * **TRANSFORM_OT_translate** (`TRANSFORM_OT_translate`, (optional)) – Move, Move selected items


bpy.ops.curves.handle_type_set(_*_ , _type ='AUTO'_)
    

Set the handle type for bezier curves

Parameters:
    

**type** (enum in [`'AUTO'`, `'VECTOR'`, `'ALIGN'`, `'FREE_ALIGN'`, `'TOGGLE_FREE_ALIGN'`], (optional)) – 

Type

  * `AUTO` Auto – The location is automatically calculated to be smooth.

  * `VECTOR` Vector – The location is calculated to point to the next/previous control point.

  * `ALIGN` Align – The location is constrained to point in the opposite direction as the other handle.

  * `FREE_ALIGN` Free – The handle can be moved anywhere, and does not influence the point’s other handle.

  * `TOGGLE_FREE_ALIGN` Toggle Free/Align – Replace Free handles with Align, and all Align with Free handles.


bpy.ops.curves.pen(_*_ , _extend =False_, _deselect =False_, _toggle =False_, _deselect_all =False_, _select_passthrough =False_, _extrude_point =False_, _extrude_handle ='VECTOR'_, _delete_point =False_, _insert_point =False_, _move_segment =False_, _select_point =False_, _move_point =False_, _cycle_handle_type =False_, _size =0.01_)
    

Construct and edit Bézier curves

Parameters:
    

  * **extend** (_boolean_ _,__(__optional_ _)_) – Extend, Extend selection instead of deselecting everything first

  * **deselect** (_boolean_ _,__(__optional_ _)_) – Deselect, Remove from selection

  * **toggle** (_boolean_ _,__(__optional_ _)_) – Toggle Selection, Toggle the selection

  * **deselect_all** (_boolean_ _,__(__optional_ _)_) – Deselect On Nothing, Deselect all when nothing under the cursor

  * **select_passthrough** (_boolean_ _,__(__optional_ _)_) – Only Select Unselected, Ignore the select action when the element is already selected

  * **extrude_point** (_boolean_ _,__(__optional_ _)_) – Extrude Point, Add a point connected to the last selected point

  * **extrude_handle** (enum in [`'AUTO'`, `'VECTOR'`], (optional)) – Extrude Handle Type, Type of the extruded handle

  * **delete_point** (_boolean_ _,__(__optional_ _)_) – Delete Point, Delete an existing point

  * **insert_point** (_boolean_ _,__(__optional_ _)_) – Insert Point, Insert Point into a curve segment

  * **move_segment** (_boolean_ _,__(__optional_ _)_) – Move Segment, Delete an existing point

  * **select_point** (_boolean_ _,__(__optional_ _)_) – Select Point, Select a point or its handles

  * **move_point** (_boolean_ _,__(__optional_ _)_) – Move Point, Move a point or its handles

  * **cycle_handle_type** (_boolean_ _,__(__optional_ _)_) – Cycle Handle Type, Cycle between all four handle types

  * **size** (_float in_ _[__0_ _,__inf_ _]__,__(__optional_ _)_) – Size, Diameter of new points


bpy.ops.curves.sculptmode_toggle()
    

Enter/Exit sculpt mode for curves

bpy.ops.curves.select_all(_*_ , _action ='TOGGLE'_)
    

(De)select all control points

Parameters:
    

**action** (enum in [`'TOGGLE'`, `'SELECT'`, `'DESELECT'`, `'INVERT'`], (optional)) – 

Action, Selection action to execute

  * `TOGGLE` Toggle – Toggle selection for all elements.

  * `SELECT` Select – Select all elements.

  * `DESELECT` Deselect – Deselect all elements.

  * `INVERT` Invert – Invert selection of all elements.


bpy.ops.curves.select_ends(_*_ , _amount_start =0_, _amount_end =1_)
    

Select end points of curves

Parameters:
    

  * **amount_start** (_int in_ _[__0_ _,__inf_ _]__,__(__optional_ _)_) – Amount Front, Number of points to select from the front

  * **amount_end** (_int in_ _[__0_ _,__inf_ _]__,__(__optional_ _)_) – Amount Back, Number of points to select from the back


bpy.ops.curves.select_less()
    

Shrink the selection by one point

bpy.ops.curves.select_linked()
    

Select all points in curves with any point selection

bpy.ops.curves.select_linked_pick(_*_ , _deselect =False_)
    

Select all points in the curve under the cursor

Parameters:
    

**deselect** (_boolean_ _,__(__optional_ _)_) – Deselect, Deselect linked control points rather than selecting them

bpy.ops.curves.select_more()
    

Grow the selection by one point

bpy.ops.curves.select_random(_*_ , _seed =0_, _probability =0.5_)
    

Randomizes existing selection or create new random selection

Parameters:
    

  * **seed** (_int in_ _[__-inf_ _,__inf_ _]__,__(__optional_ _)_) – Seed, Source of randomness

  * **probability** (_float in_ _[__0_ _,__1_ _]__,__(__optional_ _)_) – Probability, Chance of every point or curve being included in the selection


bpy.ops.curves.separate()
    

Separate selected geometry into a new object

bpy.ops.curves.set_selection_domain(_*_ , _domain ='POINT'_)
    

Change the mode used for selection masking in curves sculpt mode

Parameters:
    

**domain** (enum in [Attribute Curves Domain Items](../bpy_types_enum_items/attribute_curves_domain_items.md#rna-enum-attribute-curves-domain-items), (optional)) – Domain

bpy.ops.curves.snap_curves_to_surface(_*_ , _attach_mode ='NEAREST'_)
    

Move curves so that the first point is exactly on the surface mesh

Parameters:
    

**attach_mode** (enum in [`'NEAREST'`, `'DEFORM'`], (optional)) – 

Attach Mode, How to find the point on the surface to attach to

  * `NEAREST` Nearest – Find the closest point on the surface for the root point of every curve and move the root there.

  * `DEFORM` Deform – Re-attach curves to a deformed surface using the existing attachment information. This only works when the topology of the surface mesh has not changed.


bpy.ops.curves.split()
    

Split selected points

bpy.ops.curves.subdivide(_*_ , _number_cuts =1_)
    

Subdivide selected curve segments

Parameters:
    

**number_cuts** (_int in_ _[__1_ _,__1000_ _]__,__(__optional_ _)_) – Number of Cuts

bpy.ops.curves.surface_set()
    

Use the active object as surface for selected curves objects and set it as the parent

bpy.ops.curves.switch_direction()
    

Reverse the direction of the selected curves

bpy.ops.curves.tilt_clear()
    

Clear the tilt of selected control points
  *[*]: Keyword-only parameters separator (PEP 3102)
