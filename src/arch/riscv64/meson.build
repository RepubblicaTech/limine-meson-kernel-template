arch_sources = [
  'arch/riscv64/cpu.asm'
]

sources += arch_sources

c_args += [
  '-march=rv64imac_zicsr_zifencei',
  '-mabi=lp64',
  '-mno-relax'
]

linker_flags += [
  '-Wl,-melf64lriscv',
  '-Wl,--no-relax'
]
