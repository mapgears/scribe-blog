---
layout: page
title: "Week 5"
date: 2015-06-26 16:02
comments: true
sharing: true
footer: true
---

Hi all, this is my fifth report for the ScribeUI project.

**Completed this week**

* This week, I worked on exporting maps. I was able to add a basic function where it takes the content of the map and zips it. The user can choose how much vector/raster data is to be included in the zip. As soon as the export is complete, a popup appears to download the file and the file is deleted from the server when it's no longer needed.

**Plan for next week**

* Even though the export works, I'm not satisfied with it yet, as there's nothing indicating progress to the user. I've tried different ways to do it but none of them were very "clean" or efficient. Next week, I will try implementing Websockets so that I can send information to the client on the progress as the export process goes on. My mentors and I have never used them before so I expect it to take me all week.

**Blocking issues**

* This week was a bit slower than usual, because I was sick and there was a national holiday. Moreover, I tried a lot of different ways to send information to the client while the export process was taking place, which didn't work in the end. I have found a possible solution for it (communicating through server logs) but it's not optimal, so I'll spend next week trying to make it work with websockets, and if it doesn't work I'll simply use the solution I found.

Have a nice week-end!
