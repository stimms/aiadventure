---
title: "Types of AI"
date: 2018-09-27T12:51:19-06:00
draft: false
tags: [
    "learning",
    "basic",
    "introduction"
]
categories: [
    "Introduction"
]
image: /images/starting.jpg
---

A number of basic types of machine learning exist. Two major categories we're looking at are supervised and unsupervised learning. These describe the type of data that we're working on.

# Supervised

Supervised means that we have some answers already. So perhaps a data set of trees heights vs age. We know how tall trees are at a certain age and we want to know for some newly given age how tall we can expect the tree to be. 

![Height vs Age](/images/typesOfAI/heightage.png)

Here we look up the red blob. This is an example of a regression where we're looking for a continuous value somewhere in the range. There is a second type where we're attempting to find a discrete value - this is called classification.

![Classification](/images/typesOfAI/classification1.png)

Here we're trying to find a line which will split our data set into two or more types. An example here could be classifying types of trees based on a known value such as bark thickness. If the bark thickness falls on the left side of the classifying line then it is spruce and on the other side birch.

![Classification](/images/typesOfAI/classification2.png)

# Unsupervised

Unsupervised means that we don’t actually know what the outcome is when we start. For instance say we've got a bunch of data about 1000s of stars. We'd like to group them together based on some similar aspects. A naive approach would be to look at something like size and group them together by that, but this could miss out on some other deeper similarities. Our data could contain hundreds of features or aspects about each star (luminosity, size, temperature, age, spectrum…) and an unsupervised algorithm could find similarities based on multiple features which would be impossible for a human to find. Think about that example where machine learning found that people buy diapers and cigarettes together a lot - unexpected result which humans would not have thought to find.

There is no feedback on the results.

![Classification](/images/typesOfAI/clustering.png)

Another great example is to find market segments based on a bunch of customer data.