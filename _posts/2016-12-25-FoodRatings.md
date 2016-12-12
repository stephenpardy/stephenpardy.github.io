---
layout: post
title: "Inequalities in Food Ratings"
date: 2016-12-25
thumbnail: /images/2016-12-25_thumbnail.png
---

While eating out one night my girlfriend and I wondered whether the restaurants in Madison were rated differently if they were Asian as opposed to American. I dug into the ratings of all the Madison area restaurants to check. First, below you can see the distribution of star ratings for each category in the dataset that I used.

![Distribution of Ratings](/images/ratings/all_ratings.jpeg)

Look at the distribution of ratings for each food category. Use the two-side [Kolmogorov-Smirnov test](https://en.wikipedia.org/wiki/Kolmogorov%E2%80%93Smirnov_test) to determine if the category has a significantly different distribution than all the other restaurants. Because I am doing so many different tests, there is a high likelihood that some will happen to look significant just due to chance. To correct for this, I use the [Bonferroni correction](https://en.wikipedia.org/wiki/Bonferroni_correction). The p-value that I was looking for was 0.00125. Three categories appeared different. Food Trucks, Fast Food, and Sports Bars.

![Distribution of Ratings](/images/ratings/relative_ratings.jpeg)

Fast food restaurants have a relatively flat distribution with mostly ower and middle ratings, sports bars are highly peaked around 3 stars, and people in Madison seem to love food trucks.


Clustering using the overlap in categories between different restaurants. I tried three different approaches.

K-Means clustering with Jaccard Distances, spectral clustering using a normalized similarity Matrix between the categories, and Agglomerative Clustering using the overlap in the categories.

In each case I used 10 clusters. Although the methods differed, the results were broadly consistent: clustering the restaurants into similar groups works (mostly) but shows a fairly low difference between groups. The takeaway from this analysis is that the different types of restaurants are rated broadly consistently across the whole city.

<div class="tabbable">
  <ul class="nav nav-tabs">
    <li class="active"><a href="#tab1" data-toggle="tab">Jaccard K-Means</a></li>
    <li><a href="#tab2" data-toggle="tab">Spectral Clustering</a></li>
    <li><a href="#tab3" data-toggle="tab">Agglomerative Clustering</a></li>
  </ul>
  <div class="tab-content">
    <div class="tab-pane active" id="tab1">
      <p>K-Means is a classic algorithm that splits a dataset into K different sections. Usually, the euclidian distance is used to assign points into the closest of the K groups. Instead, I used the Jaccard Distance. The implementation was by github user <a href="https://github.com/FindKim/Jaccard-K-Means">FindKim</a>. The Jaccard distance is computed by comparing which restaurants belong to the same categories.
      <img src="/images/ratings/jaccard_kmeans_restaurants_dist.jpeg" alt="Violin_Jaccard_Groups" style="width:750px;">
      </p>
    </div>
    <div class="tab-pane" id="tab2">
      <p>Spectral Clustering using a similarity matrix. The similarity matrix was made using whether the restaurants belonged to the same categories. EQUATION
      <img src="/images/ratings/spectral_restaurants_dist.jpeg" alt="Violin Spectral Groups" style="width:750px;">
      </p>
    </div>
    <div class="tab-pane" id="tab3">
      <p>Agglomerative Clustering.
      <img src="/images/ratings/AC_restaurants_dist.jpeg" alt="Violin AC Groups" style="width:750px;">
      </p>
    </div>
  </div>
</div>

