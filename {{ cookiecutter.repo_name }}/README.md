{{cookiecutter.project_name}}
==============================

{{cookiecutter.description}}

Project Organization
------------

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

Installation
------------
```.env
$ cookiecutter https://github.com/marutimw/fhai-lineardigression-template.git
$ cd <project-name>
$ make create_environment
$ pipenv shell
```

Testing
------------
```.env
$ make test_environment
$ make unittests
```

List Commands
------------
```.env
$ make

clean               |   Delete all compiled Python files 
create_environment  |   Set up python interpreter environment. Install Python Dependencies. 
data                |   Make Dataset 
lint                |   Lint using flake8 
sync_data_from_s3   |   Download Data from S3 
sync_data_to_s3     |   Upload Data to S3 
sync_models_from_s3 |   Download Models from S3 
sync_models_to_s3   |   Upload Models to S3 
test_environment    |   Test python environment is setup correctly 
unittests           |   Run unittests
```

Note
------------
* Add all the python dependencies to Pipfile and run `pipenv install` to install those dependencies.
* Use `exit` command to escape the virtual environment
* Add environment variables to `.env` file
* Add constants/thresholds to `config.py` file
* All the unittests are inside `tests` directory and each filename starts with `test_<actual-filename>`
* Maintain the same nested folder structure inside `tests` as is present in the `src`

ToDo
------------
* Add framework for performance evaluation
* Add framework for hyper-parameter tuning
* Add drone CI/CD set up
* Add file for versioning