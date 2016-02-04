# Machine Learning(and/or Data Mining) 101

## Introduction

The goal of this brief overview is to familiarize the audience with some of the key ideas of machine learning as well as, at the end, to point out some of the applications in which natural language processing is either useful or absolutely necessary.

> "(Machine Learning) is a Field of study that gives computers the ability to learn without being explicitly programmed."
> Arthur Samuel, 1959

The terms **data mining**, **machine learning**, **artificial intelligence**, and **statistics**, etc... are words that often bandied about as kinds of "catch-all" labels, and while they may seem innately complicated, the general ideas and goals behind each field are relatively easily communicated and distinguished.

* **Data Mining** refers to the process by which useful information is "mined" from data, typically by using sophisticated algorithms and procedures, many of which come from **machine learning**.
* **Machine Learning** refers to the subset of problems encountered in trying to build processes and machines which are able to improve at their given task over time (as they acquire more data). An extreme expression of this is the study of **Artificial Intelligence**.
* **Statistics** itself is only tangentially related in that it is the field which substantiates a lot of the ideas and math behind the algorithms used in the fields mentioned above.

Another way to think about these fields is by the degree of automation that is sought.

**Statistics ==> Data Mining ==> Machine Learning ==> Artificial Intelligence**

* **Statistics:** analysis largely carried out by hand, highly theoretical, using small programming scripts when necessary
* **Data Mining:** uses many programming techniques, but is guided by human effort
* **Machine Learning:** programming with the end goal of allowing machines/processes to improve on their own, without human intervention
* **Artificial Intelligence:** the stretch goal machine learning, complete automation

To use a single example to highlight the comparison, imagine a scenario where a researcher might be trying to monitor seismic events (earthquakes) and predict their occurrence and magnitude. Each field might have its own approach.

**A Statistician** might try and model the distribution of existing data, characterize that distribution in a way that is familiar (maybe a using a gamma distribution) and make predictions from that. Beyond that, **a Statistician** might build a time series model using collected data to make more accurate predictions with more details.

**A Data Scientist** (or Data Miner, but that sounds dumb) would have the know how to employ a system that regularly (every second/minute/day) updates itself with the current seismic data, from which the **Data Scientist** can test different models to detect seismic anomalies and make predictions.

**A Computer Scientist** would use **machine learning** techniques to build a system that regular checks for anomalous seismic events on its own and to alert those necessary when something of worth is detected. The extreme extension of this would be a system sophisticated enough to recognize, classify, and predict different types of seismic events all on its own, without ever being told what to look for. This would be a limited example of **Artificial Intelligence**.

Keep in mind these are broad generalizations, but can be useful distinctions when comparing fields.

**TL;DR:** Data Mining = Machine Learning with different goals. Data Mining generally involves finding new information from data or building better models beyond those that exist. Machine Learning seeks to allow machines to improve in their ability to carry out tasks the more they do them. Artificial Intelligence and Statistics lend many ideas to both fields

