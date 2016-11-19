---
layout: post
title:  "Gem Install failed on Mac with error: Operation not permitted"
date:   2016-11-19 21:40:00 +0800
categories: blog
---

From MacOS 10.11, install apps with Gem command may failed with error:  
```
>sudo gem install jekyll bundler
Fetching: safe_yaml-1.0.4.gem (100%)
ERROR:  While executing gem ... (Errno::EPERM)
    Operation not permitted - /usr/bin/safe_yaml
```
  
A quick solution is using *-n* option to install on a different position:  
```
>sudo gem install jekyll bundler -n /usr/local/bin
```
