# python-how-to

How to set up and use Python

There are multiple ways to do this.
The simpler ways require less set up but limit the ways you can use it.
The complicated ways require more set up but give you a lot more functionality.
Use what you're comfortable with for the purposes that you need it.
Don't feel the need to try something more complicated, since it's probably going to cause you headaches.

* [Novice](#novice-setup)
* [Experienced](#experienced-setup)
* [Pro](#pro-setup)

# Novice setup

1. Make an account on [Repl.it](https://repl.it)
2. Make a new Python repl for each script you want to run

## Pros

* No set up, required
* Installing packages is handled for you

## Cons

* Can't run arbitrary code files, you can only run the `main.py` file
* Can't use your own text editor, need online access

# Experienced setup

You can install Python using the language installer [directly from their website](https://www.python.org/downloads/) or using a package manager via the terminal.
These will install Python to your computer.
Some package managers for various operating systems include:

* [Scoop](https://scoop.sh/) (Windows)
* [Homebrew](https://brew.sh/) (macOS)
* [Apt](https://wiki.debian.org/Apt) (Debian and related Linux distributions like Ubuntu, elementaryOS)
* [pkg_add](https://www.openbsd.org/faq/faq15.html) (OpenBSD and related Unix distributions)
* etc

## Pros

* Local development, no internet required
* Run whatever scripts you want
* Comes with the Python package manager `pip`
* Use whatever tool for writing code you want, like [PyCharm](https://www.jetbrains.com/pycharm/) or [Visual Studio Code](https://code.visualstudio.com/)

## Cons

* Requires some setup
* Installing the language and various tools for writing code can use up space on your computer

# Pro setup

We can use tools that create isolated environments to manage packages.
This is helpful when you have different projects with conflicting packages versions, or other requiements.
The tool we're going to use to accomplish this is [Miniconda](https://docs.conda.io/en/latest/miniconda.html).

1. Download the [Miniconda installer for your operating system](https://docs.conda.io/en/latest/miniconda.html)
2. Open the terminal and run the installer, following the prompts.
3. Install the [mamba](https://github.com/mamba-org/mamba) tool (it works as a replacement for conda and is much faster)

```shell
conda install conda-forge::mamba
```

You can now install whatever packages you want with, including different versions of Python, with `mamba install`.

## Pros

* All of the pros from the [experienced setup](#experienced-setup)
* Allows installation of multiple versions of Pythons or specific packages
* Can also manage packages from other langauges, such as R or Rust

## Cons

* Requires multiple tools to be installed, many through the command line
* Switching and managing environments can be complicated, depending on what you're doing
