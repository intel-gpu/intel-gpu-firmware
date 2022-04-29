# Intel® GPU firmware

This repo holds firmware binaries for various GPUs

## Dependencies
This firmware is part of a collection of kernel mode drivers
that together enable support for Intel graphics. The backports 
collection within https://github.com/intel-gpu includes:

  - [i915](https://github.com/intel-gpu/intel-gpu-i915-backports) - The main graphics driver (includes a compatible DRM subsystem and dmabuf if necessary).
  - [cse](https://github.com/intel-gpu/intel-gpu-cse-backports) - Converged Security Engine
  - [pmt](https://github.com/intel-gpu/intel-gpu-pmt-backports) - Intel Platform Telemetry
  - [firmware](https://github.com/intel-gpu/intel-gpu-firmware) - Contains firmware required by i915.

Each project is tagged consistently so when pulling these repos pull the same tag.

## Installation:

Copy all binaries to /lib/firmware/updates/i915/:

```
sudo mkdir -p /lib/firmware/updates/i915/
sudo cp firmware/*.bin /lib/firmware/updates/i915/
```
