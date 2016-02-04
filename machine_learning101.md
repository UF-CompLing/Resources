# Machine Learning(/data mining) 101

## Introduction

The goal of this brief overview is to familiarize the audience with some of the key ideas of machine learning as well as to point out some of the applications in which natural language processing is either useful or absolutely necessary.

> "(Machine Learning) is a Field of study that gives computers the ability to learn without being explicitly programmed."
> Arthur Samuel, 1959

What this means, I'll explain shortly, but I'd first like to give a quick few words on terminology:

The terms **data mining**, **machine learning**, **artificial intelligence**, and **statistics**, etc... are words that often bandied about as kinds of "catch-all" labels, and while they may seem inately complicated, the general ideas and goals behind each field are relatively easily communicated and distinguished.

* **Data Mining** refers to the process by which useful information is "mined" from data, typically by using sophisticated algorithms and procedures, many of which come from **machine learning**.
* **Machine Learning** refers to the subset of problems encounted in trying to build processes and machines which are able to improve at their given task over time (as they acquire more data). An extreme expression of this is the study of **Artificial Intelligence**.
* **Statistics** itself is only tangentially related in that it is the field which substantiates a lot of the ideas and math behind the algorithms used in the fields mentioned above.

Another way to think about these fields is by the degree of automation that is sought.

**Statistics ==> Data Mining ==> Machine Learning ==> Artificial Intelligence**

* **Statistics:** analysis largely carried out by hand, highly theoretical, using small programming scripts when necessary
* **Data Mining:** uses many programming techniques, but is guided by human effort
* **Machine Learning:** programming with the end goal of allowing machines/processes to improve on their own, without human intervention
* **Artificial Intelligence:** the stretch goal machine learning, complete automation

**Example** To use a single example to highlight the comparison, imagine a scenario where a researcher might be trying to monitor seismic events (earthquakes) and predict their occurence and magnitude. Each field might have its own approach.

**A Statistician** might try and model the distrubtion of existing data, characterize that distribution in a way that is familiar (maybe a using a gamma distribution) and make predictions from that. Beyond that, **a Statistician** might build a time series model using collected data to make more accurate predictions with more details.

**A Data Scientist** (or Data Miner, but that sounds dumb) would have the know how to employ a system that regularly (every second/minute/day) updates itself with the current seismic data, from which the **Data Scientist** can test different models to detect seismic anomalies and make predictions.

**A Computer Scientist** would use **machine learning** techniques to build a system that regular checks for anomalous seismic events on its own and to alert those necessary when something of worth is detected. The extreme extension of this would be a system sophisticated enough to recognize, classify, and predict different types of seismic events all on its own, without ever being told what to look for. This would be a limited example of **Artificial Intelligence**.

Keep in mind these are broad generalizations, but can be useful distinctions when comparing fields.

So what did Arthur Samuel's quote mean when he says, "give computers the ability to learn without being explicitly programmed."? He means that given very specific problems, it is possible to allow a computer to improve at a task in such a way that it "learns" on its own, using much the same methods that have been studied in other fields.

** TL;DR Data Mining = Machine Learning with different goals. Data Mining generally involves finding new information from data or building better models beyond those that exist. Machine Learning seeks to allow machines to improve in their ability to carry out tasks the more they do them. Artificial Intelligence and Statistics lend many ideas to both fields**

[A discussion of these fields and their relations](http://stats.stackexchange.com/questions/5026/what-is-the-difference-between-data-mining-statistics-machine-learning-and-ai)

## The Tasks

All machine learning tasks can be roughly divided into two categories

1. Supervised-Learning/Predictive Tasks

Supervised tasks are those in which the characteristics of the data are known, but a machine or analyst is seeking to predict future outcomes.

2. Unsupervised-Learning/Descriptive Tasks

Unsupervised tasks are those in which the characteristics of the data are unknown, and a machine or analyst wants to identifying those unknown characteristics.

**Example 1** I would like to carry out a series of analyses on stock data which I've collected, perhaps the stock values of 500 companies from January 1st to January 21st collected every 30 seconds (this is actually somewhat poor resolution for stock data).

If I wanted to try and identify groups of stocks (within the 500 I have data on) that would be an unsupervised learning task, because I don't know what these potential groups look like. I'm hoping that whatever method I'm using will be able to identify these groups based solely on their attributes represented in the data.

However if I knew that within my data about stocks that there were 3 different groups: small, medium, and large companies for instance and that each fell within a certain range of stock price, then the task of trying to identify groups of stocks could be considered a supervised learning task, because I'm classifying using existing data, **training data**.

**Example 2** A potentially more relevant example might be the task of part-of-speech (POS) tagging in **Natural Language Processing**. Using existing knowledge about words to try and label them might be considered **supervised learning**, but if you just tried to group them based on their position in relation to each then the task could be considered **unsupervised learning**.

## The Challenges

This can get technical really quickly, but I'll try and be brief. 

Ideally, the data is always perfect, you already know the model/method which fits the problem, and there are no problems whatsoever in getting actionable results. Sadly, **This never happens**.

Data Mining is always a human-guided task because of these kinds of complications: dirty data, bad models, unclear results, code bugs, etc. All of these problems apply to machine learning as well, except that there is the hope that, because only very specific problems are being handled, that a system can be built, tested, and left to run on its own after extensive testing.



* **Scalability**: bigger problems take longer, and they often take exponentially longer
* **High Dimensionality**: how do you represent something that exists in more than 3 dimensions? how do you choose what to keep
* **Heterogeneous and Complex Data**
* **Data Ownership and Distribution**
* **Non-Traditional Analysis**

## The Methods

#### Predictive Modeling

* Regression
* Naive Bayes
* Support Vector Machines
* Neural Networks

https://en.wikipedia.org/wiki/Predictive_modelling

#### Cluster Analysis

https://en.wikipedia.org/wiki/Cluster_analysis

#### Association Analysis

https://en.wikipedia.org/wiki/Association_rule_learning


#### Anomaly Detection

https://en.wikipedia.org/wiki/Anomaly_detection

## The Take-Away i.e. "Why Do We Care?"



## References

* *Introduction to Data Mining* by Tan, Steinbach, and Kumar
* *Data Mining vs. Machine Learning (and other fields)* http://stats.stackexchange.com/questions/5026/what-is-the-difference-between-data-mining-statistics-machine-learning-and-ai
* *Supervised vs. Unsupervised* https://www.quora.com/What-is-the-difference-between-supervised-and-unsupervised-learning-algorithms
* *A Wiki Breakdown of Alan Turing's seminal paper on AI, "Computing Machinery and Intelligence* https://en.wikipedia.org/wiki/Computing_Machinery_and_Intelligence
* *The difference between hidden Markov models and Markov chains* http://stats.stackexchange.com/questions/20429/what-are-the-differences-between-hidden-markov-models-and-neural-networks
