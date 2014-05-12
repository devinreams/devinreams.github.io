---
title: Grade Report
author: Devin Reams
layout: post
permalink: /2006/grade-report/
btc_comment_counts:
  - 'a:0:{}'
categories:
  - Internet
tags:
  - Lifehack
---
I like to play with numbers. Good thing I switched my major to Accounting, right? In any case, what&#8217;s one of the most important numbers to any student? That&#8217;s right: their GPA.

<p align="center">
  <img src="http://devinreams.com/wp-content/uploads/2006/05/gradeheader.png" />
</p>

A few semesters ago I sat around wondering what my GPA would look like if I were to get an &#8216;A&#8217; in X Class and a &#8216;B+&#8217; in Y Class. I didn&#8217;t understand how Credit Hours and all that stuff worked. So, I pulled up some information online and realized it&#8217;s much simpler than I first imagined&#8230; but it still takes a bit of manual work to sort things out. So, like most of my problems, I decided to solve it with Excel.

Admittedly this isn&#8217;t a revolutionary tool or anything beyond a few formulas. But, it certainly helped me play with the numbers. I could tell how well I needed to do this semester in order to stay on the Dean&#8217;s List. Being an [IB][1] kid I guess I worry about silly things like that&#8230;

<p align="center">
  <img src="http://devinreams.com/wp-content/uploads/2006/05/grade2.png" />
</p>

As you can see I&#8217;ve put in the necessary columns: course code, name, credits, grade (enter letter grade to get numerical score), quality points (score x credits). All I have to enter is the code, name, weight and then the letter grade. The rest will compute itself.

My understanding is that many colleges approach grades this way. If you&#8217;re in high school then all your classes would have a credit of &#8217;1&#8242; except for AP classes which would be more (again, depending on the school).

In any case, I&#8217;ve sent this to a few friends and they&#8217;ve found it particularly useful for keeping their own records. Plus, as I mentioned, you can play around with grades and see how well you need to do in upcoming courses.

<p align="center">
  <img src="http://devinreams.com/wp-content/uploads/2006/05/grade3.png" />
</p>

Notes: I added 30 hours to the Cumulative Credit Hours at the bottom (IB credit), you might want to take that out. If you need more semesters simply copy the Spring 2007 box, right click row 45 (empty row below it) and &#8216;Insert Copied Cells&#8217; and select &#8216;Shift Cells Down&#8217;. From there you&#8217;ll need to make sure the cumulative GPA (furthest right) includes the new grades. Go into the cell and notice how the two sums are simply column F divided by the total credits in column C. Just add a comma and include the first grades/credits. Repeat for any other semesters added. Additionally, if your school has different values for the letter grades then simply unhide columns H and I. If you look in column K I also pointed to the values of only my business classes. This way I could compute my Business (Degree) GPA. In any case, check the formulas and have fun printing out your own report card!

As always, shoot me your comments, questions and/or suggestions.

~~Click here to download Grade Report.xls~~

[tags]grades, college, school, report card[/tags]

 [1]: http://www.ibo.org/