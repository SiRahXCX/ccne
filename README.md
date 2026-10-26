# ccne

**C**ompile **C** a**N**d **E**xecute compiles and execute a C file, then wait. Every time you save the file, it recompiles and runs it again.

```bash
ccne main.c
```

## Install

```bash
mkdir -p ~/.local/bin
cp ccne ~/.local/bin/ && chmod +x ~/.local/bin/ccne
```

Requires Linux, `bash`, GNU `stat`, and a C compiler (`cc` by default).

## Usage

```
ccne [-1|--once] <file.c> [program arguments...]
```

```bash
ccne main.c            # rerun on every save (Ctrl+C to stop)
ccne main.c 5 10       # pass arguments to the program
ccne --once main.c     # run once and exit with the program's exit code
```

Output goes to `main.out` next to the source. If compilation fails, the errors are shown and `ccne` waits for the next save.

## Configuration

Edit the top of the script:

- `COMPILER` is the compiler command (default `cc`).
- `POLL_INTERVAL` is the seconds between save checks (default `0.5`).
- `CLEAR_SCREEN` clears the terminal before each rerun (default `true`).

## Limitations

- Compiles one `.c` file, with no extra compiler flags.
- Waits for the program to exit before watching for saves. If it never exits, quit it with Ctrl+C and start `ccne` again.
