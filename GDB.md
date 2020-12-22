# GDB debugger cheat sheet

## General tips & tricks
- *Auto complete*: You can use the `[tab]` key to autocomplete commands or see a list of possible options.
- *Clearing the terminal*: You can use `[Crtl]+[L]` to clear gdb (and bash!) on most terminal emulators. Alternatively you can also use the `shell clear` (posix) or `shell cls` (win) command to clear the terminal.

### Loading an executable

```
(gdb) file "path/to/exec.a"
```

### Disassemble (main) function

```
(gdb) disassemble main
```

### View stack
```
(gdb) disassemble main
```
