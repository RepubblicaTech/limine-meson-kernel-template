arch_sources = [
  'arch/x86_64/cpu.asm'
]

sources += arch_sources

if (not cc.has_argument('-march=x86-64'))
  error('C Compiler does not support x86_64 (x86-64) target!')
endif

c_args += [
  '-m64',
  '-march=x86-64',
  '-mabi=sysv',
  '-mno-80387',
  '-mno-mmx',
  '-mno-sse',
  '-mno-sse2',
  '-mno-red-zone',
  '-mcmodel=kernel'
]

linker_flags += [
  '-Wl,-melf_x86_64'
]

nasm_args += [
  '-f elf64'
]
