---
layout: post
title:  "A tale of two curves - stuff about my GSoC project"
author: "Tanmay Chavan"
date:   2021-06-01 20:47:59 +0530
categories: jekyll update
background: '/img/EFXSes9UCfsyRVoNeQ2ZTB-1200-80.png'
---

Hi everyone! I'm Tanmay Chavan, a CS Sophomore at PICT, India. This summer, I'm going to be working for Krita, to implement cleaner operations on vector shapes.

   I had taken a class on computer graphics the earlier semester, and I found it to be really interesting. There is some kind of satisfaction and a sense of fulfillment in seeing your algorithms generate reults which can be seen by our eyes. So, this project statement piqued my interest. Upon talking with Dmitry, the lead developer of the software, I came to know the issue lies in the way Qt deals with curve intersections. Their algorithm, although fast, was unsuitable for our purposes. It approximated the curve as a polygon, which meant you could get away with finding intersections for purely lines. This led to generation of an escess number of nodes, which was not efficient. I looked up the standard algorithms to handle Bezier curve intersections, and they were good. However, upon further digging, I found a neat mathematical way to solve the problem. This method was perfect for the application, as it would compute the intersection points for two curves pretty fast and with very high accuracy, especially for curves with degree 3 or less. Apparently, Qt supports Bezier curves upto degree 3 as well.

   So, I'll have to write the necessary code for the project based on [this text by Thomas Sederberg][sederberg]. Apart from the core algorithms, I'll have to write unit tests and try to keep it as abstracted as possible. Although initially daunted by the project statement, tinkering around with Qt libraries and discussing stuff with the very helpful Krita team helped me get prepared for the project. So, I hope this will be a really awesome experience, and I look forward to work with the community, and contribute as much as I can. I'll keep updating this blog, and let you know about my progress with the task at hand.

[sederberg]: https://scholarsarchive.byu.edu/facpub/1/