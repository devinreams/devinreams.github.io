---
title: 'Google Profile tips: OpenID delegate, resetting profile photo'
author: Devin Reams
layout: post
permalink: /2009/google-profile-tips-openid-delegate-resetting-profile-photo/
aktt_notify_twitter:
  - no
btc_comment_counts:
  - 'a:0:{}'
categories:
  - Internet
  - Social Media
---
I&#8217;ve been more and more interested in having Google manage, store, and maintain my entire life. Not just my digital life, but my real life. Needless to say, I&#8217;ve been using [Google Profiles][1] and have come up with a few neat tips.

<div>
</div>

<div>
  <span style="font-size: large;">Google Profile photo being reset all the time</span>
</div>

<div>
  <span style="font-size: large;"><strong><br /></strong></span>
</div>

<div>
  Some people have noticed their profile photo being reset frequently. I learned that if you use a client such as Pidgin or Adium to login to Google Chat (with the same account as your profile) then it sets your profile photo to, well, nothing.
</div>

<div>
</div>

<div>
  Simply add your profile photo in your client to the image you want to use across your Google services (chat, contacts, etc.) and it will stick. I added an profile image to Adium and haven&#8217;t seen it reset in 48 hours.
</div>

<div>
</div>

<div>
  <span style="font-size: large;">Google Profile as an OpenID delegate</span>
</div>

<div>
  <span style="font-size: large;"><br /></span>
</div>

<div>
  I was excited when Google Profiles became an OpenID provider but the domain sucked. Now you can use your profile URL (<a href="http://www.google.com/profiles/devin.reams">http://www.google.com/profiles/devin.reams</a>) as the OpenID endpoint.
</div>

<div>
</div>

<div>
  Even better, you can use your own domain (such as <a href="http://devinr.com">devinr.com</a>) and delegate it to Google. In other words, I can now login to all my OpenID-enabled sites using my own domain but using the secure authentication at Google.
</div>

<div>
</div>

<div>
  Thanks to <a href="http://www.flickr.com/photos/factoryjoe/4134418702/">Chris Messina</a> and <a href="http://friendfeed.com/dewitt/b9ad7eff/picture-of-me-signed-in-to-js-kit-with-my-openid">DeWitt Clinton</a> for the following:
</div>

<div>
</div>

<blockquote style="margin: 0 0 0 40px; border: none; padding: 0px;">
  <p>
    <span style="font-family: monospace; font-size: medium; white-space: pre-wrap; "><span style="font-size: small;"><link href=&#8221;</span><span style="font-size: small;">https://www.google.com/accounts/o8/ud</span><span style="font-size: small;">&#8221; rel=&#8221;openid2.provider&#8221; /></span></span><span style="font-size: small;"><br /></span><span style="font-size: small;"> </span><span style="font-family: monospace; font-size: medium; white-space: pre-wrap; "><span style="font-size: small;"><link href=&#8221;</span><span style="font-size: small;">https://www.google.com/profiles/</span><span style="background-color: #ffff00;"><span style="font-size: small;">{PROFILE ID}</span></span><span style="font-size: small;">&#8221; rel=&#8221;openid2.local_id&#8221; /> &nbsp;</span></span><span style="font-size: small;"><br /></span><span style="font-size: small;"> </span><span style="font-family: monospace; font-size: medium; white-space: pre-wrap; "><span style="font-size: small;"><link href=&#8221;</span><span style="font-size: small;">https://www.google.com/accounts/o8/ud</span><span style="font-size: small;">&#8221; rel=&#8221;openid.server&#8221; /></span></span><span style="font-size: small;"><br /></span><span style="font-size: small;"> </span><span style="font-family: monospace; font-size: medium; white-space: pre-wrap; "><span style="font-size: small;"><link href=&#8221;</span><span style="font-size: small;">https://www.google.com/profiles/</span><span style="background-color: #ffff00;"><span style="font-size: small;">{PROFILE ID}</span></span><span style="font-size: small;">&#8221; rel=&#8221;openid.delegate&#8221; /></span></span>
  </p>
</blockquote>

 [1]: http://www.google.com/profiles/