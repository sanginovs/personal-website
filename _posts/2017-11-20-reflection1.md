---
layout: post
title: "Open Source|CSC426|Firefox Debugger: First Pull Request "
author: "Sher Sanginov"
---

&nbsp;&nbsp;&nbsp;&nbsp;These past two weeks has been very productive. My team and I successfully finished working on the issue that we picked which is an accessibility issue. We've been following divide and conquer strategy. We created a checklist of tasks that needs to be done. Then, we split tasks among us. My task was to use **aria-activedescendant** to identify search results with a focus so the screen reader reads each search result when a user navigates through them. After adding various accessibility attributes, I was able to test it using Orca screen-reader. However, Orca screen-reader didn't read the search box results after one navigates through them. At first, I thought there was a problem with my code. Later on I realized, Orca screen reader was not working properly on my Ubuntu OS. Then, I went ahead and downloaded Chrome Vox screen-reader extension and tested my code. It worked.

&nbsp;&nbsp;&nbsp;&nbsp;It was time for us to do our first pull request. We had to squash all of our git commits so everything looks nice and smooth. When creating a pull request, we had to write a summary of changes we made and test plan for a person who will be reviewing our code. After completing all these steps, we were able to create our first pull request in the Firefox Debugger Open source project. YAY!!! Check it out through this <a href="https://github.com/devtools-html/debugger.html/pull/4760">link</a>.

&nbsp;&nbsp;&nbsp;&nbsp;My plan for the next two weeks is to take a closer look at other issues and see if we can pick another issue to work on. Also, we will also have to wait for our pull request to get merged or denied and get some feedback on it. Two weeks ago, my goal was to do an independent study on technologies used to build the Debugger and I did some self-study outside of class. I am very excited to be part of this community because Mozilla open source community is super-friendly and responsive.
