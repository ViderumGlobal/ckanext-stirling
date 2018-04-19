------------
Requirements
------------

This extension is used together with `ckanext-tayside <https://github.com/ViderumGlobal/ckanext-tayside>`_.


------------
Installation
------------

To install ckanext-stirling:

1. Activate your CKAN virtual environment, for example::

     . /usr/lib/ckan/default/bin/activate

2. Install the ckanext-perth Python package into your virtual environment::

     pip install git+https://github.com/ViderumGlobal/ckanext-stirling.git#egg=ckanext-stirling

3. Add ``perth`` to the ``ckan.plugins`` setting in your CKAN
   config file (by default the config file is located at
   ``/etc/ckan/default/production.ini``).

5. Restart CKAN. For example if you've deployed CKAN with Apache on Ubuntu::

     sudo service apache2 reload


------------------------
Development Installation
------------------------

To install ckanext-stirling for development, activate your CKAN virtualenv and
do::

    git clone https://github.com/ViderumGlobal/ckanext-stirling.git
    cd ckanext-stirling
    python setup.py develop


----------
Modify CSS
----------

This extension uses LESS for styles. All changes must be made in one of the LESS
files located in the ``ckanext-stirling/ckanext/stirling/fanstatic/less`` folder.

In order to compile those files to CSS, the `less <https://www.npmjs.com/package/less>`_
npm module is used.

First make sure that you have installed `Node.js <https://nodejs.org/en/>`_. That
will install the ``npm`` package manager. After that, open up the terminal and
change the current directory to ``ckanext-stirling/ckanext/perth/fanstatic``.

Then run the following command that is going to install LESS::

    npm install less

After a successful installation, run the next command to compile the main less
file ``stirling.less`` to ``stirling.css``::

    npm run less less/stirling.less css/stirling.css

Every time there is some change in one of the less files, the upper command
needs to be run to compile those files to one css file.


---------
Funded by
---------

.. image:: smart.png
.. image:: euro_scot.png
