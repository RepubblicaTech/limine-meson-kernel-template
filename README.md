# C kernel project template

This is a Meson-based project to build a Limine-compliant kernel executable.
This project is supposed to be a part of a larger project that creates the operating system image through a build orchestrator like `xbstrap`, `obos-strap`, etc. that builds other components e.g. userspace apps and the actual ISO.

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

# A few notes for users of the template

- x86_64 code is assembled with `nasm`. Other platforms will be assembled with `gcc`
- Common arch headers can go in `include/arch/common`.
