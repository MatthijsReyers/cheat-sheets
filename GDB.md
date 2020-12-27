<h1 align="center">GDB cheat sheet</h1>

## General tips & tricks

- **Auto complete**: You can use the `[tab]` key to autocomplete commands or see a list of possible options.
- **Clearing the terminal**: You can use `[Crtl]+[L]` to clear gdb (and bash!) on most terminal emulators. Alternatively you can also use the `shell clear` (posix) or `shell cls` (win) command to clear the terminal.
- **Assembly syntax**: You can switch to your preffered asm syntax with `set disassembly-flavor intel` or `set disassembly-flavor att`.

## Basic example commands

### Loading an executable

```
(gdb) file "path/to/exec.a"
```

### Running an executable

```
(gdb) run
(gdb) r
```

### Disassembling the main function

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

### Examining the stack/memory
Note that in the below command `4` stands for the amount of items to be printed. 
`x` stands for 'hexadecimal' and `w` stands for 'word'; these are flags that specify the format to print the memory in.
Some other possible flags include: `d` for printing the memory as decimal numbers, `i` for interpreting the data as instructions, `b` for setting the item size to be bytes, `a` for interpreting the data as memory addresses.
Lastly `$rsp` stands for the memory address in the rsp register, which is the location to start printing the memory from (other registers and a raw adress in hex format can also be used).
```
(gdb) x/4xw $rsp
```

### Viewing info about the stack/registers
```
(gdb) info frame
(gdb) info registers
(gdb) i r $rsp $rbp
```

### Exit gdb
```
(gdb) quit
(gdb) q
```
