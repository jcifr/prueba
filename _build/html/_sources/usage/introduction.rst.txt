.. Introduction:

Introduction
============

This section is a brief introduction to reStructuredText (reST) concepts and
syntax, intended to provide authors with enough information to author documents
productively.  Since reST was designed to be a simple, unobtrusive markup
language, this will not take too long.


.. Paragraphs:

Paragraphs
__________

The paragraph is the most basic block in a reST document.
Paragraphs are simply chunks of text separated by one or more blank lines.
As in Python, indentation is significant in reST,
so all lines of the same paragraph must be left-aligned to the same level of indentation.

Inline markup
_____________

The standard reST inline markup is quite simple: use

* one asterisk: *text* for emphasis (italics),
* two asterisks: **text** for strong emphasis (boldface), and
* backquotes: ``text`` for code samples.

If asterisks or backquotes appear in running text and could be confused with inline markup delimiters,
they have to be escaped with a backslash.

Be aware of some restrictions of this markup:

* it may not be nested,
* content may not start or end with whitespace: * text* is wrong,
* it must be separated from surrounding text by non-word characters.
  Use a backslash escaped space to work around that: thisis\ *one*\ word.

These restrictions may be lifted in future versions of the docutils.

reST also allows for custom “interpreted text roles”,
which signify that the enclosed text should be interpreted in a specific way.
Sphinx uses this to provide semantic markup and cross-referencing of identifiers,
as described in the appropriate section.
The general syntax is ``:rolename:`content``.`

Standard reST provides the following roles:

* emphasis – alternate spelling for *emphasis*
* strong – alternate spelling for **strong**
* literal – alternate spelling for ``literal``
* subscript – subscript text
* superscript – superscript text
* title-reference – for titles of books, periodicals, and other materials

Lists and Quote-like blocks
___________________________

List markup is natural:
just place an asterisk at the start of a paragraph and indent properly.
The same goes for numbered lists; they can also be autonumbered using a # sign:

* This is a bulleted list.
* It has two items, the second
  item uses two lines.

1. This is a numbered list.
2. It has two items too.

#. This is a numbered list.
#. It has two items too.

Nested lists are possible,
but be aware that they must be separated from the parent list items by blank lines:

* this is
* a list

  * with a nested list
  * and some subitems

* and here the parent list continues

Definition lists are created as follows:

term (up to a line of text)
   Definition of the term, which must be indented

   and can even consist of multiple paragraphs

next term
   Description.

Note that the term cannot have more than one line of text.

Quoted paragraphs are created by just indenting them more than the surrounding paragraphs.

Line blocks are a way of preserving line breaks:

| These lines are
| broken exactly like in
| the source file.


There are also several more special blocks available:

* field lists
* option lists
* quoted literal blocks
* doctest blocks

Source Code
___________


Literal code blocks (ref) are introduced by ending a paragraph with the special marker ::.
The literal block must be indented (and, like all paragraphs, separated from the surrounding ones by blank lines):

This is a normal text paragraph. The next paragraph is a code sample::

   It is not processed in any way, except
   that the indentation is removed.

   It can span multiple lines.

This is a normal text paragraph again.

The handling of the :: marker is smart:

* If it occurs as a paragraph of its own, that paragraph is completely left out of the document.
* If it is preceded by whitespace, the marker is removed.
* If it is preceded by non-whitespace, the marker is replaced by a single colon.

That way, the second sentence in the above example’s first paragraph would be rendered as “The next paragraph is a code sample:”.

Tables
______

Two forms of tables are supported.
For grid tables , you have to “paint” the cell grid yourself. They look like this:

+------------------------+------------+----------+----------+
| Header row, column 1   | Header 2   | Header 3 | Header 4 |
| (header rows optional) |            |          |          |
+========================+============+==========+==========+
| body row 1, column 1   | column 2   | column 3 | column 4 |
+------------------------+------------+----------+----------+
| body row 2             | ...        | ...      |          |
+------------------------+------------+----------+----------+

Simple tables (ref) are easier to write, but limited: they must contain more than one row, and the first column cannot contain multiple lines.
They look like this:

=====  =====  =======
A      B      A and B
=====  =====  =======
False  False  False
True   False  False
False  True   False
True   True   True
=====  =====  =======

Hyperlinks
__________

External links
++++++++++++++

Use `Link text <http://example.com/>`_ for inline web links.
If the link text should be the web address, you don’t need special markup at all, the parser finds links and mail addresses in ordinary text.

You can also separate the link and the target definition, like this:

This is a paragraph that contains `a link`_.

.. _a link: http://example.com/

Internal links
++++++++++++++

Internal linking is done via a special reST role provided by Sphinx, see the section on specific markup, Cross-referencing arbitrary locations.

Sections
________

Section headers are created by underlining (and optionally overlining) the section title with a punctuation character,
at least as long as the text:

Normally, there are no heading levels assigned to certain characters as the structure is determined from the succession of headings.
However, this convention is used in Python’s Style Guide for documenting which you may follow:

* # with overline, for parts
* * with overline, for chapters
* =, for sections
* -, for subsections
* ^, for subsubsections
* ", for paragraphs

Of course, you are free to use your own marker characters (see the reST documentation), and use a deeper nesting level,
but keep in mind that most target formats (HTML, LaTeX) have a limited supported nesting depth.

Citations
_________

Standard reST citations are supported, with the additional feature that they are “global”, i.e. all citations can be referenced from all files. Use them like so:

Lorem ipsum [Ref]_ dolor sit amet.

.. [Ref] Book or article reference, URL or whatever.

Citation usage is similar to footnote usage, but with a label that is not numeric or begins with #

Comments
________

Every explicit markup block which isn’t a valid markup construct (like the footnotes above) is regarded as a comment. For example:

.. This is a comment.

You can indent text after a comment start to form multiline comments:

..
   This whole indented block
   is a comment.

   Still in the comment.

Source encoding
_______________

Since the easiest way to include special characters like em dashes or copyright signs in reST is to directly write them as Unicode characters,
one has to specify an encoding. Sphinx assumes source files to be encoded in UTF-8 by default;
you can change this with the source_encoding config value.



Section to cross-reference
==========================

This is the text of the section.

.. las secciones van subrayadas. Esto es un comentario

.. It refers to the section itself, see For more details, see Paragraphs_.

.. los capitulos van subrayadas. Esto es un comentario

It refers to the section itself, see For more details, see :ref:`Introduction`.

Link to another :ref:`Inline markup`.

Link to another :ref:`The same<Inline markup>` at the same Inline markup.

Link to :ref:`Images`.

Link to :ref:`Figures`.





