---
layout: post
title: "TSA Claims"
date: 2017-04-14
thumbnail: /images/2017-04-14_thumbnail.png
---


TSA Claim data...

Fly a fair amount... TSA data online... Reddit... 

Data cleaning... some entries were listed as not paid, but had the amount requested as the amount paid out.

For most of the analysis I used the total amount that the TSA listed as paid, with any entries that were listed rejected set to $0 paid out.

In total, 204263 claims were filed between between 2002 and February 2016 (the most recent data available when I downloaded the dataset) and the TSA paid out more than $16 million USD.

<img src="/images/TSA/Total_avg_claims.jpeg" alt="Total and average claims per year" style="width: 1000px;"/>

The total amount spiked in 2004 before falling to around $500,000 a year since 2010. The initial years of large total claims is likely driven by a few large personal injury claims. Looking at the inner 80% range on the far right shows a fairly consistent trend. Almost all claims are not paid out, and the 80th percentile sits between $100 and $300 for all years except 2002.

![Claims vs amount paid](/images/TSA/Claim_paid.jpeg)

A look at the amount paid out versus amount claimed shows two interesting things (note: this is a symlog plot where all values under $10 are shown in linear scale, and all values over $10 are shown in log-scale, while harder to interpret, this is the only good way I could think of to show off both the enormous range of the data and the large numbers of $0 claims.) First thing is that many people seem to be trolling the TSA by filling enormous claims. The largest claim requested was a nice round $3 trillion. Surprisingly enough, it didn't get filled.

Which airports have the most claims?  


Bigger airports have more claims... 
Normalize by total passengers. Data is pulled from...

The largest airports with the most claims per passengers?

2006: Newark International Airport [EWR].  <br>
Total passengers: 36724167, total claims: 703, <br>
claims per 10,000 passengers: 1.91 <br>
2007: San Diego International [SAN].  <br>
Total passengers: 18336761, total claims: 373, <br>
claims per 10,000 passengers: 2.03 <br>
2008: John F. Kennedy International [JFK].  <br>
Total passengers: 47799090, total claims: 857, <br>
claims per 10,000 passengers: 1.79 <br>
2009: John F. Kennedy International [JFK].  <br>
Total passengers: 45915069, total claims: 696, <br>
claims per 10,000 passengers: 1.52 <br>
2010: John F. Kennedy International [JFK].  <br>
Total passengers: 46514154, total claims: 726, <br>
claims per 10,000 passengers: 1.56 <br>
2011: John F. Kennedy International [JFK].  <br>
Total passengers: 47683529, total claims: 749, <br>
claims per 10,000 passengers: 1.57 <br>
2012: John F. Kennedy International [JFK].  <br>
Total passengers: 49291765, total claims: 670, <br>
claims per 10,000 passengers: 1.36 <br>
2013: John F. Kennedy International [JFK].  <br>
Total passengers: 50423765, total claims: 694, <br>
claims per 10,000 passengers: 1.38 <br>
2014: John F. Kennedy International [JFK].  <br>
Total passengers: 53254533, total claims: 644, <br>
claims per 10,000 passengers: 1.21 <br>
2015: Orlando International Airport [MCO].  <br>
Total passengers: 38727749, total claims: 372, <br>
claims per 10,000 passengers: 0.96 <br>

The largest airports with the fewest claims per passengers?<br>
2006: Kansas City International [MCI]. <br>
Total passengers: 11237480, total claims: 36,<br>
claims per 10,000 passengers: 0.320357<br>
2007: San Francisco International [SFO]. <br>
Total passengers: 35792707, total claims: 108,<br>
claims per 10,000 passengers: 0.301737<br>
2008: Kansas City International [MCI]. <br>
Total passengers: 11166835, total claims: 15,<br>
claims per 10,000 passengers: 0.134326<br>
2009: San Francisco International [SFO]. <br>
Total passengers: 37338942, total claims: 33,<br>
claims per 10,000 passengers: 0.0883796<br>
2010: San Francisco International [SFO]. <br>
Total passengers: 39253999, total claims: 37,<br>
claims per 10,000 passengers: 0.0942579<br>
2011: Kansas City International [MCI]. <br>
Total passengers: 10400854, total claims:  6,<br>
claims per 10,000 passengers: 0.0576876<br>
2012: San Francisco International [SFO]. <br>
Total passengers: 44399885, total claims: 31,<br>
claims per 10,000 passengers: 0.06982<br>
2013: Kansas City International [MCI]. <br>
Total passengers: 9872314, total claims:  4,<br>
claims per 10,000 passengers: 0.0405173<br>
2014: Kansas City International [MCI]. <br>
Total passengers: 10166881, total claims:  3,<br>
claims per 10,000 passengers: 0.0295076<br>
2015: San Francisco International [SFO]. <br>
Total passengers: 50057887, total claims: 32,<br>
claims per 10,000 passengers: 0.063926<br>


<iframe src="/graphs/airports.html" marginwidth="0"
        marginheight="0" scrolling="no" width="1000" height="600" frameBorder="0"></iframe>


