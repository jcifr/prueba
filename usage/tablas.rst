=================
This is a tables
=================

Tables
================================

Tables 1
__________


H4 -- Subsubsection
+++++++++++++++++++


.. table:: Truth table for "not"
   :widths: auto

   =====  =====
     A    not A
   =====  =====
   False  True
   True   False
   =====  =====


+------------------------+------------+----------+----------+
| Header row, column 1   | Header 2   | Header 3 | Header 4 |
| (header rows optional) |            |          |          |
+========================+============+==========+==========+
| body row 1, column 1   | column 2   | column 3 | column 4 |
+------------------------+------------+----------+----------+
| body row 2             | ...        | ...      |          |
+------------------------+------------+----------+----------+

The tables are as seen

=====  =====  =======
A      B      A and B
=====  =====  =======
False  False  False
True   False  False
False  True   False
True   True   True
=====  =====  =======

Use `Link text <https://domain.invalid/>`_ for inline web links. If the link text should be the web address, you don’t need special markup at all, the parser finds links and mail addresses in ordinary text.

This is a paragraph that contains `a link`_.

.. _a link: https://domain.invalid/

The handling of the :: marker is smart:

If it occurs as a paragraph of its own, that paragraph is completely left out of the document.
If it is preceded by whitespace, the marker is removed.
If it is preceded by non-whitespace, the marker is replaced by a single colon.
That way, the second sentence in the above example’s first paragraph would be rendered as “The next paragraph is a code sample:”.

Doctest blocks
================================

>>> 1 + 1
2

Definition lists
================================

term (up to a line of text)
   Definition of the term, which must be indented

   and can even consist of multiple paragraphs

next term
   Description.

Broken lines
=============

| These lines are
| broken exactly like in
| the source file.