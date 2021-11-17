[![Actions Status](https://github.com/Allegheny-Mozilla-Fellows/facial_recognition_bias/workflows/build/badge.svg)](https://github.com/Allegheny-Mozilla-Fellows/facial_recognition_bias/actions)

# Table of contents

* [About](#about)
* [Features](#features)
* [Installation](#installation)
* [Run](#run)
  + [With Poetry(Recommended)](#run)
  + [Without Poetry](#Without-Poetry)
* [Development info](#Development-info)
* [Testing](#Testing)
  + [Automated Testing](#automated-testing)
  + [Code Linting](#Code-linting)
* [Contributing](#contributing)
* [Reading Material](#Reading-Material)
* [Ethical discussions](#ethical-discussions)
* [Future work](#future-work)
* [Data used](#data-used)
* [Contact](#contact)

## About

Facial recognition software is used in many industries, including but not limited to law enforcement, airports, healthcare facilities, technology manufacturing companies. As facial recognition technologies gain popularity there are some privacy and ethical concerns rising regarding the development and use of these tools. According to a report by the [National Institute of Standards and Technology](https://www.nist.gov/news-events/news/2019/12/nist-study-evaluates-effects-race-age-sex-face-recognition-software), comercial facial recognition tools exhibited biases with age, gender and race.This is an important issue because biased facial recognition technology in law enforcment may lead to false accusations and arrests, or in airports it may cause delayed flights.
Therefore the purpose of this project is to highlight ethical issues with face recognition technologies, compare efficiency of different classification algorithms and raise questions about development and use of face recognition tools.
The project is funded by Mozilla Foundation and it will be used in AI course at Allegheny College. Please visit the [Allegheny Ethical CS](https://csethics.allegheny.edu/) for more information.

## Features

- Gender classification(binary)

- Experiment with models by adjusting the training data

- Compare classification approaches:

  - Convolution Neural Network(CNN)
  - Multi-layer Perception(MLP)
  - Random Forest(RandomForest)
  - Support Vector(SVM)

## Installation

- Clone the source code onto your machine

    With HTTPS:

    ```https://github.com/Allegheny-Mozilla-Fellows/facial_recognition_bias.git```

    or With SSH:

    ```git@github.com:Allegheny-Mozilla-Fellows/facial_recognition_bias.git```

- Install Poetry(Recommended)

    Poetry is a tool for dependency managment and packaging in Python. Please follow the documentation [here](https://python-poetry.org/docs/#installation) on how to install poetry on your machine

## Run

### With Poetry(Recommended)

Use `poetry install` to install dependencies. Please refer to poetry documentation [here](https://python-poetry.org/docs/basic-usage/#installing-dependencies) for more info about dependency installation.

Please note that installation process may take a while.

After entering the virtual environment and installing the dependencies please refer to the following links for the detailed info on how to run each classifier.

- [Convolution Neural Network(CNN)](src/CNN/README.md)
- [Multi-layer Perception(MLP)](src/MLP/README.md)
- [Random Forest(RandomForest)](src/RandomForest/README.md)
- [Support Vector(SVM)](src/SVM/README.md)

### Without Poetry

Alternatively all dependencies required for this project will need to be installed
locally on your machine. You may use `pip` for that purpose.

```python3 -m pip install --upgrade pip```

```pip install package_name```

After installing all the dependencies please refer to the following links for the detailed info on how to run each classifier.

- [Convolution Neural Network(CNN)](src/CNN/README.md)
- [Multi-layer Perception(MLP)](src/MLP/README.md)
- [Random Forest(RandomForest)](src/RandomForest/README.md)
- [Support Vector(SVM)](src/SVM/README.md)

## Development info

When under developmnet always install the dependencies with `poetry install` and run the program with `poetry run python program_name`.

You can add new dependencies to `pyproject.toml` either manually or by `poetry add package_name`. Please refer to documentation [here](https://python-poetry.org/docs/cli/#add) for more information.

Use `poetry update` for updating the dependencies to their latest versions as neccessary. Please refer to documentation [here](https://python-poetry.org/docs/cli/#update) for more information.

Please use `pre-commit` hooks for linting the code. Install pre-commit with `pip install pre-commit` or follow the documentation [here](https://pre-commit.com/#install). After cloning the repository locally run `pre-commit install` to install pre-commit into your git hooks.

NOTE: You would have to run `pre-commit install` every time you clone a repository. Please refer to documentation [here](https://pre-commit.com/#usage) for more information.

NOTE: You will not be able to complete commit unless all the linters pass. Only staged changes will be checked at the time of commit.

## Testing

### Automated Testing

Developers of this program can run the test suite with `Pytest`

`poetry run pytest`

### Code linting

Use `poetry run pre-commit run --all-files` to check the code with linters and get the diagnostic info.

Currently this project uses following linters:

- pylint
- pydocstyle
- flake8
- black

You may add more linters to `.pre-commit-config.yaml`

## Contributing

We welcome everyone who is interested in helping improve this project! If you are interested in being a contributor, please review our [Code of Conduct](./CODE_OF_CONDUCT.md) and [Guidelines for Contributors](./CONTRIBUTING.md) before raising an issue, or beginning a contribution.

To create a pull request please follow this [template](./pull_request_template.md)

## Future work

Currently this project mainly examines the gender biases, and how easy it is to manipulate with the classification algorithm by modifing the training data. Users of this program can experiment with classifiers and see that more diverse the data more precicise the trained model will be. Please refer to README.md for each individual classifier for more information about how to experiment with this project. This work also allows to compare the efficency of various classification algorithms. The project can further be extended by examining biases with race and age, and adding more classification algorithms for comparison, or adding feature to visualise the efficiency of the classifiers.

## Reading Material

Here is the list of articles that may give the user more insights into the biases in facial recognition technologies.

- [facial-recognition-race](https://www.cbc.ca/news/technology/facial-recognition-race-1.5403899)

- [facial-recognition-software-dangers](https://www.nytimes.com/2020/06/25/technology/facial-recognition-software-dangers.html?smid=tw-share)

- [Facial recognition to 'predict criminals' sparks row over AI bias](https://www.bbc.com/news/technology-53165286)

- [the-computer-got-it-wrong-how-facial-recognition-led-to-a-false-arrest-in-michig](https://www.npr.org/2020/06/24/882683463/the-computer-got-it-wrong-how-facial-recognition-led-to-a-false-arrest-in-michig)

- [google-ai-will-no-longer-use-gender-labels-like-woman-or-man-on-images-of-people-to-avoid-bias](https://www.businessinsider.in/tech/news/google-ai-will-no-longer-use-gender-labels-like-woman-or-man-on-images-of-people-to-avoid-bias/articleshow/74227834.cms)

- [gender-skin-tone-facial-recognition-improvement](https://blogs.microsoft.com/ai/gender-skin-tone-facial-recognition-improvement/)

## Ethical Discussions

- Gender classification tools are usually binary, what ethical issues may this lead to? Why?

- What are some of the ways we can prevent biases in face recognition technologies as developers and as users?

- Which industries should be allowed to use facial recognition tools, who should not? Why?

## Data used

The images used in this project are retrieved from [Kaggle](https://www.kaggle.com/) and are stored in file `data/images` directory. File stores about 10 000 face images. The images are annotated with age, gender and ethnicity. The images are cropped and aligned.

The labels of each face image is embedded in the file name, formatted like
age_gender_race_date&time.jpg

- age is an integer from 0 to 116, indicating the age
- gender is either 0 (male) or 1 (female)
- race is an integer from 0 to 4, denoting White, Black, Asian, Indian, and Others (like Hispanic, Latino, Middle Eastern).

More information on data can be found [here](https://susanqq.github.io/UTKFace/).

## Contact

If you have any questions or concerns about this project please contact:

- Dr. Jumadinova(jjumadinova@allegheny.edu)
- Teona Bagashvili(bagashvilit@allegheny.edu)