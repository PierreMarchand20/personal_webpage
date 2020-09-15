---
title: "CTCW 2020: zsh"
subtitle: Contest of the most beautiful terminal
summary: Improve your terminal experience with Zsh
authors:
- admin
tags: ["computer tools","zsh","CTCW","2020"]
categories: ["computer tools","CTCW 2020"]
# date: "2020-09-09T09:00:00Z"


featured: false
draft: false
math: true

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

One crucial tool a developer needs is a *terminal*. It is a tool to interact differently with your computer, i.e., using a [command line interface](https://en.wikipedia.org/wiki/Command-line_interface#Anatomy_of_a_shell_CLI) instead of a [graphical user infercace](https://en.wikipedia.org/wiki/Graphical_user_interface). In other words, it allows you to give text commands to the operating system, instead of manipulating graphical elements (windows, icons,...). While the latter is easier to begin with, the former has the advantages to allow scripting and automation of your tasks, to use less ressources, and it only uses the keyboard which can make you more efficient.

In particular, I use it to run code, to connect on remote computers, and to use git that I presented in my [previous post]({{< ref "/post/2020_09_09_CTCW_git/index.md" >}}).

There is a steep learning curve to use a terminal so today, we will see how to improve your terminal experience with the Z shell, also called zsh. It is an alternative to bash, and it is going to be the [default shell on macOS](https://support.apple.com/en-us/HT208050) starting from Catalina 10.5.

{{%toc%}}

## 1. Terminology

{{< figure src="terminal.drawio.svg" title="Terminology" lightbox="true" >}}

- [Command-line interpreter](https://en.wikipedia.org/wiki/Command-line_interface), or *shell*: a program that processes commands, which allows users to access operating system's services. The syntax (command's names, arguments, ...) is specific to the shell. Examples of shells: `sh`, `bash` (the most common), `fish`, and `zsh` which is the focus of this post.
- [Terminal](https://en.wikipedia.org/wiki/Terminal_emulator), or *terminal emulator*: a text interface to a shell. In other words, it is the software in which users can access to the command-line interface. Before, terminal refereed to a physical hardware with a keyboard and a monitor. They are now mostly *virtual*, and in practice, it is the window in which we can interact with a shell. Examples of terminals (see [list](https://en.wikipedia.org/wiki/List_of_terminal_emulators)):
  - on macOS: [Terminal.app](https://en.wikipedia.org/wiki/Terminal_(macOS)), [iTerm2](https://www.iterm2.com), ...
  - on Linux: [Konsole](https://konsole.kde.org), [GNOME termnial](https://en.wikipedia.org/wiki/GNOME_Terminal), ...
  - on Windows: [Windows Terminal](https://devblogs.microsoft.com/commandline/introducing-windows-terminal/), [PuTTY](https://www.chiark.greenend.org.uk/~sgtatham/putty/), ...

- [Command prompt](https://en.wikipedia.org/wiki/Command-line_interface#Command_prompt): a sequence of characters in the command-line interface that tells you the shell is ready to accept a command. It *prompts* you to give a command. It usually contains other information (path of the current directory, hostname, ...).

## 2. Z Shell

We are interested in zsh, which is a shell derived from the Bourne shell `sh`, like `bash`. It is the reason why they both share a lot of features. If you already know how to use `bash` (`cd`, `mv`, `touch`, `mkdir`, ...), don't worry, you won't start from scratch again.

Personally, I mainly use a shell interactively, meaning that I do not write so many shell scripts, so I will mainly focus on this usage. Note that you can use any shell interactively and any other shell in scripts using a [shebang](https://en.wikipedia.org/wiki/Shebang_(Unix)) (`#!/usr/bin/env bash` for bash) at the beginning of your shell scripts.

Here are some features of zsh that I like and often use (see next [section](#3-plugin-managers) to activate all of them):

- **Completion** (builtin and improved with [zsh-completions](https://github.com/zsh-users/zsh-completions)): just use `tab` to complete your command line
  - **recursive path completion**: no need to write the full directory/file names
{{< asciinema key="2020_09_16_CTCW_zsh/path_expansion" rows="10" preload="1" theme="solarized-dark" title="Setup git">}}
  - **command arguments completion**: `zsh` suggests arguments to the command you wrote with a description of each option (for example, `git` we saw on the [previous post]({{< ref "/post/2020_09_09_CTCW_git/index.md" >}})) {{< asciinema key="2020_09_16_CTCW_zsh/argument_command_completion" rows="25" preload="1" theme="solarized-dark" title="Setup git">}}
  - **command arguments flags**: same as the previous feature, but for flags {{< asciinema key="2020_09_16_CTCW_zsh/flag_command_completion" rows="25" preload="1" theme="solarized-dark" title="Setup git">}}
  - **variable expansion**: {{< asciinema key="2020_09_16_CTCW_zsh/variable_expansion" rows="10" preload="1" theme="solarized-dark" title="Setup git">}}
- **Better history navigation**: you can search for a command in your history with any substring of this command using up and down arrows (with [history-substring-search](https://github.com/zsh-users/zsh-history-substring-search)) {{< asciinema key="2020_09_16_CTCW_zsh/history_substring_search" rows="20" preload="1" theme="solarized-dark" title="Setup git">}}
- **Autosuggestion**: the last command starting by what you write is suggested and you can use `tab` to autocomplete it (with [zsh-autosuggestions](https://github.com/zsh-users/zsh-autosuggestions))
{{< asciinema key="2020_09_16_CTCW_zsh/autosuggestion" rows="20" preload="1" theme="solarized-dark" title="Setup git">}}
- **Syntax highlighting**: a few examples (with [zsh-syntax-highlighting](https://github.com/zsh-users/zsh-syntax-highlighting)) {{< asciinema key="2020_09_16_CTCW_zsh/syntax_highlighting" rows="20" preload="1" theme="solarized-dark" title="Setup git">}}
- **Plugin and theme support**: zsh is known for its [plugin managers](#3-plugin-managers) that allows installing/activating the previously cited plugins and many others, but it is also known for its highly customizable [prompt](#4-prompts). We are going to see how to benefit from them.

## 3. Plugin managers

As we have seen, some features are available via plugins. You could install them by hand, each repository explains how to do it. Usually you have to download them, source them in your `.zshrc` and set some variables. But it can be tricky because the order with which you source them matters, and having a lot of plugins can add a delay when starting a new shell session.

Another possibility is to use a *plugin manager*. There are a lot of them (see [reference](#53-plugin-managers)), I personally use [Zim](https://github.com/zimfw/zimfw) that I find fast and easy to use. Besides, it is well-maintained and the maintainers were quite helpful when I had a question. I tried to use a few other plugin managers, most of them are great, but some added a delay when starting a new shell session, and that is how I tried `Zim`, which is marketed as [fast](https://github.com/zimfw/zimfw/wiki/Speed). I was convinced by the fact they [thought](https://github.com/zimfw/zimfw/issues/88) about how their project should grow.

The [installation](https://github.com/zimfw/zimfw#installation) process is quite simple and default configuration should give you most of the features described previously.

## 4. Prompts

## 5. References

### 5.1. Terminology

- Wikipedia for [command-line interface](https://en.wikipedia.org/wiki/Command-line_interface#Anatomy_of_a_shell_CLI), [terminal emulator](https://en.wikipedia.org/wiki/Terminal_emulator)
- Questions on StackEchange: [Unix&Linux](https://unix.stackexchange.com/questions/4126/what-is-the-exact-difference-between-a-terminal-a-shell-a-tty-and-a-con) and [superuser](https://superuser.com/questions/144666/what-is-the-difference-between-shell-console-and-terminal)
- [List](https://en.wikipedia.org/wiki/List_of_terminal_emulators) of terminal emulators
- [Video](https://www.youtube.com/watch?v=hMSByvFHOro) of Luke Smith defining the terminology.

### 5.2. Z Shell

- [Website](http://zsh.sourceforge.net) of zsh.
- [Some features](https://github.com/hmml/awesome-zsh) of zsh
- [Resources](https://github.com/unixorn/awesome-zsh-plugins#generic-zsh) about zsh.
- Bash vs zsh on [Stackexchange](https://apple.stackexchange.com/questions/361870/what-are-the-practical-differences-between-bash-and-zsh)

### 5.3. Plugin managers

- Some plugin managers: [zim](https://github.com/zimfw/zimfw), [oh my zsh](https://ohmyz.sh), [antigen](https://github.com/zsh-users/antigen), [zplug](https://github.com/zplug/zplug), [zinit](https://github.com/zdharma/zinit),...
- Benchmarks for plugin managers: [zim benchmarks](https://github.com/zimfw/zimfw/wiki/Speed), a reddit [thread](https://www.reddit.com/r/zsh/comments/ak0vgi/a_comparison_of_all_the_zsh_plugin_mangers_i_used/).
- Customizable and efficient prompts: [Powerlevel10k](https://github.com/romkatv/powerlevel10k), [Spaceship](https://github.com/denysdovhan/spaceship-prompt)
- a reddit [thread](https://www.reddit.com/r/zsh/comments/bj6rwz/what_is_a_good_ohmyzsh_alternative/) on plugin managers.
