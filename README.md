



<h3 align="center"> Linear Regression and Concepts of Under/Overfitting and Regularization for Diabetes Dataset</h3>

<div align="center">

  [![code coverage](coverage.svg "Code coverage")]()
</div>

---


## 🧐 About <a name = "about"></a>

In this machine learning project, I aim to analyze the diabetes dataset, which contains baseline measurements and disease progression data for 442 diabetes patients. I will apply linear regression techniques, including univariate and multivariate regression, to predict the quantitative measure of disease progression based on the available variables. Additionally, I will explore the concepts of underfitting, overfitting, and regularization to improve the model's performance and prevent overfitting.

## 🔖 Project structure

```
Project_folder/
|- bin/          # contains scripts and main files that should be run
|- config/       # config files
|- notebooks/    # notebooks for EDA, exploration, predictions and results and conclusions
|- src/          # source code - contains functions
|- tests/        # Test files should mirror the src folder
|- Makefile      # automatize taks through make utility
```

## 🏁 Getting Started <a name = "getting_started"></a>
These instructions will get you a copy of the project up and running on your local machine for development and testing purposes.

### Prerequisites
Setup your environement and install project dependencies
```
conda create -n my_project python=3.10
source activate my_project

python -m pip install pip-tools
pip-compile --output-file requirements.txt requirements.in requirements_dev.in
python -m pip install -r requirements.txt
```

### Installing

## 🔧 Running the tests
Tests are implemented in ./tests, you need to run the following command to run them.
```
make tests
```


