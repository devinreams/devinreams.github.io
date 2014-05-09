---
title: Create your own URL shortener, use it with Tweetie 2
author: Devin Reams
layout: post
permalink: /2009/add-custom-url-shortening-to-tweetie/
aktt_notify_twitter:
  - no
btc_comment_counts:
  - 'a:0:{}'
categories:
  - Internet
---
## I hate URL shorteners, but that&#8217;s not the point

<span style="font-size: small;">I really hate short URLs; on both the giving and receiving end, either way I feel like I&#8217;m handing or being handed a package of confusion and uncertainty. But, unfortunately, they&#8217;re useful if you:</span>

*   <span style="font-size: small;">Are trying to send a link to someone and have limited space (Twitter)</span>
*   <span style="font-size: small;">Want to provide a URL that is long with lots of unique variables in it (Google Maps)</span>
*   <span style="font-size: small;">Need a URL you can easily tell people or have them write-down (during a presentation)</span>

<span style="font-size: small;">The confusion comes in if nobody takes the time to tell you what they&#8217;re handing you. Take Twitter for example, people who post a link usually give little context (&#8220;this is so cool: link&#8221; or &#8220;wow, I wish I had this: link&#8221;). Screw you guys! At least give me a hint as to what you&#8217;re handing me (other than yet another bit.ly or tinyurl link). Luckily, there are some mitigating factors:</span>

*   **<span style="font-size: small;">Custom contextual short URLs:</span>**<span style="font-size: small;"> Flickr&#8217;s awesome flic.kr domain is a great start. If WordPress turned wp.me into the same for user&#8217;s posts, awesome. Even Posterous autolinks with their own post.ly. I know what kind of content is behind this domain.</span>
*   **<span style="font-size: small;">URL expanders:</span>**<span style="font-size: small;"> </span>[<span style="font-size: small;">Tweetie for Mac</span>][1]<span style="font-size: small;"> has a expander service built in for known shortener endpoints (click the bit.ly link and a popup tells you what the actual URL is). </span>[<span style="font-size: small;">LongURL</span>][2]<span style="font-size: small;"> can be used to determine where a URL will </span>*<span style="font-size: small;">really</span>*<span style="font-size: small;"> take you.</span>
*   **<span style="font-size: small;">Smarter friends:</span>**<span style="font-size: small;"> don&#8217;t follow people or ask them to stop giving you contextless links (not likely)</span>

<span style="font-size: small;">So, with all that said, I want to roll my own URL shortener to tell people: trust me, I took the time to create my own service and hand-pick this URL for you to look at. Since I wrote about this, I&#8217;ll be sure to go the extra mile and make sure I give context when a shortened URL is necessary.</span>

## How to create your own URL shortener using Lessn

<span style="font-size: small;">Shaun Inman has created a handy script and guide to create your own shortener: <a href="http://shauninman.com/archive/2009/08/17/less_n">Lessn</a></span>

<span style="font-size: small;">The installation steps are simple if you know your way around a web server:</span>

1.  <span style="font-size: small;"><strong>Pick a short domain or sub-directory:</strong> you need to first figure out what domain you want to use (I chose devinr.com), you have to own it so you may use an existing domain and stick the shortener at a sub-directory (devinr.com/x/)</span>
2.  <span style="font-size: small;"><strong>Install the Lessn package:</strong> follow the README, but basically you just drag and drop the files using a FTP client (make sure you include the top-level .htaccess file, which is hidden by default in Finder on Mac OS X), setup the config file, and you&#8217;re done.</span>

<div>
  <span style="font-size: small;">So now I immediately have my own bookmarklet, shortener endpoint (via API), etc. Now I can take it with me to <a href="http://www.atebits.com/tweetie-iphone/">Tweetie 2 for iPhone</a>.</span>
</div>

## Setup Tweetie 2 for iPhone to use a custom URL shortener

<div>
  <span style="font-size: small;"><a href="http://twitter.com/atebits">Loren Brichter</a> has done an great thing for his latest Twitter client (<a href="http://itunes.apple.com/WebObjects/MZStore.woa/wa/viewSoftware?id=333903271&mt=8">iTunes link</a>): he allows you to have a <a href="http://developer.atebits.com/tweetie-iphone/custom-shortening/">custom URL shortener</a> endpoint defined for use. In other words, every URL you post can be shortened using whatever service you want (including your own).</span>
</div>

<div>
  <ol>
    <li>
      <span style="font-size: small;">Go buy and install the latest <a href="http://www.atebits.com/tweetie-iphone/">Tweetie 2 for iPhone</a></span>
    </li>
    <li>
      <span style="font-size: small;">Browse to the settings page (bottom of the accounts screen)</span>
    </li>
    <li>
      <span style="font-size: small;">Select URL shortener > Custom&#8230;</span>
    </li>
    <li>
      <span style="font-size: small;">Insert your endpoint using your API (so that Lessn returns plaintext to Tweetie): http://example.com/-/?url=%@&api=<em>[Lessn API here]</em></span>
    </li>
  </ol>
  
  <div>
    <span style="font-size: small;">It&#8217;s as simple as that. Now all your URLs in Tweetie can be auto-shortened using your own service. Neat.</span>
  </div>
</div>

 [1]: http://www.atebits.com/tweetie-mac/
 [2]: http://longurl.org/