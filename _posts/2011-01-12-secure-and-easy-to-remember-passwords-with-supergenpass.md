---
title: Why I secure passwords with SuperGenPass
author: Devin Reams
layout: post
permalink: /2011/secure-and-easy-to-remember-passwords-with-supergenpass/
categories:
  - Internet
  - Lifehack
---
There&#8217;s been a lot of talk about security, passwords, and authentication. As we put more about us online, our passwords become ever so important. Everything from [banking][1] to [commerce][2], [friendships][3] to [resumes][4], and even our [day jobs][5] require passwords.

## Passwords are broken

Having worked in information technology auditing, I can tell you that people hate passwords. If I had so many to remember and they were all necessary for me to get my job done, I would simply pick one, easy-to-remember password. Unfortunately, businesses believe this is unsafe and force users to follow silly rules (8 characters, 2 must be numeric, and you must change this password every 60 days). Due to these rules, things become less secure. Two examples:

1.  Passwords start showing up on sticky notes next to computers. Or they are all written down in a handy notebook right next to the computer (typically open to the most frequently-used password). Now that &#8220;easy to remember&#8221; *to me* password in my head, is now written down and easy to access by anyone.
2.  Similarly, we use a database like 1Password or some other encrypted database to store all these fancy, super-secure passwords. But, then we protect them behind a single, &#8220;easy to remember&#8221; password. Now it only takes one password to unlock all your passwords, and we&#8217;re right back at square one.

[Alex][6] and I feel strongly about password security and he&#8217;s written about it many times. Here&#8217;s my thoughts and what I&#8217;ve found works best for me.

## [SuperGenPass][7]

Very similar to [PwdHash][8], [SuperGenPass][7] creates a unique, complex, secure password for every site you use. The steps are simple:

*   Enter a &#8220;master password&#8221; (eg: puppies)
*   Hash that password against the current domain (eg: facebook.com)
*   Generate a secure string using those two inputs (eg: 4ced9d6f52dc88d02028d34a3625e43d)
*   Truncate the result to X characters (eg: 10)

Here&#8217;s how SuperGenPass describes itself:

> Instead of storing your passwords on your hard disk or online—where they are vulnerable to theft and data loss—SuperGenPass uses a hash algorithm to transform a master password into unique, complex passwords for the Web sites you visit.

Arguably, the concept of a &#8220;master password&#8221; means you have one &#8220;easy to remember&#8221; password that anyone can get to and then use to generate your secure passwords. But, there are a few counterpoints:

*   An attacker would need to know I use SuperGenPass (whoops)
*   They would need to know how long my generated results are (8, 10, 20 characters long?)
*   I use a secure master password which is unguessable and not something I&#8217;d write down or use elsewhere

Now that we&#8217;re all convinced (right?), the mechanisms of using a password hashing utility are super simple.

1.  Browse to site
2.  Type in master password
3.  Use [Bookmarklet][9] or [Mobile site][10] to generate hashed password
4.  Login!

Since I use Safari, I have SuperGenPass added to my Bookmarks Bar and I can use Command + 1 on any page to trigger the bookmarklet to enter my password. It then finds any &#8220;password&#8221; fields on the page and auto-populates them with the hashed version. This is *very* fast and hardly any more intrusive than simply typing a password into a form.  
<dl id="attachment_1629" class="wp-caption aligncenter" style="max-width:580px">
  <dt>
    <a href="https://devin.rea.ms/wp-content/uploads/2011/01/supergenpass-wellsfargo.png"><img src="https://devin.rea.ms/wp-content/uploads/2011/01/supergenpass-wellsfargo.png" alt="" title="SuperGenPass in use on WellsFargo.com" width="580" height="389" class="size-full wp-image-1629" /></a>
  </dt>
  
  <dd>
    Simply entering my password into the form and hitting Command - 1 means a super-secure password is instantly replaced.
  </dd>
</dl>

This also works well for me because I can use the Bookmarklet in Mobile Safari (iPhone, iPad). I can pull up the mobile site on any machine in the world. If it&#8217;s unavailable? No problem, I&#8217;ve stored the mobile site in my Dropbox. Since all that&#8217;s needed is JavaScript to run, I can even generate my passwords offline.

Still not convinced? [Drop a line][11] or leave a comment to share your thoughts&#8230;

 [1]: http://www.schwab.com/
 [2]: http://www.amazon.com/
 [3]: https://facebook.com/
 [4]: http://www.linkedin.com/
 [5]: http://www.basecamphq.com/
 [6]: http://alexking.org/
 [7]: http://supergenpass.com/
 [8]: http://crypto.stanford.edu/PwdHash/
 [9]: http://supergenpass.com/customize/
 [10]: http://supergenpass.com/mobile/
 [11]: mailto:devin@reams.me