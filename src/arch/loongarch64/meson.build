arch_sources = [
  'arch/loongarch64/cpu.asm'
]

sources += arch_sources

c_args += [
  '-march=loongarch64',
  '-mabi=lp64s',
  '-mfpu=none',
  '-msimd=none'
]

linker_flags += [
  '-Wl,-melf64loongarch'
]
