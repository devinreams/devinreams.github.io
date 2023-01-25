---
title: I Took Down Production
layout: post
---

I took down production. I'm shocked but not surprised. I have a knack for touching things I shouldn't. I'm also surprised how easy it was, given modern tooling.

I broke our web application because I made a minor configuration change a few days ago... and that change seemingly had no impact. Everything on the website still worked fine. And then in the early hours of a Monday holiday, some routine maintenance at our hosting provider resulted in re-starting and re-deploying our production application and _then_ there was an impact. The build process stopped and would not continue due to this change and it's all my fault...

I've broken things before. I remember taking theCHIVE offline for a few minutes back when it was five-figures dollars just to advertise on their homepage for one day. I was sitting across the table from an editorial leader from National Geographic while all their blogs were down – this was mostly AWS' fault, but redundancy is on us.

I'm surprised that I could make a minor change and not have the impact felt immediately. Or that it didn't recognize _the only change_ since last successful deploy was this _one thing_ and rollback. 

On the bright but superfluous side: because of this event we now have a pre/post launch checklist (requiring tacit knowledge) and additional health and uptime monitoring in place (to react when our checklists miss something).

And to everyone at every level of experience: its okay, we've all done it. I'm still doing it. We break things and learn from it.
