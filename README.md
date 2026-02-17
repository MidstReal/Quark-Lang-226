# QUARK

<div align="center">
<img src="https://img.shields.io/badge/language-C%2B%2B-blue.svg">
<img src="https://img.shields.io/badge/assembler-NASM-orange.svg">
<img src="https://img.shields.io/badge/platform-linux-lightgrey.svg">
<img src="https://img.shields.io/badge/license-MIT-green.svg">
</div>

This language is designed for easy development of your own operating systems and programs for them.

Requires g++, NASM and Qemu. 
To install on Ubuntu/Debian:
```bash
sudo apt update
sudo apt install g++ nasm qemu-system-x86
```
If you have changed the compiler, compile it with the command:
```bash
g++ -o compiler compiler.cpp
```
Compile the .qkl file:
```bash
./compiler input.qkl -o output.asm
```
Compile the .asm file:
```bash
nasm -f bin output.asm -o boot.bin
```
Run the .bin file:
```bash
qemu-system-x86_64 boot.bin
```
