Directives
==========

.. note::

   This function is not suitable for sending spam e-mails.

.. warning::

   An important bit of information about an API that a user should be very aware of when using whatever bit of API the warning pertains to.
   The content of the directive should be written in complete sentences and include all appropriate punctuation.
   This differs from note in that it is recommended over note for information regarding security.

.. versionadded:: 2.5

   The *spam* parameter.

.. deprecated:: 3.1
   Use :func:`spam` instead.

.. seealso::

   Module :py:mod:`zipfile`
      Documentation of the :py:mod:`zipfile` standard module.

   `GNU tar manual, Basic Tar Format <http://link>`_
      Documentation for tar archive files, including GNU tar extensions.

.. rubric:: title

.. hlist::
   :columns: 3

   * A list of
   * short items
   * that should be
   * displayed
   * horizontally

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

How to include images in project:

.. image:: images/im1.jpg
   :scale: 50 %
   :alt: alternate text
   :align: center

.. productionlist::
   try_stmt: try1_stmt | try2_stmt
   try1_stmt: "try" ":" `suite`
            : ("except" [`expression` ["," `target`]] ":" `suite`)+
            : ["else" ":" `suite`]
            : ["finally" ":" `suite`]
   try2_stmt: "try" ":" `suite`
            : "finally" ":" `suite`

.. DANGER::
   Beware killer rabbits!

.. topic:: Topic Title

    Subsequent indented lines comprise
    the body of the topic, and are
    interpreted as body elements.

.. sidebar:: Sidebar Title
   :subtitle: Optional Sidebar Subtitle

   Subsequent indented lines comprise
   the body of the sidebar, and are
   interpreted as body elements.

.. compound::

   The 'rm' command is very dangerous.  If you are logged
   in as root and enter ::

       cd /
       rm -rf *

   you will erase the entire contents of your file system.

.. container:: custom

   This paragraph might be rendered in a custom way.

Parsing the above results in the following pseudo-XML:

<container classes="custom">
    <paragraph>
        This paragraph might be rendered in a custom way.

The "container" directive is the equivalent of HTML's <div> element.
It may be used to group a sequence of elements for user- or application-specific purposes.





