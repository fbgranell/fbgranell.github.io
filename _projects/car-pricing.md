---
layout: page
title: XGBoost for Car Pricing
description: Machine learning model that uses second-hand car features to predict prices <b>(R2 = 0.9)</b>.
img: assets/img/p4_main.png
importance: 1
category: fun
---

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/p4_header.png" title="Fraud detector" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

<div id="table-of-contents">
  <p style="font-size: 1.75rem; margin-bottom: .5rem;">Table of Contents:</p>
<ul>
  <li style="list-style-type: decimal;"><a href="#section1" style="font-size: 1.30rem; color:#2B2E4A">Introduction.</a></li>
  <li style="list-style-type: decimal;"><a href="#section2" style="font-size: 1.30rem; color:#2B2E4A">Materials.</a></li>
  <li style="list-style-type: decimal;"><a href="#section3" style="font-size: 1.30rem; color:#2B2E4A">Methods.</a></li>
  <li style="list-style-type: decimal;"><a href="#section4" style="font-size: 1.30rem; color:#2B2E4A">Results.</a></li>
  <li style="list-style-type: decimal;"><a href="#section5" style="font-size: 1.30rem; color:#2B2E4A">References.</a></li>
</ul></div>


<a id='section1'></a>
### Introduction

Predicting the price of a second-hand car can be a tricky business, but with the help of machine learning and XGBoost, we're here to make the process way, way easier. There's no need to rely on chance or intuition when you have a model that can predict prices with a high degree of accuracy at your disposal. Thanks to the power of XGBoost we will learn how to avoid getting ripped off on our next used car purchase in Spain.

<a id='section2'></a>
### Materials 

This project was developed using **Python** and several popular data processing and machine learning libraries. All the data was obtained through web scraping with the aid of the <em>Beautiful Soup</em> library and was then cleaned, analyzed and merged using <em>pandas</em> and <em>numpy</em>.

<em>Scikit-learn</em> library, <em>TensorFlow</em> and <em>XGBoost</em> were used for building the machine-learning models. These libraries are widely adopted in the field of machine learning and provide a comprehensive set of tools for implementing various machine learning algorithms and techniques.

<a id='section3'></a>
### Methods 

The data for this project was obtained through **web scraping over 400,000 car listings**, including their prices and technical features. To improve performance, the "concurrent" library was used to compute functions in parallel, resulting in a speed increase of $$\times10$$. The dataset was then cleaned to address missing and incorrectly-displayed values disguised as zeros in order to prevent misleading the model.

After obtaining the data, it underwent a thorough **cleaning process**. Null and NaN values were removed as it is impossible for any of the features to have a zero value. Categorical features were also unified, such as merging locations by autonomous communities, or specific colors (like ocean blue) to basic ones (blue). Likewise, feature normalization was performed to improve the performance while training the models.

In addition to data cleaning, a **visual exploratory analysis** was carried out to identify patterns within the data. To train the model, the dataset was divided into three parts: one for training, one for cross-validation (which also allowed for hyperparameter search), and one for testing. Finally, a pipeline was then created that evaluated various models through cross-validation, which allows us to choose the best one.

<a id='section4'></a>
### Results
