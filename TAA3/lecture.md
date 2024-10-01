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

# Lecture: Social Media and Natural Language Processing (NLP)

This week we will focus on how we can use Flickr data to map the spatial patterns of images, and try to uncover people's preferences for photograph locations and content. We will also learn how to perform aggregation and clustering over data to better study them.

`````{admonition} Learning objectives
:class: important
- Become familiar with the Flickr API and how its data is structured
- Gain some familiarity with querying and collecting web data
- Learn more techniques on how to filter, clean, aggregate, and plot open geodata in Python
- Learn to aggregate data on a grid in Python
- Learn how to prepare data for clustering methods
- Learn the basics of K-Means clustering to understand data beyond spatial patterns
`````

## Reading
We will once again have a look at the book [An Introduction to Statistical Learning](https://www.stat.berkeley.edu/users/rabbee/s154/ISLR_First_Printing.pdf) by James, Witten, Hastie, and Tibshirani. This time, we take a look at unsupervised learning, specifically `K-Means` clustering. Specifically, read sections 10.1, 10.3.1, and 10.3.3 of the book. Section 10.3.2 is useful for those wanting to know more about clustering methods which don't need a pre-specified number of K, but it is not necessary to read it.

For those wanting to read a little bit more about the purpose of clustering, here are some suggestions for further reading and for inspiration on how clustering can further prove useful:
- [Thunderstorm Environments in Europe](https://egusphere.copernicus.org/preprints/2023/egusphere-2022-1453/egusphere-2022-1453-manuscript-version2.pdf) - the authors use clustering to study thunderstorm variables
- [Analysis of urban heat island effect using k-means clustering](https://ieeexplore.ieee.org/document/5691908) - The authors study the urban heat island effect in a similar fashion to the first paper
- [Traffic Accidents Analytics in UK Urban Areas using k-means Clustering for Geospatial Mapping](https://ore.exeter.ac.uk/repository/bitstream/handle/10871/125145/CameraReady_PID237.pdf?sequence=1&isAllowed=y) - Applications on traffic accident data