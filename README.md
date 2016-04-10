# CS109-harvard-data-sicence

## Table of Contents
CS109 Key Facets
• data munging/scraping/sampling/cleaning in order to get an
informative, manageable data set;
• data storage and management in order to be able to access
data quickly and reliably during subsequent analysis;
• exploratory data analysis to generate hypotheses and
intuition about the data;
• prediction based on statistical tools such as regression,
classification, and clustering; and
• communication of results through visualization, stories, and
interpretable summaries.

Act I: Predictions
• Data Collection, “Munging”, and Storage
• Exploratory Data Analysis (EDA)
• Classification & Regression
• Cross Validation
• Dimensionality Reduction
• Effective Communication & Writing

Act II: Recommendations
• Support Vector Machines
• Decision Trees & Random Forests
• Bagging & Boosting
• Machine Learning Best Practices
• MapReduce, Amazon’s EC2, and Spark

Act III: Clustering & Text
• Bayesian Thinking & Naive Bayes
• Text Analysis: LDA & Topic Modeling
• Clustering
• Effective Presentations
• Deep Learning
• Guest Lecture: Experimental Design

## Requirements
```bash
pip install -r requirements.txt
```

## Python Notes
```python
per_user = ratings.groupby('user_id').apply(lambda f: f.mean())
```

## Scraping Notes
Using urllib2
```python
url = 'http://www.crummy.com/software/BeautifulSoup'
source = urllib2.urlopen(url).read()
print source.find('Soup')
```
Using BeautifulSoup
```python
soup = bs4.BeautifulSoup(source)
link_list = [l.get('href') for l in soup.findAll('a')]
external_links = [l for l in link_list if l is not None and l.startswith('http')]
```
