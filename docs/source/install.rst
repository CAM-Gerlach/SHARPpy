.. _Installation_Guide_:

Installation Guide
==================

SHARPpy code can be installed on *Windows, macOS, and Linux*, as all these platforms can run Python programs.  SHARPpy may run on other operating systems, but this has not been tested by the developers.  Chances are if it can run Python, it can run SHARPpy.  

SHARPpy can be installed from one of these three places: 

* a pre-compiled binary executable
* a Python package manager (:command:`conda`)
* from source (downloaded from Github).  

Binary executables are available for Windows and macOS (64 bit).

**If you are upgrading your version of SHARPpy, you may need to delete your ~/.sharppy folder as 
the files in that directory may be incompatable with the new version of SHARPpy.**

Installing a pre-compiled binary
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

You probably would like to go this route if you are not familiar with command line interfaces such as those on Linux or macOS. 
Pre-compiled binaries are available on the Github Releases page.  These are regenerated by Continuous 
Integration software with each update we make to the primary code base:

https://github.com/sharppy/SHARPpy/releases/

Installing a pre-compiled binary *should* be as simple as downloading the .zip file and extracting it to the location of your choice.  The zip files are named for the operating system and number of bits.  Most recently-built computers (probably post-2010 or so) should have 64-bit operating systems installed.

.. note:: The pre-compile binaries are sometimes difficult to keep up to date, so for more recent versions of SHARPpy, you may want to look into the next section, which is about installing the program via package managers. 

Installing using package managers
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

SHARPpy is also available for download through the :command:`conda` package manager.  This package manager will also take care of downloading the correct dependencies SHARPpy needs to run.  They are accessible through the command line interface of your operating system.  You may be interested in this route should you want to do scripting with the SHARPpy package and also work with the GUI.

From conda
----------

The Anaconda Python Distribution can be downloaded here: https://store.continuum.io/cshop/anaconda/
We recommend you download the *Python 3.6 or 3.7* version of the Anaconda Python distribution.  SHARPpy is
primarily tested using this distribution.  SHARPpy is available on the conda-forge channel.

To avoid compatability issues with other Python packages, we **strongly recommend** you install SHARPpy into its own Anaconda environment

.. prompt:: bash

    conda create -n sharppy-env
    conda activate sharppy-env
    conda install -c conda-forge sharppy


.. Otherwise, you can try to install SHARPpy directly into your current Anaconda environment:
   prompt:: bash

    conda config --add channels conda-forge
    conda install -c sharppy sharppy

.. From pip
   --------

   Currently, we are have difficulties deploying to PyPI and therefore do not recommend downloading SHARPpy from pip.

   ..
   If you hate snakes, you may want to use :command:`pip` instead: 
   .. prompt:: bash
   pip install sharppy

Installing the code from source
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

You may wish to go this route if you are interested in contributing to the SHARPpy project.  You should become familiar with the :command:`git` program.
:command:`git` is a version control manager that tracks changes made to the code base.  If you would like to go this route, you will need to 
install the required packages manually.  These instructions assume that you have the Anaconda Python distribution. 

*Required Python Packages/Libraries:*

* NumPy
* qtpy

Since SHARPpy requires the qtpy and Numpy packages, you will need to install them.  If you choose to use the Anaconda distribution, Numpy comes installed by default.  qtpy can be installed through the Anaconda package manager that comes with the Anaconda distribution by opening up your command line program (Terminal in macOS/Linux and Command Prompt in Windows) and typing:

* PySide 2
* requests
* python-dateutil

Since SHARPpy requires these packages, you will need to install them.  If you choose to use the Anaconda distribution, Numpy comes installed by default.  PySide 2, requests, and python-dateutil can be installed through the Anaconda package manager that comes with the Anaconda distribution by opening up your command line program (Terminal in macOS/Linux and Command Prompt in Windows) and typing:

.. prompt:: bash

    conda install -c conda-forge pyside2=5.12.* requests python-dateutil

After installing all the required Python packages for SHARPpy, you now can install the SHARPpy package to your computer.  You'll need to download it to your computer first and open up a command line prompt.  You can download it as a ZIP file (link on the right) or clone the Git respository (you will need the git program) into a directory on your computer by typing this into your command line:

.. prompt:: bash

    git clone https://github.com/sharppy/SHARPpy.git

If you decide you wish to contribute to the code, you will want to make a fork of the SHARPpy project on Github.
This will create a copy of the repository that you can work with.  After you have have made changes to your for, you can submit a "pull request"
that allows the managers of the SHARPpy project to "pull" your contributions into the main repository.

If you follow the route of cloning SHARPpy, you can update to the most recent SHARPpy package by typing the following within the folder you downloaded SHARPpy to:

.. prompt:: bash

    git pull origin master

Other branches (including development ones not called master) can be listed using the `git branch` command:

.. prompt:: bash
    
    git branch

We tend to name each version of SHARPpy after the locations where significant tornados have struck (e.g., Xenia, El Reno).  Releases will be under the "master" branch, while development versions will
tend to have another name (such as andover).  You can download those using the `checkout` command.  For example:

.. prompt:: bash

    git checkout andover

Once the package has been downloaded to your computer, use your command line to navigate into the SHARPpy directory.
The package can be installed via this command, which will allow you to edit the source code you downloaded and test it without
needing to reinstall the program each time:

.. prompt:: bash
    
    pip install -e .

After installing the package, you can run the SHARPpy GUI and interact with the SHARPpy libraries through Python scripts.
The GUI can be launched similar to the method described above in the "Installing from conda" section.
