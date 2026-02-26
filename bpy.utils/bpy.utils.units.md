# bpy.utils submodule (bpy.utils.units)

This module contains some data/methods regarding units handling.

bpy.utils.units.categories
    

Constant value bpy.utils.units.categories(NONE=’NONE’, LENGTH=’LENGTH’, AREA=’AREA’, VOLUME=’VOLUME’, MASS=’MASS’, ROTATION=’ROTATION’, TIME=’TIME’, TIME_ABSOLUTE=’TIME_ABSOLUTE’, VELOCITY=’VELOCITY’, ACCELERATION=’ACCELERATION’, CAMERA=’CAMERA’, POWER=’POWER’, TEMPERATURE=’TEMPERATURE’, WAVELENGTH=’WAVELENGTH’, COLOR_TEMPERATURE=’COLOR_TEMPERATURE’, FREQUENCY=’FREQUENCY’)

bpy.utils.units.systems
    

Constant value bpy.utils.units.systems(NONE=’NONE’, METRIC=’METRIC’, IMPERIAL=’IMPERIAL’)

bpy.utils.units.to_string(_unit_system_ , _unit_category_ , _value_ , _*_ , _precision =3_, _split_unit =False_, _compatible_unit =False_)
    

Convert a given input float value into a string with units.

Parameters:
    

  * **unit_system** (_str_) – The unit system, from `bpy.utils.units.systems`.

  * **unit_category** (_str_) – The category of data we are converting (length, area, rotation, etc.), from `bpy.utils.units.categories`.

  * **value** (_float_) – The value to convert to a string.

  * **precision** (_int_) – Number of digits after the comma.

  * **split_unit** (_bool_) – Whether to use several units if needed (1m1cm), or always only one (1.01m).

  * **compatible_unit** (_bool_) – Whether to use keyboard-friendly units (1m2) or nicer UTF8 ones (1m²).


Returns:
    

The converted string.

Return type:
    

str

Raises:
    

**ValueError** – if conversion fails to generate a valid Python string.

bpy.utils.units.to_value(_unit_system_ , _unit_category_ , _str_input_ , _*_ , _str_ref_unit =None_)
    

Convert a given input string into a float value.

Parameters:
    

  * **unit_system** (_str_) – The unit system, from `bpy.utils.units.systems`.

  * **unit_category** (_str_) – The category of data we are converting (length, area, rotation, etc.), from `bpy.utils.units.categories`.

  * **str_input** (_str_) – The string to convert to a float value.

  * **str_ref_unit** (_str_ _|__None_) – A reference string from which to extract a default unit, if none is found in `str_input`.


Returns:
    

The converted/interpreted value.

Return type:
    

float

Raises:
    

**ValueError** – if conversion fails to generate a valid Python float value.
  *[*]: Keyword-only parameters separator (PEP 3102)
