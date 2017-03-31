## Introduction to using the command line interface terminal

### Cheat sheet

https://duckduckgo.com/?q=bash+cheat+sheet



### Shortcuts

- C-c 	Interrupt running process
- C-z 	Suspend running process
- C-d 	Exit from current shell
- C-l 	Clear Screen
- C-a 	Move at the start of the line
- C-e 	Move at the end of the line
- M-← 	Move backward by a word
- M-b 	Move backward by a word (alternative)
- M-→ 	Move forward by a word
- M-f 	Move forward by a word (alternative)
- C-x, C-x 	Move cursor between start of line and current position

--

- M-t 	Swap the last two words before the cursor
- C-t 	Swap the last two characters before the cursor
- M-Backspace 	Delete a word (backward)
- C-w 	Delete a word (backward) (alternative)
- M-d 	Delete a word (forward)
- C-h 	Delete one character backward (same as Backspace)
- C-k 	Kill from cursor to the end of line
- C-u 	Kill from cursor to the beginning of line
- M-u 	Upper-case from cursor to the end of word
- M-l 	Lower-case from cursor to the end of word
- M-c 	Capitalize word (from cursor position)

--

- C-y 	Paste
- C-_ 	Undo
- M-r 	Revert to original command (before editing it)
- C-p 	Get previous command
- C-n 	Get next command
- C-r, <pattern> 	Search previous command containing <pattern>
- M-. 	Insert last argument of last command
- M-<N>, C-M-y 	Get Nth argument of previous command (N=0 gives the command)
- M-< 	Insert oldest command from history
- C-x, C-v 	Show bash version
- C-x, C-e 	Edit current line with ${EDITOR}

### Getting help

- man
- apropos     <!-- .element: class="fragment" -->
- help        <!-- .element: class="fragment" -->
- info        <!-- .element: class="fragment" -->
- google.com  <!-- .element: class="fragment" -->

++

#### man

System's manual pager

<table>
  <tr>
    <td>**man** [*section*] *page*</td>
    <td>Display the manual page for the item ___page___</td>
  <tr>
  <tr>
    <td>**man -k** *regexp*</td>
    <td>Search the short descriptions and manual page names for the keyword as regular expression</td>
  </tr>
</table>

++

##### sections

<table>
  <tr>
    <th>Section</th>
    <th>Description</th>
  </tr>
  <tr>
    <td>1</td>
    <td>General commands</td>
    </tr>
  <tr>
    <td>2</td>
    <td>System calls</td>
  </tr>
  <tr>
    <td>3</td>
    <td>Library functions, covering in particular the C standard library</td>
  </tr>
  <tr>
    <td>4</td>
    <td>Special files (usually devices, those found in /dev) and drivers</td>
  </tr>
  <tr>
    <td>5</td>
    <td>File formats and conventions</td>
  </tr>
  <tr>
    <td>6</td>
    <td>Games and screensavers</td>
  </tr>
  <tr>
    <td>7</td>
    <td>Miscellanea</td>
  </tr>
  <tr>
    <td>8</td>
    <td>System administration commands and daemons</td>
  </tr>
</table>

++

#### apropos

Search the manual page names and descriptions

**apropos** *regexp* [**--and** *regexp*]

#### help

Display information about built-in commands.

**help** *command*

#### info

GNU replacement for man pages.

++

## Piping and Redirection

- cmd1 | cmd 2
- cmd > file
- cmd >> file
- cmd &> file
- cmd &>> file
- cmd m>&n

++

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

++

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

++

#### pwd

Print name of current/working directory

#### ls

List directory contents

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

++

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

#### dirs

Display directory stack

```
$ pushd ~/Documents
~/Documents ~
$ dirs
~/Documents ~
```

++

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

++

#### tee

Read from standard input and write to standard output and files

`echo 'nameserver 8.8.8.8' | sudo tee -a /etc/resolv.conf`

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

#### touch

Change file timestamps

```
$ ll a
-rw-r--r-- 1 user user 0 mar 30 14:29 a
$ touch a
$ ll a
-rw-r--r-- 1 user user 0 mar 30 15:03 a
```

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

#### which

Locate a command

```
$ which ls
/bin/ls
```

#### whatis

Display one-line manual page descriptions

```
$ whatis printf
printf (3)           - formatted output conversion
printf (1)           - format and print data
```

#### whereis

Locate the binary, source, and manual page files for a command

```
$ whereis ls
ls: /bin/ls /usr/share/man/man1/ls.1.gz
```

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

### Pathname expansion

- * - Matches  any  string, including the null string.
- ? - Matches any single character     <!-- .element: class="fragment" -->
- [] - Matches any one of the enclosed characters   <!-- .element: class="fragment" -->

++

```
$ ls
a  aa  ab  abc  ac  ad  ae  af
```
```
$ ls a*
a aa ab abc ac ad ae af
```
```
$ ls a?
aa ab ac ad ae af
```
```
$ ls a[b-e]
ab ac ad ae
```

Parameter expansion:
```
$ ls a{,b,c}
a ab ac
```

++

## sudo

Execute a command as another user

`$ sudo apt upgrade`
`$ sudo -u user ls /Users/user/`

## grep

Print lines matching a pattern

```
$ grep "line[12]" file.txt
line1
line2
line10
```

## find

Search for files in a directory hierarchy

#### Tests
- **-name** *pattern* - Base of file name (the path with the leading directories removed) matches shell pattern *pattern*.
- **-iname** *pattern* - Like **-name**, but the match is case insensitive
- **-type** *c* - File is of type c (*f* file, *d* directory, *l* link,...)
- **-path** *pattern* - File name matches shell pattern *pattern*
- **-ipath** *pattern* - Like **-path**, but the match is case insensitive.
- **-regex** *pattern* - File  name  matches  regular  expression  *pattern*
- **-iregex** *pattern* - Like **-regex**, but the match is case insensitive.

#### Actons
- **-delete**
- **-exec** *command {} ;*
- **-execdir** *command {} ;* - GNU only
- **-ok** *command {} ;*
- **-okdir** *command {} ;*
- **-printf** *format*

`$ find DDEX/ -type f -name "*.xml" ! -name "BatchComplete_*.xml" ! -path "*/acknowledgments/*" -exec grep -lE 'MessageSchemaVersionId="ern/3(7|8|81)"' {} \;`
`$ find . -type f -name ".DS_Store" -delte`

## seed

Stream editor for filtering and transforming text

```
$ echo "http://www.example.com/index.html" | sed 's_com/index_org/home_'
http://www.example.org/home.html
```

## awk

Pattern scanning and processing language

```
$ awk '/[13]0?$/ { printf "%s was matched!\n", $1; }' file.txt
line1 was matched!
line3 was matched!
line10 was matched!
```

## tar

An archiving utility

`$ tar --verbose --gzip --extract --file ~/Downloads/linux-4.10.7.tar.gz --directory /tmp/`
```
$ tar --verbose --bzip --create --file /tmp/archive.tar.bz ./file{1..10}.txt
./file1.txt
./file2.txt
./file3.txt
./file4.txt
./file5.txt
./file6.txt
./file7.txt
./file8.txt
./file9.txt
./file10.txt
```
