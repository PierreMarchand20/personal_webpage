---
title: Computer Tools and Coding Workflow in 2020
subtitle: CTCW, a series of posts to improve your coding experience
summary: Introduction of the series of posts CTCW 2020
authors:
- admin
tags: ["computer tools","motivation","CTCW","2020"]
categories: ["computer tools","CTCW 2020"]
# date: "2020-09-02T09:00:00Z"


featured: false
draft: false
math: true
diagram: true
# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder. 
image:
  caption: "Photo by [Nick Morrison](https://unsplash.com/@nickmorrison?utm_source=unsplash&amp;utm_medium=referral&amp;utm_content=creditCopyText) on [Unsplash](https://unsplash.com/)"
  focal_point: ""

# Projects (optional).
#   Associate this post with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `projects = ["internal-project"]` references 
#   `content/project/deep-learning/index.md`.
#   Otherwise, set `projects = []`.
projects: ["computer tools"]
---

In the following weeks, I will present several tools to improve your development environment, and how I use them together to improve my coding workflow. These posts will be part of a series called Computer Tools and Coding Workflow (CTCW). Today we start with a non-technical post to give some context, motivate the reason of this series, and explain what will follow.

- [1. Disclaimers](#1-disclaimers)
- [2. Motivation](#2-motivation)
- [3. Program](#3-program)

## 1. Disclaimers

- I should say that *I am not an expert*. I have studied very little computer science and informatics in my undergraduate studies. Most of what I know now comes from self-learning, and practice. If you disagree, or if you think there is a better way than what I will present, please share your ideas in the comments!
- *A workflow is personal*, meaning that what I present may not be entirely adequate to your own way of reasoning. But I hope it can inspire you to think about your workflow, and that it can give you ideas on how to make it more efficient.
- The tools I will present are maintained and well-documented at the present moment, so I will focus on what they can bring you and refer to their documentation for installation and more technical discussions.
- In this series, I will assume you know basic command lines and how to use your terminal.
- For those doing theoretical research, I should point out that *writing a $\LaTeX$ document is coding*.
- I have not used Windows in quite some time, but [Windows Subsystem for Linux](https://docs.microsoft.com/fr-fr/windows/wsl/) allows you to use Linux on Windows without using a virtual machine or a dual boot, which can help for programming. Besides, some tools I will talk about are available on Windows anyway.

## 2. Motivation

Thinking about how you work to improve your efficiency is an effort, and it requires to challenge yourself from time to time. In my own experience, people may consider that it is a waste of time, and doing it the *quick and dirty way* is enough. Or they already know one method to accomplish a task that is enough for them, and they want to stick with it. In the short term, it is definitely faster, but I think taking the time to improve your workflow always proves worthwhile, at least in the mid-long term.

For sure, I can testify that during my PhD thesis, it allowed me to go further in my research, more than I could without trying to look for better tools to help me in my work. Without even talking about computer tools, just thinking about the way you can improve your workflow is already a great start! Challenge your habits, try to see where you spend the most time, and look around how people do it.

### A simple example <!-- omit in toc -->

When I was an undergraduate student in applied mathematics, I was always spending a lot of time, not just producing data for my numerical experiments, but post-processing them (organizing the data files, plotting the output, ...). At the time, I was more focused on the core of my work, which was solving a partial differential equation. So I did not want to spend too much time on “technical details”, and ironically, I was...

It came to a point where it was ridiculous, and something needed to be done. Like some students, I had one executable/script doing everything (computations like solving a linear system, analyses like doing a linear regression, plots, ...), and every parameter was hard coded. It was convenient (I thought) since I just had to push a button, and I had directly the results I wanted. But here are the **issues**:

- Surprisingly, nothing works the first time, and having everything in the same code makes you debug everything at the same time.
- The analysis you want to carry over your data is never relevant the first time, so you need to rerun everything each time you want to explore your data, in particular run computations which is the most expensive part.
- The first plots are always ugly, so you also need to rerun everything.
- In case of compiled code, you need to recompile each time you want to change some parameters.

My solution (that may seem obvious to you now, but remember, I was an undergraduate student at the time) consisted in formalizing my numerical experiment as a pipeline where each code component could be implemented separately and needed to take some inputs and create some outputs:

{{< figure src="pipeline.drawio.svg" title="Work pipeline" lightbox="true" >}}

Obviously, it seems more complicated than doing everything in one code/script, and you need to manage inputs and outputs for each code component. But, it has several **advantages**:

- The fact that `Compute` takes `Input` as an argument makes you able to loop over the input parameters, and to generate more data with a simple script.
- If you have several pipelines with similar `Compute` component, you can try to merge them to make one pipeline, that takes more input to recover the exact previous computations.
- You can do as many analyses as you want on `Data`.
- Using well-know formats, such as `csv`, `json` or others (depending on your data) for `Input`, `Data` and `Output` makes you able to use most of the languages/softwares I/O utilities, post-processing and plotting tools. For example, you can easily use the python modules `pandas` and `matplotlib`, $\LaTeX$ package `pgfplot`, etc.
- You can save and store your results `Data` and `Output`.

Of course, you should not break your pipeline into too many components, there is a balance to be struck, and this was a very simple example just to show you how changing your workflow actually allows you to **do more in your core work**. In this example, more computations with more inputs, and more analyses using more post-processing components.

### Take home message <!-- omit in toc -->

It is very valuable to take time to work on your workflow, even for your core work. One other reason is that it is a transferable skill that you will probably be able to use throughout your career. It is also very intellectually satisfying to see we can improve ourselves and to observe the net profit we obtain in our day-to-day live at work.

## 3. Program

There will be five other CTCW posts. Each one will be on one particular tool and what it can bring you, and you will see that each one will be even better using the previous ones :muscle::muscle::muscle:

Of course, this series of posts can only be better if I have some feedback, so please, *do not hesitate to comment and share!*
