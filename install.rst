
Installing
==========

Necessary steps before installation
-----------------------------------

**Install Git**. On Debian/Ubuntu systems::

    sudo apt-get install git-core

And on Fedora::

    sudo yum install git-core

Installing Geodevolutas
-----------------------

To install it start by cloning the main codebase repository, ``geodevolutasorg``::

    git clone git://gitorious.org/geodevolutas-org/geodevolutasorg.git

The next step will be cloning the ``files`` repository. For this, place yourself on the ``geodevolutasorg/sites/default`` folder and, once there, clone this second repository::

    cd geodevolutasorg/sites/default
    git clone git://gitorious.org/geodevolutas-org/files.git

.. NOTE:: This should be needed only at the first time, as this folder stores the user generated content that is not kept on the database.

The third step is to clone the database repository. Create an empty MySQL database and import the included dump file onto it. For easily creating Drupal databases, with the correct permissions and grants, we suggest the use of the scripts developed by perusio that can be found on https://github.com/perusio/drupal-db.

Now edit the ``geodevolutasorg/sites/default/default.settings.php`` inserting the created database attributes and save it as settings.php.

As a last step, define the proper files and folder permissions following the Drupal standards. Also, as a lazy and simple tool, we advice the use of the ``fix-permissions`` script that can be found at https://gitorious.org/drupal-fix-permissions.

