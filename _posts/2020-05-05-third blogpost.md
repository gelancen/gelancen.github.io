---
layout: post
title: 3. Making a Personal Blog Page with GitHub Pages and Jekyll
date: 2021-05-05
tags: jekyll   
---

# 3. Making a Personal Blog Page with GitHub Pages and Jekyll

Register a  [GitHub](https://github.com/) account.

![github account](https://tva1.sinaimg.cn/large/008i3skNgy1gqzctqs5kzj31l20owwk2.jpg)



Choose a theme from http://jekyllthemes.org/ and fork an authorized repository （This is the one I chose https://github.com/leopardpan/leopardpan.github.io)

![Fork](https://tva1.sinaimg.cn/large/008i3skNgy1gqzcu42acwj31iy0u0q80.jpg)



Rename the forked repository

![rename](https://tva1.sinaimg.cn/large/008i3skNgy1gqzcu2qhr3j31nn0u078q.jpg)



Clone the repository with Atom by pasting the url

![clone](https://tva1.sinaimg.cn/large/008i3skNgy1gqzctzbcbqj31d40u076v.jpg)



Finish cloning

![finish cloning](https://tva1.sinaimg.cn/large/008i3skNgy1gqzctthioej31e70u0436.jpg)



Delete the existing files under _posts 

![exsiting post](https://tva1.sinaimg.cn/large/008i3skNgy1gqzcu0brv2j31e70u0436.jpg)



Edit the _config.yml and customize it according to our personal information  

![cognfig](https://tva1.sinaimg.cn/large/008i3skNgy1gqzcu158xkj30u00w3acg.jpg)



Open the terminal in our github folder and run `jekyll server`  

 ![open terminal](https://tva1.sinaimg.cn/large/008i3skNgy1gqzctv2wm9j30vi0kymxv.jpg)

![trace](https://tva1.sinaimg.cn/large/008i3skNgy1gqzctvndgfj30vk0kewjr.jpg)



Run  `serve --trace` 

![append trace](https://tva1.sinaimg.cn/large/008i3skNgy1gqzctygyblj30vg0fwae9.jpg)



Run  `bundle add webrick`

![bundle add webrick](https://tva1.sinaimg.cn/large/008i3skNgy1gqzcu1pedgj30vi07atas.jpg)



Run  `jekyll server`  

![jekyll server](https://tva1.sinaimg.cn/large/008i3skNgy1gqzcu50f0yj30vi0kq43t.jpg)



In order to push our jekyll page to Github, we should first press ctrl-c to stop running the server.

Run  `git add -u`

Run  `git ci -m 'init'`

![git ci -m 'init'](https://tva1.sinaimg.cn/large/008i3skNgy1gqzctwjuuwj30oe0dmab1.jpg)

Run  `git commit -m 'init'`

![git commit -m 'init'](https://tva1.sinaimg.cn/large/008i3skNgy1gqzcu3k2ouj30vq080mz5.jpg)



Run  `git push`

![git push](https://tva1.sinaimg.cn/large/008i3skNgy1gqzctsc4ctj30vg080dho.jpg)



Enter the username and password 

![Enter the username and password ](https://tva1.sinaimg.cn/large/008i3skNgy1gqzctrby6fj30ve04w3zm.jpg)



Then I received a deprecation notice from GitHub through email

<img src="https://tva1.sinaimg.cn/large/008i3skNgy1gqzctxesbbj30n01dsgo6.jpg" alt="Deprecation Notice" style="zoom:50%;" />

Visit https://github.blog/2020-12-15-token-authentication-requirements-for-git-operations/

<img src="https://tva1.sinaimg.cn/large/008i3skNgy1gqzctua6l9j30n01dsdmm.jpg" alt="token authentication requirement" style="zoom: 50%;" />



# 