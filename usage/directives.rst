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

.. note::

   This function is not suitable for sending spam e-mails.

.. productionlist::
   try_stmt: try1_stmt | try2_stmt
   try1_stmt: "try" ":" `suite`
            : ("except" [`expression` ["," `target`]] ":" `suite`)+
            : ["else" ":" `suite`]
            : ["finally" ":" `suite`]
   try2_stmt: "try" ":" `suite`
            : "finally" ":" `suite`

