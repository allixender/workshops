.. _cmd.init:

GeoGig setup
------------

Before we can use GeoGig, we will need to configure the tool. Specifically we will want to enter information about the user that will be doing the commit. The information we enter here will be contained in all commits performed by this user, associating changes with its author.

User information can be set globally, for all repositories managed by GeoGig, or on a per-repository basis. We will set this information globally.

#. In a terminal, enter the following two commands, substituting your own information for what is in quotes:

   .. code-block:: console

      geogig config --global user.name "Author"

   .. code-block:: console

      geogig config --global user.email "author@example.com"

.. note:: If you encounter any errors with the ``geogig`` command line interface, please see the :ref:`cmd.troubleshoot` section.

Create a GeoGig repository
--------------------------

#. On the command line, navigate to the :file:`geogig` directory.

#. Create a new directory and call it :file:`repos`, if it doesn't exist.  This directory will house the GeoGig repos. 

   .. code-block:: console

      mkdir repos

   .. note:: As mentioned before, no spatial data needs to be contained in this directory. In fact, no files at all need to be in this directory, except for the :file:`.geogig` subdirectory.

#. Switch to this directory and create a new directory called `city_data`.

   .. code-block:: console

      cd repos
      mkdir city_data

#. Switch to the `city_data` directory and create a new GeoGig repository in this directory:

   .. code-block:: console

      cd city_data
      geogig init

#. View a directory listing that shows all files and verify that the :file:`.geogig` directory has been created.

   .. code-block:: console

      ls -al

More about the ``geogig`` command
---------------------------------

All working commands with GeoGig are in the following form:

.. code-block:: console

   geogig [command] [options]

These commands must be run from in the directory where the repository was created.

To see a full list of commands, type:

.. code-block:: console

   geogig --help

To see a list of the parameters associated with a given command, type ``help`` followed by the command. For example, to see the parameters associated with the ``show`` command, type:

.. code-block:: console

   geogig help show

::

   Displays information about a commit, feature or feature type
   Usage: show [options] <reference>
     Options:
           --raw
          Produce machine-readable output
          Default: false

