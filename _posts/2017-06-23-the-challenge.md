---
layout: post
title: "Internship Day 3: Productivity Part 3"
author: "Sher Sanginov"
---


<img class="img-responsive" src="/assets/img/intern3.jpg" alt="Drawing" style="width: 450px; height: 400px; display: block; float:left; ">

One of the issues I face very often is a **path issue**. So, what is a **PATH** in computer systems at the first place? Path is an environment variable on Operating systems like Windows and Linux which specify a set of directories where executable programs are located. So, in general, each file that is stored in some folder on your PC, has its own path which you could use to get to it. For example, a new file which you create on Documents folder in Windows could have this path: **C:/Users/administrator/Documents/new_file**.

The issue I tackled today had something to do with an absolute and relative paths. At first, I wasn't sure what those terms meant. After doing some research, I was able to understand those terms. The absolute path is a full path that points to the same location in a file system while relative path starts from some working directory that way avoiding to provide the full path. In our BCSR system, when faculty members upload their syllabus, the system needs to take a pre-defined relative path for user uploads which is **static/uploads** and create an absolute path in order to store the syllabus in that location.

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
