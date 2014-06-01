runtime.js
====

Inspired by Node.js event-driven architecture and non-blocking I/O model, runtime.js project goal is to provide a platform that is designed and optimized from the ground up to run JavaScript applications efficiently.

Project is under development and currently does not provide many essential features. If you want to contribute, your help is very welcome.

![Console](https://raw.githubusercontent.com/runtimejs/runtimejs.github.io/master/img/runtimejs_1_compressed.png)

Technical details
----

- supported x86_64 only
- software isolated applications (processes)
- no heavy context switches, single address space
- does not use cpu protection rings
- non-blocking asynchronous IPC
- drivers and system services are implemented in JavaScript
- kernel written in C++11

Status
----

####What's done

- embedded V8 engine
- multitasking (cooperative only)
- IPC transferable functions and ArrayBuffers
- SMP support
- embedded ACPICA for ACPI support
- simple keyboard and VGA display drivers
- JavaScript REPL application
- PCI bus driver device detection


Build
----
####Prerequisites
- gcc 4.8 or newer cross compiler (target x86\_64-elf)
- fasm
- scons

####Using Docker

Easiest way to setup developer environment is to use Docker https://www.docker.io/

    ./docker-prepare.sh

To build

    ./docker-build.sh

####Without Docker

You need to install fasm, scons and GCC cross compiler targeting x86\_64-elf. http://wiki.osdev.org/GCC_Cross-Compiler

To build

    scons
    
####Run using QEMU

    ./qemu.sh
    
    
License
----
BSD
