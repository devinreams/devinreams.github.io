---
title: The power of Time Machine, Dropbox, and Subversion
author: Devin Reams
layout: post
permalink: /2011/the-power-of-time-machine-dropbox-and-subversion/
categories:
  - Gadgets
  - Internet
  - Lifehack
---
I&#8217;ve been testing a certain unreleased \[operating system\](http://www.apple.com/macosx/lion/) for the past month or two and I&#8217;ve been largely pleased. That was until I ran into a nasty little bug (which has been documented to happen on Snow Leopard, too). It goes like this:

* Type on your keyboard  
* Observe as a Kernal panic wipe your screen  
* Reboot

A nasty little bugger, no doubt. But here&#8217;s the rub: you no longer have any login accounts.

Let me say that again because it&#8217;s important: once you reboot, you are prompted to log in to \*nothing\*. Not a single user account is available to select. You can type in any combination of username and password, but don&#8217;t bother, they won&#8217;t work.

The neat thing is, I could usually just grab my OS reinstall disk and do some sort of reset trick to tell the OS to create a new administrator account. But the neat part of being on the bleeding edge is&#8230; this one happens to crash when you try that.

\### &#8220;No problem&#8221; says Time Machine

I plug my computer into two \[Time Machine\](http://www.apple.com/macosx/what-is-macosx/time-machine.html) drives almost every day. One at work and one at home.

With a quick reboot and &#8220;Restore from Time Machine&#8221;, within three hours my entire computer had been brought back to the exact state it was in on a Friday morning and I was back in business (e.g.: I could log in again).

\### &#8220;I&#8217;ve already got this&#8221; says Dropbox

Once I log in, \[Dropbox\](http://db.tt/SwXMrCf)[^1] is already busily computing how many files I have on my machine and which ones are different than what they have on their servers. It was a lot, but within an hour everything had been re-downloaded and my documents, music, and photos were all back to exactly the way there were moments before the dreaded key combination occurred.

\### &#8220;Just a few more things&#8221; says Subversion

Luckily it was a Saturday evening and I wasn&#8217;t working on anything of much importance (remember kids, commit early, commit often). So, with a quick &#8220;\[svn up\](http://svnbook.red-bean.com/en/1.1/re28.html)&#8221; on my work file directories I had all the code and documents back on my drive from Friday. I&#8217;m sure a few local changes I made are missing, but nothing of much significance. I&#8217;m a manager, not a maker.

&#8212;

And with those three simple tools: local incremental backups, storage in the cloud, and a version control system I went from utter catastrophe to right-as-rain in an afternoon. If I had my Super Duper drive it would&#8217;ve been even faster.

Bad things don&#8217;t have to happen to data. This stuff really is that easy&#8230;

\[^1]: Sign up for Dropbox with [this link\](http://db.tt/SwXMrCf) and we will \*both\* get some extra megabytes!