# NodeSocketStandard(NodeSocket)

base classes — [[bpy_struct]], [[NodeSocket]]

subclasses — [[NodeSocketBool]], [[NodeSocketBundle]], [[NodeSocketClosure]], [[NodeSocketCollection]], [[NodeSocketColor]], [[NodeSocketFloat]], [[NodeSocketFloatAngle]], [[NodeSocketFloatColorTemperature]], [[NodeSocketFloatDistance]], [[NodeSocketFloatFactor]], [[NodeSocketFloatFrequency]], [[NodeSocketFloatPercentage]], [[NodeSocketFloatTime]], [[NodeSocketFloatTimeAbsolute]], [[NodeSocketFloatUnsigned]], [[NodeSocketFloatWavelength]], [[NodeSocketGeometry]], [[NodeSocketImage]], [[NodeSocketInt]], [[NodeSocketIntFactor]], [[NodeSocketIntPercentage]], [[NodeSocketIntUnsigned]], [[NodeSocketMaterial]], [[NodeSocketMatrix]], [[NodeSocketMenu]], [[NodeSocketObject]], [[NodeSocketRotation]], [[NodeSocketShader]], [[NodeSocketString]], [[NodeSocketStringFilePath]], [[NodeSocketTexture]], [[NodeSocketVector]], [[NodeSocketVector2D]], [[NodeSocketVector4D]], [[NodeSocketVectorAcceleration]], [[NodeSocketVectorAcceleration2D]], [[NodeSocketVectorAcceleration4D]], [[NodeSocketVectorDirection]], [[NodeSocketVectorDirection2D]], [[NodeSocketVectorDirection4D]], [[NodeSocketVectorEuler]], [[NodeSocketVectorEuler2D]], [[NodeSocketVectorEuler4D]], [[NodeSocketVectorFactor]], [[NodeSocketVectorFactor2D]], [[NodeSocketVectorFactor4D]], [[NodeSocketVectorPercentage]], [[NodeSocketVectorPercentage2D]], [[NodeSocketVectorPercentage4D]], [[NodeSocketVectorTranslation]], [[NodeSocketVectorTranslation2D]], [[NodeSocketVectorTranslation4D]], [[NodeSocketVectorVelocity]], [[NodeSocketVectorVelocity2D]], [[NodeSocketVectorVelocity4D]], [[NodeSocketVectorXYZ]], [[NodeSocketVectorXYZ2D]], [[NodeSocketVectorXYZ4D]], [[NodeSocketVirtual]]

_class _bpy.types.NodeSocketStandard(_NodeSocket_)
    

links
    

List of node links from or to this socket.

Type:
    

[[NodeLinks]]

Note

Takes `O(len(nodetree.links))` time.

(readonly)

draw(_context_ , _layout_ , _node_ , _text_)
    

Draw socket

Parameters:
    

  * **layout** ([[UILayout]], (never None)) – Layout, Layout in the UI

  * **node** ([[Node]], (never None)) – Node, Node the socket belongs to

  * **text** (_string_ _,__(__never None_ _)_) – Text, Text label to draw alongside properties


draw_color(_context_ , _node_)
    

Color of the socket icon

Parameters:
    

**node** ([[Node]], (never None)) – Node, Node the socket belongs to

Returns:
    

Color

Return type:
    

float array of 4 items in [0, 1]

_classmethod _draw_color_simple()
    

Color of the socket icon

Returns:
    

Color

Return type:
    

float array of 4 items in [0, 1]

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
  * [[NodeSocket.name]]
  * [[NodeSocket.label]]
  * [[NodeSocket.identifier]]
  * [[NodeSocket.description]]
  * [[NodeSocket.is_output]]
  * [[NodeSocket.select]]
  * [[NodeSocket.hide]]
  * [[NodeSocket.enabled]]
  * [[NodeSocket.link_limit]]
  * [[NodeSocket.is_linked]]
  * [[NodeSocket.is_unavailable]]
  * [[NodeSocket.is_multi_input]]

| 

  * [[NodeSocket.show_expanded]]
  * [[NodeSocket.is_inactive]]
  * [[NodeSocket.is_icon_visible]]
  * [[NodeSocket.hide_value]]
  * [[NodeSocket.pin_gizmo]]
  * [[NodeSocket.node]]
  * [[NodeSocket.type]]
  * [[NodeSocket.display_shape]]
  * [[NodeSocket.inferred_structure_type]]
  * [[NodeSocket.bl_idname]]
  * [[NodeSocket.bl_label]]
  * [[NodeSocket.bl_subtype_label]]
  * [[NodeSocket.links]]

  
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
  * [[bpy_struct.keyframe_delete]]
  * [[bpy_struct.keyframe_insert]]
  * [[bpy_struct.keys]]

| 

  * [[bpy_struct.path_from_id]]
  * [[bpy_struct.path_from_module]]
  * [[bpy_struct.path_resolve]]
  * [[bpy_struct.pop]]
  * [[bpy_struct.property_overridable_library_set]]
  * [[bpy_struct.property_unset]]
  * [[bpy_struct.rna_ancestors]]
  * [[bpy_struct.type_recast]]
  * [[bpy_struct.values]]
  * [[NodeSocket.bl_system_properties_get]]
  * [[NodeSocket.draw]]
  * [[NodeSocket.draw_color]]
  * [[NodeSocket.draw_color_simple]]
  * [[NodeSocket.bl_rna_get_subclass]]
  * [[NodeSocket.bl_rna_get_subclass_py]]

  
---|---
  *[/]: Positional-only parameter separator (PEP 570)
