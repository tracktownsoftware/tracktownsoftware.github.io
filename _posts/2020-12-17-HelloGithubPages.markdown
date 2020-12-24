---
layout: post
title:  "Hello Github Pages"
date:   2020-12-17 13:51:59 -0800
categories: jekyll github
---

# Moving my website to GitHub Pages

Going into 2021 I decided to become more active on GitHub and try my hand at a programming blog. Before [GitHub Pages](https://pages.github.com/) I hosted my website on [DiscountASP.NET](https://www.discountasp.net/). I began implementing my blog in ASP.NET but then decided it will be simpler to host it on a [GitHub Pages user site](https://docs.github.com/en/free-pro-team@latest/github/working-with-github-pages/about-github-pages#types-of-github-pages-sites) with the [Jekyll](https://jekyllrb.com/) static site generator.

There's a lot of information online for making your own GitHub Pages blog with Jekyll, so I won't document the steps here. [This post on kiltandcode.com steps you through the entire process.](https://www.kiltandcode.com/2020/04/30/how-to-create-a-blog-using-jekyll-and-github-pages-on-windows/) See my list of helpful links below.

The one issue I ran into: Jekyll required installing Ruby onto my Windows 10 computer. RubyInstaller ver 2.7 didn't seem to install correctly, so I uninstalled it and found success with RubyInstaller ver 2.6.

# Custom Domain for my Github Pages site

I needed subdomain **www.tracktownsoftware.com** and apex domain **tracktownsoftware.com** to point to my new Github Pages site.  

The subdomain was easy. On DiscountASP.NET I added a DNS CNAME record to point **www.tracktownsoftware.com** to  **tracktownsoftware.github.io** (my Github Pages repository).

The DiscountASP.NET DNS Manager doesn't support ALIAS, ANAME or A records, so **tracktownsoftware.com** still pointed to my old site. My solution was to do a redirect by making an empty "ASP.NET Web application (.NET Framework)" in VS2019 and then adding the index.html below. I deleted the existing files on DiscountASP.NET and then published my simple redirect web application.

```html
<html>
<head>
    <meta charset="utf-8" />
    <meta http-equiv="refresh" content="0; URL='https://www.tracktownsoftware.com'" />
    <title>Redirect to new www.TrackTownSoftware.com...</title>
</head>
<body>
</body>
</html>
```

# Development environment for my Github Pages site
I use [Visual Studio Code](https://code.visualstudio.com/) to open and edit the project folder in my Git local repository. VSCode supports Git actions by clicking on icons in the project Explorer window, but I prefer typing Git commands into a VSCode terminal Bash window.

In the VSCode terminal Bash window you can test your Jekyll website by running the command below. It will respond with a local server address you can click on. In VSCode you can make edits to your site, save and then refresh your browser window to see changes.
```
$ jekyll serve
```
If the above command doesn't work try using:
```
$ bundle exec jekyll serve
```

# Helpful links
- [What are GitHub Pages](https://pages.github.com/)
- [Jekyll Quickstart](https://jekyllrb.com/docs/)
- [Getting started with GitHub Pages](https://docs.github.com/en/free-pro-team@latest/github/working-with-github-pages/getting-started-with-github-pages)
- [Blogging with Jekyll on GitHub Pages](https://docs.github.com/en/free-pro-team@latest/github/working-with-github-pages/setting-up-a-github-pages-site-with-jekyll)
- [Managing a custom domain for your GitHub Pages site](https://docs.github.com/en/free-pro-team@latest/github/working-with-github-pages/managing-a-custom-domain-for-your-github-pages-site)
- [Markdown syntax](https://www.markdownguide.org/basic-syntax/)
- [Git Cheat Sheet](https://education.github.com/git-cheat-sheet-education.pdf)
- [How Git Works (video)](https://www.pluralsight.com/courses/how-git-works)
- [VSCode Working with GitHub](https://code.visualstudio.com/docs/editor/github)
- [VSCode Integrated terminal window](https://code.visualstudio.com/docs/editor/integrated-terminal)


