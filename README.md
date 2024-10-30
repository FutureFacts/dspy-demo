# DSPy Demo <!-- omit in toc -->

![Python version](https://img.shields.io/badge/python-3.12-blue) [![License](https://img.shields.io/badge/license-MIT-green)](./LICENSE) [![Code Style](https://img.shields.io/badge/code%20style-black-000000)](https://github.com/psf/black)
![PyTorch](https://img.shields.io/badge/PyTorch-%23EE4C2C.svg?style=for-the-badge&logo=PyTorch&logoColor=white)

- [Installation (Prerequisites)](#installation-prerequisites)
  - [MacOS](#macos)
    - [Pyenv](#pyenv)
    - [Poetry](#poetry)
  - [Windows](#windows)
- [Project Setup](#project-setup)

## Installation (Prerequisites)

In its current form this application has been tested to work (version 0.1.0) on MacOS.

This project depends on:

- `pyenv`: ensuring that people use the same version of python.
- `poetry`: ensuring that the *exact* dependencies will be installed, irrespective of when it is
  installed. This does not happen with a `requirements.txt` file, even when you pin the primary
  dependencies.

### MacOS

#### Pyenv

It is straightforward to install pyenv on MacOS. Full instructions can be found on the
[project website](https://github.com/pyenv/pyenv#installation).

Basically, in your terminal run:

```bash
brew update
brew install pyenv
```

and depending on your shell follow the instructions at
[step 2](https://github.com/pyenv/pyenv#basic-github-checkout).

#### Poetry

The installation of [poetry](https://github.com/python-poetry/poetry) is the same on MacOS/Linux and
Windows when using WSL2.

```bash
curl -sSL https://install.python-poetry.org | python3 -
```

After that you need to make sure that is in your `PATH`:

```bash
export PATH=~/.poetry:$PATH
```

or to do it permanently (assuming zsh, or adjust it to whatever shell you are using):

```bash
echo 'export PATH="~/.poetry:$PATH"' >> ~/.zshrc
exec $SHELL
```

### Windows

In case there is anyone who wants to set it up on Windows, go to
[this website](https://www.apple.com/nl/shop/buy-mac) and follow the instructions and then go to
[this README](https://github.com/nielsgl/dspy-demo?tab=readme-ov-file#macos).

## Project Setup

Clone the repository:

```bash
git clone git@github.com:nielsgl/dspy-demo.git
cd dspy-demo
```

Install the required python version (as defined in `.python-version`). Running below will ensure it
is installed or skip if it already is.

```bash
pyenv install `cat .python-version`
```

Next we install the dependencies, as you normally would do from a `requirements.txt` file, but since
that is bad we won't use this, ever. This command will create a virtual environment for you if it
doesn't exist and install all dependencies as specified in the `poetry.lock` file.

```bash
poetry install
```

Finally, we are ready to play with it so you can open up the `dspy-demo.ipynb` notebook in the notebooks folder.
