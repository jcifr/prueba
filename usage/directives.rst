Directives
==========

Lorem ipsum [#f1]_ dolor sit amet ... [#f2]_

Footnotes
_________

.. rubric:: Footnotes

.. [#f1] Text of the first footnote.
.. [#f2] Text of the second footnote.

note
____

.. note::

   This function is not suitable for sending spam e-mails.

warning
_______

.. warning::

   An important bit of information about an API that a user should be very aware of when using whatever bit of API the warning pertains to.
   The content of the directive should be written in complete sentences and include all appropriate punctuation.
   This differs from note in that it is recommended over note for information regarding security.

versionadded
____________

.. versionadded:: 2.5

   The *spam* parameter.

deprecated
__________

.. deprecated:: 3.1
   Use :func:`spam` instead.

seealso
_______

.. seealso::

   Module :py:mod:`zipfile`
      Documentation of the :py:mod:`zipfile` standard module.

   `GNU tar manual, Basic Tar Format <http://link>`_
      Documentation for tar archive files, including GNU tar extensions.

rubric
______
.. rubric:: title

hlist
_____

.. hlist::
   :columns: 3

   * A list of
   * short items
   * that should be
   * displayed
   * horizontally

glossary
________

.. glossary::

   environment
      A structure where information about all documents under the root is
      saved, and used for cross-referencing.  The environment is pickled
      after the parsing stage, so that successive runs only need to read
      and parse new and changed documents.

   source directory
      The directory which, including its subdirectories, contains all
      source files for one Sphinx project.

   Sphinx
      Sphinx is a tool that makes it easy to create intelligent and beautiful documentation.
      It was originally created for the Python documentation, and it has excellent facilities for the documentation of software projects in a range of languages.

   RST
      RST is an easy-to-read, what-you-see-is-what-you-get plain text markup syntax and parser system.
      It is useful for in-line program documentation (such as Python docstrings), for quickly creating simple web pages, and for standalone documents.
      RST is designed for extensibility for specific application domains. The RST parser is a component of Docutils.

   Sublime Text
      Sublime Text is a sophisticated text editor for code, markup and prose. You'll love the slick user interface, extraordinary features and amazing performance.

.. note::

   This function is not suitable for sending spam e-mails.

images
______

How to include images in project:

.. image:: images/im1.jpg
   :scale: 50 %
   :alt: alternate text
   :align: center

productionlist
______________


.. productionlist::
   try_stmt: try1_stmt | try2_stmt
   try1_stmt: "try" ":" `suite`
            : ("except" [`expression` ["," `target`]] ":" `suite`)+
            : ["else" ":" `suite`]
            : ["finally" ":" `suite`]
   try2_stmt: "try" ":" `suite`
            : "finally" ":" `suite`

DANGER
______

.. DANGER::
   Beware killer rabbits!

topic
_____

.. topic:: Topic Title

    Subsequent indented lines comprise
    the body of the topic, and are
    interpreted as body elements.

sidebar
_______


.. sidebar:: Sidebar Title
   :subtitle: Optional Sidebar Subtitle

   Subsequent indented lines comprise
   the body of the sidebar, and are
   interpreted as body elements.

compound
________

.. compound::

   The 'rm' command is very dangerous.  If you are logged
   in as root and enter ::

       cd /
       rm -rf *

   you will erase the entire contents of your file system.

container
_________

.. container:: custom

   This paragraph might be rendered in a custom way.

Parsing the above results in the following pseudo-XML:

<container classes="custom">
    <paragraph>
        This paragraph might be rendered in a custom way.

The "container" directive is the equivalent of HTML's <div> element.
It may be used to group a sequence of elements for user- or application-specific purposes.

code-block
__________

.. code-block:: python
   :emphasize-lines: 3,5

   def some_function():
       interesting = False
       print 'This line is highlighted.'
       print 'This one is not...'
       print '...but this one is.'

literalinclude
______________

.. literalinclude:: codpyhon.py
   :language: python
   :emphasize-lines: 4,12,15-18
   :linenos:

code-block1
___________

.. code-block:: python
   :caption: this.py
   :name: this-py

   print 'Explicit is better than implicit.'

abbr
____

:abbr:`LIFO (last-in, first-out)`.

menuselection
_____________

:menuselection:`Start --> Programs`

function
________

The most prominent domain is the Python domain. For example, to document Python’s built-in function enumerate(),
you would add this to one of your source files:

.. function:: enumerate(sequence[, start=0])

   Return an iterator that yields tuples of an index and an item of the
   *sequence*. (And so on.)

class y method
______________

.. py:class:: Foo

   .. py:method:: quux()

-- or --

.. py:class:: Bar

.. py:method:: Bar.quux()

Another function:

.. py:function:: send_message(sender, recipient, message_body, [priority=1])

   Send a message to a recipient

   :param str sender: The person sending the message
   :param str recipient: The recipient of the message
   :param str message_body: The body of the message
   :param priority: The priority of the message, can be a number 1-5
   :type priority: integer or None
   :return: the message id
   :rtype: int
   :raises ValueError: if the message_body exceeds 160 characters
   :raises TypeError: if the message_body is not a basestring

.. py:function:: compile(source : string, filename, symbol='file') -> ast object

seealso
_______

.. seealso::

         Module :py:mod:`zipfile`
            Documentation of the :py:mod:`zipfile` standard module.

         `GNU tar manual, Basic Tar Format <http://link>`_
            Documentation for tar archive files, including GNU tar extensions.

      .. seealso:: modules :py:mod:`zipfile`, :py:mod:`tarfile`

   .. versionadded:: 0.5
      The short form.

sectionauthor
_____________

.. rst:directive:: .. sectionauthor:: name <email>

   Identifies the author of the current section.  The argument should include
   the author's name such that it can be used for presentation and email
   address.  The domain name portion of the address should be lower case.
   Example::

      .. sectionauthor:: Guido van Rossum <guido@python.org>

   By default, this markup isn't reflected in the output in any way (it helps
   keep track of contributions), but you can set the configuration value
   :confval:`show_authors` to ``True`` to make them produce a paragraph in the
   output.

currentmodule
_____________

.. currentmodule:: sphinx














