### File system

- pwd
- ls
- cd
- pushd
- popd
- dirs
- cat
- tac
- tee
- sort
- touch
- type
- which
- whatis
- whereis
- file

+++

#### pwd

Print name of current/working directory

#### ls

List directory contents

+++

#### cd

Change the shell working directory

```
$ pwd
/tmp
$ cd
$ pwd
/home/user
```
```
$ pwd
/tmp
$ cd /usr
$ cd -
$ pwd
/tmp
```

+++

#### pushd

Add directories to stack

```
$ pwd
/home/user
$ pushd ~/Documents
~/Documents ~
$ pwd
/home/user/Documents
```

+++

#### popd

Remove directories from stack

```
$ pushd ~/Documents
~/Documents ~
$ popd
~
$ pwd
/home/user
```

+++

#### dirs

Display directory stack

```
$ pushd ~/Documents
~/Documents ~
$ dirs
~/Documents ~
```

+++

#### cat

Concatenate files and print on the standard output

```
$ cat file.txt
line1
line2
line3
line4
line5
```
```
$ cat file1.txt file2.txt
file1
file2
```

+++

#### tac

Concatenate files and print on the standard output in reverse

```
$ tac file.txt
line5
line4
line3
line2
line1
```

+++

#### tee

Read from standard input and write to standard output and files

```
echo 'nameserver 8.8.8.8' | sudo tee -a /etc/resolv.conf
```

+++

#### sort

Sort lines of text files

```
$ cat file.txt
25437
22044
31
7850
22093
$ sort file.txt
22044
22093
25437
31
7850
$ sort -h file.txt
31
7850
22044
22093
25437
```

+++

#### touch

Change file timestamps

```
$ ll a
-rw-r--r-- 1 user user 0 mar 30 14:29 a
$ touch a
$ ll a
-rw-r--r-- 1 user user 0 mar 30 15:03 a
```

+++

#### type

Display information about command type

```
$ type gcc
gcc is /usr/bin/gcc
$ type ll
ll is aliased to `ls -alhF --group-directories-first'
$ type kill
kill is a shell builtin
```

+++

#### which

Locate a command

```
$ which ls
/bin/ls
```

+++

#### whatis

Display one-line manual page descriptions

```
$ whatis printf
printf (3)           - formatted output conversion
printf (1)           - format and print data
```

+++

#### whereis

Locate the binary, source, and manual page files for a command

```
$ whereis ls
ls: /bin/ls /usr/share/man/man1/ls.1.gz
```

+++

#### file

Determine file type

```
$ file /etc/hosts
/etc/hosts: ASCII text
$ file /bin/ls
/bin/ls: ELF 64-bit LSB shared object, x86-64, version 1 (SYSV), dynamically linked, interpreter /lib64/ld-linux-x86-64.so.2, for GNU/Linux 2.6.32, BuildID[sha1]=ca48043ceac13b6eca09bce7e766844c8c1fdfbe, stripped
$ file /usr/lib/x86_64-linux-gnu/libstdc++.so.6.0.22
/usr/lib/x86_64-linux-gnu/libstdc++.so.6.0.22: ELF 64-bit LSB shared object, x86-64, version 1 (GNU/Linux), dynamically linked, BuildID[sha1]=681b1f24ae00f8a21b16ceac44f6778877c2ff66, stripped
```
