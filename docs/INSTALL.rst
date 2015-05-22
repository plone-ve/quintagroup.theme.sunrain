quintagroup.theme.sunrain Installation
=======================

 * When you're reading this you have probably already run
   ``easy_install quintagroup.theme.sunrain``. Find out how to install setuptools
   (and EasyInstall) here:
   http://peak.telecommunity.com/DevCenter/EasyInstall

 * Get `pythonproducts`_ and install it via::

       python setup.py install --home /path/to/instance

   into your Zope instance.

 * Create a file called ``quintagroup.theme.sunrain-configure.zcml`` in the
   ``/path/to/instance/etc/package-includes`` directory.  The file
   should only contain this::

       <include package="quintagroup.theme.sunrain" />

.. _pythonproducts: http://plone.org/products/pythonproducts

Alternatively, if you are using zc.buildout and the plone.recipe.zope2instance
recipe to manage your project, you can do this:

 * Add ``quintagroup.theme.sunrain`` to the list of eggs to install, e.g.:

    [buildout]
    ...
    eggs =
        ...
        quintagroup.theme.sunrain

  * Tell the plone.recipe.zope2instance recipe to install a ZCML slug:

    [instance]
    recipe = plone.recipe.zope2instance
    ...
    zcml =
        quintagroup.theme.sunrain

  * Re-run buildout, e.g. with:

    $ ./bin/buildout

You can skip the ZCML slug if you are going to explicitly include the package
from another package's configure.zcml file.