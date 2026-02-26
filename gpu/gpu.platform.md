# GPU Platform Utilities (gpu.platform)

This module provides access to GPU Platform definitions.

gpu.platform.backend_type_get()
    

Get actuve GPU backend.

Returns:
    

Backend type (‘OPENGL’, ‘VULKAN’, ‘METAL’, ‘NONE’, ‘UNKNOWN’).

Return type:
    

str

gpu.platform.device_type_get()
    

Get GPU device type.

Returns:
    

Device type (‘APPLE’, ‘NVIDIA’, ‘AMD’, ‘INTEL’, ‘SOFTWARE’, ‘QUALCOMM’, ‘UNKNOWN’).

Return type:
    

str

gpu.platform.renderer_get()
    

Get GPU to be used for rendering.

Returns:
    

GPU name.

Return type:
    

str

gpu.platform.vendor_get()
    

Get GPU vendor.

Returns:
    

Vendor name.

Return type:
    

str

gpu.platform.version_get()
    

Get GPU driver version.

Returns:
    

Driver version.

Return type:
    

str
