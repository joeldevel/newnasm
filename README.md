# newnasm Create a new assembly program

## NOTE: You need to install NetwideAssembler in order to compile assembler programs

## Installation: 

Run the install.sh. This will copy the file to `/home/USER/bin`. So it is 
available everywhere.

`$ bash install.sh`

## Usage: 

`$ newnasm YOUR_PROGRAM_NAME`

Creates a file with extension `.asm` and a makefile

Example: 

` newnasm hello_world `

will create a file named `hello_world.asm` with the following content

```
;author:      floncho
;date:        05/14/2019
;compile:     nasm hello_world.asm -f elf64
;linkedition: gcc hello_world.o <other libs> -no-pie -o hello_world.
;compile and linkedit: make

global main

section .data 

section .bss  

section .text

main: 

	ret
```

And a makefile with instructions to build the program.

So now you are ready to go!

## Build

Just run `make`