---
layout: post
title:  "GitHub Pages: User or Organization versus Project sites"
date:   2020-12-22 10:20:00 -0800
categories: jekyll github
---

# User or Organization site

Github allows one user or organization GitHub Pages site per account. This special GitHub repository must be named in the form **username.github.io** where username is your username (or organization name) on GitHub.

On GitHub your source code for this site will be the familiar GitHub repository path **https://github.com/username/username.github.io**.

What does it mean to be a GitHub Pages site? In a browser when you navigate to **https://username.github.io** then GitHub will try to present the contents of this repository as a static website.

# Project Site

Your other repositories (not named **username.github.io**) can be set up to include a GitHub Pages Project site.

On GitHub let's say you have a repository containing source code at **https://github.com/username/mygreatlibrary** where username is your username (or organization name) on GitHub.

You can publish documentation about mygreatlibrary in the same repository. A common convention is to add a folder named "docs" containing markdown files (or html/javascript/css). To designate this folder as a GitHub Pages Project site (Github describes this as [choosing a publishing source](https://docs.github.com/en/free-pro-team@latest/github/working-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site#choosing-a-publishing-source)) go to the repository settings and scroll down to Github Pages Source and select the "docs" folder from the branch where you put it (probably main or master).

After allowing a few minutes to publish you can see your mygreatlibrary Github Pages Project site in a browser by navigating to **https://username.github.io/mygreatlibrary**.

# Managing a custom domain for your Github Pages sites

Your default subdomain for all your Github Pages sites is **username.github.io**.

You can point to your own custom domain by following these instructions from Github: [Managing a custom domain for your GitHub Pages site](https://docs.github.com/en/free-pro-team@latest/github/working-with-github-pages/managing-a-custom-domain-for-your-github-pages-site)

Now I can navigate to my GitHub Pages user site with **https://www.tracktownsoftware.com** rather than **https://tracktownsoftware.github.io**.

If I had a mygreatlibrary repository with a GitHub Pages project site the address would be **https://www.tracktownsoftware.com/mygreatlibrary** rather than **https://tracktownsoftware.github.io/mygreatlibrary**.

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
