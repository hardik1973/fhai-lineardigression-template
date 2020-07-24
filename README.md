# Cookiecutter Data Science

_A logical, reasonably standardized, but flexible project structure for doing and sharing data science work._



Requirements to use the cookiecutter template:
-----------
 - Python 2.7 or 3.5
 - [Cookiecutter Python package](http://cookiecutter.readthedocs.org/en/latest/installation.html) >= 1.4.0: This can be installed with pip by or conda depending on how you manage your Python packages:

``` bash
$ pip install cookiecutter
```

or

``` bash
$ conda config --add channels conda-forge
$ conda install cookiecutter
```


To start a new project, run:
------------

```$ cookiecutter https://github.com/drivendata/cookiecutter-data-science```


[![asciicast](https://asciinema.org/a/244658.svg)](https://asciinema.org/a/244658)


The resulting directory structure
------------

The directory structure of your new project looks like this: 

```
    ├── LICENSE
    ├── Makefile           <- Makefile with commands like `make data` or `make train`
    ├── README.md          <- The top-level README for developers using this project.
    ├── data
    │   ├── interim        <- Intermediate data that has been transformed.
    │   ├── processed      <- The final, canonical data sets for modeling.
    │   └── raw            <- The original, immutable data dump.
    |
    |                         Naming convention is a number (for ordering),
    |                         date in the format DD_MM_YYYY,
    |                         the creator's first-name,
    |                         and a short `-` delimited description, e.g.
    |                         `1.0-16_07_2020-maruti-linkedin-dump-v1`.          
    │
    ├── models             <- Trained and serialized models, model predictions, or model summaries.
    |                         Naming convention is a number (for ordering),
    |                         date in the format DD_MM_YYYY, 
    |                         the creator's first-name, 
    |                         and a short `-` delimited description, e.g. 
    |                         `1.0-16_07_2020-maruti-initial-data-exploration`.      
    │
    ├── notebooks          <- Jupyter notebooks. 
    |                         Naming convention is a number (for ordering),
    │                         the creator's first-name, 
    |                         and a short `-` delimited description, e.g.
    │                         `1.0-maruti-initial-data-exploration`.
    ├── tests
    │   ├── integration    <- Place for testing scripts for integration tests
    │       ├── test_data  <- Place to store data for integration tests
    │   ├── unit           <- Place for testing scripts for unittests
    │
    ├── references         <- Data dictionaries, manuals, and all other explanatory materials.
    │
    ├── reports            <- Generated analysis as HTML, PDF, LaTeX, etc.
    │   └── figures        <- Generated graphics and figures to be used in reporting
    │
    ├── src                <- Source code for use in this project.
    │   ├── __init__.py    <- Makes src a Python module
    │   │
    │   ├── data           <- Scripts to download or generate data
    │   │   └── make_dataset.py
    │   │
    │   ├── features       <- Scripts to turn raw data into features for modeling
    │   │   └── build_features.py
    │   │
    │   ├── models         <- Scripts to train models and then use trained models to make
    │   │   │                 predictions
    │   │   ├── predict_model.py
    │   │   └── train_model.py
    │   │
    │   └── visualization  <- Scripts to create exploratory and results oriented visualizations
    │       └── visualize.py
    │
    └── tox.ini            <- tox file with settings for running tox; see tox.readthedocs.io


--------
```