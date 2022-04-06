# How to use computer? А. В. Столяров. pp. 60

Left:  day(s) 0 hour(s) 
Status: Not Started
Tags: BNotes

```bash
# Usual commands
$ cp
$ mv
$ less
# Templates
$ rm -rf *
$ rm -rf ?.txt
$ rm -rf [2345].txt
$ rm -rf *.{gif,jpg,png}
$ rm -rf [!_]*.c
# History
$ history | less
$ !!
$ !1
$ !1:1
$ !abc
```

**<Ctrl-r>** - search

**<Ctrl-c>** - cancel

**<Ctrl-d>** - end of stdin **/** конец потока ввода **/** fd=0

**<Ctrl-/>** - end 

**<Ctrl-z>** - to stop and $ bg  for resume in backgroud process

**<Ctrl-s>**  - stop

**<Ctrl-q>** - resume

```bash
$ ps
$ ps ax
$ ps axu
$ top 
$ nautilus . &
$ jobs
$ cmd > file1 < file2
$ cmd1 | cmd2
$ cmd3 2> errfile
#Vim
:r <name> 
:e <name>
:ls
:b <N>
:32 #goto line 32
```

Секции системного справочника:

- 1 - пользовательские команды OC Unix (ls, rm, mv);
- 2 - системные вызовы ядра OС Unix;
- 3 - библиотечные функции языка Си;
- 4 - описания файлов устройств;
- 5 - описания форматов системных конфигурационных файлов;
- 6 - игровые программы;
- 7 - общие понятия (man ip);
- 8 - команды системного администрирования;

```bash
$ cmd1 && cmd2 
$ cmd1 || cmd2
$ (cmd1 && cmd2) | cmd3 
$ script filename # in the end <Ctrl-d>
$ nautilus &
$ tldr
```

### Links to other pages:

- 

### Sources:

- [Программирование: введение в профессию. Том 1: азы программирования. А. В. Столяров](%D0%9F%D1%80%D0%BE%D0%B3%D1%80%D0%B0%D0%BC%D0%BC%D0%B8%D1%80%20d7bd1.md)