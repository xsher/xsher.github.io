---
layout: post
title: Custom domain for my site!
date: '2020-07-22 12:47'
excerpt: My experience with updating my github page to use a custom domain!
comments: true
---
##  \# 1/50

As a software engineer, git tool has became part of my daily tinkering. Github Pages became my go-to choice when I decided to start building my own site [finally]. As I have been more committed to building this up, I have decided to buy my first domain yesterday and set it up for my github page.

Github has provided a [documentation](https://docs.github.com/en/github/working-with-github-pages/managing-a-custom-domain-for-your-github-pages-site) on how to set up custom domains for our github pages. Here, I will summarize into 4 simple steps:

1. Go to the DNS provider of your custom domain and set up the following records:
    Type: A,     Name: @,   Value: 185.199.108.153
    Type: A,     Name: @,   Value: 185.199.109.153
    Type: A,     Name: @,   Value: 185.199.110.153
    Type: A,     Name: @,   Value: 185.199.111.153
    Type: CNAME, Name; www, Value: <Github Page URL>

   To verify: `dig <your custom domain>` and you should observe the A records corresponding to your changes.

2. Go to the root level of your github page repository and add a `CNAME` file. Add a single entry with the value: <your custom domain>.
   Commit and push your changes to github.

3. Go to the settings tab of your github page repository. Under the section `Github Pages` update the custom domain field and select the option `Enforce HTTPS`. 

4. Navigate to your site with your custom domain and you should see your github page.
   Note: You may observe some security warnings as it may take some time for `Enforce HTPPS` to fully take effect.


It took me less than 10 minutes to have everything set up and running as I intended.

Thanks for reading!




_You can, you should, and if you're brave enough to start, you will - Stephen King_
