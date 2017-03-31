## Piping and Redirection

- cmd1 | cmd 2
- cmd > file
- cmd >> file
- cmd &> file
- cmd &>> file
- cmd m>&n

+++

```
$ echo 'hello world!' | awk '{ print toupper($0); }'
HELLO WORLD!
```
```
$ echo 'hello world!' > /tmp/hello_world
$ cat /tmp/hello_world
hello world!
```
```
$ echo 'hello world!' >> /tmp/hello_world
$ cat /tmp/hello_world
hello world!
hello world!
```
```
$ ls a x > /tmp/file.txt
ls: cannot access 'x': No such file or directory
$ cat /tmp/file.txt
a
$ ls a x &> /tmp/file.txt
$ cat /tmp/file.txt
ls: cannot access 'x': No such file or directory
a
```
