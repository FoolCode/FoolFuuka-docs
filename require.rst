.. _require:

Requirements
============

Web Server
----------

You'll need to install one of the following web servers to allow users to access the web interface:

* Apache
* nginx (Recommended)

.. seealso:: `Virtual Hosts Examples <https://github.com/FoolCode/FoolFuuka-docs/tree/master/examples/vhosts>`_


Database
--------

FoolFuuka supports the following database servers:

* MariaDB 5.5+ (Recommended)
* MySQL 5.5+

.. note::

    When dealing with large amounts of data, we recommend using the ``TokuDB`` storage engine for all
    board tables which is available with MariaDB. This mainly applies to deployments used to provide a
    front-end for `Asagi <https://github.com/FoolCode/asagi>`_ and archives.


Git/Composer
------------

FoolFuuka utilizes both `Git <http://git-scm.com/>`_ and `Composer <https://getcomposer.org/>`_ to manage
all of its dependencies, software updates, and web assets.


PHP/HHVM
--------

While FoolFuuka is designed to work on PHP 5.4 or newer, it is also compatible with HHVM.


Search Server
-------------

FoolFuuka requires an additional software to index and serve search results to users. This is achieved
with `Sphinx Open Source Search Server <http://sphinxsearch.com/>`_ which must be installed to provide
users with search capabilities.

.. note::

    FoolFuuka includes a Sphinx configuration file generator in the web administration interface and
    should be used to generate a new sphinx configuration file accordingly.


ImageMagick
-----------

If you plan to use FoolFuuka as an image-based bulletin board, ImageMagick must be installed on the
server. The binary files are used to generate and manipulate image files.

.. note::

    You may be required to specify the path for ImageMagick's ``convert`` binary in the administrative
    panel.
