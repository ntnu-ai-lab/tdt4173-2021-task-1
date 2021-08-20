# tdt4173-2021-task-1

This repository contains all resources for Homework 1 of TDT4173 fall 2021.

## Problem Overview


## Setup 

Below follows instructions for getting started. Last year we got a mix of students with all sorts of backgrounds, so we will try to give a detailed set of installation instructions in the sections below.

**TL;DR** for those who are familiar with python and git 
- Python >= 3.6 
- Dependences in [requirements.txt](requirements.txt)

### Dowloading the project 

For those of you familiar with git, all you need to do is clone this repository. If you do not have git, it can be [freely downloaded](https://git-scm.com/downloads) and installed on all major platforms.

```
git clone git@github.com:ntnu-ai-lab/tdt4173-2021-task-1.git
```

This shell command will clone the repository to your local computer. You will be able to find it in the folder you executed the command from. If you don't want to bother with git, just click the green `Code` button in the top right corner of the repository and select the `Download ZIP` option from the dropdown.

### Installing Dependencies 

The boilerplate code provided here was designed with **Python 3.6 or higher** in mind. In particular, it uses [f-strings](https://realpython.com/python-f-strings/) pretty liberally, which will crash for earlier versions of python. If you don't have Python 3.6+, it can be [freely downloaded](https://www.python.org/downloads/) and installed on all major platforms too.

Once you have Python 3.6 or higher up and running, you need to install additional python packages. The main ones used are `jupyter`, `numpy`, `pandas`, `matplotlib`, and `seaborn`. However, an exahstive list of the exact packages and the

**NOTE:** For all the commands mentioned below, it is assumed that the current working directory of your shell is the root folder of this repository (wherever you cloned/downloaded it to). You can change the current working directory in your terminal with:

```
cd /path/to/project  # Linux / MacOS 
cd \path\to\project  # Windows
```

#### Installation with Virtualenv + pip

One of the most common ways to install python packages is with the pip package manager. There are several ways to install it. If you're on Linux, then just use your normal (system) package manager. If you use Homebrew on MacOS, then it can be installed from there. Alternatively, you can [install it using python](https://pip.pypa.io/en/stable/installation/) on all platforms.

When using pip, it is also good practice to install package not on a global/system level, but in "virtual environments" organized for each of your projects. The [virtualenv](https://packaging.python.org/guides/installing-using-pip-and-virtual-environments/) package helps you do this and can be installed through pip:

```
# Install only the virtualenv pacakge globally
python -m pip install --user virtualenv   # ("py -m pip ..." on windows)
# Create and activate a virtual environment with an appropriate python version 
virtualenv --python python3.6 venv  # (or another python version >= 3.6 that you have installed)
source venv/bin/actiate  # (".\venv\Scripts\activate" on windows)
```

This will create a virtual environment in a folder called `venv` that is located in the folder you executed the commands from. All subsequent python packages installed with pip should end up within this folder structure (and not in the global package folder). If you want to scrap all the packages associated with your project later, you can just delete this folder while not having to worry about breaking other projects. It also solves the problem of having to deal with different projects requireing different versions of the same pacakge. After having created and activated your new virtual environment, all the packages required for this project can be installed with:

```
python -m pip -r requirements.txt  # ("py -m pip ..." on windows)
```


#### Installation with Anaconda 

If you use [Anaconda](https://www.anaconda.com/products/individual) to manage your python versions and packages, then you can create a new python environment and install all the dependencies with the following commands.

```
conda create --name tdt4173 python=3.6   # (or another python version >= 3.6)
source activate tdt4173  # (just "activate tdt4173" on windows)
conda install --yes --file requirements.txt
```

### Running a Notebook Server

After you have installed all the dependencies, you can run a notebook server with:

```
jupyter lab
```

This will start a slightly fancier version of [jupyter notebook](https://jupyter.org). It is a single-page application that allows you to navigate, edit, and run python and jupyter notebook files from your browser. By default the server should be exposed at `localhost` port `8888`. If you're running this command from your laptop or desktop computer, it should automatically open in your default web browser. If for some reason not, try manually navigating to `localhost:8888` in your web browser (or copy the full URL from the logging output in the shell you ran the command). If it asks for a password or token, this can also be found in the shell output.

From here, you can start running and editing the files in the project. If you need more help with the interface, there are several [guides online](https://www.youtube.com/watch?v=7wfPqAyYADY).



