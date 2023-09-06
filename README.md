# Python python-oracledb Notebooks, 2023

This repository contains Jupyter notebooks showing best practices for using
[python-oracledb](https://pypi.org/project/oracledb/), the Python DB API for Oracle
Database.  Python-oracledb is the new name for cx_Oracle.

Python-oracledb's default 'Thin' mode is used.

The notebooks covers:

- Connecting
- Queries
- DML
- Data loading and Unloading (CSV Files)
- JSON
- PL/SQL
- Objects

Jupyter notebooks let you step through and execute Python code:

![A screenshot of a notebook running in a browser](./images/jupyter-notebook-screenshot.png)

## Other resources

You may also be interested in the quickstart [Quick Start: Developing Python
Applications for Oracle
Database](https://www.oracle.com/database/technologies/appdev/python/quickstartpythononprem.html)
and the tutorial [Getting Started with Python and Oracle
Database](https://apexapps.oracle.com/pls/apex/r/dbpm/livelabs/view-workshop?wid=3482).

# Setup

An existing Oracle Database is required.  The JSON demo assumes that Oracle Database 21c or later is being used.

### Install Python 3

See https://www.python.org/downloads/

### Install Jupyter

See https://jupyter.org/install:

    python3 -m pip install notebook

### Install the python-oracledb driver

    python3 -m pip install oracledb

### Install some libraries used by the examples

    python3 -m pip install numpy matplotlib

### Create the python-oracledb sample schema

Clone/download https://github.com/oracle/python-oracledb/tree/master/samples, for example in a terminal window:

    git clone https://github.com/oracle/python-oracledb.git

    cd python-oracledb/samples

Review README.md and sample_env.py

In the terminal, set desired credentials, for example:

    export PYO_SAMPLES_ADMIN_USER=system
    export PYO_SAMPLES_ADMIN_PASSWORD=oracle
    export PYO_SAMPLES_CONNECT_STRING=localhost/orclpdb1
    export PYO_SAMPLES_MAIN_USER=pythondemo
    export PYO_SAMPLES_MAIN_PASSWORD=welcome
    export PYO_SAMPLES_EDITION_USER=pythoneditions
    export PYO_SAMPLES_EDITION_PASSWORD=welcome
    export PYO_SAMPLES_EDITION_NAME=python_e1

Install the schema:

    python3 create_schema.py

### Start Jupyter:

    cd ../..
    jupyter notebook

If Jupyter is not in your path, you may need to find it on your computer and
invoke it with an absolute path, for example on macOS:

    $HOME/Library/Python/3.9/bin/jupyter notebook

Load each notebook *.ipynb file and step through the cells.

Before running the notebooks cells, edit the credentials and connect string
near the top of each notebook to match those used when installing the sample
schema.
