# Applied machine learning 

Machine learning is the practice of teaching computers how to learn patterns from data, often for making decisions or predictions.

Can break down into:


![](https://elitedatascience.com/wp-content/uploads/2018/05/What-Goes-Into-a-Successful-Model.jpg)


---

- Model - a set of patterns learned from data.

- Algorithm - a specific ML process used to train a model.

- Training data - the dataset from which the algorithm learns the model.

- Test data - a new dataset for reliably evaluating model performance.

- Features - Variables (columns) in the dataset used to train the model.

- Target variable - A specific variable you're trying to predict.

- Observations - Data points (rows) in the dataset.


![](https://elitedatascience.com/wp-content/uploads/2017/06/primary-school-example-terms.jpg)


For example, let's say you have a dataset of 150 primary school students, and you wish to predict their Height based on their Age, Gender, and Weight...

You have 150 observations...

1 target variable (Height)...

3 features (Age, Gender, Weight)...

You might then separate your dataset into two subsets:

Set of 120 used to train several models (training set)

Set of 30 used to pick the best model (test set)


## Machine Learning Tasks

1- Supervised Learning:

- Supervised learning includes tasks for "labeled" data (i.e. you have a target variable).

- Each observation must be labeled with a "correct answer."

- use:
 Regression is the task for modeling continuous target variables.

Classification is the task for modeling categorical (a.k.a. "class") target variables.

2- Unsupervised Learning

- Unsupervised learning includes tasks for "unlabeled" data (i.e. you do not have a target variable).

- use : 
Clustering is the most common unsupervised learning task, and it's for finding groups within your data.


 
## Exploratory Analysis

Exploratory Data Analysis refers to the critical process of performing initial investigations on data so as to discover patterns,to spot anomalies,to test hypothesis and to check assumptions with the help of summary statistics and graphical representations.

- First

you'll want to answer a set of basic questions about the dataset:

How many observations do I have?

How many features?

What are the data types of my features? Are they numeric? Categorical?

Do I have a target variable?

Do the columns make sense?

Do the values in those columns make sense?

Are the values on the right scale?

Is missing data going to be a big problem based on a quick eyeball test?


- Second : Plot Numerical Distributions

it can be very enlightening to plot the distributions of your numeric features.

Often, a quick and dirty grid of histograms is enough to understand the distributions.

Here are a few things to look out for:

Distributions that are unexpected

Potential outliers that don't make sense


- Third: Plot Categorical Distributions

- fourth: Plot Segmentations

- finally : Study Correlations


## Data Cleaning 

Data cleaning is the process of fixing or removing incorrect, corrupted, incorrectly formatted, duplicate, or incomplete data within a dataset. ... If data is incorrect, outcomes and algorithms are unreliable, even though they may look correct.

- First : Remove Unwanted observations(duplicate and irrelevant)

- second : Fix Structural Errors

Structural errors are those that arise during measurement, data transfer, or other types of "poor housekeeping."

For instance, you can check for typos or inconsistent capitalization. This is mostly a concern for categorical features, and you can look at your bar plots to check.


- third: Filter Unwanted Outliers

outliers are innocent until proven guilty. You should never remove an outlier just because it’s a "big number." That big number could be very informative for your model.

- finally : Handle Missing Data

Dropping observations that have missing values

Imputing the missing values based on other observations


## Feature Engineering 

Feature engineering is about creating new input features from your existing ones.
In general, you can think of data cleaning as a process of subtraction and feature engineering as a process of addition.


- First : Infuse Domain Knowledge

- second: Create Interaction Features

The first of these heuristics is checking to see if you can create any interaction features that make sense. These are combinations of two or more features.


example :

 Let's say we already had a feature called 'num_schools', i.e. the number of schools within 5 miles of a property.
Let's say we also had the feature 'median_school', i.e. the median quality score of those schools.
However, we might suspect that what's really important is having many school options, but only if they are good.
Well, to capture that interaction, we could simple create a new feature 'school_score' = 'num_schools' x 'median_school'


- Third : Combine Sparse Classes


- Fourth: Add a Dummy variables 

Dummy variables are a set of binary (0 or 1) variables that each represent a single class from a categorical feature


- Finally: Remove Unused Features

Unused features are those that don’t make sense to pass into our machine learning algorithms. Examples include:

ID columns

Features that wouldn't be available at the time of prediction

Other text descriptions



## Algorithm Selection

- Linear Regression.
- Logistic Regression.
- Linear Discriminant Analysis.
- Classification and Regression Trees.
- Naive Bayes.
- K-Nearest Neighbors (KNN)
- Learning Vector Quantization (LVQ)
- Support Vector Machines (SVM)


## Model Training : 

- Split Dataset


![](https://elitedatascience.com/wp-content/uploads/2017/06/Train-Test-Split-Diagram.jpg)