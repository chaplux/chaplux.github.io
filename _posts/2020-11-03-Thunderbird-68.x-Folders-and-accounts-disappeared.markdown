---
layout: post
title: Thunderbird 68.x Folders and accounts disappeared
date: 2020-11-03 12:45:20 +0300
description: You’ll find this post in your `_posts` directory. Go ahead and edit it and re-build the site to see your changes. # Add post description (optional)
img: Chaplux_Thunderbird0.png # Add image post (optional)
fig-caption: # Add figcaption (optional)
tags: [Thunderbird, Mozilla]
---

Thunderbird 68.x Folders and accounts disappeared

If your thunderbird version get automatic upgrade from 60.9.x to 68.2x, it will effected on your account and folder disappeard. To fix this problem, removing the 'global-messages-db.sqlite' file from profile helps Thunderbird to load correctly and the database will get repopulate.

You can find global-messages-db.sqlite in this path.
>/home/user/.thunderbird/xxx.default/global-messages-db.sqlite

