---
layout: post
title: "Internship: Day 2"
author: "Sher Sanginov"
---


<img class="img-responsive" src="/assets/img/intern2.jpg" alt="Drawing" style="width: 450px; height: 400px; display: block; float:right; ">

So far, each team has to pick an issue(bug) that is available in one of the existing systems and fix it. One of the good things about this technique is you will learn on the go. It's a very challenging learning experience at the beginning but you get used to it. The web application systems we've been working on use different Python frameworks and tools so the best way to learn them is to tackle some bugs/issues.

Today, we tackled another bug which we found on the Berea College Syllabus Repository system. The issue was that when faculty had no courses, s/he would see an empty screen. Instead, when faculty had no courses, it should say      "You have no courses."  At first, the issue didn't sound very challenging. However, we discovered that the faculty courses were stored and retrieved from the SQLite database using Python Peewee library. What we needed to do was to check whether the course query had courses in it. This part was a bit challenging since query was returning a Peewee Object  so we could not check the length of the Object class in order to see whether there were courses in it. We did some research on database concepts and different terms like models, foreign and private keys. Moreover, we read Python Peewee library documentation and how it interacts with the database. Finally, we found the <b> exist() </b> method which checks whether query has some content in it. Once we fixed the back-end part of the code, we switched to the front-end and added this code:
```
#Front-end
{% raw %}
{% for course in courses %}
    {% include "snips/coursesRows.html" %}
  {% endfor %}
  {% include "snips/tableFooter.html" %}
  {% include "snips/tableFooter.html" %}
{% else %}
  <h2>You have no courses.</h2>
  {{endif}}

```
```
#Back-end
if my_courses.exists(): #checking whether query contains courses
  peeweeObj = my_courses.execute()
  return peeweeObj
else:
    return None
```
As the result, the issue was solved. It was a good learning experience. By tackling one issue, we were able to learn about database concepts, different libraries like Peewee and Jinja, a powerful template engine in Python. So far, the internship has not been very challenging to me. I'm still learning the systems and their design. The first time I looked at them was so overwhelming because there were so many files in each system. Now, I feel more comfortable diving into system source code because I feel I'm more familiar with a system design and architecture.
