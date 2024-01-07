# Machine Learning and Statistics

This repository is submitted in partial fullfillment of a H.Dip in Science in Data Analytics.

**Name: Martin Cusack**

**Student ID: G00239124**
***

## Contents 
1. Introduction
2. Tasks
3. Project
4. Conclusion

## Introduction

This repository contains two Jupyter notebooks(*project.ipynb* and *tasks.ipynb*), a data folder, an 
images folder, a .gitignore file and a readme file.

**How to use this repository**

1. Install latest version of Anaconda.
2. Install the latest version of Visual Studio Code.
3. Clone the repository at https://github.com/martincusack979/machine_learning_statistics
4. Open the repository in Visual Studio Code.
5. Use the Python interpreter 3.9.18.

# Tasks

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

The Iris data set is based on measurements taken from three different species of Iris flower: Setosa, Versicolor and Virginica.  
There are four measurements provided for each sample of these species:  sepal length, sepal width, petal length and petal width.  
One way of establishing whether the setosa class of Iris flower is easily separable from the other two classes is to train a 
machine learning algorithm (such as K Nearest Neighbours) so that it can make predictions on which class a data point belongs to 
based on the available information. We can then produce a visualisation to further illustrate whether the setosa class is in fact 
easily separable from the other two classes.


Reference for train test split:

https://www.kaggle.com/code/grim1412/seaborn-visualization-and-knn-on-the-iris-dataset

Reference for seaborn visualisation:

https://www.kaggle.com/code/grim1412/seaborn-visualization-and-knn-on-the-iris-dataset

## Task 5

Perform Principal Component Analysis on the iris data set, reducing the number of dimensions to two. Explain the purpose
of the analysis and your results.

Principal component analysis (PCA) is a useful tool for interpreting and analysing multi-dimensional data, such as the Iris
data set.  It can be used in conjunction with Seaborn to create 2-dimensional visualisations which allow us to determine the
separability of the data. In this task we will take the four variables in the Iris data set (sepal length, sepal width, petal
length and petal width) and using PCA we can reduce the dimensionality of the data and therefore gain a deeper understanding 
of the variables in the Iris data set.

When we create a new PCA instance, if we specify "(n_components=2)" using the N_components parameter we can reduce the number 
of dimensions to two.

We can apply dimensionality reduction to the data using the "transform" method.

![pairplot](https://github.com/martincusack979/machine_learning_statistics/blob/main/Images/pairplot.png)

From the above visualisation, carried out after using PCA to reduce the dimensions of the data set, we can see that the Setosa class
is clearly separable from the other classes. However, the Versicolor and Virginica classes are much closer together in proximity and 
share a degree of overlap. This would mean that a basic machine learning classifier, such as K Nearest Neighbours, may have some difficulty
separating the classes.  In the following cells we will run Principal Component Analysis again, only this time we will use a 
standard scaler to further transform the data set so that each of the numerical variables is centered on 0, with a variance of 1.  
This ultimately should allow K Nearest Neighbours to make more effective predictions based on the available data.

I then used seaborn to create another pair plot.  As we can see from the resulting visualisation, it remains difficult to separate 
the Versicolor and Virginica classes, even after running PCA again with the scaled data.

As we can see from the above score, the K Nearest Neighbours classifier performs exceptionally well when it makes predictions 
on the scaled data.
This illustrates the importance of using a scaler before performing machine learning operations on a given set of data. It is also quite a 
surprising result considering the slight overlap between Versicolor and Virginia which was evident after performing Principal 
Component Analysis.

Reference: https://scikit-learn.org/stable/modules/generated/sklearn.decomposition.PCA.html

## End
***

# Project
***

 ## Introduction
 
 In this notebook, I will deploy a variety of machine learning algorithms to make classifications and predictions based 
 on the widely-studied Fisher's Iris flower data set.
 This data set first appeared in biologist Ronald Fisher's 1936 paper "The Use of Multiple Measurements in Taxonomic Problems". 
 Fisher's work has been highly influential 
 in the fields of data science and machine learning over the decades since its publication and has been referenced on
 innumerable occasions by teachers and academics.

 Fisher's data set comprises a study of three different species of the Iris flower (Iris setosa, Iris virginica and Iris versicolor) and
 contains six columns: ID, SepalLengthCm, SepalWidthCm, PetalLengthCm, PetalWidthCm and Species. I will fit and train a number of 
 machine learning algorithms on this data in order to assess their relative accuracy in determining the class of each sample.


 ### Supervised learning

 There are currently two main approaches to machine learning: supervised learning and unsupervised learning.  Supervised learning is 
 an approach generally used when dealing with labeled datasets, and uses the available data to train algorithms to accurately 
 classify data and make predictions. By using 
 inputs and outputs, the training model can learn from the data and as a result produce accurate outcomes.  
 
 By contrast, unsupervised learning is an approach generally used with unlabeled datasets. They do not require human intervention, 
 hence are "unsupervised".  Unsupervised techniques are often used in the preprocessing stage of machine learning in order to
 reduce the dimensionality of a given data set.
 

 ### Classification algorithms

Classification algorithms are used in the machine learning process in order to make predictions and categorise data (an example 
being an email spam detector).  Examples of commonly-used classifiers include K Nearest Neighbors, Support Vector Machines (SVM), 
Naive Bayes and Random Forest.

### Cross Validation

Evaluation using cross vaildation allows us to gain a good overall sense of the accuracy of a given algorithm. Cross validation 
works by dividing the data up into subsets or "folds" and using each of these folds as a validation set.  The average of each result
is then calculated to give a final score. Using cross validation can help "to ensure that the model selected for deployment is robust 
and generalizes well to new data". In the below cell, I will run cross-validation with five folds to determine the accuracy of 
the K Nearest Neighbours algorithm.

## End
***

### References

[1] *Supervised vs. Unsupervised Learning*, Julianna Delua. https://www.ibm.com/blog/supervised-vs-unsupervised-learning/

[2] *Iris.csv*, Saurabh Singh. https://www.kaggle.com/datasets/saurabh00007/iriscsv

[3] *Nearest Neighbors*, scikit-learn developers. https://scikit-learn.org/stable/modules/neighbors.html

[4] *Split your Dataset with train_test_split*, Mirko Stojiljković. https://realpython.com/train-test-split-python-data/ 

[5] *Cross Validation in Machine Learning*. https://www.geeksforgeeks.org/cross-validation-machine-learning/

[6] *Support Vector Machines*, Scikit-learn developers https://scikit-learn.org/stable/modules/svm.html

[7] *Support Vector Machines with Scikit-learn Tutorial*, Avinash Naviani.(2019) https://www.datacamp.com/tutorial/svm-classification-scikit-learn-python      

[8] *Naive Bayes*, Scikit-learn developers.  https://scikit-learn.org/stable/modules/naive_bayes.html

[9] *Naive Bayes Classification Tutorial using Scikit-learn*, Abid Ali Awan.(2018) https://www.datacamp.com/tutorial/naive-bayes-scikit-learn

[10] *Machine Learning*. https://www.w3schools.com/python/python_ml_getting_started.asp
***

## End
***

