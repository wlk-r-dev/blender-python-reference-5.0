# Dpaint Operators

bpy.ops.dpaint.bake()
    

Bake dynamic paint image sequence surface

bpy.ops.dpaint.output_toggle(_*_ , _output ='A'_)
    

Add or remove Dynamic Paint output data layer

Parameters:
    

**output** (enum in [`'A'`, `'B'`], (optional)) – Output Toggle

bpy.ops.dpaint.surface_slot_add()
    

Add a new Dynamic Paint surface slot

bpy.ops.dpaint.surface_slot_remove()
    

Remove the selected surface slot

bpy.ops.dpaint.type_toggle(_*_ , _type ='CANVAS'_)
    

Toggle whether given type is active or not

Parameters:
    

**type** (enum in [Prop Dynamicpaint Type Items](../bpy_types_enum_items/prop_dynamicpaint_type_items.md#rna-enum-prop-dynamicpaint-type-items), (optional)) – Type
  *[*]: Keyword-only parameters separator (PEP 3102)
