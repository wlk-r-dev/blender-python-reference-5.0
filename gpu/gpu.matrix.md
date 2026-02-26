# GPU Matrix Utilities (gpu.matrix)

This module provides access to the matrix stack.

gpu.matrix.get_model_view_matrix()
    

Return a copy of the model-view matrix.

Returns:
    

A 4x4 view matrix.

Return type:
    

[`mathutils.Matrix`](mathutils.md#mathutils.Matrix "mathutils.Matrix")

gpu.matrix.get_normal_matrix()
    

Return a copy of the normal matrix.

Returns:
    

A 3x3 normal matrix.

Return type:
    

[`mathutils.Matrix`](mathutils.md#mathutils.Matrix "mathutils.Matrix")

gpu.matrix.get_projection_matrix()
    

Return a copy of the projection matrix.

Returns:
    

A 4x4 projection matrix.

Return type:
    

[`mathutils.Matrix`](mathutils.md#mathutils.Matrix "mathutils.Matrix")

gpu.matrix.load_identity()
    

Load an identity matrix into the stack.

gpu.matrix.load_matrix(_matrix_)
    

Load a matrix into the stack.

Parameters:
    

**matrix** ([`mathutils.Matrix`](mathutils.md#mathutils.Matrix "mathutils.Matrix")) – A 4x4 matrix.

gpu.matrix.load_projection_matrix(_matrix_)
    

Load a projection matrix into the stack.

Parameters:
    

**matrix** ([`mathutils.Matrix`](mathutils.md#mathutils.Matrix "mathutils.Matrix")) – A 4x4 matrix.

gpu.matrix.multiply_matrix(_matrix_)
    

Multiply the current stack matrix.

Parameters:
    

**matrix** ([`mathutils.Matrix`](mathutils.md#mathutils.Matrix "mathutils.Matrix")) – A 4x4 matrix.

gpu.matrix.pop()
    

Remove the last model-view matrix from the stack.

gpu.matrix.pop_projection()
    

Remove the last projection matrix from the stack.

gpu.matrix.push()
    

Add to the model-view matrix stack.

gpu.matrix.push_pop()
    

Context manager to ensure balanced push/pop calls, even in the case of an error.

gpu.matrix.push_pop_projection()
    

Context manager to ensure balanced push/pop calls, even in the case of an error.

gpu.matrix.push_projection()
    

Add to the projection matrix stack.

gpu.matrix.reset()
    

Empty stack and set to identity.

gpu.matrix.scale(_scale_)
    

Scale the current stack matrix.

Parameters:
    

**scale** (_Sequence_ _[__float_ _]_) – Scale the current stack matrix with 2 or 3 floats.

gpu.matrix.scale_uniform(_scale_)
    

Parameters:
    

**scale** (_float_) – Scale the current stack matrix.

gpu.matrix.translate(_offset_)
    

Scale the current stack matrix.

Parameters:
    

**offset** (_Sequence_ _[__float_ _]_) – Translate the current stack matrix with 2 or 3 floats.
