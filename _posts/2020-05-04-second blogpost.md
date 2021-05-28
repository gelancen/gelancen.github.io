---
layout: post
title: 2. Mac Installation|Jekyll - Static Site Generator
date: 2021-05-04
tags: jekyll   
---

# **2. Mac Installation|Jekyll - Static Site Generator**

## 2.1 Install Command Line Tools

To install the command line tools to compile native extensions, open a terminal and run:

```
xcode-select --install
```

![x-code 1](/Users/mac/Desktop/KUL/online publishing/BLOG/x-code 1.png)

![x-code](/Users/mac/Desktop/KUL/online publishing/BLOG/x-code.png)

## 2.2 Install Ruby

Jekyll requires **Ruby v2.4.0** or higher. macOS Big Sur 11.x ships with Ruby 2.6.3. Check Ruby version using `ruby -v`.

A very common error people run into when trying to install any Ruby gem on macOS is a permissions error much like this one:

```
ERROR: While executing gem ... (Gem::FilePermissionError)
You don't have write permissions for the /Library/Ruby/Gems/2.6.0 directory
```

macOS returns this error because the default location for Ruby gem installations is the system Ruby directory that is preinstalled by Apple. That directory is not meant to be modified, hence Apple not giving us permissions to write to it.

There are two main options: 1) install a separate version of Ruby that we control, or 2) keep using the system Ruby via some modifications. Option 1 can be further split into two options: install the new version with Homebrew , or with a Ruby manager.

### 2.2.1 With Homebrew

To run the latest Ruby version we need to install it through [Homebrew](https://brew.sh/).

![homebrew](/Users/mac/Desktop/KUL/online publishing/BLOG/homebrew.png)

#### 2.2.1.1 Install Homebrew 

/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)" 

![homebrew installation problem](/Users/mac/Desktop/KUL/online publishing/BLOG/homebrew installation problem.jpeg)

To ensure that /opt/homebrew/bin is in our PATH, we should run 'brew help' and then echo the command above.

#### 2.2.1.2 Install Ruby 

brew install ruby

Add the brew ruby and gems path to the shell configuration:

```
# If you're using Zsh
echo 'export PATH="/usr/local/opt/ruby/bin:/usr/local/lib/ruby/gems/3.0.0/bin:$PATH"' >> ~/.zshrc

# If you're using Bash
echo 'export PATH="/usr/local/opt/ruby/bin:/usr/local/lib/ruby/gems/3.0.0/bin:$PATH"' >> ~/.bash_profile
```

Relaunch your terminal and check your Ruby setup:

![ruby version](/Users/mac/Desktop/KUL/online publishing/BLOG/ruby version.png)

## 2.3 Install Jekyll

After installing Ruby, install Jekyll and Bundler.

### Local Install

Install the bundler and jekyll gems:

```
gem install --user-install bundler jekyll
```

Get your Ruby version:

![ruby version](/Users/mac/Desktop/KUL/online publishing/BLOG/ruby version.png)

Append your path file with the following, replacing the `X.X` with the first two digits of your Ruby version:

```
# If you're using Zsh
echo 'export PATH="$HOME/.gem/ruby/X.X.0/bin:$PATH"' >> ~/.zshrc

# If you're using Bash
echo 'export PATH="$HOME/.gem/ruby/X.X.0/bin:$PATH"' >> ~/.bash_profile

```

Type  [http://localhost:4000](http://localhost:4000/) in the browser

![initial jekyll page](/Users/mac/Desktop/KUL/online publishing/BLOG/initial jekyll page.png)



It should be noted that this is just a quick way to confirm that we can create and view a Jekyll site on our computer. 