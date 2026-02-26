# InlineShaderNodes

## Inline Shader Nodes
    
    
    import bpy
    
    # The materials should be retrieved from the evaluated object to make sure that
    # e.g. edits of Geometry Nodes are applied.
    depsgraph = bpy.context.view_layer.depsgraph
    ob = bpy.context.active_object
    ob_eval = depsgraph.id_eval_get(ob)
    material_eval = ob_eval.material_slots[0].material
    
    # Compute the inlined shader nodes.
    # Important: Do not loose the reference to this object while accessing the inlined
    #   node tree. Otherwise there will be a crash due to a dangling pointer.
    inline_shader_nodes = material_eval.inline_shader_nodes()
    
    # Get the actual inlined `bpy.types.NodeTree`.
    tree = inline_shader_nodes.node_tree
    
    for node in tree.nodes:
        print(node.name)
    

_class _bpy.types.InlineShaderNodes
    

An inlined shader node tree.

node_tree
    

The inlined node tree.

Type:
    

[[bpy.types.NodeTree]]

_static _from_light(_light_)
    

Create an inlined shader node tree from a light.

Parameters:
    

**light** ([_bpy.types.Light_](../L/bpy.types.Light.md#bpy.types.Light "bpy.types.Light")) – The light to online the node tree of.

_static _from_material(_material_)
    

Create an inlined shader node tree from a material.

Parameters:
    

**material** ([_bpy.types.Material_](../M/bpy.types.Material.md#bpy.types.Material "bpy.types.Material")) – The material to inline the node tree of.

_static _from_world(_world_)
    

Create an inlined shader node tree from a world.

Parameters:
    

**world** ([_bpy.types.World_](../W/bpy.types.World.md#bpy.types.World "bpy.types.World")) – The world to inline the node tree of.
