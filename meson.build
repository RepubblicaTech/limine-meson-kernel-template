project('limine-meson',
        'c', 'nasm',
        version: '0.1',
        meson_version: '>= 1.1')

fs = import('fs')

target_arch = get_option('target')
includes = include_directories('include/arch' / target_arch)

summary('Build target', target_arch, section: 'Build information')

# user controllable C flags.
add_global_arguments('-pipe',
                     language : 'c')

limine_proto = dependency('limine-protocol', required: true)
freestanding_hdrs = dependency('freestanding_hdrs', required: true)

# build kernel executable.
subdir('src')
