# spaceship-titanic

This repo will be used in a kata at two COM-DEV sessions, the first on 3 October 2023. The working problem is extracted from Kaggle website, where a description of the problem as well as the dataset is provided. We will work with the problem [Spaceship Titanic](https://www.kaggle.com/competitions/spaceship-titanic/). Our task is to develop a Machine Learning (ML) model to predict which passengers are transported to an alternate dimension.

The work will be divided in two sessions:

- One session dedicated to setup a Python environment with all the dependencies required for working in a ML project. This session will introduce the use of Jupyter notebook and the libraries [Pandas](https://pandas.pydata.org/docs/getting_started/index.html) and [Seaborn](https://seaborn.pydata.org/tutorial/introduction.html) for the task of Data Analysis. In this session we will analyze and visualice the data and their relationships and try to prepare the data for being given later to a ML model.

- A second session dedicated to select, train and evalute ML models by employing the library [scikit-learn](https://scikit-learn.org/stable/getting_started.html), with the objective of solving the Spaceship-Titanic problem.

## Installation instructions

### Install Poetry and Pyenv
We use Pyenv to manage different installations of Python in the same machine and we use Poetry to manage the Python packages of a given project.

- To install Poetry (<https://python-poetry.org/docs/>):

```
  curl -sSL https://install.python-poetry.org | python3 -
```

- Check that Poetry is well installed:
```
poetry --version
```

- Install Pyenv (<https://brain2life.hashnode.dev/how-to-install-pyenv-python-version-manager-on-ubuntu-2004>):

```
sudo apt-get update; sudo apt-get install make build-essential libssl-dev zlib1g-dev libbz2-dev libreadline-dev libsqlite3-dev wget curl llvm libncursesw5-dev xz-utils tk-dev libxml2-dev libxmlsec1-dev libffi-dev liblzma-dev

curl https://pyenv.run | bash
```

- Follow the Pyenv post-installation instructions on the terminal. It may ask you to do something like adding some lines to a Bash Terminal configuration file.

Go to your personal folder, and edit the file .bashrc with gedit (use the command `gedit .bashrc`), including at the end the following lines:

```
# Pyenv
export PATH="$HOME/.pyenv/bin:$PATH"
eval "$(pyenv init --path)"
eval "$(pyenv virtualenv-init -)"
```

- Check that Pyenv is well installed:
```
pyenv --version
```

### Install the Python version you need
For this repository the 3.9.13 Python version is used. Proceed as

```
pyenv install 3.9.13
cd spaceship-titanic
pyenv local 3.9.13
```

### Setup your Poetry project
- Go to your project folder with `cd spaceship-titanic`

- Tell Poetry to use this particular version of Python with: 
```
poetry env use 3.9.13
```

- If you have a pyprojec.toml file then you can execute the installation command.
```
poetry install
```

## Working with VSCode and Jupyter Notebook

- Select the virtual environment (by default a folder .venv inside the project folder) in VSCode Interpreter selection.
- Open the example Jupyter notebook and select the same venv as the Kernel.
- Then you will be able to run the cells of the notebook.
