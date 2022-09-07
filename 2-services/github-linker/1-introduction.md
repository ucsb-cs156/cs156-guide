---
layout: default
title: "Introduction"
nav_order: 1
parent: github-linker
grand_parent: Services
---

# UCSB CS GitHub Linker

[ucsb-cs-github-linker.herokuapp.com](https://ucsb-cs-github-linker.herokuapp.com/)

Formerly known as Project Anacapa

The UCSB CS GitHub Linker is a set of tools developed in-house that are designed to automate the management of classroom GitHub organizations and allow for advanced analytics based on available GitHub metadata. The tool makes heavy use of GitHub's REST API to provide its functionality.

Features of the GitHub linker include (but are not limited to):
* Adding students to a GitHub organization if they're on a course roster
* Creating teams in a GitHub organization for repository access control
* Creating individual student repositories for assignments
* Creating team repositories for notes / assignments
* Analyzing commits, issues, and PRs per repository and per team
* Slack bot for easy lookup of member to team

While the GitHub Linker tool was designed with UCSB (and specifically CMPSC 156) in mind, the tool is designed in a way that it can be used with courses taught at any university.

Development of this tool is managed by Phill Conrad (<phtcon@ucsb.edu>) and is done in [this GitHub repository](https://github.com/brownfield-team/anacapa-github-linker).
