.. _install:

Installation
============


Install
-------


Via Composer
^^^^^^^^^^^^

.. code-block:: sh

    $ composer create-project foolz/foolfuuka foolfuuka --prefer-source
    $ cd foolfuuka
    $ composer dump-autoload --optimize

.. warning::

    When asked to remove the VCS files (.git), you must choose ``N`` so that the version control system
    remains intact. This will allow you to perform future upgrades.


Via Source Code
^^^^^^^^^^^^^^^

.. code-block:: sh

    $ git clone https://github.com/FoolCode/FoolFuuka foolfuuka
    $ cd foolfuuka
    $ git checkout 2-2-stable
    $ composer install --optimize-autoloader


Upgrading
---------

.. code-block:: sh

    $ git fetch --all
    $ git checkout 2-2-stable
    $ composer update --optimize

.. note::

    The commands provided above will only upgrade the FoolFuuka code. You may be required to complete
    some additional steps to completely upgrade FoolFuuka to the next version. Please consult the upgrade
    guides to ensure that the upgrade process is done properly.

.. seealso:: :doc:`/user_guide/upgrade/index`
