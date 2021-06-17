** Assembly Language
Assembly language is a low level language which is compiled into cpu-specific machine code using an assembler which is again specific to the cpu as each and every cpu has its own set of Instructions and opcodes

** Tools
1) We will use QEMU as our OS emulator
Installation: 
    - Use 'sudo apt install aqemu' to install gui frontend to qemu. This command also installs the qemu along with the gui
Running: (Reference: https://askubuntu.com/questions/138140/how-do-i-install-qemu)
    - There won't be any output if you enter 'qemu' on the terminal even after the installation. As in /usr/bin, there is not qemu, but you can use qemu-system-x86_64,qemu-system-arm , etc.
    - On terminal, just replace qemu with qemu-system-i386 or qemu-system-x86_64 as appropriate (whether you want a 32-bit or 64-bit system, and which ISO you're using). But if you need to use qemu, create a link to 'qemu-system-x86_64' in '~/bin/qemu'.
    - You can also use aqemu, which is a graphical (GUI) front-end to qemu.
    - Example of executing iso image on i386 machine 'qemu-system-i386 -net user -cdrom my_iso.iso'

2) We will use VS Code as our IDE to develop the OS.
Visit the official page of Microsoft VS Code to install it.

3) To simplify the building process we will be using docker.
Go to the docker dir inside the base info dir to know more about docker.

4) GCC-Compiler and an Assembler
    - We will be using gcc-cross-x86_64-elf as cross compiler. To simplify the process we will be using docker for this.
    Refer 'https://hub.docker.com/r/randomdude/gcc-cross-x86_64-elf/tags?page=1&ordering=last_updated' for more info.
    - We will also need NASM (Netwide Assembler) which is an assembler and disassembler for the Intel x86 CPU architecture.
    This can be used to write 16-bit, 32-bit (IA-32), 64-bit (x86-64) programs. NASM is considered to be one of the most popular assemblers for Linux.
    Install this using docker 'RUN apt-get install -y nasm' in Dockerfile

5) We will also need the package 'xorriso', add the command 'RUN apt-get install-y xorriso' to the Dockerfile

6) We will also be needing grub package for building final iso file.
Install by adding the commands 'RUN apt-get install -y grub-pc-bin' and 'RUN apt-get install -y grub-common' to Dockerfile

** Building x86_64 OS (i.e. X86 architecture and 64 bit system)
1) Creating a docker image (which is like a snapshot of a linux machine)
2) Install(add to Dockerfile) the above mentioned 4, 5, 6 tools to Dockerfile.
3) Then configure other details like VOLUME, WORKDIR, etc
4) Refer to this video to know more: 'https://youtu.be/FkrpUaGThTQ'
5) Use 'docker run --rm -it -v $PWD:/root/env myos-buildenv' while running the docker image not the one shown in the video.
The difference is to use capital PWD in place of small pwd in the command.
6) Use 'qemu-system-x86_64 -cdrom <path-to-iso-file' to run the the iso file on qemu emulator with x86 64bit qemu system.

** AQEMU config
- aqemu virtual machine configurations are present in '/home/praneeth/.aqemu/'
- QEMU Found in "/usr/bin/", version: QEMU 2.0

- When on qemu Virtual Machine fullscreen mode, use Ctrl+Alt+F to toggle the fullscreen.

