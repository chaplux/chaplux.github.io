---
layout: post
title: Remote Using SSH Jump Host
date: 2020-12-06 12:45:52 +0300
img: Chaplux_sshjumphost.png # Add image post (optional)
tags: [SSH, Tunnel, Browser, Terminal]
---
The simplest way to connect to a target server via a jump host is using the -J flag from the command line. This tells ssh to make a connection to the jump host and then establish a TCP forwarding to the target server, from there (make sure you’ve Passwordless SSH Login between machines).

ssh -J [HOST1] [HOST2]
