---
layout: post
title: "Madison Area Multifamily Vacancy"
date: 2016-03-12
thumbnail: /images/2016-03-12_thumbnail.png
---
I've been interested in all the new apartment construction in Madison over the past few years. One explanation I keep hearing is that the vacancy rate of apartments is much lower than the target of 5%. All data in this post is from <a href="https://www.mge.com/customer-service/multifamily/vacancy-rates/">MG&E</a>. <small> Caveat: This dataset contained some zipcodes with very few apartments. The vacancy rates measured in these zipcodes varied wildly and did not reflect market forces. Because of this, all zipcodes with fewer than 20 apartments have been removed from this analysis. </small>

First I looked at the general trend of vacancy rates over the past few years.

<iframe src="/graphs/vac_chart.html" marginwidth="0"
        marginheight="0" scrolling="no" width="600" height="400" frameBorder="0"></iframe>

We see the vacancy rate has come down in most Madison zipcodes, but we also see a seasonal trend. This can be seen easier if we plot the data by quarter. The vacancy rates peaked around 2005 and have been generally falling since then except for a spike in 2010. <small> Select years in the left chart to see the quarterly trend.</small>

<iframe src="/graphs/vac_trends.html" marginwidth="0"
        marginheight="0" scrolling="no" width="1000" height="400" frameBorder="0"></iframe>


Next I wanted to look at how the location affected the rates. We can see that the vacancy rate increased in the surrounding areas after 2006, but has stayed below the 5% target in the downtown zipcodes over the last ten years.

<iframe src="/graphs/vac_map.html" marginwidth="0"
        marginheight="0" scrolling="no" width="800" height="800" frameBorder="0"></iframe>

<small> Code for the plots in this post was based, in part, on examples from <a href="https://bost.ocks.org/mike/map/">Mike Bostock</a> and <a href="http://bl.ocks.org/stevenae/8362841">stevenae</a>, as well as the wonderful online documentation for D3.</small>