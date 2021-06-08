---
layout: post
title: Imagemagick Convert to PDF Not Allowed
date: 2020-11-19 10:45:52 +0300
img: Chaplux_Imagemagick1.png # Add image post (optional)
fig-caption: # Add figcaption (optional)
tags: [Imagemagick, PDF, Policy]
---

I have a bash script to convert a PDF to an image using Image Magick. But ImageMagick has some security policies disabling some rights for security reasons.

>About ImageMagick sercurity policy
The restricted policy is made to prevent unknown vulnerabilities coming from third party software as Ghostscript used here for PDF files. Be sure to update Ghostscript.

To re enable find the line below

>policy domain="coder" rights="none" pattern="PDF" and replace "none" by "read|write"
in /etc/ImageMagick-6/policy.xml


