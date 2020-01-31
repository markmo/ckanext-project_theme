.. image:: https://travis-ci.org/markmo/ckanext-project_theme.svg?branch=master
    :target: https://travis-ci.org/markmo/ckanext-project_theme

.. image:: https://coveralls.io/repos/markmo/ckanext-project_theme/badge.svg
  :target: https://coveralls.io/r/markmo/ckanext-project_theme

..  .. image:: https://pypip.in/download/ckanext-project_theme/badge.svg
        :target: https://pypi.python.org/pypi//ckanext-project_theme/
        :alt: Downloads

..  .. image:: https://pypip.in/version/ckanext-project_theme/badge.svg
        :target: https://pypi.python.org/pypi/ckanext-project_theme/
        :alt: Latest Version

..  .. image:: https://pypip.in/py_versions/ckanext-project_theme/badge.svg
        :target: https://pypi.python.org/pypi/ckanext-project_theme/
        :alt: Supported Python versions

..  .. image:: https://pypip.in/status/ckanext-project_theme/badge.svg
        :target: https://pypi.python.org/pypi/ckanext-project_theme/
        :alt: Development Status

..  .. image:: https://pypip.in/license/ckanext-project_theme/badge.svg
        :target: https://pypi.python.org/pypi/ckanext-project_theme/
        :alt: License

=============
ckanext-project_theme
=============

CKAN theme overrides including renaming of "Datasets" to "Projects".


------------
Requirements
------------

Tested with CKAN Version 2.8.3.


------------
Installation
------------

.. Add any additional install steps to the list below.
   For example installing any non-Python dependencies or adding any required
   config settings.

To install ckanext-project_theme:

1. Activate your CKAN virtual environment, for example::

     . /usr/lib/ckan/default/bin/activate

2. Install the ckanext-project_theme Python package into your virtual environment::

     pip install ckanext-project_theme

3. Add ``project_theme`` to the ``ckan.plugins`` setting in your CKAN
   config file (by default the config file is located at
   ``/etc/ckan/default/production.ini``).

4. Restart CKAN. For example if you've deployed CKAN with Apache on Ubuntu::

     sudo service apache2 reload


---------------
Config Settings
---------------

There are no specific config settings for the plugin.


------------------------
Development Installation
------------------------

To install ckanext-project_theme for development, activate your CKAN virtualenv and
do::

    git clone https://github.com/markmo/ckanext-project_theme.git
    cd ckanext-project_theme
    python setup.py develop
    pip install -r dev-requirements.txt


-----------------
Running the Tests
-----------------

To run the tests, do::

    nosetests --nologcapture --with-pylons=test.ini

To run the tests and produce a coverage report, first make sure you have
coverage installed in your virtualenv (``pip install coverage``) then run::

    nosetests --nologcapture --with-pylons=test.ini --with-coverage --cover-package=ckanext.project_theme --cover-inclusive --cover-erase --cover-tests


---------------------------------
To create package
---------------------------------

To create a source and wheel distribution::

  python setup.py sdist bdist_wheel

The artifacts are placed in ``dist/``.


---------------------------------
Install from this GitHub Repo
---------------------------------

ckanext-nbview can be installed using::

  pip install git+https://github.com/markmo/ckanext-nbedit#egg=ckanext-nbedit


---------------------------------
Registering ckanext-project_theme on PyPI
---------------------------------

ckanext-project_theme should be availabe on PyPI as
https://pypi.python.org/pypi/ckanext-project_theme. If that link doesn't work, then
you can register the project on PyPI for the first time by following these
steps:

1. Create a source distribution of the project::

     python setup.py sdist

2. Register the project::

     python setup.py register

3. Upload the source distribution to PyPI::

     python setup.py sdist upload

4. Tag the first release of the project on GitHub with the version number from
   the ``setup.py`` file. For example if the version number in ``setup.py`` is
   0.0.1 then do::

       git tag 0.0.1
       git push --tags


----------------------------------------
Releasing a New Version of ckanext-project_theme
----------------------------------------

ckanext-project_theme is availabe on PyPI as https://pypi.python.org/pypi/ckanext-project_theme.
To publish a new version to PyPI follow these steps:

1. Update the version number in the ``setup.py`` file.
   See `PEP 440 <http://legacy.python.org/dev/peps/pep-0440/#public-version-identifiers>`_
   for how to choose version numbers.

2. Create a source distribution of the new version::

     python setup.py sdist

3. Upload the source distribution to PyPI::

     python setup.py sdist upload

4. Tag the new release of the project on GitHub with the version number from
   the ``setup.py`` file. For example if the version number in ``setup.py`` is
   0.0.2 then do::

       git tag 0.0.2
       git push --tags
