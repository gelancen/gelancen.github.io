---
layout: post
title: 4. Authenticate Git Operations with GitHub.com by Using SSH key
date: 2021-05-06
tags: jekyll   
---

# 4. Authenticate Git Operations with GitHub.com by Using SSH key

Run  `ssh-keygen`

![ssh-keygen](/Users/mac/Desktop/KUL/online publishing/BLOG/ssh-keygen.jpeg)



Run `cat ~/.ssh/id_rsa.pub`![cat ~:.ssh:id_rsa.pub](/Users/mac/Desktop/KUL/online publishing/BLOG/cat ~:.ssh:id_rsa.pub.jpeg)



Open the settings in our github page

![setting](/Users/mac/Desktop/KUL/online publishing/BLOG/setting.jpg)

Click SSH and GPG keys

![SSH](/Users/mac/Desktop/KUL/online publishing/BLOG/SSH.png)

![New ssh](/Users/mac/Desktop/KUL/online publishing/BLOG/New ssh.png)

Paste the SSH keys

![add new ssh](/Users/mac/Desktop/KUL/online publishing/BLOG/add new ssh.png)

![add new ssh](/Users/mac/Desktop/KUL/online publishing/BLOG/add new ssh.png)

Open the terminal in our github folder and run $ git branch

![git branch](/Users/mac/Desktop/KUL/online publishing/BLOG/git branch.jpeg)



Run  `cd ../ ; mkdir temp; cd temp; git clone git@github.com:gelancen/gelancen.github.io.git`

![git clone](/Users/mac/Desktop/KUL/online publishing/BLOG/git clone.jpeg)

![yes](/Users/mac/Desktop/KUL/online publishing/BLOG/yes.jpeg)



Run  `ssh-keygen`

![ssh-keygen1](/Users/mac/Desktop/KUL/online publishing/BLOG/ssh-keygen1.jpeg)



Run `cd gelancen.github.io`

![cd gelancen.github.io](/Users/mac/Desktop/KUL/online publishing/BLOG/cd gelancen.github.io.jpeg)



Run `cd git branch`

![git branch1](/Users/mac/Desktop/KUL/online publishing/BLOG/git branch1.jpeg)



open ../../gelancen.github.io

Run `jekyll serve`

Run `git status`

![git status](/Users/mac/Desktop/KUL/online publishing/BLOG/git status.jpeg)



Run  `git add -u; git commit -m "init"`

![git add -u; git commit -m "init"](/Users/mac/Desktop/KUL/online publishing/BLOG/git add -u; git commit -m "init".jpeg)



Run  `git push`

![git push1](/Users/mac/Desktop/KUL/online publishing/BLOG/git push1.jpeg)

Now the push is done and the page can be accessed through this url

 https://gelancen.github.io

![homepage](/Users/mac/Desktop/KUL/online publishing/BLOG/homepage.png)Every time we update content for the blog posts by using markdown, we need to run  `git add . ; git commit -m "update"; git push` to push. 

