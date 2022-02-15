---
layout: post
title:  "Static Analyzers in AppSec and Secure-Code Review"
author: "@absoluteappsec"
date:   2022-02-04 17:05:49 -0700
permalink: /Static-Analyzers-in-AppSec/
categories: appsec tools SAST Secure-Code-Review pumascan.io .NET Semgrep
tags: appsec tools SAST Secure-Code-Review pumascan.io .NET Semgrep
---
### How to make Static Analyzers a Useful Tool in Application Security and Secure-Code Reviews: pumascan.io demo

{:refdef: style="text-align: center;"}
<iframe src='https://www.youtube-nocookie.com/embed/7YDfMwbDgp8' frameborder='0' width='640' height='480' allowfullscreen></iframe>
{: refdef}

## <span style="color:light green"> **"Over the years, I've learned that having false positives is almost as bad as having false negatives. So, the tools I tend to focus on are those that give me actionable data." --_Seth Law_** </span>

A perennial topic covered in AppSec discussions, whether on the [livestream](www.youtube.com/c/AbsoluteAppSec) or in our [slack channel](https://join.slack.com/t/absoluteappsec/shared_invite/zt-5jay66o6-tOCIelav2VpJjcxRhTBEjA) involves the use of static analyzers in security reviews or, more generally, during the dev process. On slack recently, our Australian colleague Cole Cornford directed us to his thoughtful [blogpost](https://www.colecornford.com/2021-june1/) covering the topic. And the resulting discussion compelled us to revisit some of our own episodes.

The static analyzer tools that debuted a decade or so ago arrived with a fanfare promising a definitive solution to security issues, a kind of set-it-and-forget-it panacea. In truth, while tools can provide benefits to security and dev teams alike, there can be problems that arise during implementation. One of our guests [Eric Heitzman](https://youtu.be/XJIxFYT21sw?t=57m06s), relayed sobering accounts of incorrectly set-up static analyzer tools whose false positives drove wedges between security and dev teams. In turn, this led the security team to mistrust the vendors who had first recommended the SAST solution.

The desire to limit false positives has been a common problem for Application Security professionals who want to get the best results from the tools they use. This is why Seth in the above clip recommends tools like [Puma Scan](pumascan.com) which is tailored for .NET applications, a narrow focus that helps make its findings more likely to provide actionable data.

For anyone who wants more of a background on the development of Puma Scan as a .NET static analyzing tool, you can watch this Absolute AppSec interview ([episode 32](https://youtu.be/Ttw6539Woto?t=32m28s)) with Eric Johnson. The initial inspiration for Puma Scan originated with Johnson's incidental introduction to Roslyn APIs around 2016. Seeing the syntax tools at work, he recognized their potential for developing .NET security scans with targeted rules.

### Semgrep with the ellipsis operator and the metavariable.

Another useful static analysis tool for Application Security is [Semgrep](semgrep.dev). Clint Gibler of [tl;drsec](https://tldrsec.com/) fame, visited Absolute AppSec in November 2020 (episode 115) to provide an introduction to semgrep. Along the way, Clint showed Ken and Seth how to write rules using two abstractions in order to find potentially insecure patterns in your code: first, _[ellipsis operators](https://youtu.be/yjsE_DSnK5w?t=27m15s)_ which allow a Semgrep user to find all the calls to a particular function; and second, _[metavariables](https://youtu.be/yjsE_DSnK5w?t=30m04s)_ which allow a user to search for variables where the exact variable name is unknown. Based on a vague knowledge of where variables could be implemented in insecure function calls, metavariables in concert with ellipsis operators can help Semgrep users narrow in on potential code vulnerabilities. To see how this works in some code examples as well as a good overview of Semgrep overall, check out Clint's whole episode here:

{:refder: style="text-align: center;"}
<iframe width="560" height="315" src="https://www.youtube.com/embed/yjsE_DSnK5w" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
{: refdef}

### Even more Absolute AppSec discussions about Static Analyzers!
Because static analyzers have been a perennial topic, we'd also like to point you to other episodes with more information for anyone interested.
* Justin Collins and Neal Mattatal, developers of Ruby on Rails SAST [brakeman](https://brakemanscanner.org), have both been on the show to discuss AppSec generally, but the most in depth discussion of brakeman can be found in our [12th episode](https://youtu.be/few9AN1zwPE) which we recorded with Justin at LocoMocoSec. (You can find Neal's episodes here, [8](https://youtu.be/uQ8jSL44ITY) and, more recently [159](https://youtu.be/ugXNt994TOM))
* Marc Feferman, in [episode 112](https://youtu.be/tMRH5M0rKYQ) provides some great insight into how Static Analysis tools should fit within an organization and the need to correctly implement tools in the beginning and to buttress the tools with security professionals who can truly understand the results that the tools are producing.
* Guy Podjarny from [Snyk](snyk.io) provided insight into why enterprises are likely to shift in how they position security tooling, making it as easy as possible for developers to integrate tools into their pipelines in [episode 76](https://www.youtube.com/watch?v=IxpD5GbHMWY).
