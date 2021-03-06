# MyPy Example Repo [![Build Status](https://travis-ci.org/markkohdev/mypy-example.svg?branch=master)](https://travis-ci.org/markkohdev/mypy-example)
This is an example repo that will maybe help you get MyPy integrated into your own code base :)


### What is MyPy?
[MyPy](https://github.com/python/mypy) is an optional static type checker for Python.

To understand what MyPy is and why it's awesome, I recommend you [check out the README](https://github.com/python/mypy#what-is-mypy).

## How to run this
#### Requirements
- python3.6
    - `brew install --upgrade python3`
    - `sudo apt-get update && sudo apt-get install python3.6`

#### Quick setup
In termimnal, cd into this repo's directory and run
```
./quick_setup.sh
```
and answer the prompts.  This will install some dependencies (python3, virtualenv, autoenv), create a virtualenv, and then install pip dependencies into that virtualenv.

It will also give you the option to install [autoenv](https://github.com/kennethreitz/autoenv), which is a really handy tool for automatically activating your python virtualenv when you `cd` into a directory.

## Description of Files
#### [mypy.ini](/mypy.ini)
The mypy configuration file.  [Read about how to configure your mypy here.](http://mypy.readthedocs.io/en/stable/config_file.html)

#### [tox.ini](/tox.ini)
The tox config file.  We use [tox](https://tox.readthedocs.io/en/latest/) for testing in this repo.

To run `tox` simply run
```
tox
```
and it will run your tests in fancy isolated test environments.

#### [quick_setup.sh](/quick_setup.sh)
A setup file for this repository.  It will install python3 on your linux or Mac machine, create a virtual environment, and install some other helpful things if you choose to.

#### [requirements.txt](/requirements.txt)
Our pip dependencies file.  This file includes any python packages you need in order to run this jawn.  It also specifies Mypy as a dependency.
Run `make install` to install requirements using pip.

#### [.travis.yml](/.travis.yml)
Our TravisCI configuration file.  [Travis CI](https://travis-ci.org/) is an easy to configure CI pipeline that's free for open-source projects.  This file is a simple example of how to configure travis to run your tox tests, which will in turn run your MyPy tests.
