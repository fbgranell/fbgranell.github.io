---
layout: page
title: Financial Fraud Detector
description: A compilation of Machine Learning models that detect fraudulent transactions.
img: assets/img/p2_frauddet.png
importance: 2
category: Work
---
<!-- <img src="images/header.jpg"/> -->
### Index:

* [Introduction](#section1)
* [Materials and Methods](#section2)
* [Results](#section7)
* [References](#section10)
* [License](#section11)


<a id='section1'></a>
### Introduction

In this project, I am developing several models to detect fraudulent transactions through  machine learning methods. 

I used different models: regression, decision tree, random forest and deep learning. The right model to choose depends on the plan against fraud, but the random forest is the better overall. 

<a id='section2'></a>
### Materials and Methods

In the analysis, people might be tempted to remove some correlated columns (0.99 correlation), which means that they're almost a linear combination of another column. Nevertheless, the correlation is not 1, and that means that there are some exceptions. And those exceptions are exactly a risk factor that increases the chances of being a fraudulent transaction, and hence the columns should not be dropped (because we would lose that information). This was proven by comparing models with and without said columns.

The methods of this study include the followings:
* Data cleaning
* Data wrangling
* Exploratory data analysis
* Machine learning
* Deep learning
* Hyperparameter optimization
* Data visualization

### Results

These are the parameters that measure how good a model is doing. 

<center><table style="text-align: center; vertical-align: middle;" cellpadding ="5">
    <tr>
        <td><b>Model</b></td>
        <td><b>Accuracy</b></td>
        <td><b>Recall</b></td>
        <td><b>Precision</b></td>
        <td><b>F1 Score</b></td>
    </tr>
    <tr>
        <td>Regression</td>
        <td>94.4%</td>
        <td>84%</td>
        <td>4%</td>
        <td>0.08</td>
    </tr>
    <tr>
        <td>KNN</td>
        <td>99.7%</td>
        <td>76%</td>
        <td>58%</td>
        <td>0.65</td>
    </tr>
    <tr>
        <td>Decision Tree</td>
        <td>99.9%</td>
        <td>85%</td>
        <td>89%</td>
        <td>0.87</td>
    </tr>
    <tr>
        <td>Random Forest</td>
        <td>99.9%</td>
        <td>81%</td>
        <td>95%</td>
        <td>0.88</td>
    </tr>
    <tr>
        <td>Deep learning</td>
        <td>99.3%</td>
        <td>98%</td>
        <td>30%</td>
        <td>0.46</td>
    </tr>
</table></center>
<br>If the company wanted to implement a soft safety measure, the deep learning model would be the best way to go, since it detects 98% of the fraudulent transactions. Of all the fraud alerts the model would give, 70% of them would actually be a legit transaction (wrongly flagged), but since in this case the measure is soft, it would not cause a high impact (and this 70% only represents a 0.6% of the total number of transactions). 

On the other hand, if the measures applied by the model was more agressive towards the customer (ex: blocking the account), Random Forest is the best choice. It only detects 81% of the fraudulent transactions, but it's more precise (only 5% of the alerts are wrongly flagged, which equals a 0.01% of the total number of transactions). With this model, we detect a high portion of the fraud and we don't cause a negative impact towards normal customers. 

<a id='section10'></a>
### References
The synthetic data was obtained through <a href="https://www.kaggle.com/datasets/ealaxi/paysim1">kaggle</a>, and it was created from a  real transactions extracted from one month of financial logs from a mobile money service.

<a id='section11'></a>
### License
This is an educational project; therefore, all materials can be used freelly.
