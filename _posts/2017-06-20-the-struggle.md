---
layout: post
title: "Internship Week 2: Productivity - Part 1"
author: "Sher Sanginov"
---


<img class="img-responsive" src="/assets/img/intern5.png" alt="Drawing" style="width: 450px; height: 400px; display: block; float:left; ">

&nbsp;&nbsp;&nbsp;The second week of my internship started and I feel confident after being in a struggle mode throughout my first week interning. One thing I learnt from last week is to ask your peers for things that don't make sense to you when it comes to fixing bugs. I feel like I heavily rely on websites like **"Stackoverflow"**(technical question & answer website) when I'm having technical problems with something. Sometimes, it does make sense to ask other interns for help when facing a problem which I rarely did in my first week. This was one of my weaknesses. I realized that I should be asking other interns for help when I get stuck on something.  

&nbsp;&nbsp;&nbsp;This week we are focusing on learning different architectural design patterns like Model-View-Controller. Being able to design a web application system is not an easy task and requires some planning especially when your application becomes popular all of a sudden.  

In order to solve this issue, I had to learn about **sys module** to predefine the path from the root directory. E.g. **sys.path.insert(0,‘/home/users/sher/Documents/bcsr/’)**. Of course, this depends on the environment you are running the system in. Then, I needed to create a function that takes **a relative path** as an input and returns **an absolute path**. Here's the function:
```
#Back-end
def getAbsolutePath(self, relativePath, filename=None, makeDirs=False):
   '''Creates the AbsolutePath based off of the relative path.
   Also creates the directories in path if they are not found.
   @param {string} relaitivePath - a string of directories found in config.yaml
   @param {string} filename - the name of the file that should be in that directory
   @return {string} filepath -returns the absolute path of the directory'''
   '''TODO: ADD @PARAm for make dirs'''
   filepath = os.path.join(sys.path[0], relativePath) #adding relative path and absolute
   if makeDirs == True:
       try:
           os.makedirs(filepath)
       except:
           pass
   if filename != None:
       filepath = os.path.join(filepath, filename)
   return filepath
```
Finally, the problem was solved.

What did I learn by working in this issue?
<br>First of all, I learn about **PATH** and **file hierarchy** in OS systems like Linux. Secondly, I was able to learn about **"sys"** and **"os"** modules and use them in my implementation.

Was it challenging to me?<br>
Not really. Even though I got stuck a bit, I was able to figure my way out by doing some extra research.

How do I value my effort for the first three day of the internship?<br>
I am working hard and learning a lot of new things. While in the process of getting familiar with our systems, I'm also working on building my own web application using the same design in order to get a better grasp of the whole system design and implementation.
