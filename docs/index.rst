|Build status| |Documentation Status|

newslynx-sc-rss
===============

Installation
------------

Production
~~~~~~~~~~

To install ``newslynx-sc-rss`` for an active installation of
``newslynx-core``, clone it and copy into ``~/.newslynx/sous-chefs``

.. code:: bash

    $ git clone https://github.com/newslynx/newslynx-sc-rss.git
    $ mv newslynx-sc-rss/ ~/.newslynx/sous-chefs/

Now install it within the same virtual environment as ``newslynx``:

.. code:: bash

    $ cd ~/.newslynx/sous-chefs/newslynx-sc-rss/
    $ pip install .

... and if you're running ``newslynx`` as ``sudo``

.. code:: bash

    $ cd ~/.newslynx/sous-chefs/newslynx-sc-rss/ 
    $ sudo pip install .

Finally, run ``newslynx sc-sync`` to ``newslynx-sc-rss``'s Sous Chefs
for all organizations.

.. code:: bash

    $ newslynx sc-sync

Development
~~~~~~~~~~~

If you want to run this SousChef on it's own environment, install it in
a separate virutal environ

Tests
-----

Requires ``nose``

.. code:: bash

    $ make all_tests

Documentation
-------------

Documentation for ``newslynx-sc-rss`` is hosted on `Read The
Docs <http://newslynx-sc-rss.readthedocs.org/>`__.

It's generated via the following steps

-  converts this file (``README.md``) into a ReStructured Text file,
   saving it to
   `docs/index.rst <https://github.com/newslynx/newslynx-sc-rss/blob/master/docs/index.rst>`__
-  runs ``newslynx sc-docs newslynx_sc_rss -f rst`` to generate
   documentation for all the Sous Chefs in ``newslynx-sc-rss`` and saves
   the output to
   `docs/sous-chefs.rst <https://github.com/newslynx/newslynx-sc-rss/blob/master/docs/sous-chefs.rst>`__
-  Builds Sphinx Documentation from these files.

Continuous Integration
----------------------

Builds for ``newslynx-sc-rss`` can be found on
`Travis <https://travis-ci.org/newslynx/newslynx-sc-rss>`__

Contributing
------------

See the `contributing
guidelines <https://github.com/newslynx/newslynx-sc-rss/blob/master/CONTRIBUTING.md>`__.

What's in this module ?
-----------------------

-  `README.md <https://github.com/newslynx/newslynx-sc-rss/blob/master/README.md>`__

   -  This file

-  `VERSION <https://github.com/newslynx/newslynx-sc-rss/blob/master/VERSION>`__

   -  ``newslynx-sc-rss``'s source-of-truth version.

-  `requirements.txt <https://github.com/newslynx/newslynx-sc-rss/blob/master/requirements.txt>`__

   -  ``newslynx-sc-rss``'s python dependencies.

-  `MANIFEST.in <https://github.com/newslynx/newslynx-sc-rss/blob/master/MANIFEST.in>`__

   -  Specifications for which files to include in the PyPI
      distribution.
   -  See the docs on this
      `here <https://docs.python.org/2/distutils/sourcedist.html#specifying-the-files-to-distribute>`__.

-  `setup.py <https://github.com/newslynx/newslynx-sc-rss/blob/master/setup.py>`__

   -  Specification's for building ``newslynx-sc-rss``'s PyPI
      distribution.

-  `.travis.yml <https://github.com/newslynx/newslynx-sc-rss/blob/master/.travis.yml>`__

   -  Configurations for Travis Continuous Integration
   -  You must activate this project on
      `travis-ci.org <https://github.com/newslynx/newslynx-sc-rss/blob/master/http://travis-ci.org/>`__
      for this to run on subsequent updates.

-  `Makefile <https://github.com/newslynx/newslynx-sc-rss/blob/master/Makefile>`__

   -  Helpers for managing ``newslynx-sc-rss``.
   -  Includes:

      -  ``make clean``:

         -  Cleans out cruft from this directory.

      -  ``make install``:

         -  Installs ``newslynx-sc-rss``. Assumes that you're in a
            virtual environment.

      -  ``make all_tests``:

         -  Runs the tests.

      -  ``make readme``

         -  Converts this file to ``.rst``, including a table of
            contents, and saves it to
            `docs/index.rst <https://github.com/newslynx/newslynx-sc-rss/blob/master/docs/index.rst>`__

      -  ``make sous_chef_docs``

         -  Programmtically generates `Sous Chef
            documentation <https://github.com/newslynx/newslynx-sc-rss/blob/master/docs/sous-chefs.rst>`__
            by running
            ``newslynx sc-docs newslynx_sc_rss/ --format=rst > docs/sous-chefs.rst``.

      -  ``make all_docs``:

         -  Builds the sphinx docs for ``newslynx-sc-rss`` by running
            the above two commands.

      -  ``make view_docs``

         -  Serves documentation at
            `localhost:8000 <http://localhost:8000>`__

      -  ``make register``:

         -  Registers ``newslynx-sc-rss`` on
            `PyPI <https://pypi.python.org/pypi>`__.

      -  ``make distribute``:

         -  Publishes a new version of ``newslynx-sc-rss`` to PyPI.

-  `CONTRIBUTING.md <https://github.com/newslynx/newslynx-sc-rss/blob/master/CONTRIBUTING.md>`__

-  `newslynx\_sc\_rss <https://github.com/newslynx/newslynx-sc-rss/blob/master/newslynx_sc_rss/>`__

   -  ``newslynx-sc-rss``'s source code and Sous Chef configuration
      files.

-  `docs <https://github.com/newslynx/newslynx-sc-rss/blob/master/docs/>`__

   -  Sphnix documentation for ``newslynx-sc-rss``

-  `tests <https://github.com/newslynx/newslynx-sc-rss/blob/master/tests/>`__

   -  ``nose`` tests for ``newslynx-sc-rss``

.. |Build status| image:: https://travis-ci.org/newslynx/newslynx-sc-rss.svg
   :target: https://travis-ci.org/newslynx/newslynx-sc-rss
.. |Documentation Status| image:: https://readthedocs.org/projects/newslynx-sc-rss/badge/?version=latest
   :target: https://readthedocs.org/projects/newslynx-sc-rss/?badge=latest

Contents
--------
.. toctree::
	:maxdepth: 2

	index
	sous-chefs
