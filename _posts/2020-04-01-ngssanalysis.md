---
title: "Data Science Project: NGSS Analysis"
date: 2020-04-01
tags: [data science, education, science]
header:
    image: "/images/mountains.jpg"
excerpt:  "Data Science, NGSS, Visualization"
---

#Analysis and Visualization of the Next Generation Science Standards

## Summary


## Introduction
So here's the challenge: we need to support the development of teachers' science [content knowledge](https://www.wcu.edu/WebFiles/PDFs/Shulman.pdf) as they gain their Master's of Arts in Teaching. But not every teacher begins their degree with the same baseline of knowledge. This is in addition to the fact that they are not all teaching classes that leverage their formal science educations. Oh, and they are teaching content from a multitude of disciplines and across all grade levels. And - to top it off - they are also trying to learn about all the other aspects of teaching at the same time!

One solution is to focus our teachers' content knowledge development through the [Next Generation Science Standards](https://www.nextgenscience.org/)(NGSS). The NGSS are a framework for teaching science in a three-dimensional manner: content, practices, and cross-cuttting concepts. The NGSS have been [widely adopted](https://ngss.nsta.org/about.aspx) in the United States, which is great because the NGSS represent a much more progressive approach to science education (i.e., not just memorizing science facts). Using the NGSS also means that we can focus on the [cross-cutting concepts](https://ngss.nsta.org/CrosscuttingConceptsFull.aspx)(CCCs) - seven concepts that universally applicable across all science domains (and, I would argue, across all subjects!).

However, we cannot likely cover all the of the CCCs in great depth while providing a coherent and cohesive experience for our teachers. So we need to prioritize. But, which CCCs are the most important? Or are they all equally important? And if we choose specific CCCs to focus on, are they connected to specific [science and engineering practices](https://ngss.nsta.org/PracticesFull.aspx)(SEPs)? Let's boil these wonderings down into a couple research questions:

### Research Questions
1. How are the CCCs and SEPs represented in the NGSS? Is there a difference between middle and high school?
2. Is there a relationship between CCCs and SEPs?

## Methodology
The NGSS organizes the content, SEPs, and CCCs into statements called [performance expectations](https://www.nextgenscience.org/glossary/performance-expectation-pe)(PEs) which are freely available on the Internet. However, there are 208 of them, which would mean that taking the time to go to each webpage to figure out which SEPs and CCCs are specific to a PE would take a whole lot of time. And be super repetitive. So it's time for some webscraping!

### Gathering Data via Web Scraping
To create a data set of all the PEs, CCCs, and SEPs, I started with some light investigation of the official NGSS website. I found that you could [search](https://www.nextgenscience.org/search-standards) for the PEs, or download a full [PDF](https://www.nextgenscience.org/sites/default/files/AllDCI.pdf) of the standards. You can also access the individual pages for each PE, if you know the number and the full name. I don't know all 208 PEs, so I looked for another route.

Given my familiarty with science education, I quickly realized that the [National Science Teaching Association](https://www.nsta.org/) might have a better solution. And they do! They have created id numbers for each PE page, which means that I could easily set up a web scraper using BeautifulSoup and a looping URL:

```python
from bs4 import BeautifulSoup
import requests
import pandas as pd

#Create empty list to gather site links
urls = []
#Append all links to urls list
for i in [x for x in range(23,234) if x != 24 and x != 25 and x!=201]:
   urls.append('https://ngss.nsta.org/DisplayStandard.aspx?view=pe&id=' + str(i))
```

### DataFrame Manipulation with pandas

## Results

### RQ #1: The cross-cutting concepts are **not** represented equally

### RQ #2: There is not a substantional relationship between the cross-cutting concepts and the science and engineering practices

## Conclusions 


To put text in *italics*

To put text in **bold**

A link goes like [link]https://www.nba.com

Numbered list:
1. First
2. Second
3. Third


Bulleted List
*

Python code block:
```python
    import numpy as np

    def test_function(x,y):
        z = np.sum(x,y)
```

