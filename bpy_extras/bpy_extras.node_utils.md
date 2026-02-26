# bpy_extras submodule (bpy_extras.node_utils)

bpy_extras.node_utils.connect_sockets(_input_ , _output_)
    

Connect sockets in a node tree.

This is useful because the links created through the normal Python API are invalid when one of the sockets is a virtual socket (grayed out sockets in Group Input and Group Output nodes).

It replaces node_tree.links.new(input, output)

bpy_extras.node_utils.find_base_socket_type(_socket_)
    

Find the base class of the socket.

Sockets can have a subtype such as NodeSocketFloatFactor, but only the base type is allowed, e. g. NodeSocketFloat

bpy_extras.node_utils.find_node_input(_node_ , _name_)
