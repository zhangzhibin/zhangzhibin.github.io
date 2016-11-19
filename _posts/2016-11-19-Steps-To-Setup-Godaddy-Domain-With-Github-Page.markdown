---
layout: post
title:  "Steps To Setup Godday Domain With Github Page"
date:   2016-06-10 10:45:29 +0800
categories: blog
---

A quick guide for setting up Godaddy domain/subdomain with Github pages:

1. create a repo on Github
2. Repo -> *Settings* -> *GitHub Pages* -> *Source*  choose a branch (ie. master)
3. *Settings* -> *GitHub Pages* -> *Custom domain* Choose your prefered domain and Save.

> For quick testing, you may use *Settings* -> *Automatic page generator* to quickly generate a page.

Now go to GoDaddy to manage your domain. Assume your domain is example.com, and your github name is gituser.

1.Two A links
|Type|Host|Points to|TTL|
|----|----|----|----|
|A|@|192.30.252.153|1 Hour|
|A|@|192.30.252.154|1 Hour|

2.Add CNAME for www
|Type|Host|Points to|TTL|
|----|----|----|----|
|CNAME|www|gituser.github.io|1 Hour|

[ ] Your domain (www.example.com) will connect to GitHup page in a few minutes.

3.Add CNAME for other subdomain
|Type|Host|Points to|TTL|
|----|----|----|----|
|CNAME|blog|gituser.github.io|1 Hour|
[ ] Your sub-domain (blog.example.com) will connect to GitHup page in a few minutes.