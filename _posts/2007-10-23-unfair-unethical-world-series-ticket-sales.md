---
title: Unfair, unethical World Series ticket sales
author: Devin Reams
layout: post
permalink: /2007/unfair-unethical-world-series-ticket-sales/
btc_comment_counts:
  - 'a:0:{}'
categories:
  - Internet
tags:
  - Rants
  - Technology
---
I have a huge issue with how tickets were sold here on Monday/Tuesday to the World Series games in Denver. My biggest issue is with the lying, unfair company behind the online ticket sales, Paciolan Inc.

Here&#8217;s a run-down of all the issues and what I suspect really happened:

*   **No tickets were sold in-person:** They said putting them all online would be more fair to the public. **Wrong!** It would&#8217;ve been *more* fair to put some tickets at Coors Field because Denver locals would be guaranteed fairly-priced tickets. Instead, people without internet access had to go to the local library (they still took the day off!). Someone (probably at Paciolan) convinced the Rockies to sell all their tickets online. You know, because people at work couldn&#8217;t go down and wait in line.
*   **Delayed their press conference over an hour:** Rockies officials said they&#8217;d talk about what would happen to ticket sales at 5:00pm yesterday. Nobody showed up until around 6:30pm. Unprofessional. Two problems, 1) it doesn&#8217;t take 5 hours to fix a server issue unless your code or architecture are severely unscalable, 2) you don&#8217;t leave millions of people hanging around waiting unless you really don&#8217;t have a good answer. They didn&#8217;t.
*   **They were [taken down][1] by a DDoS attack:** I think this is a downright lie. Paciolan says the Rockies ticket sales had nothing to do with their servers suddenly crawling to a halt on Monday. Thus, causing ticket sales to be suspended until noon the next day. No, this was not an attack, it was a lot of people trying to buy a ticket all at once. How do I know? They said they had backup plans ready for Tuesday. Yet&#8230; the servers crawled to a halt again. That&#8217;s how the internet works! No way was there an attack that couldn&#8217;t have been prevented (by a competent service provider).
*   **Monday had many evenue web servers, Tuesday had one:** On Monday we were directed to ev15.evenue.net&#8230; along with ev8, ev14 and a slew of other subdomains. On Tuesday I only saw ev3. My suspicion: they blocked certain users and sent them to a default error page that only refreshed with no intention of allowing a ticket purchase. I tried connecting to all the other evenue.net servers today with no luck. They obviously exist though, go [search on Google][2]. I have a strong suspicion because&#8230;.
*   **IP-blocking was occurring:** Paciolan outright said they had blocked &#8216;suspicious&#8217; IP addresses (you know, because of all that attacking going on). **No way!** By saying that we know they blocked people, but not specifically who or what. They could go straight to the firewall and deny multiple connections from the same IP-address and send them off to some phony page (like, the ev3 server). So, then Company A has 50 employees and they all try to connect at once. Paciolan then denies all of them sending them to ev3 and an eternity of refreshing. No intention of ever selling tickets to these people. Oops, what happened to the fairness of people buying tickets at work? Rumor has it they were also trying to blocking IPs that weren&#8217;t &#8220;local.&#8221;
*   **Lying about refreshing a page:** Paciolan put up [a message][3] on Tuesday saying that manually refreshing the page will put you at the &#8216;end of the line&#8217;. Despite the obvious fact their own page was a simple countdown that then, you guessed it, [refreshed the page][4]. Just another way to manipulate people and try to keep them from taking down their servers (again).

Long story short: Paciolan gets hit hard on Monday. Blocks a lot of people from buying tickets Tuesday. Lies to users and tells them not to refresh their pages. All because they don&#8217;t want to look like idiots that couldn&#8217;t handle World Series sales (or DDoS attacks for that matter).

If I were the Colorado Rockies (or [any client][5] of theirs for that matter) I would drop this company real quick for the shady, unprofessional job they did this week.

 [1]: http://sports.espn.go.com/mlb/playoffs2007/news/story?id=3074302
 [2]: http://www.google.com/search?q=site%3Aevenue.net&#038;ie=utf-8&#038;oe=utf-8&#038;aq=t&#038;rls=org.mozilla:en-US:official&#038;client=firefox-av
 [3]: http://www.flickr.com/photos/devdev/1716011773/
 [4]: http://www.flickr.com/photos/devdev/1716859600/
 [5]: http://www.paciolan.com/public_clients.htm