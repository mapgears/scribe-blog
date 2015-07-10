---
layout: page
title: "Week 6"
date: 2015-07-03 20:07
comments: true
sharing: true
footer: true
author: "Samuel Lapointe"
---

Hello everyone, this is my sixth report for the ScribeUI project.

**Completed this week**

* I fixed a few bugs reported to me by a user this week (Issues #128 and #130)
* Implemented websockets in a test project using gevent-socketio, but they're not compatible with apache so it won't be possible to add them to ScribeUI
* Improved the export feature by dealing with more unexpected situations

**Plan for next week**

* Unfortunatly I wasn't able to implement websockets as planned last week as the only library I could find for pyramid isn't compatible with apache. I will have to spend the next week to find another way to display progression to the user, possibly through a log file or using the same method as the mapcache feature.

**Blocking issues**

* I had problems with a lack of space on my main partition, which prevented me from testing large exports. I managed to move some directories to a bigger partition so the problem is solved, but it slowed me down a bit
* Work on websockets was a fun learning experience but it didn't advance the project

Have a nice weekend, and for those of you in the US a nice independance day!
