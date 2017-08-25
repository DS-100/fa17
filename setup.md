---
layout: page
title: "Computer Setup"
description: "Instructions to set up your data science environment."
---


## Contents

- **Installation**
  - [OSX](#osx)
  - [Windows](#windows)
  - [Linux](#linux)
- [Working on assignments](#working-on-assignments)
- [Opening notebooks](#opening-notebooks)

## OSX

0. First things first. Your terminal program allows you to type commands to
   control your computer. On a Mac, you can open the Terminal by going to your
   Applications screen and selecting Terminal (it might be in the folder named
   "Other"). Or, you can open Spotlight (Cmd + Space) and type "Terminal".

1. First, let's install `brew` if you haven't done that yet. Homebrew is a
   program that allows you to easily install other software on OSX. In your
   terminal, run:

        # This downloads the Ruby code of the installation script and runs it
        /usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"

   Verify your installation by making sure `brew --version` doesn't error at
   your terminal.


2. Download and install Anaconda:

        # Uses curl to download the installation script
        curl https://repo.continuum.io/archive/Anaconda3-4.4.0-MacOSX-x86_64.sh > miniconda.sh

        # Run the miniconda installer (you will need to enter your password)
        bash miniconda.sh

   Ensure the installation worked by running `conda --version`.

3. Run these commands to create a new [conda environment][env]. Each conda
   environment has its own package versions. This allows us to switch between
   package versions easily. For example, this class uses Python 3, but you
   might have another that uses Python 2. With a conda environment, you can
   switch between those at will.

        # Create a python 3 conda environment with the full set
        # of anaconda packages (jupyter, numpy, pandas, ...)
        conda create --name ds100 python=3 anaconda

        # Switch to the ds100 environment
        source activate ds100

   From now on, you can switch to the `ds100` env with `source activate ds100`,
   and switch back to the default env with `source deactivate`.


You may remove the `install_anaconda.sh` script now if you'd like since it's
quite large.

[**Click here to continue to the next part of the setup.**](#working-on-assignments)

## Windows

Getting set up on Windows is especially prone to error if you aren't careful
about your configuration. If you've already had Anaconda or `git` installed and
can't get the other to work, try uninstalling everything and starting from
scratch.

### Installing Anaconda:

1. Visit [the Anaconda website](https://www.continuum.io/downloads#windows) and
   download the installer for Python 3.5. Download the 64-bit installer if your
   computer is 64-bit (more likely), the 32-bit installer if not. You can
   Google how to check whether your computer is 64 or 32 bit.

2. Leave all the options as default (install for all users, in the default
   location). Make sure both of these checkboxes are checked:

   ![conda4](https://cloud.githubusercontent.com/assets/2468904/21345446/24440520-c655-11e6-9d3d-f56d32ed7029.PNG)

3. Install.

4. Verify that the installation is working by starting the Anaconda Prompt (you
   should be able to start it from the Start Menu) and typing `python`:

   ![conda6](https://cloud.githubusercontent.com/assets/2468904/21345449/24497f5a-c655-11e6-9181-d253e5c0d07c.PNG)

   Notice how the `python` prompt shows that it is running from Anaconda. Now
   you have `conda` installed!

   **From now on, when we talk about the "Terminal" or "Command Prompt", we are
   referring to the Anaconda Prompt that you just installed.**

5. Run these commands to create a new [conda environment][env]. Each conda
   environment has its own package versions. This allows us to switch between
   package versions easily. For example, this class uses Python 3, but you
   might have another that uses Python 2. With a conda environment, you can
   switch between those at will.

        # Create a conda env called ds100 that uses python 3
        conda create --name ds100 python=3 anaconda

        # Switch to the ds100 environment
        activate ds100


   From now on, you can switch to the `ds100` env with `activate ds100`,
   and switch back to the default env with `deactivate`.

## Linux

These instructions assume you have `apt-get` (Ubuntu and Debian).
For other distributions of Linux, substitute the available package manager.

1. You likely already know this if you're running Linux, but just in case: your
   terminal program allows you to type commands to control your computer. On
   Linux, you can open the Terminal by going to the Applications menu and
   clicking "Terminal".

2. Install `wget`. This is a command-line tool that lets you download
   files / webpages at the command line.

        sudo apt-get install wget

3. Download the Anaconda installation script:

        wget -O install_anaconda.sh https://repo.continuum.io/archive/Anaconda3-4.2.0-Linux-x86_64.sh

   If you have a 32-bit operating system, use this command instead.

        wget -O install_anaconda.sh https://repo.continuum.io/archive/Anaconda3-4.2.0-Linux-x86.sh

4. Install Anaconda:

        bash install_anaconda.sh

   Ensure the installation worked by running `conda --version`.

5. Run these commands to create a new [conda environment][env]. Each conda
   environment has its own package versions. This allows us to switch between
   package versions easily. For example, this class uses Python 3, but you
   might have another that uses Python 2. With a conda environment, you can
   switch between those at will.

        # Create a conda env called ds100 that uses python 3
        conda create --name ds100 python=3 anaconda

        # Switch to the ds100 environment
        source activate ds100

  
   From now on, you can switch to the `ds100` env with `source activate ds100`,
   and switch back to the default env with `source deactivate`.

[env]: http://conda.pydata.org/docs/using/envs.html

[**Click here to continue to the next part of the setup.**](#working-on-assignments)

## Working on assignments

These instructions are the same for OSX, Windows, and Linux.

To work on assignments, you should download the assignment zipfile (looks like
`hw1.zip`). Then you can unzip the files into a folder of your choosing. The
staff recommend that you create a parent folder that holds all the assignments
for this class for easier access.

Remember the location of your assignment files because you'll need to navigate
to the folder to open the notebook.

You'll notice that all the assignments for this class have a folder structure
that looks something like:

```
hw1/
  func.png
  ok_tests/
  images/
  hw1.ipynb
  hw1.ok
  something_cool.csv
```

The file containing the actual assignment ends in `.ipynb` (short for IPython
notebook). The other files are used for the assignment but you don't have to
open them unless we ask you to.

## Opening notebooks

To open Jupyter notebooks, you'll navigate to parent directory of the
assignment in your terminal and run:

    source activate ds100 # omit the `source` part on Windows
    jupyter notebook

This will automatically open the notebook interface in your browser. You can
then browse to a notebook and open it.
