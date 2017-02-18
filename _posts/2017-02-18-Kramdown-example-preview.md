---
layout:     post
title:      "Kramdown example preview"
date:       2017-02-18 19:41:00+0800
categories: [stuff]
tags:       [kramdown, markdown]
---
* * *

This \`is not a code\` span!

* * *

First level header
==================

Second level header
------

   Other first level header
=

* * *

This is a normal
paragraph.

And A Header
------------
And a paragraph

> This is a blockquote.

And A Header
------------

* * *

header
---
para

* * *

# First level header

### Third level header    ###

## Second level header ######

* * *

Hello        {#id}
-----

# Hello      {#id}

# Hello #    {#id}

* * *

> This is a blockquote.
>     on multiple lines
that may be lazy.
>
> This is the second paragraph.

* * *

> This is a paragraph.
>
> > A nested blockquote.
>
> ## Headers work
>
> * lists too
>
> and all other block-level elements

* * *

> A code block:
>
>     ruby -e 'puts :works'

* * *

> This is a paragraph inside
a blockquote.
>
> > This is a nested paragraph
that continues here
> and here
> > and here

* * *

    Here comes some code

    This text belongs to the same code block.

* * *

    Here comes some code
^
    This one is separate.

* * *

~~~~~~~~
Here comes some code.
~~~~~~~~

* * *

~~~
def what?
  42
end
~~~
{: .language-ruby}

* * *

~~~ ruby
def what?
  42
end
~~~

* * *

* kram
+ down
- now

1. kram
2. down
3. now

* * *

* This is the first line. Since the first non-space characters appears in
  column 3, all other indented lines have to be indented 2 spaces.
However, one could be lazy and not indent a line but this is not
recommended.
*       This is the another item of the list. It uses a different number
   of spaces for indentation which is okay but should generally be avoided.
   * The list item marker is indented 3 spaces which is allowed but should
     also be avoided and starts the third list item. Note that the lazy
     line in the second list item may make you believe that this is a
     sub-list which it isn't! So avoid being lazy!

* * *

* This is the first list item bla blabla blabla blabla blabla blabla
  blabla blabla blabla blabla blabla blabla blabla blabla blabla blabla
  blabla blabla blabla bla
* This is the another item of the list. bla blabla blabla blabla blabla
  blabla blabla blabla blabla blabla blabla blabla blabla blabla blabla

* * *

* list 1 item 1
 * list 1 item 2 (indent 1 space)
  * list 1 item 3 (indent 2 spaces)
   * list 1 item 4  (indent 3 spaces)
    * lazy text belonging to above item 4

* * *

1. list 1 item 1
 2. list 1 item 2 (indent 1 space)
  3. list 1 item 3 (indent 2 spaces)
   4. list 1 item 4  (indent 3 spaces)
    5. lazy text belonging to above item 4

* * *

* list 1 item 1
  * nested list item 1
  * nested list item 2
* list 1 item 2
  * nested list item 1

* * *

1. list 1 item 1
   1. nested list item 1
   2. nested list item 2
10. list 1 item 2
    1. nested list item 1

* * *

1. text for this list item
   further text (indent 3 spaces)

10. text for this list item
    further text (indent 4 spaces)

* * *

*   Using a tab to indent this line, the tab only counts as three spaces
    and therefore the overall indentation is four spaces.

   1.   The tab after the marker counts here as three spaces. Since the
        indentation of the marker is three spaces and the marker itself
        takes two characters, the overall indentation needed for the
        following lines is eight spaces or two tabs.

* * *

* kram

* down
* now

* * *

* Not wrapped in a paragraph
* Wrapped in a paragraph due to the following blank line.

* Also wrapped in a paragraph due to the
  following blank line and the EOB marker.

^

* * *

* First list item

* Second list item

* Last list item

* * *

*   First item

    A second paragraph

    * nested list

    > blockquote

*   Second item

* * *

*   This is a list item.

    The second para of the list item.
^
    A code block following the list item.

* * *

* List one
^
* List two

* * *

*   This is just text.
    * this is a sub list item
      * this is a sub sub list item
* This is just text,
    spanning two lines
  * this is a nested list item.

* * *

1984\. It was great
\- others say that, too!

* * *

* {:.cls} This item has the class "cls".
  Here continues the above paragraph.

* This is a normal list item.

* * *

kramdown
: A Markdown-superset converter

Maruku
:     Another Markdown-superset converter

* * *

definition term 1
definition term 2
: This is the first line. Since the first non-space characters appears in
column 3, all other lines have to be indented 2 spaces (or lazy syntax may
  be used after an indented line). This tells kramdown that the lines
  belong to the definition.
:       This is the another definition for the same term. It uses a
        different number of spaces for indentation which is okay but
        should generally be avoided.
   : The definition marker is indented 3 spaces which is allowed but
     should also be avoided.

* * *

definition term
: This definition will just be text because it would normally be a
  paragraph and the there is no preceding blank line.

  > although the definition contains other block-level elements

: This definition *will* be a paragraph since it is preceded by a
  blank line.

* * *

{:#term} Term with id="term"
: {:.cls} Definition with class "cls"

{:#term1} First term
{:#term2} Second term
: {:.cls} Definition

* * *

| First cell|Second cell|Third cell
| First | Second | Third |

First | Second | | Fourth |

* * *

|----+----|
+----|----+
|---------|
|-
| :-----: |
-|-

* * *

|---+---+---|
+ :-: |:------| ---:|
| :-: :- -: -
:-: | :-

* * *

|====+====|
+====|====+
|=========|
|=

* * *

|-----------------+------------+-----------------+----------------|
| Default aligned |Left aligned| Center aligned  | Right aligned  |
|-----------------|:-----------|:---------------:|---------------:|
| First body part |Second cell | Third cell      | fourth cell    |
| Second line     |foo         | **strong**      | baz            |
| Third line      |quux        | baz             | bar            |
|-----------------+------------+-----------------+----------------|
| Second body     |            |                 |                |
| 2 line          |            |                 |                |
|=================+============+=================+================|
| Footer row      |            |                 |                |
|-----------------+------------+-----------------+----------------|

* * *

|---
| Default aligned | Left aligned | Center aligned | Right aligned
|-|:-|:-:|-:
| First body part | Second cell | Third cell | fourth cell
| Second line |foo | **strong** | baz
| Third line |quux | baz | bar
|---
| Second body
| 2 line
|===
| Footer row

* * *

---

  _  _  _  _

---------------

* * *

$$
\begin{align*}
  & \phi(x,y) = \phi \left(\sum_{i=1}^n x_ie_i, \sum_{j=1}^n y_je_j \right)
  = \sum_{i=1}^n \sum_{j=1}^n x_i y_j \phi(e_i, e_j) = \\
  & (x_1, \ldots, x_n) \left( \begin{array}{ccc}
      \phi(e_1, e_1) & \cdots & \phi(e_1, e_n) \\
      \vdots & \ddots & \vdots \\
      \phi(e_n, e_1) & \cdots & \phi(e_n, e_n)
    \end{array} \right)
  \left( \begin{array}{c}
      y_1 \\
      \vdots \\
      y_n
    \end{array} \right)
\end{align*}
$$

* * *

The following is a math block:

$$ 5 + 5 $$

But next comes a paragraph with an inline math statement:

\$$ 5 + 5 $$

* * *

\$\$ 5 + 5 $$

* * *

This is a para.
<div>
Something in here.
</div>
Other para.

* * *

<p>This is a para.</p>
<div>
Something in here.
</div>
<p>Other para.</p>

* * *

<div id="content"><div id="layers"><div id="layer1">
This is some text in the `layer1` div.
</div>
This is some text in the `layers` div.
</div></div>
This is a para outside the HTML block.

* * *

<div markdown="1">This is the first part of a para,
which is continued here.
</div>

<p markdown="1">This works without problems because it is parsed as
span-level elements</p>

<div markdown="1">The end tag is not found because
this line is parsed as a paragraph</div>

* * *

This is a para.
<div markdown="1">
Another para.
</p>

* * *

<p>This is a para.</p>
<div>
  <p>Another para.</p>
</div>

* * *

This is a para.
<!-- a *comment* -->
<? a processing `instruction`
   spanning multiple lines
?> First part of para,
continues here.

* * *

Information can be found on the <http://example.com> homepage.
You can also mail me: <me.example@example.com>

* * *

This is [a link](http://rubyforge.org) to a page.
A [link](../test "local URI") can also have a title.
And [spaces](link with spaces.html)!

* * *

This is a [link](http://example.com){:hreflang="de"}

* * *

This is a [reference style link][linkid] to a page. And [this]
[linkid] is also a link. As is [this][] and [THIS].

* * *

[linkid]: http://www.example.com/ "Optional Title"

* * *

The next paragraph contains a link and some text.

[Room 100]\: There you should find everything you need!

[Room 100]: link_to_room_100.html

* * *

[linkid]: http://example.com
{:hreflang="de"}

* * *

Here comes a ![smiley](../images/smiley.png)! And here
![too](../images/other.png 'Title text'). Or ![here].
With empty alt text ![](see.jpg)

* * *

Here is an inline ![smiley](smiley.png){:height="36px" width="36px"}.

And here is a referenced ![smile]

[smile]: smile.png
{: height="36px" width="36px"}

* * *

*some text*
_some text_
**some text**
__some text__

* * *

This is un*believe*able! This d_oe_s not work!

* * *

This is a ***text with light and strong emphasis***.
This **is _emphasized_ as well**.
This *does _not_ work*.
This **does __not__ work either**.

* * *

This is a * literal asterisk.
These are ** two literal asterisk.
As \*are\* these!

* * *

Use `<html>` tags for this.

* * *

Here is a literal `` ` `` backtick.
And here is ``  `some`  `` text (note the two spaces so that one is left
in the output!).

