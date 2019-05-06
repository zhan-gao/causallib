[![Build Status](https://travis-ci.org/IBM/causallib.svg?&branch=master)](https://travis-ci.org/IBM/causallib)
# IBM Causal Inference Library
A Python package for computational inference of causal effect.

## Description
Causal inference analysis allows estimating of the effect of intervention
on some outcome from observational data.
It deals with the selection bias that is inherent to such data.  

This python package allows creating modular causal inference models
that internally utilize machine learning models of choice,
and can estimate either individual or average outcome given an intervention.
The package also provides the means to evaluate the performance of the 
machine learning models and their predictions.

The machine learning models must comply with scikit-learn's api 
and contain `fit()` and `predict()` functions. 
Categorical models must also implement `predict_proba()`. 

## Installation
```bash
pip install git+https://github.com/IBM/causallib.git
```

##Usage
In general, the package is imported using the name `causallib`. 
For example, use 
```Python
from sklearn.linear_model import LogisticRegression
from causallib.estimation import IPW 
ipw = IPW(LogisticRegression())
```
