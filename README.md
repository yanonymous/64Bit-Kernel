# 64Bit-Kernel

Designed a kernel for a 64-bit OS

Right now it just prints a single Hardcoded string "64 Bit KERNEL --Yeshasvi" (Even this required Lots of work)

# PreRequisites

  * Any Code editor (I used VsCode)
  * Docker for building environment
  * Qemu for emulation purpose (add it to path)

# Setup

Build env using Docker

  * `docker build buildenv -t myos-buildenv` // _-t_ is used for giving tag and _myos-buildenv_ is your tag
  * To enter into buildenv
      - Windows cmd: `docker run --rm -it -v "%cd%":/root/env myos-buildenv`
      - Windows powershell: `docker run --rm -it -v "${pwd}:/root/env" myos-buildenv`

  * Now to get iso and other output files run make file as: `make build-x86_64`
  * Now `exit` to leave buildenv

# Emulate

As mentioned before, use Qemu for emulation

  - Run: `qemu-system-x86_64 -cdrom dist/x86_64/kernel.iso`

That's it for now :) 
