---
title: 'Theory: why YouTube is slow on iPad'
author: Devin Reams
layout: post
permalink: /2010/theory-why-youtube-is-slow-on-ipad/
btc_comment_counts:
  - 'a:0:{}'
categories:
  - Gadgets
  - Internet
---
<img src="https://devin.reams.me/wp/wp-content/uploads/2010/09/ipad_hometimes.jpg" alt="" title="ipad_hometimes" width="580" height="408" class="aligncenter size-full wp-image-1523" />

The iPad appears to have had an issue from day one: videos from YouTube can sometimes take extremely long to buffer and play. As with any inconsistent behavior, you don&#8217;t notice this the 95% of the time when there is no problem. But that 5% will frustrate you to no end. Especially since other devices (laptops, smartphones) can load the same videos blazingly fast on the same network. Plus, other video providers including Vimeo, Hulu, and Netflix have no issue at the same time.

\## Current theories

There have been [plenty of discussions about this across message boards and blogs][1] since the early days of the iPad. I&#8217;ve tried everything and most seemingly sound like a wild-ass guess (WAG). Some of the highlights:

- **Your DNS settings are wrong:** the DNS lookup is taking too long and by switching to OpenDNS or Google&#8217;s (conspiracy theory alert) DNS everything fixes itself. This makes no sense during video buffer (DNS lookup is complete) and does not explain why other devices don&#8217;t have this issue.  
- **Other router configurations will fix it:** I&#8217;ve seen some obscure router settings thrown around about packet rates or loss or this or that. Again, the problem is not at the network level, it&#8217;s at the device (iPad).  
- **Low brightness setting:** somehow the wifi power corresponds to the brightness setting and the lowest level will prevent video loading. Interesting theory but I almost always keep my brightness at the lowest setting other internet applications have no issue: video (Hulu Plus, Netflix), web pages (Safari) and even Instapaper.  
- **Auto-join networks enabled:** I have no idea why this is discussed as I&#8217;m already on a wifi network and am never prompted. The network is fine as all other devices load YouTube and the iPad still gets blazing (10 MB/s) speeds.

In short, these theories miss the key points:

- the wireless network is always fully operational and experiences no other issues with any other providers  
- other devices on the same network are not experiencing the slowness specific to YouTube  
- the iPad is still downloading at very fast speeds, even for large video files  
- other applications are not experiencing any issues at the same exact time  
- the timing of the slow buffers is inconsistent (may happen once a week with in a one-hour window)

\## YouTube&#8217;s iPad experience

I&#8217;ve had plenty of experience with YouTube and other video hosting sites. Since YouTube was a launch partner with Apple&#8217;s iPad, it&#8217;s clear to me there is some behind-the-scenes stuff that is loading iPad-specific video types. Here&#8217;s a few points:

First, it appears to only be higher-quality videos (so that Apple&#8217;s YouTube app is always loading beautiful videos?) can be displayed on the iPad, you don&#8217;t even have the option of viewing a lesser quality version. Keeping in mind that at upload time, YouTube creates various formats and sizes from the small mobile-friendly videos to the 1080p high quality versions.

Second, it&#8217;s also clear that not all videos will load on the iPad. For instance, Cee Lo Green&#8217;s &#8220;F*ck You&#8221; will not load on the iPad. From the mobile website [this NSFW video][2] ([mobile link][3]) will not load even if you try to tap the big play button. To confirm this is not just a bad video, I&#8217;ve saved this video as a &#8216;favorite&#8217; and tried loading it from the YouTube app itself. At which point it returns the error: &#8220;The author of this video does not allow playback on iPad.&#8221; Curious&#8230;

\## My theory

The iPad is always trying to load a very high quality version of a video, but it&#8217;s not the same version as the desktop or other mobile versions. It&#8217;s clear that from both the mobile site and the YouTube app that there is a different video format being delivered to the iPad.

The very slow buffer and download speeds may be explained by:

- an iPad-specific video is being compressed, or converted on-the-fly which requires much more time on the YouTube server&#8217;s side of things (doubtful as the same video may load quick one day, slow the other)  
- a larger file size like 1080p being loaded where this is not the default on the desktop nor a mobile device. This could explain the perception of slower loads as more data is being delivered (this would only explain the slowness simply being magnified)  
- <span class="background-color:yellow">a different set of servers or content delivery providers are responsible for an iPad-specific version of the video</span>. This network is not part of the same resources as the remainder of of YouTube.

Why would YouTube keep the server resources for one device separate from the rest of the powerful mega data centers that power the other billions of videos being served? My thinking is that YouTube was required to maintain serious secrecy up to the iPad launch and quarantined any iPad-specific delivery, formats, servers, CDN resources, etc.

This has only seemingly been getting worse with time. I have had plenty of weeks where I&#8217;ll load funny [cheezburger][4] YouTube videos with no problem. I&#8217;ll even watch music videos, [CollegeHumor][5] videos, all on YouTube with no problem. But lately, the buffering has been getting worse. A 90 second video will take more than five minutes to load during &#8220;peak&#8221; hours (weekends, after dinner). My guess is there is many more iPad users coming online but nothing new happening on the YouTube infrastructure side.

I&#8217;m sure the plan is ultimately to move everything into the same data warehouses but this takes a few months of careful coordination. Especially since the iPad cannot load Flash, which means it cannot load ads, this is now a cross-departmental issue with far reaching intentions and consequences that was only just surfaced on the day the iPad was announced. Video publishers want to do things right for the iPad and, as we&#8217;ve seen, change takes a long time and the technical hurdles will remain on-hold. Note the huge ad beneath Cee Lo Green&#8217;s music video to buy his new album. You don&#8217;t see that on a stripped-down mobile version of YouTube.

 [1]: http://www.google.com/search?client=safari&#038;rls=en&#038;q=youtube+ipad+slow&#038;ie=UTF-8&#038;oe=UTF-8
 [2]: http://www.youtube.com/watch?v=pc0mxOXbWIU
 [3]: http://m.youtube.com/watch?gl=US&#038;client=mv-google&#038;hl=en&#038;v=pc0mxOXbWIU
 [4]: http://cheezburger.com/
 [5]: http://collegehumor.com/