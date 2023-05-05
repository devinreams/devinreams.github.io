---
title: Archive your bookmarks with WordPress
author: Devin Reams
layout: post
permalink: /2010/backup-bookmarks-using-rss-feedwordpress/
aktt_notify_twitter:
  - yes
aktt_tweeted:
  - 1
categories:
  - Internet
  - Social Media
---
Many people use some sort of social bookmarking service to collect their favorite how-to guides, recipes, interesting articles, and funny cat pictures. There are a number of services available: [Delicious][1], [Gnolia][2], and my personal favorite [pinboard.in][3].

I found Doug Bowman&#8217;s guide to creating your own [browsable, searchable archive of tweets][4] to be perfect: create a self-hosted website using WordPress to archive your content in a format you prefer.

I wanted to do the same for [my bookmarks][5] from pinboard but couldn&#8217;t find an existing process, so I hacked together my own. Basically, I use FeedWordPress to parse the RSS feed from my bookmarking service to store all future bookmarks, and use a conversion tool to import all the old links. The following assumes a bit of existing knowledge and is mostly unsupported.

## Step 1: Export your bookmarks

Delicious and pinboard export into terrible little format called 
<pre>NETSCAPE-Bookmark-file-1</pre>

which is simply an HTML page with all your links and descriptions output in a list. There&#8217;s not much you can do with this, but at least you are able to export your links. (apparently the delicious API is much more robust now, but no matter)

## Step 2: Convert bookmarks to XBEL

Using [linkaGoGo&#8217;s bookmark conversion tool][6] you can upload your HTML bookmark file from delicious and download it as a XML file format called XBEL. Note: this doesn&#8217;t pull over your tags (let me know if you find something that does).

Some people prefer [OPML][7] as their XML-flavor for bookmarks. But I couldn&#8217;t find a conversion tool better than this.

## Step 3: Convert XBEL to RSS

Using this Yahoo Pipe I created, you can convert your [XBEL file to an RSS feed][8] (title, description, link, pubDate, and guid). Simply &#8216;Run&#8217; the pipe, &#8216;Get as RSS&#8217; and save your newly minted feed.

The point is to get your file in a format that FeedWordPress can import and parse because it can rewrite your WordPress permalinks to the original bookmark URL.

## Step 4: Import your RSS feed using FeedWordPress

Upload the feed somewhere so that it can be accessed by the plugin. Install the [FeedWordPress plugin][9] and point it to your newly created RSS feed and, huzzah, all your links should import as blog posts on the date you saved the bookmark. I created a completely [separate WordPress instance][5] so that my links archive is separate from my blog.

Bonus: under the Syndication menu, browse to the &#8216;Posts and Links&#8217; section to enable the permalinks to &#8220;point to the original URL.&#8221; This means that the permalink (link in the post title, link in your RSS feed) will point to the bookmarked link and not the WordPress post.

## Step 5: Point FeedWordPress to your bookmarking service

At this point, you can automatically capture all future links by setting up FeedWordPress to syndicate your bookmarking service&#8217;s private RSS feed. Some sites support tags and other niceties, your mileage may vary.

Check out the final result: [Devin Reams Bookmarks][10].

 [1]: http://delicious.com/
 [2]: http://gnolia.com/
 [3]: http://pinboard.in
 [4]: http://stopdesign.com/archive/2010/03/02/browsable-searchable-archive-of-tweets.html
 [5]: https://devin.rea.ms/bookmarks/
 [6]: http://www.linkagogo.com/go/Convert/Home
 [7]: http://en.wikipedia.org/wiki/OPML
 [8]: http://pipes.yahoo.com/devinreams/xbeltorss
 [9]: http://wordpress.org/extend/plugins/feedwordpress/
 [10]: https://devin.rea.ms/bookmarks