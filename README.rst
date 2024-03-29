DCOS HelloWorld Subcommand
==========================
Basic DCOS subcommand

Setup
-----
#. Make sure you meet requirements for installing packages_
#. Clone git repo for the dcos helloworld cli::

    git clone git@github.com:mesosphere/dcos-helloworld.git

#. Change directory to the repo directory::

    cd dcos-helloworld

#. Make sure that you have virtualenv installed. If not type::

    sudo pip install virtualenv

#. Create a virtualenv for the project::

    make env

Configure Environment and Run
-----------------------------

#. TODO: Talk about how to configure the root dcos cli

#. :code:`source` the setup file to add the :code:`dcos-helloworld` command line interface to your
   :code:`PATH`::

    source env/bin/activate

#. Get started by calling the DCOS HelloWorld CLI's help::

    dcos helloworld help

Running Tests:
--------------

Setup
#####

Tox, our test runner, tests against both Python 2.7 and Python 3.4 environments.

If you're using OS X, be sure to use the officially distributed Python 3.4 installer_ since the
Homebrew version is missing a necessary library.

Running
#######

Tox will run unit and integration tests in both Python environments using a temporarily created
virtualenv.

You should ensure :code:`DCOS_CONFIG` is set and that the config file points to the Marathon
instance you want to use for integration tests.

There are two ways to run tests, you can either use the virtualenv created by :code:`make env`
above::

    make test

Or, assuming you have tox installed (via :code:`sudo pip install tox`)::

    tox

Other Useful Commands
#####################

#. List all of the supported test environments::

    tox --listenvs

#. Run a specific set of tests::

    tox -e <testenv>

.. _packages: https://packaging.python.org/en/latest/installing.html#installing-requirements
