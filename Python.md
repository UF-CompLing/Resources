# Python Basics

A good program to use to learn Python is [Codecademy](https://www.codecademy.com/learn/python). It's free, make an account and try it out!

## Some sample code snippets:

#### Hello world

```python
print('Hello world')
```

#### A loop

```python
i = 0
for x in range(0,5):
	i += x
print(i)
```

#### First time you run NLTK

```python
import nltk

nltk.download()
```

#### Sample NLTK Parse tree
```python
from nltk.corpus import treebank

t = treebank.parsed_sents('wsj_0001.mrg')[0]
t.draw()
```