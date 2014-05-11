---
title: Post Formats and WordPress 3.6
layout: post
permalink: /2013/post-formats-and-wordpress-3-6/
excerpt: "The initial implementation of Post Formats in WordPress were confusion. This is why we (and theme designers) need to standardize."
---
I found some confusion in [an interesting discussion over on WordPress Tavern around Post Formats][1]:

> I used post formats for a few months on WPTavern.com and I’ve made a few conclusions. The first is that post formats encourage short form content. Not only is short form content easy to do, it also promotes creating a fire hose of content. The second, the majority of people were reading WPTavern.com via their favorite feedreader. Feedreaders don’t display content the same as a website. Third, some of the formats I selected displayed on the home page without a post title or an ability to comment. I think this had more to do with how my theme was displaying the formats more than anything else. Last but not least, I started treating post formats as categories. 

Here are my thoughts and response republished:

As [Chip has described][2], the concept of a &#8220;format&#8221; really just started as supported taxonomy to allow theme developers to apply consistent treatment across any blog (instead of one theme using post meta, one using a category, etc.).

Jump forward to (the in-progress) version 3.6 of WordPress and everyone has come to the same conclusion and realized there is more nuance and potential. What if this is a video post and my theme wants the video on top of the content and her theme wants it below? Standardized meta[^1] on that allows for more interesting things and the ability to solve more interesting problems.

To [Rob&#8217;s point][3], the initial implementation was confusing, but we ([Crowd Favorite][4]) created the FavePersonal theme and the [Post Formats UI plugin][5] because if we standardized on meta and fields, we could do fun stuff in the loop views, single views, and feed very easily (eg: put a full width image on the single view of &#8220;Image&#8221; posts and drop the sidebar, replace the permalink in the feed with the &#8220;Link URL&#8221; a la Daring Fireball or other linkblogs, etc.).

Hopefully this leads to more interesting uses of WordPress in the near future&#8230;

[^1]:    I don&#8217;t think the PressThis bookmarklet has done us a good long-term service here because now some display is coupled to the_content and for others the theme itself.

 [1]: http://www.wptavern.com/post-format-history-and-wordpress-3-6
 [2]: http://www.wptavern.com/post-format-history-and-wordpress-3-6#comment-21980
 [3]: http://www.wptavern.com/post-format-history-and-wordpress-3-6#comment-21856
 [4]: http://crowdfavorite.com/
 [5]: https://github.com/crowdfavorite/wp-post-formats