---
layout: post
title: "How Many Birthdays do your Facebook Friends Have?"
date: 2016-05-25
thumbnail: /images/2016-05-25_thumbnail.png
---

The more friends on Facebook you have, the more birthdays you have to remember. I started wondering at what point I would be wishing friends happy birthday everyday. Although having more friends at first increases the number of different birthdays represented, the returns quickly diminish as your friends become more likely to share a common birthday than have a unique one.

To test this, I randomly simulated 1000 groups of friends with an equal probability to have a birthday on every day. On average, you need 1902 friends before you have sampled every day of the year.

![Number of Unique Birthdays](/images/BirthdaysperFriend.jpeg)

But is our assumption of a flat distribution correct? To see I went to the Wikipedia list of Births used in my previous [post]({% post_url 2016-04-25-Calendar %}). I sampled from that density of birthdays, again with 1000 simulated groups of friends. Turns out that the flat distribution is a pretty good assumption. You need about 2037 friends to have an average chance of hitting every day.
