# CCNE
or **C Compile aNd Execute** is a command line utility written in bash that compiles and executes C source file in a single step\
Generated using Claude

## How to execute
`ccne <filename.c>`
- Usage example - `ccne foo.c`

## How it executes
CCNE compiles the provided C source code into object file with the same name in the current working directory
- For example - `foo.c` to `foo.out`

After which it simply executes the `.out` file or `./foo.out`

## Compiler configuration
CCNE, by default, uses Gnu C Compiler or **GCC**\
If one wishes to use other compiler, simply edit the global variable `COMPILER`
