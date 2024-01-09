# oztimur-probability Package

## Summary

The `oztimur-probability` package provides a Python implementation of probability distributions. The package includes a parent distribution class and two specific distribution classes: `Gaussian` and `Binomial`. This README provides an overview of the package and explains the purpose of each file.

## Files

### 1. `Generaldistribution.py`

This file contains the `Distribution` class, which serves as the parent class for probability distributions. It provides a basic structure and common functionality that can be inherited by specific distribution classes.

#### Usage:

```python
from .Generaldistribution import Distribution

# Create an instance of the Distribution class
dist = Distribution()

### 2. `Gaussiandistribution.py`

The `Gaussiandistribution.py` file contains the `Gaussian` class, representing a Gaussian (normal) distribution. This class is designed to model continuous random variables with a bell-shaped probability distribution.

#### Gaussian Class:

The `Gaussian` class inherits from the `Distribution` class, providing a foundation for probability distributions. It introduces specific methods and properties related to the Gaussian distribution.

##### Key Properties:

- **`mu`:** Represents the mean (average) of the distribution.
- **`sigma`:** Represents the standard deviation, a measure of the spread of the distribution.


#### Usage:

```python
from .Gaussiandistribution import Gaussian

# Create an instance of the Gaussian class with a specified mean and standard deviation
gaussian_dist = Gaussian(mu=0, sigma=1)

# Access mean and standard deviation properties
mean_value = gaussian_dist.mean
stdev_value = gaussian_dist.stdev

# Calculate Probability Density Function (PDF)
pdf_result = gaussian_dist.pdf(x=2)

### 3. `Binomialdistribution.py`

The `Binomialdistribution.py` file contains the `Binomial` class, representing a binomial distribution. This class is designed to model discrete random variables that represent the number of successes in a fixed number of independent Bernoulli trials.

#### Binomial Class:

The `Binomial` class inherits from the `Distribution` class, providing a foundation for probability distributions. It introduces specific methods and properties related to the binomial distribution.

##### Key Properties:

- **`trials`:** Represents the number of independent Bernoulli trials.
- **`probability`:** Represents the probability of success in a single trial.

#### Usage:

```python
from .Binomialdistribution import Binomial

# Create an instance of the Binomial class with a specified number of trials and success probability
binomial_dist = Binomial(n=10, p=0.5)

# Access properties such as the number of trials and success probability
num_trials = binomial_dist.n
success_prob = binomial_dist.p

# Calculate Probability Density Function (PDF)
pdf_result = binomial_dist.pdf(k=5)

## Installation
pip install oztimur-probability

## Dependencies

The package requires a Python environment (3.6 and above) and has the following external dependencies:

- `matplotlib`: A 2D plotting library for creating visualizations in Python.

To install both the package and its dependencies, you can use the following `pip` command:

```bash
pip install oztimur-probability[all]
