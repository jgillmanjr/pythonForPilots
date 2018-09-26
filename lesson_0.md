pythonForPilots - Lesson 0 - Preflight
==============
So you're interested in tinkering with Python. Excellent!

## Prerequisites

Before we begin, let's get some things taken care of first.

### Installing Python

My preferred method for this is using [Miniconda](https://conda.io/docs/user-guide/install/index.html) for a couple of reasons:
1. You don't need root level / administrative privileges on the machine you're using to install it
1. It doesn't come with all the data science packages that Anaconda does.

If you do happen to dabble in data science already, it may be worth it to install Anaconda.

I'll defer to the installation documentation instead of reproducing it here. Link is above. Just make sure you add it to your path.

### Configuration

Now that you have either Miniconda or Anaconda (which I'll just refer to as Conda from now on) installed, let's get some initial housekeeping taken care of.

For Windows users, you'll perform these actions in the Anaconda prompt (since I don't use Windows, I'm unsure if it's called the same if you're using Miniconda - I'm just looking at the documentation). Linux users will just run these commands at a terminal.


Let's make sure that your Conda installation is up to date:
```
conda update conda
```

Even though you just installed Conda, there's a good chance there will still be an update. If so, you'll see something like this:
```
Fetching package metadata .............
Solving package specifications: .

Package plan for installation in environment /home/jgillman/anaconda3:

The following packages will be UPDATED:

    conda: 4.3.34-py36_0 conda-forge --> 4.5.11-py36_0 conda-forge

Proceed ([y]/n)? y

conda-4.5.11-p 100% |################################################################################################################################| Time: 0:00:00   2.56 MB/s
```

Once that's out of the way, let's prepare an environment for these set of lessons:

```
conda create -n pythonForPilots python=3.7 pip
```

Basically, what we're doing is creating an environment called `pythonForPilots` that will run Python 3.7 and install pip into the environment. This is important so that `pip` from the root environment isn't used when packages are installed. I'll discuss what `pip` is in a later lesson.

Ultimately though, this will keep things nice and contained.

Anyway, you'll see something like this and be asked to proceed:

```
Solving environment: done

## Package Plan ##

  environment location: /home/jgillman/anaconda3/envs/pythonForPilots

  added / updated specs:
    - pip
    - python=3.7


The following packages will be downloaded:

    package                    |            build
    ---------------------------|-----------------
    wheel-0.31.1               |        py37_1001          62 KB  conda-forge
    python-3.7.0               |       h5001a0f_1        22.1 MB  conda-forge
    libffi-3.2.1               |       hfc679d8_5          51 KB  conda-forge
    pip-18.0                   |           py37_1         1.7 MB  conda-forge
    setuptools-40.4.0          |        py37_1000         555 KB  conda-forge
    certifi-2018.8.24          |        py37_1001         139 KB  conda-forge
    ------------------------------------------------------------
                                           Total:        24.6 MB

The following NEW packages will be INSTALLED:

    bzip2:           1.0.6-h470a237_2     conda-forge
    ca-certificates: 2018.8.24-ha4d7672_0 conda-forge
    certifi:         2018.8.24-py37_1001  conda-forge
    libffi:          3.2.1-hfc679d8_5     conda-forge
    libgcc-ng:       7.2.0-hdf63c60_3     conda-forge
    libstdcxx-ng:    7.2.0-hdf63c60_3     conda-forge
    ncurses:         6.1-hfc679d8_1       conda-forge
    openssl:         1.0.2p-h470a237_0    conda-forge
    pip:             18.0-py37_1          conda-forge
    python:          3.7.0-h5001a0f_1     conda-forge
    readline:        7.0-haf1bffa_1       conda-forge
    setuptools:      40.4.0-py37_1000     conda-forge
    sqlite:          3.25.1-hb1c47c0_0    conda-forge
    tk:              8.6.8-ha92aebf_0     conda-forge
    wheel:           0.31.1-py37_1001     conda-forge
    xz:              5.2.4-h470a237_1     conda-forge
    zlib:            1.2.11-h470a237_3    conda-forge

Proceed ([y]/n)?
```

Once done, you can enter the environment like so:

```
source activate pythonForPilots
```

To get out of the environment:

```
source deactivate
```

From here on out, for each lesson you'll want to make sure you're in the environment.


## Executing the Code
There are a few different ways to run the code and work along with the lessons:

1. Create a script and then run it from the command line.
1. Use IPython and run the code interactively from a terminal.
1. Use Jupyter Notebook and run the code interactively from a web interface.

### Create and run a script
This is the most straight forward. You just create a script with your favorite text editor and then run it:
```
python script.py
```

Easy.

### IPython
IPython is nice because you can interactively run your code.

To install, make sure you're in your Conda environment and:
```
pip install ipython
```

Then to use it:
```
ipython

Python 3.7.0 (default, Jun 28 2018, 13:15:42)
Type 'copyright', 'credits' or 'license' for more information
IPython 6.5.0 -- An enhanced Interactive Python. Type '?' for help.

In [1]: a = 1

In [2]: b = 2

In [3]: c = a + b

In [4]: print(c)
3

In [5]:

```
And to exit, hit `CTRL+D`

### Jupyter Notebook
Jupyter Notebook is similar to IPython, but it uses a web interface and offers numerous other niceties.

I think instead of trying to stuff information about that in here, I'll create a lesson for installation and usage. Please note that I am **not** an expert on all the things you can do with it.

If you want, you can also look at the documentation [here](https://jupyter.org/install) and work from there. Besides, it will probably take me a hot minute to write a lesson on that anyways.

## Recap

So for this lesson, you should have installed Conda and subsequently created an environment called `pythonForPilots` that uses Python 3.7.

You should also know a couple of the different ways to run python code.

If you have any questions, create an issue and I'll try to answer them.
