---
title: Add missing file extension to file names
author: Devin Reams
layout: post
permalink: /2011/add-missing-file-extension-to-file-names/
categories:
  - Asides
  - Lifehack
format: aside
---
For Mac users: if you ever happen to download a bunch of similar files and they&#8217;re all missing extensions (like a directory full of photos crawled using wget), here&#8217;s a quick one-line command to add the extension to all the files: `for i in * ; do mv $i $i.txt; done;`