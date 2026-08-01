# C kernel project template

This is a Meson-based project to build a Limine-compliant kernel executable.
This project is supposed to be a part of a larger project that creates the operating system image through a build orchestrator like `xbstrap`, `obos-strap`, etc. that builds other components like userspace apps.

# Building

Make sure you have Meson and a C compiler and linker installed on your system.

Setup the build directory:
```sh
meson setup build
```

Build the kernel:
```sh
meson compile -C build
# or
cd build
ninja
```
