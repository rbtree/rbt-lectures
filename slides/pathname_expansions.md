### Pathname expansion

- * - Matches  any  string, including the null string.
- ? - Matches any single character     <!-- .element: class="fragment" -->
- [] - Matches any one of the enclosed characters   <!-- .element: class="fragment" -->

+++

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

+++

Parameter expansion:
```
$ ls a{,b,c}
a ab ac
```
