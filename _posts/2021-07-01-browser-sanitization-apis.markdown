---
layout: post
title:  "A Client-Side Solve: Browser Sanitization APIs"
author: "@absoluteappsec"
date:   2021-07-01 14:46:49 -0700
categories: browser client appsec apis
tags: browser client appsec apis
---
### Why Browser Sanitization APIs could usher in a new era of client-side security?

{:refdef: style="text-align: center;"}
<iframe src='https://www.youtube-nocookie.com/embed/bUtaE6D2jf0' frameborder='0' width='640' height='480' allowfullscreen></iframe>
{: refdef}

In April 2021, Google and Firefox both announced that a [sanitization API](https://portswigger.net/daily-swig/google-and-mozilla-unveil-plans-to-bake-html-sanitization-into-their-browsers) would be integrated within their browsers. Ken Johnson (cktricky) and Seth Law (sethlaw) discussed these new developments on the Absolute AppSec podcast with a good deal more sanguinity than regular podcast listeners may be accustomed to.

According to the two hosts, the browser update could go along way toward addressing client-side vulnerabilities, especially certain cross-site scripting weaknesses. Sanitized languages can drastically reduce attack surfaces, helping prevent potential attacks. And Mozilla and Google’s partnership with Cure53 represents a natural alliance in developing a browser-side response to many Cross-Site Scripting attacks. Developers have already used Cure53’s [DOMPurify](https://github.com/cure53/DOMPurify) libraries to positive affect in reducing attack surfaces.

![XSS]({{ site.baseurl }}{{ '/assets/images/xss.svg' }})

In Seth Law’s view, the sanitization API is analogous to earlier library-adoption methods to reduce the threat of SQL Injection attacks.

> SQL Injection was a problem for years until the underlying way we passed data to databases changed….The number of exploits we saw dropped drastically because of the way we changed the underlying technology and the way developers interacted with it.

A Browser Sanitization makes sense as a technology solution that could standardize how developers address html content that accepts client-side data. Seeing how the Browser Sanitization API works going forward could reduce the onus on developers in solving the problem of XSS attacks by researching and implementing the correct bespoke library for their own organization’s purposes.

To see more of Ken and Seth’s discussion of Browser Sanitization API’s, among other topics, checkout the youtube broadcast [here](https://www.youtube.com/watch?v=zsN2FNoUZIc&amp). Subscribe to our youtube [channel](https://www.youtube.com/channel/UCo9CDrIB0rJwG4GGz8CZEaQ) to be made aware of new content. Absolute AppSec covers Application Security content in weekly YouTube livestreams buttressed with lively discussion in our [Slack Channel](absoluteappsec.slack.com).

#### Footnotes

* To read a more academic discussion of Cure53’s work, see Mario Heiderich, Christopher Späth, and Jörg Schwenk’s research paper [“DOMPurify: Client-Side Protection Against XSS and Markup Injection,” in <em>European Symposium on Research in Computer Security</em> 2017: 116-134](https://link.springer.com/chapter/10.1007/978-3-319-66399-9_7).
* Researchers can also look at Cure53’s all-encompassing [Browser Security White Paper](https://github.com/cure53/browser-sec-whitepaper/blob/master/browser-security-whitepaper.pdf).

[back](/)
