---
tags:
- random
---

### Features

Document contained examples of [GFM spec](https://github.github.com/gfm/#overview)

## Thematic breaks

[A line consisting of 0-3 spaces of indentation, followed by a sequence of three or more matching -, _, or * characters, each followed optionally by any number of spaces or tabs, forms a thematic break.](https://github.github.com/gfm/#example-13)


```
***
```
***

```
---
```
---

```
___
```
___

[Wrong charactes](https://github.github.com/gfm/#example-14)

```
+++
```
+++

```
===
```
===

[Not enough characters](https://github.github.com/gfm/#example-16)

```
**
```
**

```
--
```
--

```
__
```
__

[One to three spaces indent are allowed](https://github.github.com/gfm/#example-17)

```
 ***
```
 ***

```
  ***
```
  ***

```
   ***
```
   ***

[Four spaces is too many](https://github.github.com/gfm/#example-18)

```
    ****
```
    ****

[More than three characters may be used](https://github.github.com/gfm/#example-20)

```
********
```
********

[Spaces are allowed between the characters and at the end](https://github.github.com/gfm/#example-21)

```
 - - -
```
 - - -

```
 ** *   ** *
```
 ** *   ** *

```
_ _ _   
```
_ _ _   

[Evene more then 4 spaces between](https://github.github.com/gfm/#example-23)

```
-    -    - -
```
-    -    - -
 
[No other characters may occur in the line](https://github.github.com/gfm/#example-25)

```
_ _ _ _ a
```
_ _ _ _ a

```
a------
```
a------

```
---a---
```
---a---

[It is required that all of the non-whitespace characters be the same](https://github.github.com/gfm/#example-26)

```
 *-*
```
 *-*

[When both a thematic break and a list item are possible interpretations of a line, the thematic break takes precedence](https://github.github.com/gfm/#example-30)

```
* Foo
* * *
* Bar
```
* Foo
* * *
* Bar

[If you want a thematic break in a list item, use a different bullet](https://github.github.com/gfm/#example-31)

```
- Foo
- * * *
```
- Foo
- * * *

## Headings

[Simple headings](https://github.github.com/gfm/#example-32)

```
# foo
## foo
### foo
#### foo
##### foo
###### foo
```
# foo
## foo
### foo
#### foo
##### foo
###### foo

[More than six # characters is not a heading](https://github.github.com/gfm/#example-33)

```
####### foo
```
####### foo

[At least one space is required between the # characters and the heading’s contents](https://github.github.com/gfm/#example-34)

```
#not heading
```
#not heading

[Not a heading, because the first # is escaped](https://github.github.com/gfm/#example-35)

```
\## not heading
```
\## not heading

[Contents are parsed as inlines](https://github.github.com/gfm/#example-36)

```
# foo *bar* \*baz\*
```
# foo *bar* \*baz\*

[Leading and trailing whitespace is ignored in parsing inline content](https://github.github.com/gfm/#example-37)

```
#                  foo                     
```
#                  foo                     

[One to three spaces indentation are allowed](https://github.github.com/gfm/#example-38)

```
 ### foo
  ## foo
   # foo
```
 ### foo
  ## foo
   # foo

[Four spaces are too much](https://github.github.com/gfm/#example-39)

```
    # foo
```
    # foo

[A closing sequence of # characters is optional](https://github.github.com/gfm/#example-41)

```
## foo ##
  ###   bar    ###
```
## foo ##
  ###   bar    ###

[It need not be the same length as the opening sequence](https://github.github.com/gfm/#example-42)

```
# foo ##################################
##### foo ##
```
# foo ##################################
##### foo ##

[Spaces are allowed after the closing sequence](https://github.github.com/gfm/#example-43)

```
### foo ###     
```
### foo ###     

[A sequence of # characters with anything but spaces following it is not a closing sequence, but counts as part of the contents of the heading](https://github.github.com/gfm/#example-44)

```
### foo ### b
```
### foo ### b

[The closing sequence must be preceded by a space](https://github.github.com/gfm/#example-45)

```
# foo#
```
# foo#

[Backslash-escaped # characters do not count as part of the closing sequence](https://github.github.com/gfm/#example-46)

```
### foo \###
## foo #\##
# foo \#
```
### foo \###
## foo #\##
# foo \#

## Setext headings

[Simple examples](https://github.github.com/gfm/#example-50)

```
Foo *bar*
=========
```
Foo *bar*
=========

```
Foo *bar*
---------
```
Foo *bar*
---------

[The content of the header may span more than one line](https://github.github.com/gfm/#example-51)

```
  Foo *bar
baz*→
====
```
  Foo *bar
baz*→
====

[The underlining can be any length](https://github.github.com/gfm/#example-53)

```
Foo
-------------------------
```
Foo
-------------------------

```
Foo
=
```
Foo
=

[The heading content can be indented up to three spaces, and need not line up with the underlining](https://github.github.com/gfm/#example-54)

```
   Foo
---
```
   Foo
---

```
  Foo
-----
```
  Foo
-----

```
  Foo
  ===
```
  Foo
  ===

[The setext heading underline cannot contain internal spaces](https://github.github.com/gfm/#example-58)

```
Foo
= =
```
Foo
= =

[A blank line is needed between a paragraph and a following setext heading, since otherwise the paragraph becomes part of the heading’s content](https://github.github.com/gfm/#example-65)

```
Foo
Bar
---
```
Foo
Bar
---

[Blank line is not required before or after setext headings](https://github.github.com/gfm/#example-66)

```
---
Foo
---
Bar
---
Baz
```
---
Foo
---
Bar
---
Baz

[Setext headings cannot be empty](https://github.github.com/gfm/#example-67)

```

====
```

====


## Indented code blocks 

[Simple example](https://github.github.com/gfm/#example-77)

```
    a simple
      indented code block
```
    a simple
      indented code block

[The contents of a code block are literal text, and do not get parsed as Markdown](https://github.github.com/gfm/#example-80)

```
    <a/
    *hi*

    - one
```
    <a/
    *hi*

    - one

## Fenced code blocks 

[Simple example](https://github.github.com/gfm/#example-89)

~~~
```
<
 
```
~~~
```
<
 
```

```
~~~
<
 
~~~
```
~~~
<
 
~~~

## Link reference definitions
[Spec](https://github.github.com/gfm/#link-reference-definition)

```
[foo1]: /url "title"

[foo1]
```
[foo1]: /url "title"

[foo1]

```
   [foo2]: 
      /url  
           'the title'  

[foo2]
```
   [foo2]: 
      /url  
           'the title'  

[foo2]

```
[Foo3*bar\]]:my_(url) 'title (with parens)'

[Foo3*bar\]]
```
[Foo3*bar\]]:my_(url) 'title (with parens)'

[Foo3*bar\]]

```
[Foo4 bar]:
<my url
'title'

[Foo4 bar]
```
[Foo4 bar]:
<my url
'title'

[Foo4 bar]

```
[foo5]: /url '
title
line1
line2
'

[foo5]
```
[foo5]: /url '
title
line1
line2
'

[foo5]

[The title may be omitted](https://github.github.com/gfm/#example-167)

```
[foo6]:
/url

[foo6]
```
[foo6]:
/url

[foo6]

## Paragraphs

[Simpl example](https://github.github.com/gfm/#example-189)

```
aaa

bbb
```
aaa

bbb

[Paragraphs can contain multiple lines, but no blank lines](https://github.github.com/gfm/#example-190)

```
aaa
bbb

ccc
ddd
```
aaa
bbb

ccc
ddd

[Multiple blank lines between paragraph have no effect](https://github.github.com/gfm/#example-191)

```
aaa


bbb
```
aaa


bbb

[Leading spaces are skipped](https://github.github.com/gfm/#example-192)

```
  aaa
 bbb
```
  aaa
 bbb

[Lines after the first may be indented any amount, since indented code blocks cannot interrupt paragraphs](https://github.github.com/gfm/#example-193)

```
aaa
             bbb
                                       ccc
```
aaa
             bbb
                                       ccc

[Final spaces are stripped before inline parsing, so a paragraph that ends with two or more spaces will not end with a hard line break](https://github.github.com/gfm/#example-196)

```
aaa     
bbb     
```
aaa     
bbb     

## Tables(GFM extension)

[Simple example](https://github.github.com/gfm/#example-198)

```
| footable | bartable |
| -------- | -------- |
| baztable | bimtable |
```
| footable | bartable |
| -------- | -------- |
| baztable | bimtable |


[Cells in one column don’t need to match length, though it’s easier to read if they are. Likewise, use of leading and trailing pipes may be inconsistent](https://github.github.com/gfm/#example-199)

```
| abc | defghi |
:-: | -----------:
bartable | baztable
```
| abc | defghi |
:-: | -----------:
bartable | baztable

[Include a pipe in a cell’s content by escaping it, including inside other inline spans](https://github.github.com/gfm/#example-200)

```
| f\|oo  |
| ------ |
| b `\|` az |
| b **\|** im |
```
| f\|oo  |
| ------ |
| b `\|` az |
| b **\|** im |

[The table is broken at the first empty line, or beginning of another block-level structure](https://github.github.com/gfm/#example-201)

```
| abc | def |
| --- | --- |
| bartable | baztable |
> bartable
```
| abc | def |
| --- | --- |
| bartable | baztable |
> bartable

[The header row must match the delimiter row in the number of cells. If not, a table will not be recognized](https://github.github.com/gfm/#example-203)

```
| abc | def |
| --- |
| bartable |
```
| abc | def |
| --- |
| bartable |

[The remainder of the table’s rows may vary in the number of cells. If there are a number of cells fewer than the number of cells in the header row, empty cells are inserted. If there are greater, the excess is ignored](https://github.github.com/gfm/#example-204)

```
| abc | def |
| --- | --- |
| bartable |
| bartable | baztable | bootable |
```
| abc | def |
| --- | --- |
| bartable |
| bartable | baztable | bootable |

[If there are no rows in the body, no <tbody> is generated in HTML output](https://github.github.com/gfm/#example-205)

```
| abc | def |
| --- | --- |
```
| abc | def |
| --- | --- |
