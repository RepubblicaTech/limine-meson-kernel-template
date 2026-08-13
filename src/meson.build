c_args = [
  '-Wall',
  '-Wextra',
  '-std=gnu11',
  '-nostdinc',
  '-ffreestanding',
  '-fno-stack-protector',
  '-fno-stack-check',
  '-fno-lto',
  '-fno-PIC',
  '-ffunction-sections',
  '-fdata-sections',
  '-MMD',
  '-MP'
]

nasm_args = [
  '-F dwarf'
]

sources = [
  'kernel/kernel.c'
]

linker_script = join_paths(meson.current_source_dir(), 'arch'/target_arch/'linker.ld')

linker_flags = [
  '-nostdlib',
  '-static',
  '-Wl,-z,max-page-size=0x1000',
  '-Wl,--gc-sections',
  '-Wl,-T,' + linker_script
]

# adds all platform-specific flags and sources.
subdir('arch'/target_arch)

install_dir = meson.global_source_root()/join_paths('out', target_arch + '-' + get_option('buildtype'))

executable('kernel',
           sources,
           dependencies: [limine_proto, freestanding_hdrs],
           include_directories: includes,
           c_args: c_args,
           nasm_args: nasm_args,
           link_args: linker_flags,
           link_depends: 'arch'/target_arch/'linker.ld',
           install: true,
           install_dir: install_dir)
