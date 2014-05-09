---
title: Simple tweaks to your iPhone-friendly website
author: Devin Reams
layout: post
permalink: /2010/simple-tweaks-to-your-iphone-friendly-website/
categories:
  - Internet
tags:
  - design
  - interface
  - iphone
  - mobile
  - web
---
If you own and operate a website, odds are you have mobile users browsing it. Be sure you take care of these people as their numbers are ever-growing.

## Get me out of here!

*Hopefully* you already have a mobile-friendly version of your site (for WordPress users, I recommend the [Carrington Mobile theme][1]). Bonus points if you have a mobile-friendly version but users can exit out of that version. Though the simpler, faster interfaces are often appreciated, users get frustrated if they&#8217;re trapped in a &#8216;dumbed down&#8217; version of the site (especially if they have a &#8216;smart&#8217; browser like MobileSafari on the iPhone).

<center>
  <dl id="attachment_934" class="wp-caption aligncenter" style="max-width:300px">
    <dt>
      <a href="http://devin.reams.me/wp/wp-content/uploads/2010/01/espn-mobile-exited.png"><img src="http://devin.reams.me/wp/wp-content/uploads/2010/01/espn-mobile-exited-300x208.png" alt="ESPN Mobile vs Standard" title="ESPN Mobile and Standard on Mobile Safari" width="300" height="208" class="size-medium wp-image-934" /></a>
    </dt>
    
    <dd>
      click to enlarge
    </dd>
  </dl>
</center>

For example, on my iPhone, I open <http://espn.com> which smartly detects my [browser&#8217;s user-agent][2] and serves me a nice, big iPhone-friendly version of their website. But, while out to lunch, I may want to show a client the layout, design, and colors of the espn.com website. No problem, I can scroll to the footer of the mobile page and click the &#8216;ESPN.com&#8217; link. Suddenly I&#8217;m out of the mobile site and presented with the &#8220;real&#8221; espn.com for demonstration purposes. Sadly, many sites don&#8217;t allow this. Don&#8217;t let your visitors become trapped in user-agent hell.

## Give me an Web Clip icon, not a thumbnail

Hopefully your site already has a [favicon][3], that nice square icon that usually appears in your browsers address bar next to the URL, or in the tab next to the page title. Favicons are an important detail that everyone appreciates. With ten tabs open, a user can quickly locate Gmail and switch to it immediately.

So why do most web developers overlook the iPhone&#8217;s Web Clip icon? It&#8217;s a simple 57&#215;57 PNG file used when a visitor bookmarks your website and adds it to their homescreen. Your website can looks a million times more professional if you define your icon. I can&#8217;t think of a single site that looks good as a 57-pixel thumbnail screenshot. Compare the icons for the [Colorado Department of Transportation&#8217;s mobile site][4] and [Colorado Snow][5] (my website) to that of [Colorado Ski Country USA][6] and [GO I-70][7]:

<center>
  <dl id="attachment_939" class="wp-caption aligncenter" style="max-width:320px">
    <dt>
      <a href="http://devin.reams.me/wp/wp-content/uploads/2010/01/compare-web-icons.png"><img src="http://devin.reams.me/wp/wp-content/uploads/2010/01/compare-web-icons.png" alt="Web Application icons vs. thumbnails" title="Web Application icons vs. thumbnails" width="320" height="480" class="size-full wp-image-939" /></a>
    </dt>
    
    <dd>
      Web Application icons vs. thumbnails
    </dd>
  </dl>
</center>

The [Apple iPhone SDK (Web Applications)][8] can&#8217;t make it any more simpler for you, either:

> To specify an icon for the entire website (every page on the website), place an icon file in PNG format in the root document folder called apple-touch-icon.png or apple-touch-icon-precomposed.png. If you use apple-touch-icon-precomposed.png as the filename, Safari on iPhone OS won’t add any effects to the icon.

Kudos for having the mobile site, but please, create the icon.

## Save some space, go fullscreen

One of the less-used features available to iPhone Web Application&#8217;s is the &#8220;fullscreen&#8221; mode where the viewport is the only item on the screen. The URL text field and button bar are completely removed. Compare CoTrip to Colorado Snow:

<center>
  <dl id="attachment_941" class="wp-caption aligncenter" style="max-width:300px">
    <dt>
      <a href="http://devin.reams.me/wp/wp-content/uploads/2010/01/iphone-fullscreen.png"><img src="http://devin.reams.me/wp/wp-content/uploads/2010/01/iphone-fullscreen-300x208.png" alt="Compare fullscreen vs. standard" title="Compare fullscreen vs. standard" width="300" height="208" class="size-medium wp-image-941" /></a>
    </dt>
    
    <dd>
      Compare fullscreen vs. standard
    </dd>
  </dl>
</center>

Much less space is wasted on browser &#8220;chrome&#8221; and more is dedicated to the viewport meaning less scrolling and more immediate information can be consumed by the visitor. And again, the implementation is very simple:

> Set the apple-mobile-web-app-capable meta tag to yes to turn on this feature.</blockquote
> 
> Admittedly, these two sites are bad examples. This feature is not suitable for all websites as any subsequent click requires a re-load of the site into Mobile Safari. So, if you intend to have users browsing around the site, this isn't the best. But, if your site is a simple weather application, or a board game of checkers written in JavaScript, users likely don't need a back and forth button, and they don't need to edit the URL. So give users their space.
> 
> ## In conclusion&#8230;
> 
> There are a number of subtle tweaks that can help optimize your website for mobile users. Again, the number of smart phones and web-enabled devices are only going to increase. Getting in the habit of implementing some of these considerations will only help your reputation. And remember, these are just three suggestions I quickly came up with for the iPhone. Think of the variations: Palm, Android, Blackberry, and so on&#8230;

 [1]: http://carringtontheme.com/themes/
 [2]: http://en.wikipedia.org/wiki/User_agent
 [3]: http://en.wikipedia.org/wiki/Favicon
 [4]: http://m.cotrip.org/
 [5]: http://cosnow.com/
 [6]: http://m.coloradoski.com/
 [7]: http://goi70.com/mobile
 [8]: http://developer.apple.com/iphone/library/documentation/AppleApplications/Reference/SafariWebContent/ConfiguringWebApplications/ConfiguringWebApplications.html#//apple_ref/doc/uid/TP40002051-CH3-SW3