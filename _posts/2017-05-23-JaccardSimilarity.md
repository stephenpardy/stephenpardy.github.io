---
layout: post
title: "Jaccard Similarity"
date: 2017-05-22
thumbnail: /images/2017-05-22_thumbnail.png
---


I've been using the [Jaccard similarity index](https://en.wikipedia.org/wiki/Jaccard_index) in a lot of work recently. Given two sets, the Jaccard index is the ratio between the length of their intersection and the length of their union. Basically divide the number of items shared between two collections by the total number of unique items the collections have.

The Jaccard index is a quick and easy way to compare the similarity of two collections that are not in ordinary Euclidian space (like a collection of words or shared neighbors in a friends-of-friend algorithm). You can convert it to the Jaccard distance by taking 1 - Jaccard Index.

It is commonly used in text analysis, although other, more sophisticated tools such as word2vec have become more common recently. I've been trying to develop a better intuition for the Jaccard index and realized that I have not seen a good interactive demonstration of it. An example using d3 was surprisingly straightforward and also let me try out text input in javascript. Try it out below!

<iframe src="/graphs/jaccard.html" marginwidth="0"
        marginheight="0" scrolling="no" width="1000" height="500" frameBorder="0"></iframe>


Text input inspired by [eesur](http://bl.ocks.org/eesur/9910343).