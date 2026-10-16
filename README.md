# CCNE
or **C Compile aNd Execute** is a command line utility written in bash that compiles and executes C source file in a single step
Code generated using Claude

## How to run
`ccne <filename.c>`
Usage example - `ccne foo.c`

## How it executes
CCNE compiles the provided source file into object file with the same name in the current working directory
For example - `foo.c` -> `foo.out`
After which it simply executes the `.out` file

## Compiler configuration
CCNE, by default, uses Gnu C Compiler or **GCC**
If one wishes to use other compiler, simply edit the global variable `COMPILER` to one's liking
