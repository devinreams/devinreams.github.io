---
title: Add Twitter Favorites to your site
author: Devin Reams
layout: post
permalink: /2009/add-twitter-favorites-to-your-site/
aktt_notify_twitter:
  - yes
openid_comments:
  - 's:21:"a:1:{i:0;s:4:"1828";}";'
btc_comment_counts:
  - 'a:0:{}'
categories:
  - Social Media
  - WordPress
tags:
  - best practices
  - rss
  - simplepie
  - Social Media
  - twitter
  - WordPress
---
*Hint: if you&#8217;ve never used [Twitter][1] the following won&#8217;t make much sense to you.*

I easily annoyed by people on Twitter who &#8216;RT&#8217;, or &#8216;re-tweet&#8217;; they simply post an update that says exactly what someone else says, plus attribution. Frankly, answering the Twitter mantra &#8220;What are you doing?&#8221; with &#8220;this is what someone else smarter, funnier, or more charming is doing&#8221; seems inane. It&#8217;s poetic, though, in the sense that it&#8217;s a quick litmus test for people worth &#8220;following.&#8221; [Alex][2] has always been against this practice and suggested [an alternative to RTs:][3] favorites.

[<img src="http://devin.reams.me/wp/wp-content/uploads/2009/04/twitter-history-2.png" alt="Screenshot: History doesn&#039;t retweet itself" title="Screenshot: History doesn&#039;t retweet itself" width="490" height="119" class="aligncenter size-full wp-image-709" />][4]

There are very few features on Twitter: updates, direct messages, replies, *favorites*, followers, followings. I charge everyone to use the favorites feature more often. In fact, there&#8217;s a site dedicated to finding the real good ones: [favrd][5].

Point being: I&#8217;m a huge proponent of using the little star. I&#8217;ve started publicizing my favorites here in the sidebar of [Mind/Averse][6] and it took less than 30 seconds using WordPress. It&#8217;s really quite simple.

## Add Twitter favorites with the WordPress RSS widget

<img src="http://devin.reams.me/wp/wp-content/uploads/2009/04/rss-widget.png" alt="Screenshot: WordPress RSS widget" title="Screenshot: WordPress RSS widget" width="441" height="328" class="aligncenter size-full wp-image-706" />

Assuming you have a widget-friendly WordPress theme installed, simply do the following:

1.  From the WordPress dashbord, Browse to Appearance > Widgets
2.  Select the &#8216;Add&#8217; button next to the &#8220;RSS&#8221; widget
3.  Visit your [Twitter favorites][7] page and determine your personal RSS feed (view the page source if you&#8217;re stuck here; find the <link> tag with http://twitter.com/favorites/*youridhere*.rss)
4.  Insert the favorites feed into your RSS widget, give the widget a title, pick your options, etc.
5.  Save the widget and save the changes to your sidebar

Now everyone who visits your site can immediately find the tweets you find useful. You&#8217;ll get to be cooler, smarter, and funnier simply by association.

## Other ways to integrate Twitter favorites

I can think of various creative ways for individuals and businesses to use Twitter favorites.

For example, if I were a company with customers sending @replies to me telling me how great I was, I may favorite those. I can then use something like [SimplePie][8] to integrate my favorites into my blog as a separate page of testimonials. I know 37signals uses &#8216;buzz&#8217; from Twitter on their site.

[<img src="http://devin.reams.me/wp/wp-content/uploads/2009/04/37signals-twitter.png" alt="Screenshot: 37signals buzz around the web" title="Screenshot: 37signals buzz around the web" width="411" height="304" class="aligncenter size-full wp-image-707" />][9]

## Bonus: do the same with @replies

The @replies RSS feed is a bit different and uses the Twitter API and 401 authentication, not a custom RSS feed, for your replies. No worries, you can either pull the RSS feed from [Twitter Search][10] or you can do the same thing using the following syntax:

> http://twittername:twitterpassword@twitter.com/statuses/replies.rss

In theory, the API will include all mentions (any time @devinreams is included in an update, not just at the beginning of an update).

Ha, this is why they call me a [social media pro][11].

 [1]: http://twitter.com/devinreams
 [2]: http://alexking.org/
 [3]: http://alexking.org/blog/2009/01/29/an-alternative-to-rts-on-twitter
 [4]: http://twitter.com/devinreams/status/1461301788
 [5]: http://favrd.textism.com/
 [6]: http://mindaverse.com/
 [7]: http://twitter.com/favorites
 [8]: http://simplepie.org/
 [9]: http://37signals.com/
 [10]: http://search.twitter.com/
 [11]: http://twitter.com/bleikamp/statuses/1423172299