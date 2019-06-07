+++
title = "Extensions for VS Code"
subtitle = ""

# Add a summary to display on homepage (optional).
summary = ""

date = 2019-06-06T23:53:10+02:00
draft = false

# Authors. Comma separated list, e.g. `["Bob Smith", "David Jones"]`.
authors = ["admin"]

# Is this a featured post? (true/false)
featured = false

# Tags and categories
# For example, use `tags = []` for no tags, or the form `tags = ["A Tag", "Another Tag"]` for one or more tags.
tags = ["computer tools","vscode"]
categories = []

# Projects (optional).
#   Associate this post with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `projects = ["deep-learning"]` references 
#   `content/project/deep-learning/index.md`.
#   Otherwise, set `projects = []`.
projects = ["Computer tools"]

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder. 
[image]
  # Caption (optional)
  caption = ""

  # Focal point (optional)
  # Options: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight
  focal_point = ""
+++

As of today, VS Code is one of the [most popular editor](https://insights.stackoverflow.com/survey/2019?utm_source=Iterable&utm_medium=email&utm_campaign=dev-survey-2019#technology-_-most-popular-development-environments) and I have used it for a year now. One of its advantage, like most of the editors nowadays, is its versatility, which allows me to use it for most of my work as a PhD student.

In this blog, I will present the extensions for VS Code I used. To choose an extension, I usually looks at two parameters:

- it must do the job (obviously),
- it has to be maintained.

To check the latter, I look at the number of downloads, the number of open issues, the date of the last commit and the number of stars/watch on their repository.

Do not hesitate to click on the link for each extension, they usually have gifs and pictures to show visually what they offer.

## General improvements

- [Code Spell Checker](https://marketplace.visualstudio.com/items?itemName=streetsidesoftware.code-spell-checker): every editor needs a good spell checker. This extension provides spell check in english for several types of files (yes, even your python/C++ files), checking also [camelCase](https://en.wikipedia.org/wiki/Camel_case) code. There are addons for French, Spanish, German, etc. Another alternative is to use the [Language tool](https://marketplace.visualstudio.com/items?itemName=adamvoss.vscode-languagetool) extension, but it only works for plaintext or markdown files.
- [Project Manager](https://marketplace.visualstudio.com/items?itemName=alefragnani.project-manager): it allows you to define workspaces (meaning a window in VS Code) as "projects" and to go from one project to another easily. It also define automatically a project for any git/Mercurial/SVN repository.
- [Setting Sync](https://marketplace.visualstudio.com/items?itemName=Shan.code-settings-sync): all your preferences (settings, keybindings, extensions, workspaces...) are saved in a GitHub Gist and can sync all your devices where you use VS Code.
- [TODO Highlight](https://marketplace.visualstudio.com/items?itemName=wayou.vscode-todo-highlight): it allows highlighting and an easy access to all your TODOs in all your files. In pratice, you can define keywords (by default, TODO: and FIXME:) that will by picked by this extension accross all you files.
- [vscode-icons](https://marketplace.visualstudio.com/items?itemName=vscode-icons-team.vscode-icons): it just adds nice icons in the tree view. Several extensions exist for this, I just chose this one because it has the most of downloads...
- [GitLens](https://marketplace.visualstudio.com/items?itemName=GitHub.vscode-pull-request-github): git is already well supported by VS Code but this extension adds a lot of interesting features: a File history view and a Repository view to look at their commit history, blame annotations at current line, etc.

## For research

- [LaTeX Workshop](https://github.com/James-Yu/LaTeX-Workshop): it turns VS Code into the best editor I know for $\LaTeX$. It already has all you need but they find ways to add new features anyway. You have the usual features (definition of compiling toolchain, support for multi file project, snippets, shortcuts...). But take the time to read their documentation, but here's some original features:
  - Errors and warnings (and linting if you use ChkTeX) will appear in the document and the Problems pane.
  - Hovering: putting the cursor on elements can have several effects:
    - On a package name, you will be able to open its documentation,
    - On a math environnement, it previews environnement,
    - On a reference, it previews what is referenced,
    - On a citation, it previews the bibtex reference, etc.
  - Intellisense: it will autocomplete bib citations, references, commands, files... with an easy way to look for the right keyword.
- [Markdown All in One](https://github.com/yzhang-gh/vscode-markdown): really useful to take notes during a meeting or a presentation. VS Code comes with a built-in previewer and this extension adds some editing features for markdown (shortcuts, list editing, table formatter...). There are other extensions to add linting and other previewers.
- [VSNotes](https://marketplace.visualstudio.com/items?itemName=patricklee.vsnotes): a handy extension to organize your markdown note (see previous bullet point).
- In research, we usually have to handle data stored in several format, and it can be useful to look at the raw data.
  - JSON: it is the format used for the configuration files, so it has built-in support.
  - YAML: I do not use it, but [YAML](https://marketplace.visualstudio.com/items?itemName=redhat.vscode-yaml) seems to be popular.
  - TOML: I use [Better TOML](https://marketplace.visualstudio.com/items?itemName=bungcip.better-toml) for hightlighting.
  - CSV: [Rainbow CSV](https://marketplace.visualstudio.com/items?itemName=mechatroner.rainbow-csv) highlights columns, provides info about column, check consistency, and have a SQL-like editing mode. [Excel Viewer](https://marketplace.visualstudio.com/items?itemName=GrapeCity.gc-excelviewer) is also quite nice and works for Excel files, but is read-only.
  - ENO: it is a new format that I like, the author built an extension called [vscode-eno](https://marketplace.visualstudio.com/items?itemName=eno-lang.vscode-eno) for syntax highlighting.
- [SSH-FS](https://marketplace.visualstudio.com/items?itemName=Kelvin.vscode-sshfs): to access clusters, this extension "mounts" a remote folder over SSH to a local workspace, so that you can used all your favorite shortcuts. But most of the other extensions do not work in this case. [Remote-SSH](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-ssh) should fix this.

## For coding

Most of the languages are supported, here's the ones I used:

- [Python](https://marketplace.visualstudio.com/items?itemName=ms-python.python): it provides everything you need: IntelliSense, linting, debugging, formatting, etc. One thing I like is that Jupyter Notebooks can be used directly in VS Code (and easily exported or imported with the usual format), and the format of the file is easier to version since it is a simple `.py` file.
- [C/C++](https://marketplace.visualstudio.com/items?itemName=ms-vscode.cpptools): it also provides everything you need: auto-completion, debugging, previews declaration when hovering, code navigation, etc.

## Conclusion

The community around VS Code is really alive and brings a lot of new features to this editor. Microsoft (who develops the core of VS Code) also pushes for new developments and regularly adds new features. Each time I had a problem with an extension, I contacted the people who were developing it and I always received useful help and advise, so do not hesitate to leave issues (after checking that it had not already been done of course :wink:).

*Do not hesitate to contact me if you have any remarks or questions !*
