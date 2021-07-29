---
title: "CTCW 2020: dotfiles"
subtitle: Feel at ${HOME} wherever you are
summary: "How to save your ${HOME} configuration and deploy it everywhere"
authors:
- admin
tags: ["computer tools","dotfiles","CTCW","2020"]
categories: ["computer tools","CTCW 2020"]
# date: "2020-09-09T09:00:00Z"


featured: false
draft: false
math: false


# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder. 
image:
  caption: ""
  focal_point: ""

# Projects (optional).
#   Associate this post with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `projects = ["internal-project"]` references 
#   `content/project/deep-learning/index.md`.
#   Otherwise, set `projects = []`.
projects: ["computer tools"]
---

If you followed my previous posts, you may find in your `${HOME}` directory several files starting with a dot, or dotfiles: `.gitconfig` for your git configuration, `.zsh` for you zsh configuration, and `.p10.zsh` if you tried Powerlevel10k.

Of course, there are probably a lot of other dotfiles from

- your editor or your terminal (`.vimrc`, `.bashrc`, etc),
- softwares or libraries you use (I have one for [iTerm2](https://iterm2.com) and [matplotlib](https://matplotlib.org) for example).

This is not an exhaustive list, but `${HOME}` is the place where user configurations are usually stored in plain-text files. 



{{%toc%}}

## 1. The goal

Since all these dotfiles are just plain-text files, a natural idea is to save them, or to version them, to actually backup your settings, sync them across multiple machines and be able to deploy them quickly. This is particularly useful when getting a new computer, using a remote computer, or for some other reasons we will see in a later post. 😉

That is why, when talking about *dotfiles*, there is usually a repository that stores all these dotfiles, but also contains some scripts (sometimes called *bootstrap*) to set everything on a new environment:

- install the dotfiles into `${HOME}`,
- install utilities (for example, a plugin manager for `zsh` or a enhanced prompt as we have seen in my [previous post]({{< ref "/post/2020_CTCW_3_zsh/index.md" >}})),
- install libraries (via [HomeBrew](https://brew.sh/index_fr) and processing a `.BrewFiles` on MacOS for example),
- etc.

And it needs to be easy to deploy, with a one-line command in the terminal for example.


## 2. How-to

As always , there are lots of possibilities to achieve this, and it also depends on your particular needs, so you need to try and fail to find what is the best for you.

That being said, there exists 

## 3. References

### 3.1. Lists of dotfiles

- An unofficial [guide](https://dotfiles.github.io) to dotfiles

### 3.2. Other tutorials/introductions

- The [missing semester](https://missing.csail.mit.edu/2019/dotfiles/) from MIT
