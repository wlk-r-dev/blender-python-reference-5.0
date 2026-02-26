# Application Timers (bpy.app.timers)

## Run a Function in x Seconds
    
    
    import bpy
    
    
    def in_5_seconds():
        print("Hello World")
    
    
    bpy.app.timers.register(in_5_seconds, first_interval=5)
    

## Run a Function every x Seconds
    
    
    import bpy
    
    
    def every_2_seconds():
        print("Hello World")
        return 2.0
    
    
    bpy.app.timers.register(every_2_seconds)
    

## Run a Function n times every x seconds
    
    
    import bpy
    
    counter = 0
    
    
    def run_10_times():
        global counter
        counter += 1
        print(counter)
        if counter == 10:
            return None
        return 0.1
    
    
    bpy.app.timers.register(run_10_times)
    

## Assign parameters to functions
    
    
    import bpy
    import functools
    
    
    def print_message(message):
        print("Message:", message)
    
    
    bpy.app.timers.register(functools.partial(print_message, "Hello"), first_interval=2.0)
    bpy.app.timers.register(functools.partial(print_message, "World"), first_interval=3.0)
    

bpy.app.timers.is_registered(_function_)
    

Check if this function is registered as a timer.

Parameters:
    

**function** (_Callable_ _[__[__]__,__float_ _|__None_ _]_) – Function to check.

Returns:
    

True when this function is registered, otherwise False.

Return type:
    

bool

bpy.app.timers.register(_function_ , _*_ , _first_interval =0_, _persistent =False_)
    

Add a new function that will be called after the specified amount of seconds. The function gets no arguments and is expected to return either None or a float. If `None` is returned, the timer will be unregistered. A returned number specifies the delay until the function is called again. `functools.partial` can be used to assign some parameters.

Parameters:
    

  * **function** (_Callable_ _[__[__]__,__float_ _|__None_ _]_) – The function that should called.

  * **first_interval** (_float_) – Seconds until the callback should be called the first time.

  * **persistent** (_bool_) – Don’t remove timer when a new file is loaded.


bpy.app.timers.unregister(_function_)
    

Unregister timer.

Parameters:
    

**function** (_Callable_ _[__[__]__,__float_ _|__None_ _]_) – Function to unregister.
  *[*]: Keyword-only parameters separator (PEP 3102)
