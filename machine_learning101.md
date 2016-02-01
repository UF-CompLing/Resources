# Machine Learning 101 (for computational-linguistics)

## Introduction

The goal of this brief overview is to familiarize the audience with some of the ideas of machine learning and the aspects of natural language processing which are innately useful.

> "(Machine Learning) is a Field of study that gives computers the ability to learn without being explicitly programmed."
> Arthur Samuel, 1959

A quick few words on terminology:

The terms **data mining**, **machine learning**, **artificial intelligence**, and **statistics**, etc... are words that often bandied about, and while they may seem inately complicated, the general ideas and goals behind each field are relatively easily communicated.

* **Data Mining** refers to the process by which useful information is "mined" from data, typically by using sophisticated algorithms and procedures, many of which come from **machine learning**.
* **Machine Learning** refers to the subset of problems encounted in trying to build processes and machines which are able to improve at their given task over time (as they acquire more data). An extreme expression of this is the study of **Artificial Intelligence**.
* **Statistics** itself is only tangentially related in that it is the field which substantiates a lot of the ideas and math behind the algorithms used in the fields mentioned above.

Another way to think about these fields is by the degree of automation that is sought.

**Statistics ==> Data Mining ==> Machine Learning ==> Artificial Intelligence**

* **Statistics:** analysis largely carried out by hand, highly theoretical, using small programming scripts when necessary
* **Data Mining:** uses many programming techniques, but is guided by human effort
* **Machine Learning:** programming with the end goal of allowing machines/processes to improve on their own, without human intervention
* **Artificial Intelligence:** the stretch goal machine learning, complete automation

To use a single example to highlight the comparison, imagine a scenario where a researcher might be trying to monitor seismic events (earthquakes) and predict their occurence and magnitude. Each field might have its own approach.

**A Statistician** might try and model the distrubtion of existing data, characterize that distribution in a way that is familiar (maybe a using a gamma distribution) and make predictions from that. At a stretch, **A Statistician** might build a time series model using collected data to make more accurate predictions with more details.

**A Data Scientist** (or Data Miner, but that sounds dumb) would have the know how to employ a system that regular (every second/minute/day) updates itself with the current seismic data, from which the **Data Scientist** can test different models to detect seismic anomalies and make predictions.

**A Computer Scientist** would use **machine learning** techniques to build a system that regular checks for anomalous seismic events on its own and to alert those necessary when something of worth is detected. The dream would be a system sophisticated enough to recognize, classify, and predict different types of events all on its own. This would be a limited example of **Artificial Intelligence**.

Keep in mind these are broad generalizations, but can be useful distinctions when comparing fields.

** TL;DR Data Mining = Machine Learning with different goals, Artificial Intelligence and Statistics lend many ideas to both fields**

[A discussion of these fields and their relations](http://stats.stackexchange.com/questions/5026/what-is-the-difference-between-data-mining-statistics-machine-learning-and-ai)

## The Tasks

All machine learning tasks can be roughly divided into two categories

1. Supervised-Learning/Predictive Tasks
2. Unsupervised-Learning/Descriptive Tasks

## The Challenges

* Scalability
* High Dimensionality
* Heterogeneous and Complex Data
* Data Ownership and Distribution
* Non-Traditional Analysis

## The Methods

#### Cluster Analysis

https://en.wikipedia.org/wiki/Cluster_analysis

#### Association Analysis

https://en.wikipedia.org/wiki/Association_rule_learning

#### Predictive Modeling

https://en.wikipedia.org/wiki/Predictive_modelling

#### Anomaly Detection

https://en.wikipedia.org/wiki/Anomaly_detection

## The Take-Away (from the perspective of Computational Linguistics)

## References

* *Introduction to Data Mining* by Tan, Steinbach, and Kumar
* *Stack exchange discussion* http://stats.stackexchange.com/questions/5026/what-is-the-difference-between-data-mining-statistics-machine-learning-and-ai
