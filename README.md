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