* * *

This is a ` literal backtick.
As \`are\` these!

* * *

This is a Ruby code fragment `x = Class.new`{:.language-ruby}

* * *

<p>This is .</p>

<p>This <span>is automatically closed.</span></p>

* * *

Link: <a href="some
link">text</a>

* * *

<p>Link: <a href="some link">text</a></p>

* * *

This is some text.[^1]. Other text.[^footnote].

* * *

[^1]: Some *crazy* footnote definition.

[^footnote]:
    > Blockquotes can be in a footnote.

        as well as code blocks

    or, naturally, simple paragraphs.

[^other-note]:       no code block here (spaces are stripped away)

[^codeblock-note]:
        this is now a code block (8 spaces indentation)

* * *

This is some text not written in HTML but in another language!

*[another language]: It's called Markdown

*[HTML]: HyperTextMarkupLanguage
{:.mega-big}

* * *

* list item one

* list item two

* * *

* list one
^
* list two

* * *

{:ref-name: #myid .my-class}
{:other: ref-name #id-of-other title="hallo you"}
{:test: key="value \" with quote" and other='quote brace \}'}

* * *

{:id: .cls1 .cls2}
{:id: class="cls1" .cls2}
{:id: class="something" class="cls1" .cls2}
{:id: class="cls1 cls2"}

* * *

A simple paragraph with an ID attribute.
{: #para-one}

> A blockquote with a title
{:title="The blockquote title"}
{: #myid}

{:.ruby}
    Some code here

* * *

This *is*{:.underline} some `code`{:#id}{:.class}.
A [link](test.html){:rel='something'} and some **tools**{:.tools}.

* * *

This *is italic*{::}*marked*{:.special} text

* * *

{::comment}
This text is completely ignored by kramdown - a comment in the text.
{:/comment}

Do you see {::comment}this text{:/comment}?
{::comment}some other comment{:/}

{::options key="val" /}

* * *
