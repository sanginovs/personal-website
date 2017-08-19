---
layout: post
title: "Internship Day 2: Facing Challenges "
author: "Sher Sanginov"
---

<img class="img-responsive" src="/assets/img/intern2.jpg" alt="Drawing" style="width: 450px; height: 400px; display: block; float:left; ">

So far, each team has to pick an issue(bug) that is available in one of the existing systems and fix it. One of the good things about this technique is you will learn on the go. It's a very challenging learning experience at the beginning but you get used to it. The web application systems we've been working on use different Python frameworks and tools so the best way to learn them is to tackle some bugs/issues.

Today, we tackled another bug which we found on the Berea College Syllabus Repository system. The issue was that when faculty had no courses, s/he would see an empty screen. Instead, when faculty had no courses, it should say      "You have no courses."  At first, the issue didn't sound very challenging. However, we discovered that the faculty courses were stored and retrieved from the SQLite database using Python Peewee library. What we needed to do was to check whether the course query had courses in it. This part was a bit challenging since query was returning a Peewee Object  so we could not check the length of the Object class in order to see whether there were courses in it. We did some research on database concepts and different terms like models, foreign and private keys. Moreover, we read Python Peewee library documentation and how it interacts with the database. Finally, we found the <b> exist() </b> method which checks whether query has some content in it. As the result, the issue was solved. It was a good learning experience. By tackling one issue, we were able to learn about database concepts, different libraries like Peewee and Jinja, a powerful templating engine in Python.

So, what else have I learnt today?
One of the interesting things I learnt about system design was that each system has a file called "**config**".They are used by developers to change settings without recompiling applications. For example, they can be used to declare global variables that are used throughout the system. A **config** file is very beneficial to the system. For example, while developing the system, one could set debugging option to **True**. However, if the system is live in the production, one sets the debug option to **False**.

So far, the internship has not been very challenging to me. I'm still learning the systems and their design. The first time I looked at them was so overwhelming because there were so many files in each system. Now, I feel more comfortable diving into system source code because I feel I'm more familiar with a system design and architecture.
