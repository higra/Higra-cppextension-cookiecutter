[![Build status](https://ci.appveyor.com/api/projects/status/0cuehlbeaxoql1hj/branch/master?svg=true)](https://ci.appveyor.com/project/PerretB/higra-cppextension-cookiecutter/branch/master)
[![Build Status](https://travis-ci.com/higra/Higra-cppextension-cookiecutter.svg?branch=master)](https://travis-ci.com/higra/Higra-cppextension-cookiecutter)

# higra-cppextension-cookiecutter

A [cookiecutter](https://github.com/audreyr/cookiecutter) template for creating a custom Python extension with [Higra](https://github.com/higra/Higra).

## What is higra-cppextension-cookiecutter?

`higra-cppextension-cookiecutter` helps creating Python extension modules making use of [Higra](https://github.com/higra/Higra).

It takes care of the initial work of generating a project skeleton with

- A complete `setup.py` compiling the extension module
- An example included in the resulting project
- Unit tests associated to the example


## Usage

**Project setup**

Install [cookiecutter](https://github.com/audreyr/cookiecutter):

    $ pip install cookiecutter

Now, retrieve `higra-cppextension-cookiecutter` with  *cookiecutter*:

    $ cookiecutter https://github.com/higra/higra-cppextension-cookiecutter.git

You will be asked for basic information about your custom extension project:

- `author_name`: your name or the name of your organization,
- `project_name`: name of your project,
- `python_package_name`: name of the Python package created by your extension, and
- `project_short_description`: a short description for your project.

This will produce a directory containing all the required content for a minimal extension
project making use of Higra with all the required boilerplate for package management,
together with a few basic examples. 

**Project usage**

Project usage (compilation, installation, tests) will be described in the `README.md` file in the produced directory

## Resources

- [Documentation of Higra](https://higra.readthedocs.io/)
- [Documentation of xtensor](https://xtensor.readthedocs.io/en/latest/)
- [Documentation of xtensor-python](https://xtensor-pyhton.readthedocs.io/en/latest/)

