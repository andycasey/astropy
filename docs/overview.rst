Overview
========

Here we describe a broad overview of the astropy project and its associated
modules and packages.


`astropy` Package Layout
------------------------

Astropy contains the following base-level modules:


* :mod:`~astropy.config`
    This module contains configuration and setup utilities, including the 
    affiliated package install tools.
* :mod:`~astropy.utils`
    This module contains utilities of general use for multiple modules or
    affiliated packages.
* :mod:`~astropy.version`
    This module contains the version number information for the package. Note
    that the version is also copied to the base level of the package as
    :attr:`astropy.__version__`.
* :mod:`~astropy.extern`
    This module contains small python packages that are not unique to astropy
    but are convinient to include as part of the astropy source code.
* :mod:`~astropy.tests`
    This module contains astropy tests and test helpers.


Affiliated Packages
-------------------

Astropy also includes the concept of "affiliated packages." An affiliated
package is an astronomy-related python package that is not included as part of
the Astropy source code, but has officially requested to be included in the
Astropy community. Such a package may be a candidate for eventual inclusion in
the main `astropy` package. Astropy comes with a tool to install a affiliated
packages by name, and a single official index with a list and description of
each package. See the :mod:`~astropy.config` module documentation for details
regarding this install tool.

Affiliated packages do not use the `astropy` namespace, but rather either use
their package name directly, or `awastropy.packagename` ("affiliated with
astropy"). These packages may later be merged into the `astropy` package, in
which case the original package may still be used, but it is recommended that
users switch to the `astropy.packagename` version as soon as possible.
Alternatively, some affiliated packages may not wish to ever be merged with the
`astropy` source code, but rather remain as separate packages that make use of
other astropy modules or affiliated packages.

