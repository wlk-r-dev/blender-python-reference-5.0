# Additional Math Functions (bl_math)

Miscellaneous math utilities module.

bl_math.clamp(_value_ , _min =0_, _max =1_)
    

Clamps the float value between minimum and maximum. To avoid confusion, any call must use either one or all three arguments.

Parameters:
    

  * **value** (_float_) – The value to clamp.

  * **min** (_float_) – The minimum value, defaults to 0.

  * **max** (_float_) – The maximum value, defaults to 1.


Returns:
    

The clamped value.

Return type:
    

float

bl_math.lerp(_from_value_ , _to_value_ , _factor_)
    

Linearly interpolate between two float values based on factor.

Parameters:
    

  * **from_value** (_float_) – The value to return when factor is 0.

  * **to_value** (_float_) – The value to return when factor is 1.

  * **factor** (_float_) – The interpolation value, normally in [0.0, 1.0].


Returns:
    

The interpolated value.

Return type:
    

float

bl_math.smoothstep(_from_value_ , _to_value_ , _value_)
    

Performs smooth interpolation between 0 and 1 as value changes between from and to values. Outside the range the function returns the same value as the nearest edge.

Parameters:
    

  * **from_value** (_float_) – The edge value where the result is 0.

  * **to_value** (_float_) – The edge value where the result is 1.

  * **factor** (_float_) – The interpolation value.


Returns:
    

The interpolated value in [0.0, 1.0].

Return type:
    

float
