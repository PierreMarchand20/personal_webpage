+++
title = "Computer tools"
date = 2018-10-01T13:51:35+02:00
draft = false

authors = ["admin"]

# Tags: can be used for filtering projects.
# Example: `tags = ["machine-learning", "deep-learning"]`
tags = ["computer tools","personal project"]

# Project summary to display on homepage.
summary = "computer tools for mathematicians and computer scientists"

# Optional external URL for project (replaces project detail page).
external_link = ""

# Does the project detail page use math formatting?
math = true

# Does the project detail page use source code highlighting?
highlight = true

# Featured image
# To use, add an image named `featured.jpg/png` to your project's folder. 
[image]
  # Caption (optional)
  caption = "Photo by [Bill Oxford](https://unsplash.com/@bill_oxford?utm_source=unsplash&amp;utm_medium=referral&amp;utm_content=creditCopyText) on [Unsplash](https://unsplash.com/)"

  # Focal point (optional)
  # Options: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight
  focal_point = "Smart"

  # Show image only in page previews?
  preview_only = false
+++
I am interested in computer tools that improve your workflow and I truly believe it needs to be more widespread in the mathematical/research community. It helps to be more efficient, to convey your new ideas and simply to be more comfortable in your research. I am far from being an expert, and I am still learning every day, do not hesitate to contact me if you have remarks or suggestions.

With this in mind, I was one of the organizers of the seminar [Infomath](https://ljll.math.upmc.fr/infomath) and I gave some talks about tools that may interest you. In this page, I will also put some tools/information that I think could be helpful for others. If needed, I could write a post to go more in-depth on a particular tool.

Here's some of my repositories with the tools that I use:

- [dotfiles](https://github.com/PierreMarchand20/dotfiles): it is a way to save your preferences, that are saved in your `$HOME` using dotfiles, `.bashrc` or `.zshrc` for example. It also contains an executable (usually called `bootstrap`) that install your environment (packages, preferences...). It helps when you have to change computer, sync your environment between different computers etc. To do so, I am using [yadm](https://thelocehiliosan.github.io/yadm/) which is like `git` but allows you to easily have your `$HOME` as a git repository. You can find a list of references on the subject [here](https://dotfiles.github.io).
- [personal webpage](https://github.com/PierreMarchand20/personal_webpage): a personal webpage helps to present your research, but it is a full-time job to maintain a website so I am using the framework [Academic](https://sourcethemes.com/academic/), that allows us to easily create a simple website using [Hugo](https://gohugo.io), which is a static site generator, and optionally [Netlify](https://www.netlify.com) to deploy my webpage. It uses Markdown (a lightweight markup language) to write content, with support for code highlighting and $\LaTeX$ math formatting.

Here are some softwares I use:

- [Homebrew](https://brew.sh) is a package manager for macOS, so that you can install most of the packages you want and it will deal with the dependencies. With the extensions [Homebrew Cask](https://github.com/Homebrew/homebrew-cask) and [mas-cli](https://github.com/mas-cli/mas), you can also install, respectively, GUI macOS applications and Mac App Store applications, using command line. Using [Homebrew Bundle](https://github.com/Homebrew/homebrew-bundle), you can save all your packages/applications in a file called `Brewfile` that you can then use to reinstall everything in one command. It should also work to some extent with Linux and [Linuxbrew](http://linuxbrew.sh) but I am yet to try it.
- [VS Code](https://code.visualstudio.com) is a free source code editor developed by Microsoft. It is available on Windows, Linux and macOS. It is similar to Atom, but I found it faster and the community packages seemed way more developed, at least for my personal use. For example, for writing in $\LaTeX$, you can use the package [Latex](https://marketplace.visualstudio.com/items?itemName=James-Yu.latex-workshop) that has about 1.8 millions downloads (in november 2018) and about everything you want to write in $\LaTeX$.
- [JabRef](http://www.jabref.org) is an open source bibliography reference manager, that can use BibTeX or BibLaTeX. It can help you classify your references, generate them automatically, open their associated pdf files and export them in various format. I use it to navigate through my bibliography and generate my `.bib` files.
