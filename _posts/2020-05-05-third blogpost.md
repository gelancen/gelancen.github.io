---
layout: post
title: 3. Making a Personal Blog Page with GitHub Pages and Jekyll
date: 2021-05-05
tags: jekyll   
---

# 3. Making a Personal Blog Page with GitHub Pages and Jekyll

Register a  [GitHub](https://github.com/) account.

![github account](/Users/mac/Desktop/KUL/online publishing/BLOG/github account.png)



Choose a theme from http://jekyllthemes.org/ and fork an authorized repository （This is the one I chose https://github.com/leopardpan/leopardpan.github.io)

![Fork](/Users/mac/Desktop/KUL/online publishing/BLOG/Fork.png)



Rename the forked repository

![rename](/Users/mac/Desktop/KUL/online publishing/BLOG/rename.png)



Clone the repository with Atom by pasting the url

![clone](/Users/mac/Desktop/KUL/online publishing/BLOG/clone.png)



Finish cloning

![finish cloning](/Users/mac/Desktop/KUL/online publishing/BLOG/finish cloning.png)



Delete the existing files under _posts 

![exsiting post](/Users/mac/Desktop/KUL/online publishing/BLOG/exsiting post.png)



Edit the _config.yml and customize it according to our personal information  

![cognfig](/Users/mac/Desktop/KUL/online publishing/BLOG/cognfig.png)



Open the terminal in our github folder and run `jekyll server`  

 ![open terminal](/Users/mac/Desktop/KUL/online publishing/BLOG/open terminal.png)

![trace](/Users/mac/Desktop/KUL/online publishing/BLOG/trace.jpeg)



Run  `serve --trace` 

![append trace](/Users/mac/Desktop/KUL/online publishing/BLOG/append trace.jpeg)



Run  `bundle add webrick`

![bundle add webrick](/Users/mac/Desktop/KUL/online publishing/BLOG/bundle add webrick.jpeg)



Run  `jekyll server`  

![jekyll server](/Users/mac/Desktop/KUL/online publishing/BLOG/jekyll server.jpeg)



In order to push our jekyll page to Github, we should first press ctrl-c to stop running the server.

Run  `git add -u`

Run  `git ci -m 'init'`

![git ci -m 'init'](/Users/mac/Desktop/KUL/online publishing/BLOG/git ci -m 'init'.jpeg)

Run  `git commit -m 'init'`

![git commit -m 'init'](/Users/mac/Desktop/KUL/online publishing/BLOG/git commit -m 'init'.jpeg)



Run  `git push`

![git push](/Users/mac/Desktop/KUL/online publishing/BLOG/git push.jpeg)



Enter the username and password 

![Enter the username and password ](/Users/mac/Desktop/KUL/online publishing/BLOG/Enter the username and password .jpeg)



Then I received a deprecation notice from GitHub through email

<img src="/Users/mac/Desktop/KUL/online publishing/BLOG/Deprecation Notice.jpeg" alt="Deprecation Notice" style="zoom:50%;" />

Visit https://github.blog/2020-12-15-token-authentication-requirements-for-git-operations/

<img src="/Users/mac/Desktop/KUL/online publishing/BLOG/token authentication requirement.png" alt="token authentication requirement" style="zoom: 50%;" />

