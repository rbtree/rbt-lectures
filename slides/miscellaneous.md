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
