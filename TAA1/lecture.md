---
jupytext:
  cell_metadata_filter: -all
  formats: md:myst
  text_representation:
    extension: .md
    format_name: myst
    format_version: 0.13
    jupytext_version: 1.11.5
kernelspec:
  display_name: Python 3
  language: python
  name: python3
---

# Lecture: Introduction to Statistical Learning on Geospatial Data
We will start off this course with a primer on statistical learning for geospatial data. You will become acquainted with the basic principles of statistical learning, and we will run a couple of models on data collected from Google Earth Engine.

`````{admonition} Learning objectives
:class: important
- Gain a basic understanding of Google Earth Engine's Python bindings.
- Become acquainted with common terms and methods for supervised statistical learning.
- Learn the basic workflow of supervised statistical learning for classification tasks.
- Learn some tricks to more efficiently train and evaluate models.
- Understand some of the nuances of applying models on geopatial data.
`````
In this tutorial we only consider `supervised learning`, which is the process of learning from labelled reference data in order to predict. In TAA3, you will become aquainted with `unsupervised learning` methods as well, such as clustering.

## Reading
The book [An Introduction to Statistical Learning](https://www.stat.berkeley.edu/users/rabbee/s154/ISLR_First_Printing.pdf) by James, Witten, Hastie, and Tibshirani provides an excellent introduction to statistical learning. For this tutorial, we suggest to read sections 2.1 and 2.2 in its entirety, to gain a foundational understanding of statistical learning. Our goal in this tutorial is to provide the basic *why* understanding of statistical learning, because at the end of the day, modelling is a mindset, and individual models are just tools to support this mindset.

With that in mind, the following sections cover parts of the tutorial that may be useful for further reading, but are entirely optional.
- 4.3, for a better understanding of the logistic regression
- 8.1.2, for a primer on decision tree models
- 8.2.2, for more infomation about random forest models

## Google Earth Engine
Google Earth Engine (often abbreviated to GEE) is a cloud-based platform for planetary-scale geospatial analysis that brings Google's computational capabilities to bear on a variety of high-impact societal issues including deforestation, drought, disaster, disease, food security, water management, climate monitoring and environmental protection.

The Google Earth Engine consists of a multi-petabyte analysis-ready data catalog co-located with a high-performance, intrinsically parallel computation service. It is accessed and controlled through an Internet-accessible application programming interface (API) and an associated web-based interactive development environment (IDE) that enables rapid prototyping and visualization of results.

The data catalog houses a large repository of publicly available geospatial datasets, including observations from a variety of satellite and aerial imaging systems in both optical and non-optical wavelengths, environmental variables, weather and climate forecasts and hindcasts, land cover, topographic and socio-economic datasets. All of this data is preprocessed to a ready-to-use but information-preserving form that allows efficient access and removes many barriers associated with data management.

Users can access and analyze data from the public catalog as well as their own private data using a library of operators provided by the Earth Engine API. These operators are implemented in a large parallel processing system that automatically subdivides and distributes computations, providing high-throughput analysis capabilities. Users access the API either through a thin client library or through a web-based interactive development environment built on top of that client library.

## How to gain access to Google Earth Engine
To be able to use the Google Earth Engine during the tutorial, we will need to sign up.

The first step is to register. To do so, you have to go to the [Sign-up page](https://signup.earthengine.google.com/#!/). You can use your university account to register.