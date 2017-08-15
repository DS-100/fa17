---
layout: page
title: "Syllabus"
description: "Course Syllabus"
group: navigation
order: 2
---
{% include JB/setup %}


This syllabus is still under development and is subject to change.  


<table class="table table-striped">
   <colgroup>
      <col class="col-md-1">
      <col class="col-md-1">
      <col class="col-md-2">
      <col class="col-md-8">
   </colgroup>
<thead>
   <tr>
      <th> Week </th>
      <th> Lecture </th>
      <th> Date </th>
      <th> Topic </th>
   </tr>
</thead>
<tbody>


<!-- This is the dates for all the lectures -->
<!--
import datetime
import pandas as pd

d1 = datetime.date(2017,8,24) 
d2 = datetime.date(2017,12,14)
days = pd.date_range(d1,d2) 

for d in days[(days.dayofweek == 1) | (days.dayofweek == 3)]:
     print(str(d.month) + "/" + str(d.day) + "/" + str(d.year))

-->

{% capture dates %}
8/24/2017
8/29/2017
8/31/2017
9/5/2017
9/7/2017
9/12/2017
9/14/2017
9/19/2017
9/21/2017
9/26/2017
9/28/2017
10/3/2017
10/5/2017
10/10/2017
10/12/2017
10/17/2017
10/19/2017
10/24/2017
10/26/2017
10/31/2017
11/2/2017
11/7/2017
11/9/2017
11/14/2017
11/16/2017
11/21/2017
11/23/2017
11/28/2017
11/30/2017
12/5/2017
12/7/2017
12/12/2017
12/14/2017
{% endcapture %}
{% assign dates = dates | split: " " %}


<!--
The actual lectures.  Dates are rendered automatically using Jekyll
 -->





<!-- ######################################################### -->
{% include syllabus_entry dates=dates %}

### Course Overview and The Data Science Life Cycle [Gonzalez]

In this lecture we provide an overview of the class, discuss what it means to be a data scientist by examining recent surveys of data scientists, and then introduce the data science lifecycle spanning question formation, data acquisition and cleaning, exploratory data analysis and visualization, and finally prediction and inference.

#### Homework 1 Released: Python Refresher



<!-- ######################################################### -->
{% include syllabus_entry dates=dates %}

### Data Generation [Nolan]

Fundamentally, (data) science is the study of using data to learn about the world and solve problems.  However, how and what data is collected can have a profound impact on what we can learn and the problems we can solve.   In this lecture, we will begin to explore various mechanisms for data collection and their implications on our ability to generalize.  In particular we will discuss differences between census, surveys, controlled experiments, and observational studies.  We will highlight the power of simple randomization and the fallacies of data scale.




<!-- ######################################################### -->
{% include syllabus_entry dates=dates %}

### Data Tables, Indexes, and Pandas [Lau]

While data comes in many forms, most data analysis are done on tabular data Mastering the skills of constructing, cleaning, joining, aggregating, and manipulating tabular data is essential to data science.  In this lecture, we will introduce the Pandas, the open-source Python data manipulation library widely used by data scientists.  In addition to introducing new syntax, we will introduce new concepts including indexes, the role of column operations on system performance, and basic tools to begin visualizing data.




<!-- ######################################################### -->
{% include syllabus_entry dates=dates %}

### EDA and Data Cleaning [ Gonzalez ]

Whether collected by you or obtained from someone else, raw data is seldom ready for immediate analysis.  Through exploratory data analysis we can often discover important anomalies, identify limitations in the collection process, and better inform subsequent goal oriented analysis.  In this lecture we will discuss how to identify and correct common data anomalies and their implications on future analysis.  We will also discuss key properties of data including structure, granularity, faithfulness, temporality and scope and how these properties can inform how we prepare, analyze, and visualize data.


#### Homework 2 Released: Food Safety Data Cleaning and EDA


<!-- ######################################################### -->
{% include syllabus_entry dates=dates %}

