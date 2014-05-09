---
title: 'How to: merge existing GMail accounts'
author: Devin Reams
layout: post
permalink: /2009/howto-move-or-migrate-gmail-account/
aktt_notify_twitter:
  - no
btc_comment_counts:
  - 'a:0:{}'
categories:
  - Internet
  - Lifehack
tags:
  - communications
  - email
  - gmail
  - google apps
  - howto
  - imap
  - tips
---
*If you&#8217;re like me you have a GMail account (something like yourname@gmail.com). But, one day, [Google Apps][1] came along and offered the opportunity for Google to host and act as your domains&#8217; email provider. I immediately forwarded all my incoming gmail.com email to devinreams.com and set up the domain on Google Apps. Then a year later, I decided to change my domain to reams.me, so I set up another Google Apps instance and started forwarding email there.</p> 
Now I had three GMail accounts, all with different email saved in them. Oh, and suddenly, Google Voice and Contacts appered on the scene. I realized I wanted go go back to my gmail.com account. I had email all over the place.</em>

## I had Google email stored in three difference places

I wanted to consolidate the email from my two Google Apps accounts (devinreams.com, reams.me) and have my thousands of emails stored all in one place (gmail.com). &#8220;No sweat&#8221;, I thought. But, this process is harder than may appear on the surface. Below I outline a multi-step process where I 

1.  physically copy email to one account to another, and 
2.  setup rules so that new mail (incoming and outgoing) is coming to/from the right places.

### Step 1: Setup Mail.app using IMAP

