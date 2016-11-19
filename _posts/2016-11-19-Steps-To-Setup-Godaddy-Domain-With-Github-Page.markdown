---
layout: post
title:  "Steps To Setup Godday Domain With GitHub Page"
date:   2016-11-19 20:00:00 +0800
categories: blog
---

A quick guide for setting up Godaddy domain/subdomain with GitHub pages:

### On GitHub ###
1. create a repo on GitHub
2. Repo -> *Settings* -> *GitHub Pages* -> *Source*  choose a branch (ie. master)
3. *Settings* -> *GitHub Pages* -> *Custom domain* Choose your prefered domain and Save.

> For quick testing, you may use *Settings* -> *Automatic page generator* to quickly generate a page.

### On GoDaddy ###
Assume your domain is *example.com*, and your GitHub name is *gituser*.

1.Two A links

<table>
    <tr>
        <td>Type</td>
        <td>Host</td>
        <td>Points to</td>
        <td>TTL</td>
    </tr>
     <tr>
        <td>A</td>
        <td>@</td>
        <td>192.30.252.153</td>
        <td>1 Hour</td>
    </tr>
    <tr>
        <td>A</td>
        <td>@</td>
        <td>192.30.252.154</td>
        <td>1 Hour</td>
    </tr>    
</table>  

2.Add CNAME for www

<table>
    <tr>
        <td>Type</td>
        <td>Host</td>
        <td>Points to</td>
        <td>TTL</td>
    </tr>
    <tr>
        <td>CNAME</td>
        <td>www</td>
        <td>gituser.github.io</td>
        <td>1 Hour</td>
    </tr>    
</table>
  
> Your domain (www.example.com) will connect to GitHub page in a few minutes.

  
3.Add CNAME for other subdomain (ie, blog)

<table>
    <tr>
        <td>Type</td>
        <td>Host</td>
        <td>Points to</td>
        <td>TTL</td>
    </tr>
    <tr>
        <td>CNAME</td>
        <td>blog</td>
        <td>gituser.github.io</td>
        <td>1 Hour</td>
    </tr>    
</table>

> Your sub-domain (blog.example.com) will connect to GitHub page in a few minutes.