### Working with Text [Nolan]

Whether in documents, tweets, or records in a table, text data is ubiquitous and presents a unique set of challenges for data scientists.  How do you extract key phrases from text?  What are meaningful aggregate summaries of text?  How do you visualize textual data?  In this lecture we will introduce a set of techniques (e.g., bag-of-words) to transform text into numerical data and subsequent tabular analysis.  We will also introduce regular expressions as a mechanism for cleaning and transforming text data data.




<!-- ######################################################### -->
{% include syllabus_entry dates=dates %}

### Visualization and Communication [Nolan]

A large fraction of the human brain is devoted to visual perception.   As a consequence, visualization is a critical tool in both exploratory data analysis and communicating complex relationships in data.   However, making informative and clear visualizations of complex concepts can be challenging.  In this lecture, we will explore good and bad visualizations and describe how to choose visualizations for various kinds of data and goals.  

#### Homework 3 Released: Food Safety Text Analysis and Mapping

<!-- 
##### Lecture Notes:
* Slides ([pptx](https://drive.google.com/open?id=0B7gkaDYGT5X5LUVVa1JuM3RZeTQ), [pdf](https://drive.google.com/open?id=0Bze55lezLJhITWROdV9PNEE2RGs), [pdf 6up](https://drive.google.com/open?id=0Bze55lezLJhISVpKUU95VmFRcUU))
 -->


<!-- ######################################################### -->
{% include syllabus_entry dates=dates %}

### Visualization and Relationships and Transformations [Gonzalez]

Often directly visualizing data and relationships can result in less informative plots. However by combining basic data transformations and additional analytics we can often reveal and visualize important and informative patterns in data.  In this lecture we will continue to explore visualization and discuss several data transformations to address noise, heavy tail behavior, and high-dimensional data.




<!-- ######################################################### -->
{% include syllabus_entry dates=dates %}

### Simple Probability Models and Estimation [Gonzalez]

The statistician (and data scientist ahead of his time) George Box once wrote “Essentially, all models are wrong, but some are useful.”  A key step in data science is developing models that capture the basic essential patterns in data and whose parametric shape can provide inferential insight and enable prediction.  Data scientists build models from basic distributions to describe ever increasingly complex phenomena.  In this lecture we will begin to introduce basic statistical distributions and discuss how to fit these distributions to data.  We begin to discuss the art of model design.

#### Homework 4 Released: Bike Sharing and Multivariate Visualization



<!-- ######################################################### -->
{% include syllabus_entry dates=dates %}

### Model Estimation Continued [Gonzalez]

How do we characterize a model estimation procedure?  In this lecture we will continue our exploration of model estimation and examine how the estimation procedure relates to the underlying distributions.  In particular we will begin to explore the bias-variance trade-off.





<!-- ######################################################### -->
{% include syllabus_entry dates=dates %}

### Hypothesis Testing [Nolan]

A key step in inference is often answering a question about the world.  Are students more likely to succeed if they study?  Answering these inferential questions is hypothesis testing.  In this lecture we will examine a collection non-parametric hypothesis tests.  These powerful procedures build on the basic idea of random simulation to help quantify our certainty in a particular conclusion.  In the process of using these procedures we will also touch on the challenges of false discovery and multiple hypothesis testing.

#### Project 1 Released: Twitter Analysis

<!-- ######################################################### -->
{% include syllabus_entry dates=dates %}

### Randomized Trials [Nolan]






<!-- ######################################################### -->
{% include syllabus_entry dates=dates %}

### Least Squares Linear Regression [Gonzalez]

Modeling the relationships between variables is a common task in data science and perhaps one of the most widely used models is linear regression.  In this lecture we introduce least squares linear regression through the lens of empirical risk minimization. 



<!-- ######################################################### -->
{% include syllabus_entry dates=dates %}

### Prediction Bias and Variance [Gonzalez]

In this lecture we continue our introduction to least square linear regression and provide a formal analysis of the bias and variance as it relates to the least squares objective.



<!-- ######################################################### -->
{% include syllabus_entry dates=dates %}

### Midterm Review [Gonzalez]



<!-- ######################################################### -->
{% include syllabus_entry dates=dates %}

### Midterm [Gonzalez]



<!-- ######################################################### -->
{% include syllabus_entry dates=dates %}

### Introduction to SQL and the Relational Model [Gonzalez]

SQL is the most widely used language for accessing and manipulating data.  In this lecture we introduce the SQL language and more broadly the Relational Model of data.  We will describe some of the basic SQL operations and provide some motivation behind the relational model of tabular data.


<!-- ######################################################### -->
{% include syllabus_entry dates=dates %}

### More Advanced SQL [Gonzalez]

In this lecture we continue to dig into more advanced SQL expressions.  We will introduce common table expressions, group by, and join operations. 


<!-- ######################################################### -->
{% include syllabus_entry dates=dates %}

### Feature Engineering [Gonzalez]



<!-- ######################################################### -->
{% include syllabus_entry dates=dates %}

### Overfitting [Gonzalez]


<!-- ######################################################### -->
{% include syllabus_entry dates=dates %}

### Regularization [Gonzalez]



<!-- ######################################################### -->
{% include syllabus_entry dates=dates %}

### Classification [Nolan]




<!-- ######################################################### -->
{% include syllabus_entry dates=dates %}

### Method of Maximum Likelihood [Nolan]



<!-- ######################################################### -->
{% include syllabus_entry dates=dates %}

### Logistic Regression [Nolan]


<!-- ######################################################### -->
{% include syllabus_entry dates=dates %}

### Gradient Descent [Nolan]


<!-- ######################################################### -->
{% include syllabus_entry dates=dates %}

### Bagging [Nolan]


<!-- ######################################################### -->
{% include syllabus_entry dates=dates %}

### TBD 



<!-- ######################################################### -->
{% include syllabus_entry dates=dates %}

<h2> Holiday!! </h2>


<!-- ######################################################### -->
{% include syllabus_entry dates=dates %}

### Big Data Ecosystem [Gonzalez]


<!-- ######################################################### -->
{% include syllabus_entry dates=dates %}

### Spark [Gonzalez]



<!-- ######################################################### -->
{% include syllabus_entry dates=dates %}

### RRR Review [Gonzalez]




<!-- ######################################################### -->
{% include syllabus_entry dates=dates %}

### RRR Review [Nolan]



<!-- ######################################################### -->
{% include syllabus_entry dates=dates %}

<center><h3> Study! </h3></center>


<!-- ######################################################### -->
{% include syllabus_entry dates=dates %}

# Final Exam 
The final exam is currently in [exam group 13](http://registrar.berkeley.edu/sis-SC-message) and therefore will be from 8:00AM to 11:00AM on Thursday 12/14/2017.  



{% comment %}
This command should go at the end and must not include the dates=dates
{% endcomment %}

{% include syllabus_entry last_tag=True  %}


</tbody>
</table>


<!--

A little script to highlight the week that is next

There is currently a bug in this script which someone needs to fix.  When I wrote this script for my graduate seminar class we only had one lecture a week. We should modify the Jekyll code to render the syllabus with each row tagged so we can automatically identify the week and lecture day.

-->



<script type="text/javascript">
var current_date = new Date();
var rows = document.getElementsByTagName("th");
var finished =  false;
for (var i = 1; i < rows.length && !finished; i++) {
   var r = rows[i];
   if (r.id.startsWith("counter_")) {
      var fields = r.id.split("_")
      var week_div_id = "week_" + fields[2]
      var lecture_date = new Date(fields[1] + " 23:59:00")
      if (current_date <= lecture_date) {
         finished = true;
         r.style.background = "orange"
         r.style.color = "black"
         var week_td = document.getElementById(week_div_id)
         week_td.style.background = "#043361"
         week_td.style.color = "white"
      }
   }
}
</script>

