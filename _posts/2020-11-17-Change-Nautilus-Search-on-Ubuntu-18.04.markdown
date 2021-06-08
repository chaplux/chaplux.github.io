---
layout: post
title: Change Nautilus Search on Ubuntu 18.04
date: 2020-11-17 10:45:52 +0300
img: Chaplux_Nautilus_Search0.png # Add image post (optional)
fig-caption: # Add figcaption (optional)
tags: [Ubuntu, Nautilus,search]
---
In ubuntu 18.04, search file using nautilus will bring up the result just on existing directory. If you want to search including sub directories you can change preferences as below.

Open the dconf Editor Via Application > System Tools > dconf Editor.
change recursive-search from 'local-only' to 'always'
Find the recursive-search on this directory org > gnome > nautilus > preferences > recursive-search
