---
layout: post
title:      A frank download of the Sinatra project
date:       2018-09-14 22:49:05
permalink:  a_frank_download_of_the_sinatra_project
categories: assignments, projects
---


**My project idea**

Because I’ve recently gotten back into learning piano through Youtube videos, I decided to base my Sinatra project on that use case. So I made Virtual Virtuoso, an app for users who want to keep track of the songs they're mastering and the videos they use to learn them. Below are a few thoughts on the project…

**Problem area: has many through**

One of my biggest mental blocks was the has_many :through type of many-to-many relationship, which I struggled to understand for a while. In addition to our lessons and labs, I found [this](https://teamtreehouse.com/library/has-many-through-associations) teamtreehouse explanation helpful because they illustrate an app with Magazine, Subscriber, and Subscription models, which for some reason made things click for me. Magazines and Subscribers have a has_many through relationship - magazines have many subscribers and subscribers have many magazine subscriptions, but they're associated through a third model, the Subcription. This was parallel to my app, in which users can have many songs in their libraries, and songs can be learned by multiple users. So it’s also a many-to-many relationship between users and songs. In my join table UserSongs, each instance is made up of one user and one song, linking them. Each “UserSong” has only one user and one song - a belongs-to relationship. When I started thinking about that model like a user library, it became much more intuitive and easy to work with mentally.

Tux was a godsend for association testing, helping me cement what would happen behind the scenes when using join tables. For example, I didn’t immediately realize that adding a song to a user using something like `@user.songs << song` automatically triggers the reverse association (i.e., that the user is added to the collection of song.users). For a while I was making the UserSong instance directly, which wasn’t necessary and made my code more confusing.

**Slowly but cssurely**

I knew my html/css skills needed some work, so I decided to play around with Bootstrap for the views in my app. I wanted to practice getting familiar with the framework without spending too much time editing the styles to my liking, so I used it right out of the box. It also helped keep me motivated - it was satisfying when views turned out looking nice aesthetically.

**Help along the way**

Usually I have a hard time being patient enough to sit through video explanations, but the ones included in the Sinatra lessons are incredibly useful for illustrating the structure of the project, which is often the hardest part for me to troubleshoot. (A structural problem that stumped me for a while was not including any of my controllers besides the main Application controller in my config.ru file…) Additionally, the live screen shares instructors did were extremely helpful - hearing other students asking questions and watching the organic thought process of creating/designing an application was invaluable.

I enjoyed this project even more than the last, and am very excited to see what Rails will be like!
