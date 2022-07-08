Usage
=====

cryoHub uses React as the frontend framework, Node.js for backend and MariaDB as the database.

.. _installation:

Installation
------------

We wrapped the installation commands in a separate shell script. It will automatically download
and install the required prerequisites (Node and MariaDB).

.. code-block:: console

   $ something

.. note::

   cryoHub works as a “wrapper” for the existing tools and software.
   Therefore, cryoHub **does not** include or distribute any cryo-EM software by itself.
   For example, although we provide the support for RELION commands, installing cryoHub will not
   install RELION on your machine.

.. _deployment:

Deployment
------------

.. note::

   cryoHub is designed to run on a GPU workstation, therefore it cannot handle CPU cluster
   with a scheduler for now. If you want to use it in such environment, the best way
   would be using cryoHub in an interactive session.

We wrapped the commands to start the application in a separate shell script. It will start both
the server and the client sides on the workstation.

.. code-block:: console

   $ something

You can access the application with the URL: xyzxyz.
This URL is customizable in somefile.
