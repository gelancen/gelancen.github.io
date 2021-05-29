---
layout: post
title: 4. Authenticate Git Operations with GitHub.com by Using SSH key
date: 2021-05-06
tags: jekyll   
---

# 4. Authenticate Git Operations with GitHub.com by Using SSH key

Run  `ssh-keygen`

![ssh-keygen](https://tva1.sinaimg.cn/large/008i3skNgy1gqzcv60nyzj30qw05k0ts.jpg)



Run `cat ~/.ssh/id_rsa.pub`

![cat ~:.ssh:id_rsa.pub](https://tva1.sinaimg.cn/large/008i3skNgy1gqzcuztzapj30vm0kogpi.jpg)



Open the settings in our github page

![setting](https://tva1.sinaimg.cn/large/008i3skNgy1gqzcurjkcqj306t0ciq34.jpg)

Click SSH and GPG keys

![SSH](https://tva1.sinaimg.cn/large/008i3skNgy1gqzcuvp39aj30790iwjs3.jpg)

![New ssh](https://tva1.sinaimg.cn/large/008i3skNgy1gqzcv5hiwvj30lo04hq35.jpg)

Paste the SSH keys

![add new ssh](https://tva1.sinaimg.cn/large/008i3skNgy1gqzcuxitslj30pv0d0mxt.jpg)

![add new ssh](https://tva1.sinaimg.cn/large/008i3skNgy1gqzcuryr4aj306t0ciq34.jpg)

Open the terminal in our github folder and run $ git branch

![git branch](https://tva1.sinaimg.cn/large/008i3skNgy1gqzcusxa2fj30q805wq3u.jpg)



Run  `cd ../ ; mkdir temp; cd temp; git clone git@github.com:gelancen/gelancen.github.io.git`

![git clone](https://tva1.sinaimg.cn/large/008i3skNgy1gqzcv1pwt2j30vo09m76k.jpg)

![yes](https://tva1.sinaimg.cn/large/008i3skNgy1gqzcuyiuk4j30vm06edhe.jpg)



Run  `ssh-keygen`

![ssh-keygen1](https://tva1.sinaimg.cn/large/008i3skNgy1gqzcurz3mnj30w405mq47.jpg)



Run `cd gelancen.github.io`

![cd gelancen.github.io](https://tva1.sinaimg.cn/large/008i3skNgy1gqzcutrue9j30u005sab5.jpg)



Run `cd git branch`

![git branch1](https://tva1.sinaimg.cn/large/008i3skNgy1gqzcuwnhauj60u405w0ts02.jpg)



open ../../gelancen.github.io

Run `jekyll serve`

Run `git status`

![git status](https://tva1.sinaimg.cn/large/008i3skNgy1gqzcv3qi9sj30so0jytbl.jpg)



Run  `git add -u; git commit -m "init"`

![git add -u; git commit -m "init"](https://tva1.sinaimg.cn/large/008i3skNgy1gqzcuuxi65j30vu0hwq6l.jpg)



Run  `git push`

![git push1](https://tva1.sinaimg.cn/large/008i3skNgy1gqzcv2xz1pj30vi0kqaeg.jpg)

Now the push is done and the page can be accessed through this url

 https://gelancen.github.io

![homepage](https://tva1.sinaimg.cn/large/008i3skNgy1gqzcv4iomxj31bu0u0jsv.jpg)Every time we update content for the blog posts by using markdown, we need to run  `git add . ; git commit -m "update"; git push` to push. 

