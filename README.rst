MPinterfaces is a python package that enables high throughput Density
Functional Theory(DFT) analysis of arbitrary material interfaces(ligand capped
nanoparticles, surfaces in the presence of solvents and hetero-structure
interfaces) using VASP_, VASPsol_ and materialsproject_ database as well
as their open source tools_.

.. _materialsproject: https://github.com/materialsproject

.. _VASPsol: https://github.com/henniggroup/VASPsol

.. _VASP: http://www.vasp.at/

.. _tools: https://github.com/materialsproject

   
Installation
==============

The following steps applies only to linux and OSX(with xcode) operating systems.

Prepping
-------------

1. Make sure that you are using python>=2.7 (do a "python --version").

   Note: ASE does not work with python3

2. it is highly recommended that you use gcc compiler. So type::

   export CC=gcc

   Note: *Don't use gcc if the already available numpy/scipy packages
   were setup using intel MKL*

3. Unless you have admin privilege on the machine you are installing, it is
   better to install this package and all its dependencies in a virtual environment.

   - get the latest version from https://pypi.python.org/pypi/virtualenv#downloads
   
   - tar xvfz virtualenv-X.X.X.tar.gz
   
   - cd virtualenv-X.X.X
   
   - setup the virtual environment in ~/myvenv (or set to some other path and folder name)
     
     * python virtualenv.py ~/myvenv
       
   -  activate the virtual environment

      * source ~/myvenv/bin/activate
   
   For detailed instructions and documentation see

   http://virtualenv.readthedocs.org/en/latest/installation.html

4. Install numpy::

   pip install numpy


Get the latest version
-----------------------

If you already have a local copy, steps 1 and 2 of the following instructions
can be skipped. Just do a "git pull" from the MPInterfaces folder and go to
step 3(if the local copy was installed in the develop mode this step can be skipped too).

1. Clone the latest version from github

  - git clone https://github.com/henniggroup/MPInterfaces.git
  
2. cd MPInterfaces
	
3. python setup.py install(or develop)

4. set the evironment variables:
   
   - MAPI_KEY=the_key_obtained_from_materialsproject
     
   - VASP_PSP_DIR=path_to_vasp_potcar_files
   

  
Documentation
==============

A very minimal documentation is avaiable at the moment and work is underway
to improve it. We use the sphinx package to generate the documentation.
First install the package 'sphinx' and the theme package 'sphinx-rtd-theme'
using pip and then to generate the documentation either in html or pdf format
do the following:

  * html format
    
    - cd docs; make html

    - open _build/html/index.html in a webbrowser to see the documentation

  * pdf

    - cd docs; make latexpdf

    - The pdf will be in the _build/latex folder 

      
Usage
==========

We use pymatgen tools for all structure manipulation tasks, so it would
be a good idea to start from here:

http://pymatgen.org/#using-pymatgen

The examples folder contain some sample scripts that demonstrate the
usage of mpinterfaces as well as materialsproject packages. For basic
usage please see **docs/usage.rst**.


Contributing
=============

We try to follow the coding style used by pymatgen(PEP8):

http://pymatgen.org/contributing.html#coding-guidelines


Authors
=========
   
Kiran Mathew
	
Joshua Gabriel

Arunima Singh

Richard G. Hennig
