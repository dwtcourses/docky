Install on Ubuntu
====================

Prerequisite
---------------

* You need a 64 bits architecture.
* You will need to install the Python development headers (python-dev)
* You will need to install the Python package manager PIP

Install or upgrade your Docker:
----------------------------------

Please go to docker documentation installation page : `Install Docker
<https://docs.docker.com/engine/installation>`_

* Give non root access to Docker if not done already:

.. code-block:: shell

  sudo gpasswd -a ${USER} docker
  sudo service docker restart

**you may have to LOGOUT and LOG BACK IN AGAIN for the group change to take effect!**

* A simple test to see if you have non root access is to list your docker images with

.. code-block:: shell

   docker images # make sure you don't need sudo anymore here


Install Docky:
------------------

.. code-block:: shell

    sudo pip install docky

Update Docky:
------------------

.. code-block:: shell

    sudo pip install docky --upgrade
    docker pull akretion/docky

Configuration:
--------------

The configuration file is in your home : '~/.docky/config.yml'

verbose [True, False]:
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Verbose mode is activated by default in order to help you to learn what docky do


env [dev, prod, preprod]:
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Specify which kind of environment is used

maintainer_quality_tools [url]:
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

URL for the maintainer-quality-tools of OCA used for testing the code

shared_gems [True or False]:
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

If true the ~/.docky/shared/gems will be mounted as gems folder in your docker
This mean that the gems will be shared between your docky projects saving some download and space.
