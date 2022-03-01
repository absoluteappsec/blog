---
layout: post
title:  "The Absolute AppSec Secure-Code Review Methodology"
author: "@absoluteappsec"
date:   2022-02-22 07:05:49 -0700
permalink: /Secure-Code-Review/
categories: Secure-Code-Review appsec Circle-K bug-hunting training
tags: Secure-Code-Review appsec Circle-K bug-hunting training
---
### The Secure-Code Review Methodology provides a framework for efficiently managing the time you have to review a codebase.

{:refdef: style="text-align: center;"}
<iframe src='https://www.youtube-nocookie.com/embed/lzRdkbjrnkc' frameborder='0' width='640' height='480' allowfullscreen></iframe>
{: refdef}

### _In a useful introduction to the Absolute AppSec Secure-Code Review methodology, Seth Law at DevSecCon attempted to TL;DR the two- preferably three-day Secure-Code Review course_

In the last couple years, Ken and Seth's Secure-Code Review course has generated enough interest that we regularly traveled to deliver it (before Covid) to groups on four continents as well as regularly to virtual audiences. The course design walks through the method we've developed for code review in real-world settings with exercises that familiarize students with the architecture of applications in a variety of languages.

![Methodology]({{ site.baseurl }}{{ '/assets/images/absolute-appsec-scr-method.png' }})
### _The Absolute AppSec Method for Secure-Code Review_

Organizing your approach to Secure-Code review involves recognizing typical application behaviors in general as well as the ability to research (read: targeted googling) language/application documentation as you dial down into specifics. To that end, information gathering is a vitally important part of Secure-Code Reviews because it informs how we divvy up the time allotted for a review and determines what we look at first. The idea is to develop a framework and direction to your review so you avoid either freezing up because you don't know where to start or, more seriously, following a wild hare down the rabbit hole.

## Avoiding Rabbit Holes

Rabbit holing is the most likely outcome for code-reviewers who get distracted by research avenues that they're interested in (see SQL injection or XSS dopamine hits) or by source files that look potentially interesting. It's a nemesis to the type of time management expected by enterprises or even the type needed to maximize the value of your work devoted to looking for bug-bounty payouts. Our methodology aims especially to avoid this particular pitfall.

No better example exists of implementing this methodology than the accelerated/caffeinated secure code-review that Ken Johnson does during the course. Check out a recorded example of this walkthrough to see how a codebase can be sifted through in a limited time.

{:refdef: style="text-align: center;"}
<iframe src='https://www.youtube-nocookie.com/embed/f6UOBCJ9pjw' frameborder='0' width='640' height='480' allowfullscreen></iframe>
{: refdef}

Ken's walkthrough illustrates how to organize a secure-code review by: information gathering for relatively unknown Django application; digging through source files to tease out promising testing avenues; and overall prioritizing routes for review by sketching out source-to-sink data flows: that is from user input to application handling and storage. 

In the course, we provide [template materials](https://github.com/zactly/handouts) that can organize students' ideas about what expected application behaviors and routes could be. But the template is intentionally the most rudimentary form of a skeleton. It gets fleshed out by the checklists you create during information gathering, which is further developed by the circle-k framework (because no matter where your code review goes, you end up back here).

![The Circle-K Framework]({{ site.baseurl }}{{ '/assets/images/billnted-circle-k-framework.png' }})
_"We're Back in San Dimas!"_

The initial list we build during information gathering, gets revisited and refreshed in the Circle-K framework. But now we can even better target routes and controllers that represent the biggest risks to the application. 

From our perspective the greatest outcome from these events comes on the second, or ideally, third day when we watch new initiates to the secure-code review method dig into their own selected codebase. Groups regularly find bugs that generate jira tickets or bug-bounty reports (and payouts) in just the short time we're together. It's genuinely amazing to see real-life examples of the method implemented to better protect the collective work that goes into developing an application as well as the data and privacy of its potential users. 








