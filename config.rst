.. _config:

Configuration
=============

While most of the configurable settings are exposed through the web administrative panel, there are still a
number of settings that can only be modified manually due to security concerns.


Administrative Panel
--------------------


Config Files
------------

In this documentation, we will use ``dot`` notations to specify the location of
the config key being listed.


FoolFrame
^^^^^^^^^

These config files are used to manage many of the core settings in the FoolFuuka
framework. You can locate these files in the following path after installation:
``vendor/foolz/foolframe/config/``.

.. note::

    We recommend that you copy these config files into and edit them in the
    following directory: ``app/foolz/foolframe/config/``. The software is
    designed to load these files instead of the default config files.


cache
+++++


config
++++++


db
++


foolauth
++++++++


FoolFuuka
^^^^^^^^^

These config files are used to manage many of the core settings in FoolFuuka
that we considered very important and shouldn't be exposed in the web interface.
You can locate these files in the following path after installation: ``assets/config/``.

.. note::

    We recommend that you copy these config files into and edit them in the
    following directory: ``app/foolz/foolfuuka/config/``. The software is
    designed to load these files instead of the default config files.


config
++++++

comment.secure_tripcode_salt
""""""""""""""""""""""""""""

============ ===============
**Scope:**   COMMENT
**Type:**    STRING
============ ===============

This is the salt used to for secure tripcodes. It is recommend that this salt key
be changed when exposed or kept consistent between installations.


media.filecheck
"""""""""""""""

============ ===============
**Scope:**   MEDIA
**Type:**    BOOLEAN
**Default:** true
============ ===============

Checks if the media file exists on the disk. The setting does impact disk performance
when enabled due to lstat calls for each file being checked.

+-------+------------------------------------------------------------------------+
| Value | Effect                                                                 |
+=======+========================================================================+
| true  | enables the check and returns a generated link based on file existence |
+-------+------------------------------------------------------------------------+
| false | disables the check and returns a full link                             |
+-------+------------------------------------------------------------------------+


foolauth
++++++++
