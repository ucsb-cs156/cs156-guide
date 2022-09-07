---
layout: default
title: "Introduction"
nav_order: 1
parent: GitHub
grand_parent: Services
---

# GitHub

One of the main goals of CMPSC 156 is to allow students to get acquainted with professional software development tools used in industry. One commonly used tool is GitHub, whose core product is a hosting platform for source code repositories using Git. 

GitHub is continuously introducing more features to enhance the software development lifecycle. The GitHub tools we use in this class are:

* `git` Repository Hosting
* Pull Requests - code reviewing tool
* Pages - static website hosting
* Actions - continuous integration and continuous delivery
* Issues - issue backlog and epic management
* Projects - Kanban boards for tracking team progress

## Why do we use `git` and GitHub?

Each of the tools listed above is designed to address a gap between student development in academia and professional software development in industry.

### 1. `git` Repository Hosting

Here at UCSB, usage of `git` and GitHub is encouraged (and in some cases required) in our introductory lower-division courses, but only as a place to dump code. Many of the core features of `git`, which is a version control software (VCS) at its core, remain unused, such as learning when and how to properly create commits, push and pull from different branches and remotes, view file diffs, and revert code, to name a few. In this course, we aim to teach the fundamentals of how to use version control software and apply them to `git` specifically, as it is the industry standard VCS in many modern tech companies.

### 2. Pull Requests - code reviewing tool

In academia, students often write code by themselves or in small groups for the purposes of learning a specific concept and to get a grade on an assignment. Code written by students affects only themselves, and is often only designed to be used once, as code is often left untouched after an assignment is submitted and graded. 

In industry, the opposite is often true. Software developers write code in large teams, for which there are often multiple teams working within a larger organization. Codebases that software developers iterate on are often products that serve end users, thus having a large impact. Such code will often go on to exist for many years, maintained by a new set of developers. For these reasons (and many others), code written by software developers are often reviewed by one or more members of the team, where others can check the code for regressions, styling, places for optimization, consistency, and more.

GitHub's Pull Requests feature is one such mechanism for reviewing code. With its tight integration to GitHub and organizations, Pull Requests allow authors of a new branch to request the changes in a branch to be reviewed by select contributors / members of a repository before being merged into the upstream branch. 

More on how we use GitHub Pull Requests in this class can be found in the section below.

### 3. Pages - static website hosting

GitHub Pages is a feature that allows a repository to be hosted as a static webpage (i.e. a website serving only static files) on GitHub's servers. While this tool does not directly address a gap between academia in industry, we use GitHub Pages to assist in the hosting of our course website, as well as project Storybook repositories, which serve as a development / validation tool for frontend components in our legacy code projects.

See the section on "Development" for information about how to set up GitHub Pages to host Storybook.

### 4. Actions - continuous integration and continuous delivery



* Issues - issue backlog and epic management
* Projects - Kanban boards for tracking team progress











---

## Setting Up Teams in GitHub






Inviting phtcon as an owner for linker