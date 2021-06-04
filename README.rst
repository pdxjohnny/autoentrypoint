autoentrypoint Sphinx extension
===============================

Sphinx extension for autoclassing every item registered for an entrypoint.

Install from pip

.. code-block:: console

    $ pip install autoentrypoint

Create a Sphinx project

.. code-block:: console
    :test:

    $ sphinx-quickstart --no-sep  --no-makefile --no-batchfile \
        --language english -v 0.0.0 --release 0.0.0 \
        --project "My Project" --author "First Last" docs/

**docs/conf.py**

Add it to your list of extensions.

.. code-block:: python
    :test:
    :filepath: docs/conf.py


    extensions.append("autoentrypoint")

Use the ``autoentrypoint`` directive to have all the classes which are in an
entrypoint to be documented.

**docs/index.rst**

.. code-block:: rst
    :test:
    :filepath: docs/index.rst

    distutils.commands

Run the build.

.. code-block:: console
    :test:

    $ sphinx-build -W -b html docs built_html_docs/
