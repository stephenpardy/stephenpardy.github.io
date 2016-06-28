---
layout: post
title: "Voting on Science"
date: 2016-06-27
thumbnail: /images/2016-06-27_thumbnail.png
---

An important part of the scientific process is publishing results in peer-reviewed journals. Although these journals all have some quality control, peer-review is not the end of the process and many results are judged on their correctness only after many years of follow-up studies. Further, peer-reviewed journals can be very expensive, both to read and to publish in. One faster, and free, alternative for natural sciences is the arXiv. This daily list of new research is supposed to act as a place to rapidly disseminate new results. There are many different aggregators for arXiv papers, the most common in astronomy is VoxCharta which lets you up and down-vote papers and make comments. There is a long history of studying the effects of arXiv on citations over time, but I was curious about the voting patterns and how they correlated with citations. I downloaded all the votes for every paper in 2013, and then counted the number of citations those papers had by April in 2016 (note: this means that some papers have more time to get citations, but as I will show later, this didn't seem to matter).


The most voted paper over this year was 'A Rapidly Star-forming Galaxy 700 Million Years After the Big Bang at z=7.51' by S.L. Finkelstein et al. with 107 votes and 99 citations. The most cited paper was  'Planck 2013 results. XVI. Cosmological parameters' by the Planck collaboration with 50 votes and 3880 citations.

![Very slight negative trend on number of citations and number of votes with position on ArXiV](/images/voxcharta/position_votes_citations.jpeg)

The first thing I noticed is that there is indeed a very slight negative trend with papers appearing later in the arXiv receiving fewer citations and votes (see work by Haque and Ginsparg: [http://arxiv.org/abs/0907.4740](http://arxiv.org/abs/0907.4740)). The default sorting order of the arXiv is by submission time, which favors papers that are submitted by dedicated researchers who have fast internet connections.

![Distributions of votes and citations are different](/images/voxcharta/cumulativeVoteFraction.jpeg)

If we look at the distributions of votes and citations, we can see that the vast majority of papers have no votes or citations. Beyond that we can see that the two distributions are different (the two sided KS test statistic is 0.35 with a p-value nearly 0).

![Very weak correlation between votes and citations](/images/voxcharta/votes_citations.jpeg)

There does appear to be a very weak correlation between the votes and citations, but not nearly as strong as I initially suspected. It is likely that people are voting for papers for different reasons than they are citing them. It is also possible that papers that sounds appealing at first end up being duds, or that seemingly uninteresting papers end up making significant contributions.  

Next I wanted to check some confounding factors.

![No real difference between different days of the week](/images/voxcharta/Votes_day.jpeg)

There is no significant difference in voting patterns between the days of the week.


![No real difference of citations over the whole year](/images/voxcharta/Citations_Votes_year.jpeg)

And no trend over the whole year for either votes or citations. If there was a significant bias for the papers later in the year, I would expect to see it here. The large bump toward the end of March is for the Planck paper.


