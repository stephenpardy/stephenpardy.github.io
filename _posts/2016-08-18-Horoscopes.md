---
layout: post
title: "Horoscope Analysis"
date: 2016-08-18
thumbnail: /images/2016-08-18_thumbnail.png
---

<style type="text/css">
    td, th {
        text-align: center;
    };
</style>

I have been interested in text analysis and recurrent neural networks for a while. If you don't know what a recurrent neural network is, I highly encourage you to check out Andrej Karpathy's blog post [The Unreasonable Effectiveness of Recurrent Neural Networks](http://karpathy.github.io/2015/05/21/rnn-effectiveness/). While recurrent neural networks (RNNs) can be used on a wide range of data, one of their most promising applications is simulating conversations and other text data. Encouraged by Andrej's post and the wide variety of Twitter bots I've been seeing in the wild I decided to take a stab at RNNs on astrology horoscope.

After downloading 10 years worth of daily horoscopes I looked into them with text analysis tools from SciKit Learn. First I wanted to see which words were most unique to each horoscope and which were most general (while writing this post I found a post by [billpmurphy](https://github.com/billpmurphy/old_website/blob/master/_posts/2015-08-28-are-all-horoscopes.md) looking at a very similar question). For this analysis I used 'Term Frequency - Inverse Document Frequency' which ranks words based on their frequency in the document, but penalizes words that are common across the entire corpus.

So which words are most unique and most common? The following table lists the five most and least common words along with their TF-IDF score.

<table border="1">
<tr>
<th>Aries</th>
<th>Leo</th>
<th>Sagittarius</th>
<th>Taurus</th>
<th>Virgo</th>
<th>Capricorn</th>
<th>Gemini</th>
<th>Libra</th>
<th>Aquarius</th>
<th>Cancer</th>
<th>Scorpio</th>
<th>Pisces</th>
</tr>
<tr><th colspan = "12">Most Unique</th></tr>

<tr>
<td>folk (0.20)</td>
<td>lions (0.69)</td>
<td>archer (0.45)</td>
<td>taurean (0.21)</td>
<td>virgos (0.87)</td>
<td>capricorns (0.64)</td>
<td>geminis (0.61)</td>
<td>libran (0.49)</td>
<td>aquarians (0.81)</td>
<td>geminis (0.11)</td>
<td>scorpios (0.89)</td>
<td>remote (0.10)</td>
</tr>
<tr>
<td>aggressive (0.11)</td>
<td>methodically (0.06)</td>
<td>sagittarian (0.21)</td>
<td>variety (0.13)</td>
<td>immerse (0.05)</td>
<td>goat (0.14)</td>
<td>versatile (0.09)</td>
<td>virgos (0.13)</td>
<td>loom (0.06)</td>
<td>fluctuate (0.11)</td>
<td>hunting (0.04)</td>
<td>contains (0.09)</td>
</tr>
<tr>
<td>pique (0.11)</td>
<td>im (0.06)</td>
<td>scorpios (0.10)</td>
<td>uninvited (0.10)</td>
<td>utter (0.05)</td>
<td>sagittariuss (0.07)</td>
<td>witted (0.08)</td>
<td>resulting (0.09)</td>
<td>shaking (0.06)</td>
<td>confront (0.10)</td>
<td>volcanic (0.04)</td>
<td>doldrums (0.09)</td>
</tr>
<tr>
<td>perseverance (0.10)</td>
<td>gusto (0.06)</td>
<td>classroom (0.08)</td>
<td>dedicated (0.10)</td>
<td>imposing (0.04)</td>
<td>rainbows (0.06)</td>
<td>fatigued (0.08)</td>
<td>disenchanted (0.09)</td>
<td>fighting (0.05)</td>
<td>refresh (0.09)</td>
<td>virgos (0.04)</td>
<td>rate (0.08)</td>
</tr>
<tr>
<td>intricate (0.08)</td>
<td>hate (0.05)</td>
<td>scale (0.08)</td>
<td>indulgent (0.08)</td>
<td>exasperated (0.04)</td>
<td>prompted (0.06)</td>
<td>ether (0.07)</td>
<td>covered (0.08)</td>
<td>designer (0.05)</td>
<td>emerges (0.09)</td>
<td>unstoppable (0.04)</td>
<td>temperamental (0.08)</td>
</tr>
<tr><th colspan = "12">Most Common</th></tr>
<tr>
<td>tingling (0.00)</td>
<td>miscalculated (0.00)</td>
<td>miserly (0.00)</td>
<td>overnight (0.00)</td>
<td>outshining (0.00)</td>
<td>overloaded (0.00)</td>
<td>overestimating (0.00)</td>
<td>overreactions (0.00)</td>
<td>output (0.00)</td>
<td>overstating (0.00)</td>
<td>overactive (0.00)</td>
<td>overview (0.00)</td>
</tr>
<tr>
<td>merrily (0.00)</td>
<td>miscalculate (0.00)</td>
<td>miserably (0.00)</td>
<td>overloading (0.00)</td>
<td>outs (0.00)</td>
<td>overload (0.00)</td>
<td>overestimated (0.00)</td>
<td>overreaction (0.00)</td>
<td>outperformed (0.00)</td>
<td>overstated (0.00)</td>
<td>outwardly (0.00)</td>
<td>overuse (0.00)</td>
</tr>
<tr>
<td>merrier (0.00)</td>
<td>miracles (0.00)</td>
<td>miserable (0.00)</td>
<td>overload (0.00)</td>
<td>outrageously (0.00)</td>
<td>overindulging (0.00)</td>
<td>overestimate (0.00)</td>
<td>overreacted (0.00)</td>
<td>outlived (0.00)</td>
<td>oversights (0.00)</td>
<td>outward (0.00)</td>
<td>overturn (0.00)</td>
</tr>
<tr>
<td>tip (0.00)</td>
<td>tip (0.00)</td>
<td>misdirection (0.00)</td>
<td>overindulging (0.00)</td>
<td>outrageous (0.00)</td>
<td>overhauls (0.00)</td>
<td>overemotional (0.00)</td>
<td>overloading (0.00)</td>
<td>outline (0.00)</td>
<td>overshadowing (0.00)</td>
<td>outshining (0.00)</td>
<td>overstretched (0.00)</td>
</tr>
<tr>
<td>lain (0.00)</td>
<td>13th (0.00)</td>
<td>lain (0.00)</td>
<td>13th (0.00)</td>
<td>13th (0.00)</td>
<td>13th (0.00)</td>
<td>lain (0.00)</td>
<td>13th (0.00)</td>
<td>13th (0.00)</td>
<td>13th (0.00)</td>
<td>13th (0.00)</td>
<td>13th (0.00)</td>
</tr>
</table>

Not surprisingly, each sign talks about itself the most. Next I fed the different horoscopes into a RNN. For this I used the python version of [char-rnn](https://github.com/sherjilozair/char-rnn-tensorflow) with an RNN size of 512, three layers, and 75 epochs.

The algorithm sometimes spits out good advice: "This summer could lead to some exciting opportunities: stick rigidly to what you can do and no more! Friends prove to be worth it!"
But there are lots of misspellings, fragments, and general nonsense: "That leonine indicates close to you might hove or to concentrate on what could be a lot happening side! The current influences working as it may sound look."

As I train it more, I hope that the results will be better. You can check out daily horoscopes [here](/horoscope).
