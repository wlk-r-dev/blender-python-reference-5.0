# Attribute(bpy_struct)

Attributes are used to store data that corresponds to geometry elements. Geometry elements are items in one of the geometry domains like points, curves, or faces.

An attribute has a `name`, a `type`, and is stored on a `domain`.

`name`
    

The name of this attribute. Names have to be unique within the same geometry. If the name starts with a `.`, the attribute is hidden from the UI.

`type`
    

The type of data that this attribute stores, e.g. a float, integer, color, etc. See [Attribute Type Items](../../bpy_types_enum_items/attribute_type_items.md).

`domain`
    

The geometry domain that the attribute is stored on. See [Attribute Domain Items](../../bpy_types_enum_items/attribute_domain_items.md).

## Using Attributes

Attributes can be stored on geometries like [`Mesh`](../M/bpy.types.Mesh.md#bpy.types.Mesh "bpy.types.Mesh"), [`Curves`](../C/bpy.types.Curves.md#bpy.types.Curves "bpy.types.Curves"), [`PointCloud`](../P/bpy.types.PointCloud.md#bpy.types.PointCloud "bpy.types.PointCloud"), etc. These geometries have attribute groups (usually called `attributes`). Using the groups, attributes can then be accessed by their name:
    
    
    radii = curves.attributes["radius"]
    

Creating and storing custom attributes is done using the `attributes.new` function:
    
    
    # Add a new attribute named `my_attribute_name` of type `float` on the point domain of the geometry.
    my_attribute = curves.attributes.new("my_attribute_name", 'FLOAT', 'POINT')
    

Removing attributes can be done like so:
    
    
    attribute = drawing.attributes["some_attribute"]
    drawing.attributes.remove(attribute)
    

Note

Some attributes are required and cannot be removed, like `"position"`.

Attribute values are read by accessing their `attribute.data` collection property. However, in cases where multiple values should be read at once, it is better to use the [`bpy_prop_collection.foreach_get`](../_other/bpy.types.bpy_prop_collection.md#bpy.types.bpy_prop_collection.foreach_get "bpy.types.bpy_prop_collection.foreach_get") function and read the values into a `numpy` buffer.
    
    
    import numpy as np
    
    # Get the radius attribute.
    radii = curves.attributes["radius"]
    # Print the radius of the first point.
    print(radii.data[0].value)
    # Output: 0.005
    
    # Get the total number of points.
    num_points = attributes.domain_size('POINT')
    # Create an empty buffer to read all the radii into.
    radii_data = np.zeros(num_points, dtype=np.float32)
    # Read all the radii of the curves into `radii_data` at once.
    radii.data.foreach_get('value', radii_data)
    # Print all the radii.
    print(radii_data)
    # Output: [0.1, 0.2, 0.3, 0.4, ... ]
    

Note

Some attribute types use different named properties to access their value. Instead of `value`, vectors use `vector`, and colors use `color`.

Writing to different attribute types is very similar. You can simply assign to a value directly. Again, when writing to multiple values, it is recommended to use the [`bpy_prop_collection.foreach_set`](../_other/bpy.types.bpy_prop_collection.md#bpy.types.bpy_prop_collection.foreach_set "bpy.types.bpy_prop_collection.foreach_set") function to write the values from a `numpy` buffer.
    
    
    import numpy as np
    
    radii = curves.attributes["radius"]
    # Write a radius with a value of 0.5 to the first point.
    radii.data[0].value = 0.5
    print(radii.data[0].value)
    # Output: 0.5
    
    num_points = attributes.domain_size('POINT')
    # Generate random radii with values between 0.001 and 0.05 using numpy.
    new_radii = np.random.uniform(0.001, 0.05, num_points)
    # Write the new radii to the radius attribute.
    radii.data.foreach_set('value', new_radii)
    

The [`bpy_prop_collection.foreach_get`](../_other/bpy.types.bpy_prop_collection.md#bpy.types.bpy_prop_collection.foreach_get "bpy.types.bpy_prop_collection.foreach_get") / [`bpy_prop_collection.foreach_set`](../_other/bpy.types.bpy_prop_collection.md#bpy.types.bpy_prop_collection.foreach_set "bpy.types.bpy_prop_collection.foreach_set") methods require a flat array. This is sometimes not desirable, e.g. when reading/writing positions, which are 3D vectors. In these cases, it’s possible to use `np.ravel` to pass the data as a flat array:
    
    
    num_points = attributes.domain_size('POINT')
    positions = curves.attributes['position']
    # Here, we're using a numpy array with shape (num_points, 3) so that each
    # element is a 3d vector.
    positions_data = np.zeros((num_points, 3), dtype=np.float32)
    # The `np.ravel` function will pass the `positions_data` as a flat array
    # without changing the original shape.
    positions.data.foreach_get('vector', np.ravel(positions_data))
    print(positions_data)
    # Output: [[0.1, 0.2, 0.3], [0.4, 0.5, 0.6], ...]
    

base class — [`bpy_struct`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct "bpy.types.bpy_struct")

subclasses — [`BoolAttribute`](../B/bpy.types.BoolAttribute.md#bpy.types.BoolAttribute "bpy.types.BoolAttribute"), [`ByteColorAttribute`](../B/bpy.types.ByteColorAttribute.md#bpy.types.ByteColorAttribute "bpy.types.ByteColorAttribute"), [`ByteIntAttribute`](../B/bpy.types.ByteIntAttribute.md#bpy.types.ByteIntAttribute "bpy.types.ByteIntAttribute"), [`Float2Attribute`](../F/bpy.types.Float2Attribute.md#bpy.types.Float2Attribute "bpy.types.Float2Attribute"), [`Float4x4Attribute`](../F/bpy.types.Float4x4Attribute.md#bpy.types.Float4x4Attribute "bpy.types.Float4x4Attribute"), [`FloatAttribute`](../F/bpy.types.FloatAttribute.md#bpy.types.FloatAttribute "bpy.types.FloatAttribute"), [`FloatColorAttribute`](../F/bpy.types.FloatColorAttribute.md#bpy.types.FloatColorAttribute "bpy.types.FloatColorAttribute"), [`FloatVectorAttribute`](../F/bpy.types.FloatVectorAttribute.md#bpy.types.FloatVectorAttribute "bpy.types.FloatVectorAttribute"), [`Int2Attribute`](../I/bpy.types.Int2Attribute.md#bpy.types.Int2Attribute "bpy.types.Int2Attribute"), [`IntAttribute`](../I/bpy.types.IntAttribute.md#bpy.types.IntAttribute "bpy.types.IntAttribute"), [`QuaternionAttribute`](../Q/bpy.types.QuaternionAttribute.md#bpy.types.QuaternionAttribute "bpy.types.QuaternionAttribute"), [`Short2Attribute`](../S/bpy.types.Short2Attribute.md#bpy.types.Short2Attribute "bpy.types.Short2Attribute"), [`StringAttribute`](../S/bpy.types.StringAttribute.md#bpy.types.StringAttribute "bpy.types.StringAttribute")

_class _bpy.types.Attribute(_bpy_struct_)
    

Geometry attribute

data_type
    

Type of data stored in attribute

Type:
    

enum in [Attribute Type Items](../../bpy_types_enum_items/attribute_type_items.md#rna-enum-attribute-type-items), default `'FLOAT'`, (readonly)

domain
    

Domain of the Attribute

Type:
    

enum in [Attribute Domain Items](../../bpy_types_enum_items/attribute_domain_items.md#rna-enum-attribute-domain-items), default `'POINT'`, (readonly)

is_internal
    

The attribute is meant for internal use by Blender

Type:
    

boolean, default False, (readonly)

is_required
    

Whether the attribute can be removed or renamed

Type:
    

boolean, default False, (readonly)

name
    

Name of the Attribute

Type:
    

string, default “”, (never None)

storage_type
    

Method used to store the data

  * `ARRAY` Array – Store a value for every element.

  * `SINGLE` Single – Store a single value for the entire domain.


Type:
    

enum in [`'ARRAY'`, `'SINGLE'`], default `'ARRAY'`, (readonly)

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

### Inherited Properties

  * [`bpy_struct.id_data`](../_other/bpy.types.bpy_struct.md#bpy.types.bpy_struct.id_data "bpy.types.bpy_struct.id_data")

| 


  
---|---  
  
### Inherited Functions

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
  
### References

  * [`AttributeGroupCurves.active`](bpy.types.AttributeGroupCurves.md#bpy.types.AttributeGroupCurves.active "bpy.types.AttributeGroupCurves.active")
  * [`AttributeGroupCurves.new`](bpy.types.AttributeGroupCurves.md#bpy.types.AttributeGroupCurves.new "bpy.types.AttributeGroupCurves.new")
  * [`AttributeGroupCurves.remove`](bpy.types.AttributeGroupCurves.md#bpy.types.AttributeGroupCurves.remove "bpy.types.AttributeGroupCurves.remove")
  * [`AttributeGroupGreasePencil.active`](bpy.types.AttributeGroupGreasePencil.md#bpy.types.AttributeGroupGreasePencil.active "bpy.types.AttributeGroupGreasePencil.active")
  * [`AttributeGroupGreasePencil.new`](bpy.types.AttributeGroupGreasePencil.md#bpy.types.AttributeGroupGreasePencil.new "bpy.types.AttributeGroupGreasePencil.new")
  * [`AttributeGroupGreasePencil.remove`](bpy.types.AttributeGroupGreasePencil.md#bpy.types.AttributeGroupGreasePencil.remove "bpy.types.AttributeGroupGreasePencil.remove")
  * [`AttributeGroupGreasePencilDrawing.active`](bpy.types.AttributeGroupGreasePencilDrawing.md#bpy.types.AttributeGroupGreasePencilDrawing.active "bpy.types.AttributeGroupGreasePencilDrawing.active")
  * [`AttributeGroupGreasePencilDrawing.new`](bpy.types.AttributeGroupGreasePencilDrawing.md#bpy.types.AttributeGroupGreasePencilDrawing.new "bpy.types.AttributeGroupGreasePencilDrawing.new")
  * [`AttributeGroupGreasePencilDrawing.remove`](bpy.types.AttributeGroupGreasePencilDrawing.md#bpy.types.AttributeGroupGreasePencilDrawing.remove "bpy.types.AttributeGroupGreasePencilDrawing.remove")
  * [`AttributeGroupMesh.active`](bpy.types.AttributeGroupMesh.md#bpy.types.AttributeGroupMesh.active "bpy.types.AttributeGroupMesh.active")
  * [`AttributeGroupMesh.active_color`](bpy.types.AttributeGroupMesh.md#bpy.types.AttributeGroupMesh.active_color "bpy.types.AttributeGroupMesh.active_color")
  * [`AttributeGroupMesh.new`](bpy.types.AttributeGroupMesh.md#bpy.types.AttributeGroupMesh.new "bpy.types.AttributeGroupMesh.new")
  * [`AttributeGroupMesh.remove`](bpy.types.AttributeGroupMesh.md#bpy.types.AttributeGroupMesh.remove "bpy.types.AttributeGroupMesh.remove")

| 

  * [`AttributeGroupPointCloud.active`](bpy.types.AttributeGroupPointCloud.md#bpy.types.AttributeGroupPointCloud.active "bpy.types.AttributeGroupPointCloud.active")
  * [`AttributeGroupPointCloud.new`](bpy.types.AttributeGroupPointCloud.md#bpy.types.AttributeGroupPointCloud.new "bpy.types.AttributeGroupPointCloud.new")
  * [`AttributeGroupPointCloud.remove`](bpy.types.AttributeGroupPointCloud.md#bpy.types.AttributeGroupPointCloud.remove "bpy.types.AttributeGroupPointCloud.remove")
  * [`Curves.attributes`](../C/bpy.types.Curves.md#bpy.types.Curves.attributes "bpy.types.Curves.attributes")
  * [`Curves.color_attributes`](../C/bpy.types.Curves.md#bpy.types.Curves.color_attributes "bpy.types.Curves.color_attributes")
  * [`GreasePencil.attributes`](../G/bpy.types.GreasePencil.md#bpy.types.GreasePencil.attributes "bpy.types.GreasePencil.attributes")
  * [`GreasePencil.color_attributes`](../G/bpy.types.GreasePencil.md#bpy.types.GreasePencil.color_attributes "bpy.types.GreasePencil.color_attributes")
  * [`GreasePencilDrawing.attributes`](../G/bpy.types.GreasePencilDrawing.md#bpy.types.GreasePencilDrawing.attributes "bpy.types.GreasePencilDrawing.attributes")
  * [`GreasePencilDrawing.color_attributes`](../G/bpy.types.GreasePencilDrawing.md#bpy.types.GreasePencilDrawing.color_attributes "bpy.types.GreasePencilDrawing.color_attributes")
  * [`Mesh.attributes`](../M/bpy.types.Mesh.md#bpy.types.Mesh.attributes "bpy.types.Mesh.attributes")
  * [`Mesh.color_attributes`](../M/bpy.types.Mesh.md#bpy.types.Mesh.color_attributes "bpy.types.Mesh.color_attributes")
  * [`PointCloud.attributes`](../P/bpy.types.PointCloud.md#bpy.types.PointCloud.attributes "bpy.types.PointCloud.attributes")
  * [`PointCloud.color_attributes`](../P/bpy.types.PointCloud.md#bpy.types.PointCloud.color_attributes "bpy.types.PointCloud.color_attributes")

  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