The biggest endeavor is moving the mail which is a process of: configuring multiple IMAP accounts in [Apple&#8217;s Mail][2] (I assume you can do the same in any IMAP-compatible email client), and physically copying the messages between the two servers. A few notes before we get setup:

*   **Labels:** Using IMAP, GMail labels will appear as &#8216;folders&#8217;. This means that one email with a label applied can appear in at least two places (All Mail, Label 1, Label 2). For simplicity&#8217;s sake, I decided to abandon the two-dozen-or-so unique labels that I had across the three accounts. There was no easy way to reconcile the different wording or usage I had evolved over the three years of different accounts. So, I stuck to simply moving &#8216;All Mail&#8217; to &#8216;All Mail&#8217; across accounts.
*   **Connectivity:** In order to make this (potentially HUGE) move, your network connection (upstream) will be in use the entire time. Basically, the email client is constantly sending commands such as &#8220;Copy Message A from Account A to Account B.&#8221; Needless to say, this will take a while and will require some bandwidth.
*   **Timeouts means batching:** In my experience, Google had a hard time keeping a connection open if I simply tried to copy 12,000 emails at once. I couldn&#8217;t tell if it was idling out (idle commands were queued to be sent *after* the copy commands&#8230;) or just choking on the request. I found I could easily queue a month (about 1,000) emails without Google disconnecting.
*   **Duplicates**: Despite my initial connection failures, IMAP and Google were smart enough not to copy duplicate messages. In other words, if I copied Message A already, and tried it again, it didn&#8217;t. So, if you lose your place when batching, don&#8217;t worry about it.
*   **Crashes:** Mail will crash when you first try to open your &#8216;All Mail&#8217; folder (or any large IMAP folder for that matter). Just relaunch a few times and it&#8217;ll get there eventually. Trust me, it may take a few tries. This is where the &#8216;Activity Window&#8217; can help tell you what&#8217;s going on.

With all that said, here&#8217;s the process:

1.  Go into your Gmail accounts and enable IMAP (Settings > Forwarding and POP/IMAP).
2.  Open Mail.app and set up your first GMail account (do not check &#8216;Automatically set up account&#8217;) following these [IMAP instructions][3]. **DO NOT** check &#8216;Take account online&#8217;.
3.  In the &#8216;Accounts&#8217; screen, select your first account and disable all the &#8216;Mailbox Behaviors&#8217; (not necessary, but prevents server-side things from happening).
4.  Switch to the &#8216;Advanced&#8217; tab and change the &#8216;Keep copies of messages..&#8217; setting to: &#8216;Don&#8217;t keep copies of any messages&#8217;.
5.  Repeat this process to set up your other account(s) that you&#8217;re moving to/from.
6.  Close the &#8216;Accounts&#8217; screen and save your changes.
7.  Open the &#8216;Activity Window&#8217; (command + 0) so you can watch what&#8217;s going on in the background.
8.  Now you can &#8216;Take All Accounts Online&#8217; from the Mailbox menu.

At this point, you now have a Mail client setup so that your emails can simply copy across accounts without locally downloading each message. Now the fun part.

### Step 2: Copy all your email from one account to the other

1.  Browse to the account you want to move email from and open the &#8216;[Gmail] All Mail&#8217; folder (this is where the crashing is likely to happen, relaunch, watch your &#8216;Activity Window&#8217;, repeat).
2.  Start wherever suits you and select a good batch of emails (I would do one month at a time, approximately 1,000 emails per month). Do **not** try to copy all of them at once. If it works, congrats, if it doesn&#8217;t, you&#8217;ll have no idea how far it got before crashing or timing out.
3.  Right click your selection and select &#8216;Copy To&#8217;. Browse to the &#8216;[Gmail] All Mail&#8217; folder of your other account. (notes: you can also drag/drop or &#8216;Copy and Paste&#8217;, you can also repeat this process using your labels instead of &#8216;All Mail&#8217;).
4.  Sit back and watch the bits and bytes fly through the internet in the Activity Window.
5.  Go ahead and queue the next batch of emails (eg: February). Repeat as much as you&#8217;d like. You can see these batches saved in the Activity Window and monitor progress.

Over the course of 3 days I was able to move about 30,000 emails in the background (set this up before you go to sleep and use an application like [Caffeine][4] to keep your computer awake). Trust me, this is *much* faster than the &#8216;POP import&#8217; process that GMail has built-in (don&#8217;t even look it up). 

Once you&#8217;ve arrived here you&#8217;ve successfully copied all your email from at least one account to another. You can confirm by browsing to your account online and doing some math. Now, I want to make sure all my future email goes to and comes from the right place.

### Step 3: Setup forwarding from the old account

Very simply, all you need to do now is visit the old accounts and browse to &#8216;Settings > Forwarding and POP/IMAP&#8217;. Configure your old address to forward to your new address. Perfect&#8230; moving on.

### Step 4: Setup your new account to send &#8216;from&#8217; your old account

You&#8217;re likely aware that GMail can send email &#8220;on behalf of&#8221; other email addresses. Set your primary email account to send from your old ones (if so desired):

1.  Browse to &#8216;Settings > Accounts&#8217;
2.  Under &#8220;Send mail as&#8221; click the &#8216;Add another email address you own&#8217; link
3.  Follow the instructions, your old address will be sent a confirmation (it should appear in your new account if you followed Step 3)
4.  If you want to use an old address as your primary outgoing address (eg: all email comes to gmail.com but I want to still send as if I&#8217;m at reams.me), then click &#8216;Default&#8217; next to that address and check the &#8220;When receiving a message:&#8221; options below.

Now you can send email from your primary account as if you were still at your old ones. [Learn more about custom &#8216;From&#8217; addresses][5].

## The consolidated life

Great, now I have all my email accounts flowing into my gmail.com account. My GMail contacts and Google Voice contacts are all synchronized (in addition to my iPhone contacts and Apple Address Book contacts).

Plus, I have over 4 years of email all in one place. I can find receipts from 2004 without having to login to my old accounts!

I tell you, I&#8217;m living the dream&#8230;

*If you have any questions, be sure to post them in the comments.*

 [1]: http://www.google.com/apps/intl/en/business/index.html
 [2]: http://www.apple.com/macosx/what-is-macosx/mail-ical-address-book.html
 [3]: http://mail.google.com/support/bin/answer.py?hl=en&#038;ctx=mail&#038;answer=75726
 [4]: http://lightheadsw.com/caffeine/
 [5]: http://mail.google.com/support/bin/answer.py?hl=en&#038;ctx=mail&#038;answer=22370