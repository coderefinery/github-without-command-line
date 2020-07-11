sphinx-lesson template
======================

In this lesson, we learn how to make a CodeRefinery lesson using
sphinx.  It is designed to replace the Jekyll-based software carepntry
templates.  The source is on `github
<https://github.com/coderefinery/sphinx-test-lesson>`__.

An expanded explination of *why* this lesson is useful can go here.

.. prereq:: Required software

   Here, you should list the software requirements

   * [Jupyter](https://coderefinery.github.io/installation/jupyter/)


The following directives are implemented:

* ``callout``
* ``challenge``
* ``checklist``
* ``discussion``
* ``keypoints``
* ``objectives``
* ``prereq``
* ``solution``
* ``testimonial``

All that remains is some proper CSS

.. toctree::
   :maxdepth: 2
   :caption: Episodes

   01_intro
   01_intro_md
   02_rst_tests
   03_md_tests
   04_executing
   05_jupyter

.. toctree::
   :caption: Other material

   cheatsheet
   guide

Installation and usage
----------------------

This is a normal Sphinx project, with one extension,
``sphinx_lesson``, which is installed as normal via pip (note: not yet
on PyPI, will be later if there is update).

Then, enable the extension in your Sphinx ``conf.py``.  This will both
define our special directives, and load the other required extensions
(``myst_nb``).  The ``myst_nb`` extension, which can execute notebook
files and code, can be configured `normally
<https://myst-nb.readthedocs.io/en/latest/>`__.  Setting the
extension::

  extensions = [
      'sphinx_lesson',
  ]

We are in theory compatible with any theme, but are most tested with
the sphinx_rtd_theme::

  html_theme = 'sphinx_rtd_theme'



* :ref:`genindex`
* :ref:`search`
