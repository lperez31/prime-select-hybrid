# prime-select for hybrid laptops

## What is it?

A modified version of prime-select. It adds an 'hybrid' profile in which the Nvidia GPU is available for tensorflow or pytorch, while the graphics remain on Intel GPU.

It works on Ubuntu 18.04.

## Installation

* Make your installation work with the standard version of prime-select (install cuda drivers, tensorflow, etc.)
* Replace /usr/bin/prime-select by the version of this repo

## Usage

To switch to the hybrid profile:

```
sudo prime-select hybrid
```

Other options remain similar to standard prime-select command:

```
prime-select   nvidia|intel|hybrid|query
    nvidia:   switches to NVIDIA's version of libGL.so
    intel: switches to the open-source version of libGL.so
    hybrid: use intel GPU for display and enables nvidia driver for tensorflow or pytorch
    query: checks which version is currently active and writes
        "nvidia", "intel", "hybrid" or "unknown" to the standard output
```
