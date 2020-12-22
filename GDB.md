# GDB debugger cheat sheet

## General tips & tricks
- **Auto complete**: You can use the `[tab]` key to autocomplete commands or see a list of possible options.
- **Clearing the terminal**: You can use `[Crtl]+[L]` to clear gdb (and bash!) on most terminal emulators. Alternatively you can also use the `shell clear` (posix) or `shell cls` (win) command to clear the terminal.

### Loading an executable

```
(gdb) file "path/to/exec.a"
```

### Disassembling (main) function

```
(gdb) disassemble main
```

### Placing breakpoints

```
# Using the name of a function:
(gdb) break main
# Breaking at a given instruction:
(gdb) break *0x0000000000400452
```

### Running an executable

```
(gdb) run
```


### View stack
```
info frame
(gdb) info
```
