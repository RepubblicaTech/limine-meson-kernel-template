arch_sources = [
  'arch/aarch64/cpu.asm'
]

sources += arch_sources

c_args += [
  '-mtune=generic',
  '-march=armv8-a+nofp+nosimd',
  '-mgeneral-regs-only'
]

linker_flags += [
  '-Wl,-maarch64elf'
]
