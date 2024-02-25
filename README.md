# DL-Template: Python GitHub template with Poetry and Pre-Commit hooks

A template for DL python projects with fastai/pytorch, jupyter notebooks and a standard repository structure.
IT 
also has pre-commit hooks, poetry, mypy and pytest

## Features:
- a standard repository structure
- `.gitignore` - for python, pycharm and vscode files
- `poetry` - for dependency management and virtual environment
- `pytest` setup for success
- `mypy` for type checking
- `pre-commit` hooks:
    - `isort` - to sort `import` statements
    - `ruff` - for linting and static analysis
    - `black` - for source code formatting
    - `docformatter` - for formatting docstrings
    - `mypy` - for typechecking


  
## repository structure
```
/
├── README.md      # edit this file to write your own readme
├── pyproject.toml # edit this file to setup the name and authors of your project
├── .gitignore     # preconfigured ignores for python, pycharm and vscode files
├── src/           # place your source files and packages here
│   ├── your_module.py
│   ├── your_package/
│   │   ├── ... 
│   ├── ...
├── notebooks/     # place your jupyter notebooks here
│   ├── your_notebook.ipynb
│   ├── ...
├── tests/         # place your pytest files here
│   ├── test_your_stuff.py   # example
│   ├── ...
├── .pre-commit-config.yaml  # preconfigured pre-commit hooks
```

## How to use
1. Fork this repository as the basis of your own project
2. Clone the repository to your own computer
3. Follow the setup steps 

## Setup
- edit the `name`/`description`/`version`/`author` fields in `pyproject.toml`

make sure you have poetry installed by running
  ```bash
  poetry --version
  ```
  - > if you don't, visit https://python-poetry.org/docs/#installing-with-the-official-installer

- next , install all tools and dependencies using poetry
  ```bash
  poetry install
  ```
  - > this will also install `pre-commit` for you

- now you can use the poetry virutal environment to run all your tools
  ```bash
  poetry shell
  ```
  
- inside the poetry shell you have jupyter lab available
    ```bash
    jupyter lab
    ```
  
### Optional: pre-commit hooks
- now run `pre-commit` to setup all your tools
  ```bash
  poetry run pre-commit run --all-files
- install your pre-commit hooks into the repository
  ```bash
  poetry run pre-commit install

## Howto
- run all hooks
  ```bash
  poetry run pre-commit run --all-files
  ```
- run tests
  ```bash 
  poetry run pytest
  ```
