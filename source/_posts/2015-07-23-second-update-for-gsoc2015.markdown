---
layout: post
title: "Second update for GSoC2015"
date: 2015-07-23 08:08:13 -0400
comments: true
categories:
author: "Samuel Lapointe"
---

## Summary of the update

I am releasing today version 1.6, the second update for [Google Summer of Code 2015](https://www.google-melange.com/gsoc/homepage/google/gsoc2015). The main objective of this update was to add map import and export.

### Map export
To export a map, select a map in the manager tab and press on the **Export Map** button. This popup will open:

![Example](https://cloud.githubusercontent.com/assets/2997638/8852231/e7ca5b9a-3121-11e5-859c-dbebbf1c99e7.png)

Pressing on Export will generate a .zip file containing the map files. You can use it as a way to backup your maps or to share them with other users.

### Map import

To import a map, go in the manager tab and press the **Import Map** button. This popup will open:

![Example](https://cloud.githubusercontent.com/assets/2997638/8851763/79f4dd7c-311f-11e5-9b14-8ae38ce59eb8.png)

You can choose a name for the map to be imported, select a .zip file and press import. While the file is uploading, the logs won't update and the status will stay on "In progress". It can take a long time if the map is large or if your connection is slow. Once the process is complete, you will see the map in the manager view.


## Changelog

* [Fix #33](https://github.com/mapgears/scribeui/issues/33) - Add map import
* [Fix #51](https://github.com/mapgears/scribeui/issues/51) - Add a WMS Url for each map
* [Fix #67](https://github.com/mapgears/scribeui/issues/67) - Add map export
* [Fix #107](https://github.com/mapgears/scribeui/issues/107) - Fix some comment blocks not working in the Scribe syntax
* [Fix #128](https://github.com/mapgears/scribeui/issues/128) - Fix standard maps not being saved when there are accents in it
* [Fix #129](https://github.com/mapgears/scribeui/issues/129) - Fix includes not being removed when deleting a group on standard maps
* [Fix #130](https://github.com/mapgears/scribeui/issues/130) - Fix name tags having numbers appended to them in the Scribe syntax
* [Fix #131](https://github.com/mapgears/scribeui/issues/131) - Fix VOID keyword appearing with some comments with the Scribe syntax
* [Fix #132](https://github.com/mapgears/scribeui/issues/132) - Fix log files becoming very large
* [Fix #134](https://github.com/mapgears/scribeui/issues/134) - Fix french characters creating internal server errors
* [Fix #135](https://github.com/mapgears/scribeui/issues/135) - Fix import and export fields not emptying after the popup is closed
* Changed the map debug to use mapserv instead of shp2img

## Updating

You will need to add a link to your server's cgi-bin location in the local.ini file, in the [app:main] section. It will probably be very similar to the mapserver.url parameter, so you could place it next to it. The format is

    cgi.url = http://myserver.com/mypath/mycgi

For example, this is what I had to add to the demo's local.ini file:

    cgi.url = http://demo.scribeui.org/cgi-bin

You can update ScribeUI to v1.6 by using these commands:

    sudo chown -R youruser .
    git pull
    git checkout v1.6
    sudo make perms

## Plan for the rest of the summer

The last month of this summer will be spent on the data classifying feature. The goal is to provide a way to create a range of classes with different colors from a set of data. You can find more information about the summer's plan [here](http://blog.scribeui.org/blog/2015/05/26/scribeui-on-gsoc-2015/).
