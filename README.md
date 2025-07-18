# 🧠 Hello World in NASM (x86 Assembly on Linux)

This repository contains a simple **"Hello, World!"** program written in **x86 NASM Assembly**, executed on a **Linux environment** using **syscalls**. It demonstrates basic concepts of assembly programming, system calls, and debugging using **GDB**.

---

## 🔧 Requirements

- Linux OS (preferably Ubuntu)
- NASM (Netwide Assembler)
- GNU LD (Linker)
- GDB (GNU Debugger)
- Terminal and basic text editor (like `gedit`, `nano`, or `vim`)

Install tools (if not already installed):
```bash
sudo apt update
sudo apt install nasm gdb build-essential

Build & Run Instructions

; Commands to execute this code; 
;$gedit hello.asm              
;$nasm -f elf32 -g hello.asm -o hello.o         
;$ld -m elf_i386 hello.o -o hello
;$./hello

; It will show output on terminal prompt as $ Hello World !

; -g flag to include debugging info in the object file.
;-f option specifies the output file format that NASM should generate. elf32 , elf64,win32

; commands for GDB GNU Debbugger
;$ gdb ./hello  ; if it works properly, you will get prompt as gdb
;(gdb)
;(gdb)  break _start
;(gdb)  run
;(gdb)  set disassembly-flavor intel
;(gdb)  disassemble _start
;(gdb)  layout asm
;(gdb)  layout regs
;(gdb)  nexti ;continue to fetch and execute the instrucion

File Structure :

├── hello.asm      # Assembly source code
├── hello.o        # Assembled object file (after NASM)
├── hello          # Final executable binary (after linking)
└── README.md      # This documentation file
