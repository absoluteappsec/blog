---
layout: post
title:  "Three takeaways from an episode with James Kettle"
author: "@absoluteappsec"
date:   2021-09-21 14:46:49 -0700
permalink: /James-Kettle-Portswigger/
categories: appsec research http desync portswigger
tags: appsec research http desync portswigger
---
## How Portswigger Research's James Kettle approaches Application Security Research

<video width="80%" preload="auto" muted controls>
    <source src="{{ site.baseurl }}{{ '/assets/videos/Kettle-promo2.mp4' }}" type="video/mp4"/>
</video>

Absolute AppSec's [147th episode](https://www.youtube.com/watch?v=b5IVhnboDIY) featured a can't-miss discussion with James Kettle ([@albinowax](https://twitter.com/albinowax) on Twitter), a world-class exploit researcher from [Portswigger](https://portswigger.com). As the episodes overly dramatic promo highlights, Ken and Seth discovered some interesting details regarding Kettle's path into security research. But the fun didn't end there – Kettle provided some valuable insights that could help appsec professionals and bug bounty researchers in furthering their own goals going forward.

### Episode takeaways

#### 1. Good research serves as a clue that there is more good research from that same source

In the course of the episode, Kettle credited researchers such as (a) orangetsai [(research blog here)](https://blog.orange.tw), (b) regilero [(research page here)](https://regilero.github.io)
, and (c) Amit Klein [(research here)](http://www.securitygalore.com/site3/) as influential touchpoints for Kettle. Kettle's personal generosity with acknowledgment and respect is also a nice reminder that the security community can be downright collegial: there's no reason not to be a mensch.

#### 2. Dig into something you don't understand

This works as a way to address many researchers' desire to play with something new, not just re-creating XSS all day. Kettle's first introduction to post-smuggling was listening to regilero's presentation at defcon 24 "Hiding Wookies in HTTP – HTTP smuggling is a thing we should know better and care about,"; [(infocondb.org)](https://infocondb.org/con/def-con/def-con-24/hiding-wookiees-in-http-http-smuggling-is-a-thing-we-should-know-better-and-care-about) and Kettle's first impulse was to tell himself he probably didn't need to understand HTTP smuggling on any deeper level. However, if you fast forward three years, one can see how much work Kettle did to illuminate HTTP smuggling attacks. For example, read his deep dive and watch his discussion of the technique from defcon 27 – ["HTTP Desync Attacks: Request Smuggling Reborn"](https://portswigger.net/research/http-desync-attacks-request-smuggling-reborn)

Relatedly, Kettle recommends digging into not just exploit vectors, but single applications as well. This is especially true for people looking to increase income in bug bounty research. Truly understanding an application provides greater opportunities for finding the types of vulnerabilities that pay out handsomely.

#### 3. Document, Document

There are two main points to highlight related to good note-keeping and documentation. First is that a good finding is the key to bug bounty payouts. Show the application owners as articulately and precisely as you can how to re-create your exploit, and your chance of big payouts directly increases. The more long-term benefits for documenting ideas are highlighted by the research trajectory of <em>ALL</em> Kettle's ideas. As Kettle relates, he keeps a list of things that might work, will ruminate on how he can create quick tests to check those ideas regardless of whether he considers the idea "smart"; or "dumb"; when it first germinates.

Generally speaking, while these were some takeaways we wanted to highlight, the interview provides a lot of insights into the life of a security professional with a well-deserved stellar reputation. Definitely watch [the whole episode](https://youtube.com/watch?v=b5IVhnboDIY), already one of Absolute AppSec's most popular, and let us know (by [email](mailto:info@absoluteappsec.com) or in our [slack channel](https://join.slack.com/t/absoluteappsec/shared_invite/zt-5jay66o6-tOCIelav2VpJjcxRhTBEjA)) if you have any other particular guests you'd like to see on upcoming episodes of the show.
