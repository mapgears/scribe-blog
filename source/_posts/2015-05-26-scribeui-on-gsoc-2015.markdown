---
layout: post
title: "ScribeUI on GSoC 2015"
date: 2015-05-26 08:45:38 -0400
comments: true
categories: GSoC
---
ScribeUI is back as a Google Summer of Code project with OSGeo. 

We decided to put the old developement blog back up, and use it to post news on what's going on with the project. I will post a getting started guide this week to help new users use ScribeUI. This summer's plan involves fixing bugs and adding a few features:

### Improve the error detection of ScribeUI

Right now, the only way we have to know something is wrong with a Scribe map file is when it is converted to the Mapserver Mapfile format and Mapserver can't read it. ScribeUI displays Mapserver's error output in the logs, allowing the user to have an idea of the problem. However, the line numbers displayed in the logs do not fit with the Scribe files since it is a different format. The goal is to have an error output that displays the correct location of errors in the code.
  
### Import and export workspaces

I want to add the possibility to export workspaces into a single zipped file, and allow other users to import it on their installation of ScribeUI. This would make sharing maps easier.
  
### Classify the data

One of the commonly requested features to automatically add classes based on a set of data and scales. For example, most demographics can be displayed with a map colored with a scale based from brighter to darker colors. Adding a way to automatically create these classes would be very useful to ScribeUI users.

My objective is to complete all these features by the end of the summer and release a new stable version of ScribeUI. 
