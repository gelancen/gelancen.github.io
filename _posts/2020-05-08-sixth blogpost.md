---
layout: post
title: 6. Another Way to Make GitHub Pages with Jekyll
date: 2021-05-08
tags: jekyll   
---

# 6. Another Way to Make GitHub Pages with Jekyll

GitHub Pages makes it easy to publish and host a Jekyll site for free.There is a solution that allows us to automate this process. We can use [GitHub Actions](https://github.com/features/actions), which is a feature that allows us to automate workflows based on certain events that happen on our repo. For example, we can create a workflow that automatically builds the site using the same version of Jekyll and other gems in our project, and deploys it every time we push to the `main` branch. It can also automatically create the `gh-pages` branch.

There are some prerequistites we need to follow along.

- A [GitHub](https://github.com/) account.

  ![github account](https://tva1.sinaimg.cn/large/008i3skNgy1gqzcwstbdyj610k0ne0v602.jpg)

- A working Ruby development environment with Homebrew, chruby, ruby-install, Bundler, Git and the GitHub CLI. 

- A configured Git environment, with our name, email, editor, and `main` as our default branch.

  Here are the example commands to set your name and email:

  ```
  git config --global user.name "Your Name"
  git config --global user.email you@example.com
  ```

   To set our preferred editor, use a command like this one, which sets Sublime Text as the default editor:

  ```
  git config --global core.editor "subl -n -w"
  ```

  We can set the default branch name for any new repos we create locally to `main` by running this command:

  ```
  git config --global init.defaultBranch main
  ```

  As for the global `.gitignore` file, we can create it like this:

  ```
  touch ~/.gitignore_global
  ```

  ![git config](https://tva1.sinaimg.cn/large/008i3skNgy1gqzcwu60xhj60vm06g0u702.jpg)

  And then open it:

  ```
  open ~/.gitignore_global
  ```

  And paste the following in it:

  ```
  # Logs and databases #
  ######################
  *.log
  *.sqlite
  
  # OS generated files #
  ######################
  .DS_Store
  .DS_Store?
  ._*
  .Spotlight-V100
  .Trashes
  Icon?
  ehthumbs.db
  Thumbs.db
  ```

  ![gitignore](https://tva1.sinaimg.cn/large/008i3skNgy1gqzcwsetknj311q0n8q43.jpg)

  

- Ruby 3.0.0 isn't fully compatible with Jekyll yet, so we'll need to also install Ruby 2.7.2.



First, check if we already have Ruby 2.7.2:

```
chruby 2.7.2
```

If it doesn't say anything, we already have it. If it says `unknown Ruby`, we'll need to install it:

```
ruby-install ruby-2.7.2
```

Next, we'll create a new `playground` folder, where we can put temporary projects for testing things out. 

```
cd ~ 
mkdir playground && cd playground
```

Then, we need to create a new folder called `jekyll-github-actions` and initialize it as a Git repository:

```
git init jekyll-github-actions && cd jekyll-github-actions
```

![ruby 2.7.2.jepg](https://tva1.sinaimg.cn/large/008i3skNgy1gqzcxzdtxjj310k0b0wmw.jpg)

To make sure we're using Ruby 2.7.2, we'll switch to it:

```
chruby 2.7.2
```

And then we can create a new Jekyll project:

```
gem install bundler jekyll
jekyll new .
```

![gem install bundler jekyll](https://tva1.sinaimg.cn/large/008i3skNgy1gqzcwxqleuj30us0u0ag1.jpg)

Next, we'll add a `.ruby-version` file so that the correct Ruby version is used whenever we `cd` into our `jekyll-github-actions` directory:

```
echo 'ruby-2.7.2' >> .ruby-version
```



Open the jekyll-github-actions folder

![gemfile folder](https://tva1.sinaimg.cn/large/008i3skNgy1gqzcwra894j317y0eugml.jpg)

Update the `Gemfile` so that it looks like this:

```
source "https://rubygems.org"
# Hello! This is where you manage which Jekyll version is used to run.
# When you want to use a different version, change it below, save the
# file and run `bundle install`. Run Jekyll with `bundle exec`, like so:
#
#     bundle exec jekyll serve
#
# This will help ensure the proper Jekyll version is running.
# Happy Jekylling!

ruby "2.7.2"

gem "jekyll", "~> 4.2.0"
# This is the default theme for new Jekyll sites. You may change this to anything you like.
gem "minima", "~> 2.5"
# If you want to use GitHub Pages, remove the "gem "jekyll"" above and
# uncomment the line below. To upgrade, run `bundle update github-pages`.
# gem "github-pages", group: :jekyll_plugins
# If you have any plugins, put them here!
group :jekyll_plugins do
  gem "jekyll-feed", "~> 0.12"
  gem "jekyll-timeago", "~> 0.13.1"
end
```

![gemfile](https://tva1.sinaimg.cn/large/008i3skNgy1gqzcwuspoaj31020n0q6c.jpg)

Save the file, then run `bundle install`.

![bundle install](https://tva1.sinaimg.cn/large/008i3skNgy1gqzcwyjd9gj60yi0u0dkf02.jpg)

Open the `Gemfile.lock`, and look towards the bottom in the `PLATFORMS` section. If `ruby` is not listed, add it with this command:

```
bundle lock --add-platform ruby
```

![add platform ruby.jepg](https://tva1.sinaimg.cn/large/008i3skNgy1gqzcwvosd1j30ve052jsd.jpg)

![gemfile lock folder](https://tva1.sinaimg.cn/large/008i3skNgy1gqzcwt58w3j31l20owwk2.jpg)

![gemfile lock](https://tva1.sinaimg.cn/large/008i3skNgy1gqzcwrpoi0j317y0eugml.jpg)

Now we are able to locate the file of our Jekyll site

![locating the jekyll site](https://tva1.sinaimg.cn/large/008i3skNgy1gqzcwzgrehj611q0nu41n02.jpg)

When we open it, it looks like this.

![initial Jekyll site](https://tva1.sinaimg.cn/large/008i3skNgy1gqzcwwpglvj31jt0u0tcv.jpg)

To test that the `jekyll-timeago` plugin works, we'll update our `index.markdown`to make use of it:

```
---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: home
---

Testing the timeago plugin on GitHub Pages

{% assign date = '2020-04-13T10:20:00Z' %}

- Original date - {{ date }}
- With timeago filter - {{ date | timeago }}
```

![index markdown folder.jepg](https://tva1.sinaimg.cn/large/008i3skNgy1gqzcx0esejj317q0agdgo.jpg)

![index markdown](https://tva1.sinaimg.cn/large/008i3skNgy1gqzcww6o0jj30zi0jkta5.jpg)

