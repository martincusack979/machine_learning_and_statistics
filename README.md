# Machine Learning and Statistics

This repository is submitted as partial fullfillment of a H.Dip in Data Analytics in Computing.

Martin Cusack
Student ID: G00239124
This repository contains a Jupyter notebook, a dataset folder, a .gitignore file and a readme file.

## Task 1

Square roots are difficult to calculate. In Python, you typically use the power operator (a double asterisk) or a package such
as `math`.  In this task,1 you should write a function `sqrt(x)` to approximate the square root of a floating point number x without
using the power operator or a package.

Rather, you should use the Newton’s method. Start with an initial guess for the square root called $z0$. You then repeatedly
improve it using the following formula, until the difference between some previous guess $zi$ and the next $zi+1$
is less than some threshold, say 0.01.

$$ z_{1 +1} = z_1 - \frac{zi × zi − x}{2z_i} $$

## Task 2

Consider the below contingency table based on a survey asking respondents whether they prefer coffee or tea and whether they
prefer plain or chocolate biscuits. Use scipy.stats to perform a chi-squared test to see whether there is any evidence of an 
association between drink preference and biscuit preference in this instance.

![contingency](https://github.com/martincusack979/machine_learning_statistics/assets/79522561/67ca69c3-afc7-4bb3-81f0-bc3e2b0f95df)


## Task 3

Perform a t-test on the famous penguins data set to investigate whether there is evidence of a significant difference in the body
mass of male and female gentoo penguins

## Task 4 

The Iris data set is based on measurements taken from three different species of Iris flower: Setosa, Versicolor and Virginica.  There are four measurements provided for each sample of these species:  sepal length, sepal width, petal length and petal width.  One way of establishing whether the setosa class of Iris flower is easily separable from the other two classes is to train a machine learning algorithm (such as K Nearest Neighbours) so that it can make predictions on which class a data point belongs to based on the available information. We can then produce a visualisation to further illustrate whether the setosa class is in fact easily separable from the other two classes.


Reference for train test split:

https://www.kaggle.com/code/grim1412/seaborn-visualization-and-knn-on-the-iris-dataset

Reference for seaborn visualisation:

https://www.kaggle.com/code/grim1412/seaborn-visualization-and-knn-on-the-iris-dataset

### Task 5

Perform Principal Component Analysis on the iris data set, reducing the number of dimensions to two. Explain the purpose
of the analysis and your results.

Principal component analysis (PCA) is a useful tool for interpreting and analysing multi-dimensional data, such as the Iris data set.  It can be used in conjunction with Seaborn to create 2-dimensional visualisations which allow us to determine the separability of the data. In this task we will take the four variables in the Iris data set (sepal length, sepal width, petal length and petal width) and using PCA we can reduce the dimensionality of the data and therefore gain a deeper understanding of the variables in the Iris data set.
