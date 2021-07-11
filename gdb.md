https://www.youtube.com/watch?v=PorfLSr3DDI
## Enter TUI mode
```c-x a```
## refresh screen
```c-l```
## get other windows
```c-x 2```
```tui reg float```
```c-p```last command
```c-n```next command
## shell
```shell ls```
## python
there's python interpreter
```gdb
python print('hello world')
``` 
```import os```
## reversible debugging
can step back when failed
### core dunped
```bash
gdb -c core.xxxx
```
## build with more debug info
```gcc -ggdb3 hello.c``` for more debug information
## in ~/.gdbinit
```gdb
set history save on
set print pretty on
set pagination off
set confirn off
```

ptrace
```info signals```
## watch point
stop when target is modified
```gdb
watch target
```
```gdb
watch -l target
```
watch location
```gdb
rwatch target
```
stop when target is read
```gdb
watch target thread 3
```
stop when thread 3 modifies target
```gdb
watch target if target > 10
```
stop when target is > 10
## Thread apply
```gdb
info threads 
# list thread info
thread apply 1-4 print $sp
thread aplly all backtrace
thread apply all backtrace full
```
