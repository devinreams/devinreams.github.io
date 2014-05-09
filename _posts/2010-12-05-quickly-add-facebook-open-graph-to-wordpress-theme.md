---
title: Quickly add Open Graph to WordPress theme
author: Devin Reams
layout: post
permalink: /2010/quickly-add-facebook-open-graph-to-wordpress-theme/
btc_comment_counts:
  - 'a:0:{}'
categories:
  - Internet
  - WordPress
---
I&#8217;ve found a lot of benefit adding [Open Graph][1] properties to my blogs. Primarily: more visitors. By adding simple code to my WordPress theme headers, social plugins like the &#8216;Like&#8217; button will make your content display more meaningful within Facebook.

Which of these two articles would you be drawn to? Which would cause you to stop, read, and consider clicking through to? 

Yet another easily ignorable line item:

[<img src="http://devin.reams.me/wp/wp-content/uploads/2010/12/without-open-graph.png" alt="" title="without-open-graph" width="555" height="25" class="aligncenter size-full wp-image-1600" />][2]

Or this rich image and excerpt:

[<img src="http://devin.reams.me/wp/wp-content/uploads/2010/12/with-open-graph-properties.png" alt="" title="with-open-graph-properties" width="555" height="187" class="aligncenter size-full wp-image-1599" />][3]

With WordPress I can easily drop a few lines of code into my theme&#8217;s header and make any &#8216;Liked&#8217; content a little more compelling.

## The Source

In the header, I&#8217;ve added a quick snippet to grab only the image URL of the featured image for the current post ([via wpcanyon.com][4]):

    
    $thumb = get_the_post_thumbnail($post->ID);
    $pattern= "/(?<=src=['|\"])[^'|\"]*?(?=['|\"])/i";
    preg_match($pattern, $thumb, $thePath);
    $theSrc = $thePath[0];</blockquote>
    
    

I then add the following to define the [required Open Graph properties][5]:

    
    <meta property="fb:admins" content="<strong>FACEBOOK ID</strong>" />
    <? if (is_single()) { ?>
    <meta property="og:title" content="<?php echo get_the_title(); ?>"/>
    <meta property="og:type" content="article"/>
    <meta property="og:image" content="<?php echo $theSrc; ?>" />
    <meta property="og:url" content="<?php the_permalink() ?>" />
    <meta property="og:description" content="<?php the_excerpt_rss() ?>" />
    <meta propert="og:site_name" content="<?php bloginfo('name'); ?>" />
    <? } ?>
    

And just like that, you&#8217;ve added all the necessary properties to your theme to tell anything that respects Open Graph (primarily Facebook) to your blog articles.

Be sure to use the [Facebook URL Linter][6] to test this out. Here&#8217;s [an example][7] of a recent post of mine.

 [1]: http://opengraphprotocol.org/
 [2]: http://devin.reams.me/wp/wp-content/uploads/2010/12/without-open-graph.png
 [3]: http://devin.reams.me/wp/wp-content/uploads/2010/12/with-open-graph-properties.png
 [4]: http://wpcanyon.com/tipsandtricks/get-the-src-attribute-from-wordpress-post-thumbnail/
 [5]: http://developers.facebook.com/docs/opengraph
 [6]: http://developers.facebook.com/tools/lint/
 [7]: http://developers.facebook.com/tools/lint/?url=http%3A%2F%2Fdevin.reams.me%2F2010%2Fhalloween-2010-in-colorado%2F