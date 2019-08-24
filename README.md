# prime-select for hybrid laptops

## What is it?

On hybrid GPU laptopts with Ubuntu 18.04, the prime-select utility enables you to choose between intel and nvidia GPU.

However, it does not let you use your intel GPU for display and your nvidia GPU for deep learning with tensorflow or pytorch.

This repo contains a modified version of prime-select, which adds an 'hybrid' mode: display on intel GPU and deep learning on nvidia GPU.

## Installation

* Make your installation work with the standard version of prime-select (install cuda drivers, tensorflow, etc.)
* Replace /usr/bin/prime-select by the version of this repo

## Usage

```
prime-select   nvidia|intel|hybrid|query
    nvidia:   switches to NVIDIA's version of libGL.so
    intel: switches to the open-source version of libGL.so
    hybrid: use intel GPU for display and enables nvidia driver for tensorflow or pytorch
    query: checks which version is currently active and writes
        "nvidia", "intel", "hybrid" or "unknown" to the standard output
```
