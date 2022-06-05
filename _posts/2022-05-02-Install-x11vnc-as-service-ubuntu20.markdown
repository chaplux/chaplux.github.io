---
layout: post
title: Install x11vnc as service on Ubuntu 20.04
date: 2022-06-03 10:32:52 +0300
img: Chaplux_x11vnc.png # Add image post (optional)
tags: [Ubuntu 20.04, Remote Desktop, x11vnc, Terminal]
---
Install x11vnc
> sudo apt-get install x11vnc

Add service on systemd
> sudo nano /lib/systemd/system/x11vnc.service

Add this file
> [Unit]
 
> Description=x11vnc service
 
> After=display-manager.service network.target syslog.target


> [Service]
 
> Type=simple

> ExecStart=/usr/bin/x11vnc -forever -display :0 -auth guess -passwd YOURPASSWD

> ExecStop=/usr/bin/killall x11vnc

> Restart=on-failure
 

> [Install]
 
> WantedBy=multi-user.target

Reload service on systemd daemon
> systemctl daemon-reload

Enable x11vnc services
> systemctl enable x11vnc.service

Start x11vnc services
> systemctl start x11vnc.service

Check status x11vnc service
> systemctl status x11vnc.service
