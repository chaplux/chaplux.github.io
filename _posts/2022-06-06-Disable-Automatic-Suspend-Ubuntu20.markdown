---
layout: post
title: Disbale automatic suspend Ubuntu 20.04
date: 2022-06-06 13:31:52 +0300
img: Chaplux_sshjumphost.png # Add image post (optional)
tags: [ubuntu, hibernate, suspend, systemd]
---
To prevent Ubuntu 20.04 system from suspending or going into hibernation, you need to disable the following systemd targets:

> $ sudo systemctl mask sleep.target suspend.target hibernate.target hybrid-sleep.target

Verify if the changes have been effected using the command:

> sudo systemctl status sleep.target suspend.target hibernate.target hybrid-sleep.target
