<h1 align="center">GDB cheat sheet</h1>

## General tips & tricks

- **Auto complete**: You can use the `[tab]` key to autocomplete commands or see a list of possible options.
- **Clearing the terminal**: You can use `[Crtl]+[L]` to clear gdb (and bash!) on most terminal emulators. Alternatively you can also use the `shell clear` (posix) or `shell cls` (win) command to clear the terminal.

## Example commands

### Loading an executable

```
(gdb) file "path/to/exec.a"
```

### Running an executable

```
(gdb) run
(gdb) r
```

### Disassembling (main) function

```
(gdb) disassemble main
```

### Placing breakpoints
```
(gdb) break main
(gdb) b main
```
```
(gdb) break *0x0000000000400452
(gdb) b *0x0000000000400452
```

### Continuing after hitting breakpoint
```
(gdb) continue
(gdb) c
```

### Viewing the stack
```
info frame
(gdb) info
```
