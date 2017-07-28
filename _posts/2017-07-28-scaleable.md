---
layout: post
title: "Internship Week 7: Scalable Web Applications "
author: "Sher Sanginov"
---


<img class="img-responsive" src="/assets/img/intern16.jpg" alt="Drawing" style="width: 450px; height: 400px; display: block; float:left; ">

&nbsp;&nbsp;&nbsp;&nbsp;When working with BART(Berea College Analytics and Reporing tool), I realized how much heavy work is done in the back-end of the application. For example, a user uploads  a huge Excel file that has thousands of row. BART has to parse all these data and write them in a database. I've never worked with a huge data before and it was very interesting to me see the time it takes BART to parse and store all the datasets in a database. For testing purposes, I used Excel file with more than 10k rows  and 61 columns and tested it on my Intel CORE i5 laptop that has 12Gb of RAM. As a result, it took 55 minutes to write all the datasets into a database. The front-end timed out and I realized I needed to turn this into a background process for best user experience. I realized that it was the first time I ran into such problem and I needed to do some research. I found a library called **Sidekiq**, a simple, efficient background processing for Ruby. By reading its documentation, I was able to use it in BART, however there are still couple things left for me to handle. This is a very exciting and challenging project for me and I feel like it's making me a better programmer.

&nbsp;&nbsp;&nbsp;&nbsp;Heavy background jobs for web applications is a very interesting design problem that software developers need to consider. I realized working with such applications drew my interest into the design side and scalability of web applications. Imagine all of a sudden BART becomes a very popular software and is used by thousands every day. That is when scalability comes in place. A service is said to be scalable if when we increase the resources in a systems, it results in increased performance in a manner proportional to resources added. After learning about scalability, I became very excited to make BART as scalable as possible. Actually, my capstone research paper is about scalability, and I'm using BART as an example. I feel like these are the topics that make me a better designer as a software developer and I'm learning things which I did not know before. I'm very satisfied with my internship because it taught me so many things that are super-useful when pursuing the career of a software developer.
&nbsp;&nbsp;&nbsp;&nbsp;
