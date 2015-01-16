.. _config:

Configuration
=============

While most of the configurable settings are exposed through the web administrative
panel, there are still a number of settings that can only be modified manually due
to security concerns.

.. note::

    In this documentation, we will use ``dot`` notations to specify the location of
    the config key being listed.

FoolFrame
---------

These config files are used to manage many of the core settings in the FoolFuuka
framework. You can locate these files in the following path after installation:
``vendor/foolz/foolframe/config/``.

.. note::

    We recommend that you copy these config files into and edit them in the
    following directory: ``app/foolz/foolframe/config/``. The software is
    designed to load these files instead of the default config files.


cache
^^^^^

    .. describe:: type

        :Type:    ``STRING``
        :Default: dummy

    .. describe:: format

        :Type:    ``STRING``
        :Default: smart_json

    .. describe:: prefix

        :Type:    ``STRING``
        :Default: ``empty``

    .. describe:: servers

        :Type:    ``ARRAY``
        :Default: ``empty``


config
^^^^^^

    .. describe:: config.cookie_prefix

        :Type:    ``STRING``
        :Default: ``empty``

    .. describe:: install.installed

        :Type:    ``BOOLEAN``
        :Default: false

    .. describe:: modules.installed

        :Type:    ``ARRAY``


db
^^

    .. describe:: active

        :Type:    ``STRING``
        :Default: default

    .. describe:: default.driver

        :Type:    ``STRING``
        :Default: pdo_mysql

    .. describe:: default.host

        :Type:    ``STRING``
        :Default: localhost

    .. describe:: default.port

        :Type:    ``INT``
        :Default: 3306

    .. describe:: default.dbname

        :Type:    ``STRING``
        :Default: ``empty``

    .. describe:: default.user

        :Type:    ``STRING``
        :Default: ``empty``

    .. describe:: default.password

        :Type:    ``STRING``
        :Default: ``empty``

    .. describe:: default.persistent

        :Type:    ``BOOLEAN``
        :Default: false

    .. describe:: default.prefix

        :Type:    ``STRING``
        :Default: ``empty``

    .. describe:: default.charset

        :Type:    ``STRING``
        :Default: utf8mb4


foolauth
^^^^^^^^

    .. describe:: db_connection

        :Type:    ``STRING``
        :Default: null

    .. describe:: table_name

        :Type:    ``STRING``
        :Default: users

    .. describe:: table_autologin_name

        :Type:    ``STRING``
        :Default: user_autologin

    .. describe:: table_login_attempts_name

        :Type:    ``STRING``
        :Default: user_login_attempts

    .. describe:: table_columns

        :Type:    ``ARRAY``

    .. describe:: guest_login

        :Type:    ``BOOLEAN``
        :Default: true

    .. describe:: groups

        :Type:    ``ARRAY``

    .. describe:: roles

        :Type:    ``ARRAY``

    .. describe:: login_hash_salt

        :Type:    ``STRING``
        :Default: ``empty``

    .. describe:: salt

        :Type:    ``STRING``
        :Default: ``empty``

    .. describe:: username_post_key

        :Type:    ``STRING``
        :Default: username

    .. describe:: password_post_key

        :Type:    ``STRING``
        :Default: password

    .. describe:: attempts_to_lock

        :Type:    ``INT``
        :Default: 10


FoolFuuka
---------

These config files are used to manage many of the core settings in FoolFuuka
that we considered very important and shouldn't be exposed in the web interface.
You can locate these files in the following path after installation: ``assets/config/``.

.. note::

    We recommend that you copy these config files into and edit them in the
    following directory: ``app/foolz/foolfuuka/config/``. The software is
    designed to load these files instead of the default config files.


config
^^^^^^

    .. describe:: comment.secure_tripcode_salt

        :Type:    ``STRING``
        :Default: null

    This is the salt used to for secure tripcodes. It is recommend that this salt key
    be changed when exposed or kept consistent between installations.


    .. describe:: media.filecheck

        :Type:    ``BOOLEAN``
        :Default: true

    Checks if the media file exists on the disk. The setting does impact disk performance
    when enabled due to lstat calls for each file being checked.

    +-----------+------------------------------------------------------------------------+
    | Value     | Effect                                                                 |
    +===========+========================================================================+
    | ``true``  | enables the check and returns a generated link based on file existence |
    +-----------+------------------------------------------------------------------------+
    | ``false`` | disables the check and returns a full link                             |
    +-----------+------------------------------------------------------------------------+


foolauth
^^^^^^^^

    .. describe:: roles

        :Type:    ``ARRAY``
