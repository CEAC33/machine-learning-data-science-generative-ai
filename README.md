# machine-learning-data-science-generative-ai

## Statistics and Probability Refresher

### Types of Data (Numerical, Categorical, Ordinal)

Many Flavors of Data

<img width="556" alt="Screenshot 2023-10-06 at 19 27 46" src="https://github.com/CEAC33/machine-learning-data-science-generative-ai/assets/51218415/d4cb6f04-6634-445b-ad5b-66689bd4d58e">

**Major Types of Data**
- Numerical
- Categorical
- Ordinal

**Numerical**

<img width="378" alt="Screenshot 2023-10-06 at 19 36 17" src="https://github.com/CEAC33/machine-learning-data-science-generative-ai/assets/51218415/73396f48-9c10-47cd-8eaa-95c9aa5ff4bf">

- Represents some sort of quantitative measurement
  - Heights of people, page load times, stock prices, etc.
- Discrete Data
  - Integer based: often counts of some event
    - How many purchases did a customer make in a year?
    - How many times did I flip "heads"?
- Continuous Data
  - Has an infinite number of possible values
    - How much time did it take for a user to chek out?
    - How much rain fell on a given day?

**Categorical**

<img width="437" alt="Screenshot 2023-10-06 at 19 38 08" src="https://github.com/CEAC33/machine-learning-data-science-generative-ai/assets/51218415/b109acfd-2ab7-43c5-8de5-36004a284653">

- Qualitative data that has no inherent mathematical meaning
  - Gender, Yes/No (Binary Data), Race, State of Residence, Product Category, Political Party, etc.
- You can assign numbers to categories in order to represent them more compactly, but the numbers don't have mathematical meaning

**Ordinal**

<img width="255" alt="Screenshot 2023-10-06 at 19 42 08" src="https://github.com/CEAC33/machine-learning-data-science-generative-ai/assets/51218415/7d367d38-4594-4308-8716-89cb48f58932">

- A mixture of numerical and categorical
- Categorical data has mathematical meaning
- Example: movie ratings on a 1-5 scale.
  - Ratings must be 1, 2, 3, 4, or 5
  - But these values have mathematical meaning; 1 means it's a worse movie than a 2

### Mean, Median, Mode

**MEAN**

- AKA Average
- Sum / number of samples
- Example:
  - Number of children in each house on my street
    
0, 2, 3, 2, 1, 0, 0, 2, 0
The MEAN is (0+2+3+2+1+0+0+2+0) / 9 = 1.11

**MEDIAN**

- Sort the values, and take the value at the midpoint
- Example:

0, 2, 3, 2, 1, 0, 0, 2, 0

Sort it:

0, 0, 0, 0, **1**, 2, 2, 2, 3

- If you have an even number of samples, take the average of the two in the middle
- Median is less susceptible to outliers than the mean
  - Example: mean household income in the US is $72,641, but the median is only $51,939 because the mean is skewed by a handful of billionaires
  - Median better represents the "typical" American in this example

**MODE**

- The most common value in a data set
  - Not relevant to continuous numerical data
- Back to our number of kids in each house example:

0, 2, 3, 2, 1, 0, 0, 2, 0

How many of each value are there?

0: 4, 1: 1, 2: 3, 3: 1

The MOODE is 0

### Using mean, median, and modoe in Python

**Mean vs. Median**

Let's create some fake income data, centered around 27,000 with a normal distribution and standard deviation of 15,000, with 10,000 data points. (We'll discuss those terms more later, if you're not familiar with them.)

Then, compute the mean (average) - it should be close to 27,000:

```python
import numpy as np

incomes = np.random.normal(27000, 15000, 10000)
np.mean(incomes)
# 26933.720599154913
```

We can segment the income data into 50 buckets, and plot it as a histogram:

```python
%matplotlib inline
import matplotlib.pyplot as plt
plt.hist(incomes, 50)
plt.show()
```

Now compute the median - since we have a nice, even distribution it too should be close to 27,000:

```python
np.median(incomes)
# 27092.39320043316
```

Now we'll add Jeff Bezos into the mix. Darn income inequality!

```python
incomes = np.append(incomes, [1000000000])
```

The median won't change much, but the mean does:

```python
np.median(incomes)
#27092.571036571815
```

```python
np.mean(incomes)
#126921.0284963053
```

**Mode**

Next, let's generate some fake age data for 500 people:

```python
ages = np.random.randint(18, high=90, size=500)
ages
```

```python
from scipy import stats
stats.mode(ages)
# ModeResult(mode=array([20]), count=array([15]))
```
