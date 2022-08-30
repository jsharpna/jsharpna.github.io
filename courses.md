---
layout: page
title: Courses
permalink: /courses/
---

# STA 208: Statistical Machine Learning

Machine learning is how to get computers to automatically learn and improve with experience. Experience comes in the form of data, improvement is with respect to some performance metric, and learning is done by a learning algorithm. There are always computational constraints, such as the architecture, computation time, bandwidth limitations, and so on. So we can more precisely restate the goal thus: to construct learning algorithms that use data to improve with respect to a performance metric and do so under computational constraints.

Due to the COVID-19 lockdown this course has been flipped!  You can find the syllabus and download the jupyter notebooks in the [Github content page](https://github.com/jsharpna/DavisSML).  I am recording my lectures on youtube, which can be found in [this playlist](https://www.youtube.com/playlist?list=PLCTcZfebNw2kcgWfMu41CMCA1c03lVLBE).  Here is the first video...

<iframe width="560" height="315" src="https://www.youtube.com/embed/vflpw7_p-Pg" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

# STA 220/141B: Data Science with Python

Statistics is the science of extracting knowledge from data. Before the advent of computers, datasets were restricted to what could be measured and painstakingly recorded by hand (think of Mendel's genetics experiments). Now, the pipeline of turning observable phenomena into data has been dramatically broadened by the ubiquitousness of sensors and input devices, and the internet to transfer the extracted data across the world. The Data Sciences represent all of the facets of working with and extracting knowledge from data, such as data extraction, processing, curation, maintainance, representation, visualization, exploration, hypothesis testing, parameter estimation, prediction.

In this course, we will focus on data science tools in Python and Javascript.  First, we will see collaboration, presentation, and containerization tools git, jupyter, pip, virtualenv.  Second we will go over data processing and munging tools such as python base language (strings, input/output), numpy, pandas, sqlite.  Third, we will learn data extraction from the web with requests, html parsing, and APIs.  Fourth, we will learn data visualization tools such as matplotlib, plotnine, and D3.

I am posting the lectures to this [github repo](https://github.com/jsharpna/141Blectures-sp2021) and to serve the lectures you can clone and run jupyter in the following way...
```
git clone https://github.com/jsharpna/141Blectures-sp2021.git
cd 141Blectures-sp2021/lecture1
jupyter nbconvert lecture1.ipynb --to slides --post serve
```
You can find an old draft of some [book chapters here](http://anson.ucdavis.edu/~jsharpna/DSBook/index.html) to an external site.