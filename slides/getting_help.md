### Getting help

- man
- apropos     <!-- .element: class="fragment" -->
- help        <!-- .element: class="fragment" -->
- info        <!-- .element: class="fragment" -->
- google.com  <!-- .element: class="fragment" -->

+++

#### man

System's manual pager

<table>
  <tr>
    <td>**man** [*section*] *page*</td>
    <td>Display the manual page for the item *page*</td>
  <tr>
  <tr>
    <td>**man -k** *regexp*</td>
    <td>Search the short descriptions and manual page names for the keyword as regular expression</td>
  </tr>
</table>

+++

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

+++

#### apropos

Search the manual page names and descriptions

**apropos** *regexp* [**--and** *regexp*]

#### help

Display information about built-in commands.

**help** *command*

#### info

GNU replacement for man pages.
