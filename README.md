# Machine Learning Notebooks

This repository contains Jupyter Python notebooks demonstrating some common  Machine Learning Python Models and algorithms. Notebooks contains example code to solve some real-world projects using scikit-learn and tensorflow. 

Developers new to scikit-learn and tensorflow hopefully find them useful to improve their learning process by using real-world datasets.
---
## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes. See deployment for notes on how to deploy the project on a live system.

Simply open the Jupyter notebooks you are interested in using one of the three methods:

- Using Google Colab notebook (i.e. cloud-based Python programming platform). It comes with everyday python packages already installed, like numpy, skit-learn. You need to signup and apply for access before you start using google colab. Once you get the access, you can upload notebooks using File->Upload Notebook. https://colab.research.google.com. One of the unique feature of Google Colab is that you can use a GPU for free in the backend. 

- Using jupyter's notebook viewer

- by cloning this repository and running Jupyter locally. This option lets you play around with the code. In this case, follow the installation instructions below

### Installing

First, you will need to install git, if you don't have it already.

Next, clone this repository by opening a terminal and typing the following commands:

```
$ cd $HOME  # or any other development directory you prefer
$ git clone https://github.com/hatimnaitlho/ml-sklearn.git
$ cd ml-sklearn
```
If you do not want to install git, you can instead download master.zip, unzip it, rename the resulting directory to handson-ml and move it to your development directory.

If you are using google colab or familiar with Python and you know how to install Python libraries, go ahead and install the libraries listed in requirements.txt and jump to the Starting Jupyter section. If you need detailed instructions, please read on.

### Prerequisites

Python 3 is already preinstalled on many systems nowadays. You can check which version you have by typing the following command (you may need to replace `python3` with `python`):

    $ python3 --version  # for Python 3

Any Python 3 version should be fine, preferably 3.5 or above. If you don't have Python 3, I recommend installing it. To do so, you have several options: on Windows or MacOSX, you can just download it from [python.org](https://www.python.org/downloads/). On MacOSX, you can alternatively use [MacPorts](https://www.macports.org/) or [Homebrew](https://brew.sh/). If you are using Python 3.6 on MacOSX, you need to run the following command to install the `certifi` package of certificates because Python 3.6 on MacOSX has no certificates to validate SSL connections (see this [StackOverflow question](https://stackoverflow.com/questions/27835619/urllib-and-ssl-certificate-verify-failed-error)):

    $ /Applications/Python\ 3.6/Install\ Certificates.command

On Linux, unless you know what you are doing, you should use your system's packaging system. For example, on Debian or Ubuntu, type:

    $ sudo apt-get update
    $ sudo apt-get install python3 python3-pip

Another option is to download and install [Anaconda](https://www.continuum.io/downloads). This is a package that includes both Python and many scientific libraries. You should prefer the Python 3 version.

If you choose to use Anaconda, read the next section, or else jump to the [Using pip](#using-pip) section.

## Using Anaconda
Once you have [installed Anaconda](https://docs.anaconda.com/anaconda/install/) (or Miniconda), you can run the following command:

    $ conda env create -f environment.yml

This will give you a conda environment named `mlbook`, ready to use! Just activate it and you will have everything setup
for you:

    $ conda activate mlbook

You are all set! Next, jump to the [Starting Jupyter](#starting-jupyter) section.

## Using pip
If you are not using Anaconda, you need to install several scientific Python libraries that are necessary for this project, in particular NumPy, Matplotlib, Pandas, Jupyter and TensorFlow (and a few others). For this, you can either use Python's integrated packaging system, pip, or you may prefer to use your system's own packaging system (if available, e.g. on Linux, or on MacOSX when using MacPorts or Homebrew). The advantage of using pip is that it is easy to create multiple isolated Python environments with different libraries and different library versions (e.g. one environment for each project). The advantage of using your system's packaging system is that there is less risk of having conflicts between your Python libraries and your system's other packages. Since I have many projects with different library requirements, I prefer to use pip with isolated environments. Moreover, the pip packages are usually the most recent ones available, while Anaconda and system packages often lag behind a bit.

These are the commands you need to type in a terminal if you want to use pip to install the required libraries. Note: in all the following commands, if you chose to use Python 2 rather than Python 3, you must replace `pip3` with `pip`, and `python3` with `python`.

First you need to make sure you have the latest version of pip installed:

    $ python3 -m pip install --user --upgrade pip

The `--user` option will install the latest version of pip only for the current user. If you prefer to install it system wide (i.e. for all users), you must have administrator rights (e.g. use `sudo python3` instead of `python3` on Linux), and you should remove the `--user` option. The same is true of the command below that uses the `--user` option.

Next, you can optionally create an isolated environment. This is recommended as it makes it possible to have a different environment for each project (e.g. one for this project), with potentially very different libraries, and different versions:

    $ python3 -m pip install --user --upgrade virtualenv
    $ python3 -m virtualenv -p `which python3` env

This creates a new directory called `env` in the current directory, containing an isolated Python environment based on Python 3. If you installed multiple versions of Python 3 on your system, you can replace `` `which python3` `` with the path to the Python executable you prefer to use.

Now you must activate this environment. You will need to run this command every time you want to use this environment.

    $ source ./env/bin/activate

On Windows, the command is slightly different:

    $ .\env\Scripts\activate

Next, use pip to install the required python packages. If you are not using virtualenv, you should add the `--user` option (alternatively you could install the libraries system-wide, but this will probably require administrator rights, e.g. using `sudo pip3` instead of `pip3` on Linux).

    $ python3 -m pip install --upgrade -r requirements.txt

Great! You're all set, you just need to start Jupyter now.

## Starting Jupyter
Okay! You can now start Jupyter, simply type:

    $ jupyter notebook

This should open up your browser, and you should see Jupyter's tree view, with the contents of the current directory. If your browser does not open automatically, visit [127.0.0.1:8888](http://127.0.0.1:8888/tree). Click on `index.ipynb` to get started!

Congrats! You have finished the installation of python and required libraries. 


## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details