[A discussion of these fields and their relations](http://stats.stackexchange.com/questions/5026/what-is-the-difference-between-data-mining-statistics-machine-learning-and-ai)

## The Tasks

All machine learning tasks can be roughly divided into two categories.

* **Supervised-Learning/Predictive Tasks**

Supervised tasks are those in which the characteristics of the data are known, but a machine or analyst is seeking to predict future outcomes.

* **Unsupervised-Learning/Descriptive Tasks**

Unsupervised tasks are those in which the characteristics of the data are unknown, and a machine or analyst wants to identifying those unknown characteristics.

**Example 1** I would like to carry out a series of analyses on stock data which I've collected, perhaps the stock values of 500 companies from January 1st to January 21st collected every 30 seconds (this is actually somewhat poor resolution for stock data).

If I wanted to try and identify groups of stocks (within the 500 I have data on) that would be an unsupervised learning task, because I don't know what these potential groups look like. I'm hoping that whatever method I'm using will be able to identify these groups based solely on their attributes represented in the data. Again, the goal here is identify a characteristic(s) of the stock data in the form of unknown groupings of stocks.

However if I knew that within my data about stocks that there were 3 different groups: financial, technology, and energy companies for instance, then the task of trying to identify the members of each group of stocks could be considered a supervised learning task, because I'm trying to make a prediction based off of known characteristics of the data.

**Example 2** A potentially more relevant example might be the task of part-of-speech (POS) tagging in **Natural Language Processing**. Trying to predict the part-of-speech of the next word a sequence would be a **supervised learning** task, because I'm using information about preceding words and their characteristics (POS) to make my predictions. On the other hand, pretending you don't know what potential categories there are for POS tagging and trying to identify the parts-of-speech of words based on their positioning would be **unsupervised learning** because you're trying to describe the data without any outside knowledge.

A final word on this, the lines between **supervised** and **unsupervised learning** are often incredibly vague and hard to define. Technically, **semi-supervised learning** is another category of its own, but the concepts discussed above are good rules of thumb.

## The Challenges

This can get technical really quickly, but I'll try and be brief. 

Ideally, the data is always perfect, you already know the model/method which fits the problem, and there are no problems whatsoever in getting actionable results. Sadly, **this never happens**.

Data Mining is always a human-guided task because of these kinds of complications: dirty data, bad models, unclear results, code bugs, etc. All of these problems apply to machine learning as well, except that there is the hope that, because you're trying to build a system to handle very specific problems, that said system can be built, tested, and allowed to run on its own after/if its shown to work. 

In short, data mining requires a degree of intuition because you don't necessarily know the end goal. Machine learning typically has clear end goals. Again, these are broad generalizations, but essentially correct.

Here's an overview of typical challenges from an exceedingly brief, non-technical perspective.

* **Scalability**: Bigger problems take longer, and they often take exponentially longer to reach solutions.
* **High Dimensionality**: How do you represent something that exists in more than 3 dimensions? If you have to choose fewer dimensions, how do you decide what to keep?
* **Heterogeneous and Complex Data**: Data is messy, disorganized, and generally ill-disposed to be of any use, bullying it into usable quality is a full time job.
* **Data Ownership and Distribution**: Who owns what data? How do you get the data? If it's easy to get to, is it worthwhile?
* **Non-Traditional Analysis**: Dealing with problems that don't fit scenarios you're familiar with.

## The Methods

A discussion of methods rapidly approaches technical "territory" which I'm trying to avoid for the sake of this discussion so, time allowing, I'll only briefly touch on the broader classes of methods some examples of each.

#### Predictive Modeling

A vague label for a large number of techniques involved in any number of predictive tasks.

* Regression
* Naive Bayes
* Support Vector Machines
* Neural Networks

[<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/3/3a/Linear_regression.svg/400px-Linear_regression.svg.png">]
[<img src="http://image.slidesharecdn.com/irepresentation-140417120301-phpapp01/95/tweets-classification-using-naive-bayes-and-svm-10-638.jpg?cb=1397803178">]

https://en.wikipedia.org/wiki/Predictive_modelling

#### Cluster Analysis

Cluster analysis is exactly what it sounds like, typically involving trying to find clusters/groups in the data based on their relative closeness or shape.

* K-means
* DBSCAN
* Hierarchical

[<img src="http://blog.mpacula.com/wp-content/uploads/2011/04/kmeans1.png">]
[<img src="http://www.hypertextbookshop.com/dataminingbook/public_version/artifacts/images/pictures/chpt4interSec4Fig4.jpg">]
[<img src="http://www.hypertextbookshop.com/dataminingbook/public_version/artifacts/images/pictures/chpt4interSec4Fig5.jpg">]

https://en.wikipedia.org/wiki/Cluster_analysis

#### Association Analysis

In a nutshell, association analysis is the identification of groups of items that occur together/have similar characteristics.

* Apriori
* Eclat
* FP-growth

[<img src="http://web.fhnw.ch/personenseiten/taoufik.nouri/Data%20Mining/Course/Course4/DM-Par14.gif">]
[<img src="http://image.slidesharecdn.com/lecture13-090305022154-phpapp01/95/lecture13-association-rules-15-728.jpg?cb=1236219721">]

https://en.wikipedia.org/wiki/Association_rule_learning

#### Anomaly Detection

Anomaly detection often comes as a by-product of other methods, but is a separate problem in its own right. The premise being that if normally, when you want to make a good model, you identify the good data for predicting/classifying, you've also identified that which is bad, or anamolous.

[<img src="https://statistics.laerd.com/spss-tutorials/img/lr/outliers.png">]
[<img src="http://web.fhnw.ch/personenseiten/taoufik.nouri/Data%20Mining/Course/Course4/DM-Par14.gif">]

https://en.wikipedia.org/wiki/Anomaly_detection

## The Take-Away

So why is any of this important to you?

* Any sophisticated work in computational linguistics will run across these terms and ideas, making at least a cursory knowledge valuable.
* Cleaning and preparing any kind of linguistics data relies heavily on some of the topics we've covered: regular expressions, tokenization, etc. and the fact is the cleaning and preparation often take >=80% of the time and any particular project.
* Often people will try and make what they're working on sound more complicated than it by using buzz words, of which machine learning is one, being able to call people on their nonsense is an invaluable skill.
* **For fun and profit:** a lot of this stuff is rather cool and especially interesting and being able to use some of the methods and ideas discussed looks great with employers.



## References and Readings

* *Introduction to Data Mining* by Tan, Steinbach, and Kumar
* *Data Mining vs. Machine Learning (and other fields)* http://stats.stackexchange.com/questions/5026/what-is-the-difference-between-data-mining-statistics-machine-learning-and-ai
* *Supervised vs. Unsupervised* https://www.quora.com/What-is-the-difference-between-supervised-and-unsupervised-learning-algorithms
* *A Wiki Breakdown of Alan Turing's seminal paper on AI, "Computing Machinery and Intelligence* https://en.wikipedia.org/wiki/Computing_Machinery_and_Intelligence
* *The difference between hidden Markov models and Markov chains* http://stats.stackexchange.com/questions/20429/what-are-the-differences-between-hidden-markov-models-and-neural-netwo
* *Visual Intro to Machine Learning* http://www.r2d3.us/visual-intro-to-machine-learning-part-1/
